# JDP Desa Jone — Module Map V1

## 1. Tujuan

`module-map.md` memetakan hubungan antara **Entity** dan **Module** dalam JDP.

Module digunakan untuk mengelompokkan fungsi pengelolaan sistem berdasarkan kebutuhan. Pemetaan ini menjadi penghubung antara model konseptual/entity dengan implementasi aplikasi.

Prinsip utama:

* sederhana dan bertahap;
* tidak membuat module hanya karena secara teknis memungkinkan;
* satu entity dapat menjadi dasar sebuah module;
* hubungan antar-entity tidak otomatis menjadi module tersendiri;
* struktur dapat berkembang apabila kebutuhan nyata muncul.

---

# 2. Struktur Utama JDP

Secara konseptual JDP V1 dibagi menjadi tiga lapisan:

### A. Content

Berisi informasi yang ditampilkan dan dikelola sebagai konten Desa.

* News
* Agenda
* Announcement
* Gallery
* Document
* Page

### B. Asset

Berisi aset/file yang digunakan oleh content.

* Media

### C. Management

Berisi pengelolaan pengguna dan aktivitas sistem.

* User / Operator
* Role
* Permission
* Audit Log

---

# 3. Content Modules

## 3.1 Page Module

**Entity:** Page

**Fungsi:**
Mengelola informasi Desa yang relatif tetap, mendasar, baku, dan tidak temporer.

**Contoh:**

* Sejarah Desa
* Profil Desa
* Visi dan Misi
* Sambutan Kepala Desa

**Catatan V1:**
Page menggunakan struktur sederhana:

`id, title, slug, content, status, created_by, created_at, updated_by, updated_at`

Status:

`draft → published`

Media yang hanya digunakan di dalam isi Page untuk sementara dianggap sebagai bagian dari `content`; relationship Page–Media khusus belum dibuat.

---

## 3.2 News Module

**Entity:** News

**Fungsi:**
Mengelola informasi mengenai sesuatu yang sudah terjadi.

**Contoh:**

* Berita gotong royong
* Berita kegiatan Desa
* Berita penerbitan Peraturan Desa

**Catatan V1:**

* News dapat dibuat tanpa Media.
* Media bersifat pelengkap.
* Satu peristiwa tetap dapat direpresentasikan sebagai satu News meskipun mempunyai banyak foto/video.
* News yang masih draft tidak ditampilkan kepada masyarakat.
* News yang sudah published tetap dapat diedit.
* News lama tidak otomatis dihapus karena dapat berfungsi sebagai arsip digital.

---

## 3.3 Agenda Module

**Entity:** Agenda

**Fungsi:**
Mengelola kegiatan atau rencana kegiatan yang akan berlangsung.

**Contoh:**

* Jadwal rapat Desa
* Kegiatan gotong royong yang akan datang
* Agenda kegiatan masyarakat

**Catatan:**
Agenda berbeda dari News.

Agenda menggambarkan kegiatan yang akan berlangsung, sedangkan News digunakan untuk sesuatu yang sudah terjadi.

---

## 3.4 Announcement Module

**Entity:** Announcement

**Fungsi:**
Mengelola penyampaian informasi resmi kepada masyarakat.

**Contoh:**

* Pengumuman pelayanan
* Informasi resmi Kantor Desa
* Informasi yang memiliki masa berlaku

**Catatan:**
Masa berlaku substansi informasi dapat menggunakan:

* `mulai_berlaku`
* `berakhir`

Status publikasi tidak dicampur dengan masa berlaku informasi.

---

## 3.5 Gallery Module

**Entity:** Gallery

**Fungsi:**
Mengelola kumpulan dokumentasi gambar dan video.

Gallery dapat dikaitkan dengan News atau Agenda apabila diperlukan.

**Relationship V1:**

`Gallery ↔ Media`

Satu Gallery dapat memiliki banyak Media.

Urutan Media menggunakan:

`sort_order`

Media dengan `sort_order = 1` menjadi media pertama sekaligus cover Gallery.

Tidak diperlukan attribute `cover_media` khusus pada V1.

---

## 3.6 Document Module

**Entity:** Document

**Fungsi:**
Mengelola produk atau dokumen resmi Kantor Desa.

**Contoh:**

* Peraturan Desa
* SK
* Surat edaran
* Laporan
* Panduan
* Formulir
* Dokumen informasi publik

**Model V1:**

Satu Document menggunakan satu Media.

Dengan demikian:

`Document → Media`

Struktur lampiran dan relationship banyak Media belum diperlukan pada V1.

---

# 4. Asset Module

## 4.1 Media Module

**Entity:** Media

**Fungsi:**
Mengelola aset/file yang digunakan oleh JDP.

Media bukan hanya untuk Gallery.

Media dapat berupa:

* image
* video
* document

Satu Media dapat digunakan oleh beberapa content tanpa menggandakan file fisiknya.

### Struktur Media V1

* `id`
* `nama/file`
* `type`
* `mime_type`
* `lokasi`
* `size`

`size` disimpan dalam byte.

### Gambar V1

Gambar cukup memiliki satu versi yang sudah dioptimalkan.

Alur konseptual:

`Foto asli → resize + compression → Media JDP → website`

Thumbnail, multi-resolution, width, height, original size, dan metadata tambahan belum dimasukkan ke V1.

---

# 5. Management Modules

## 5.1 User / Operator Module

**Entity:** User

**Fungsi:**
Mengelola akun yang digunakan untuk mengoperasikan JDP.

V1 mendukung lebih dari satu Operator.

### Struktur User V1

* `id`
* `nama`
* `username`
* `password`
* `role`
* `status`

Status:

* `active`
* `inactive`

User yang sudah mempunyai riwayat aktivitas tidak perlu dihapus. User dapat dinonaktifkan agar referensi historis tetap aman.

---

## 5.2 Role

Pada V1, Role **belum menjadi entity terpisah**.

Role masih menjadi attribute pada User.

Role V1:

* `operator`
* `administrator`

### Pembagian sederhana

**Operator**

* berfokus pada pengelolaan content.

**Administrator**

* berfokus pada pengelolaan sistem.

Apabila kebutuhan hak akses menjadi lebih rinci, Role dan Permission dapat dikembangkan pada tahap berikutnya.

---

## 5.3 Permission

Permission tetap dikenal sebagai konsep arsitektur JDP.

Namun pada V1:

> Permission belum dibuat sebagai entity/module terpisah.

Kewenangan dasar masih ditentukan berdasarkan Role agar sistem tetap sederhana.

---

## 5.4 Audit Log Module

**Entity:** Audit Log

**Fungsi:**
Mencatat aktivitas yang dilakukan dalam sistem.

Secara konseptual Audit Log menjawab:

* siapa melakukan;
* melakukan apa;
* terhadap apa;
* kapan dilakukan.

Audit Log berbeda dari metadata entity.

Contoh:

`created_by` menunjukkan siapa yang membuat data saat ini.

Audit Log menunjukkan riwayat tindakan yang pernah terjadi terhadap data tersebut.

---

# 6. Relationship Utama

Relationship yang sudah dipahami dalam V1:

```text
News ──────── Media
  │
  └────────── Gallery

Agenda ────── Announcement
   │
   ├───────── News
   │
   └───────── Gallery

Gallery ───── Media

Document ──── Media

Page ──────── content
```

Catatan:

Diagram di atas adalah gambaran konseptual, bukan struktur database final.

Tidak semua kemungkinan relationship harus dibuat hanya karena secara teknis memungkinkan.

---

# 7. Prinsip Module Map V1

Module Map mengikuti prinsip berikut:

1. **Sederhana dulu.**
2. Entity ditentukan berdasarkan fungsi dan makna data.
3. Tidak semua entity harus memiliki struktur yang sama.
4. Tidak semua relationship harus dibuat menjadi module.
5. Jangan membuat entity atau module hanya untuk kemungkinan kebutuhan masa depan.
6. Role masih menjadi attribute User pada V1.
7. Permission terpisah belum diperlukan pada V1.
8. Media merupakan aset bersama.
9. Audit Log menyimpan riwayat aktivitas.
10. Entity menyimpan keadaan data saat ini.
11. Status publikasi tidak dicampur dengan status domain lainnya.
12. Pengembangan berikutnya dilakukan berdasarkan kebutuhan nyata.

---

# 8. Pemetaan Ringkas

| Lapisan    | Module          | Entity       | Status V1            |
| ---------- | --------------- | ------------ | -------------------- |
| Content    | Page            | Page         | Digunakan            |
| Content    | News            | News         | Digunakan            |
| Content    | Agenda          | Agenda       | Digunakan            |
| Content    | Announcement    | Announcement | Digunakan            |
| Content    | Gallery         | Gallery      | Digunakan            |
| Content    | Document        | Document     | Digunakan            |
| Asset      | Media           | Media        | Digunakan            |
| Management | User / Operator | User         | Digunakan            |
| Management | Role            | —            | Attribute User       |
| Management | Permission      | —            | Konsep, belum entity |
| Management | Audit Log       | Audit Log    | Digunakan            |

---

# 9. Batasan V1

Hal-hal berikut **belum menjadi bagian implementasi V1**:

* Permission sebagai entity terpisah
* Role sebagai entity terpisah
* approval workflow formal
* publication scheduling
* content versioning
* thumbnail dan multi-resolution Media
* relationship Page–Media khusus
* Document dengan banyak lampiran
* Media cover khusus News
* metadata Media tambahan
* workflow formulir pelayanan/submission

Hal-hal tersebut dapat dipertimbangkan apabila kebutuhan nyata sudah muncul.

---

# 10. Arah Berikutnya

Setelah Module Map cukup stabil, tahap berikutnya adalah:

**Entity → Attribute → Data Dictionary**

Data Dictionary akan menjelaskan setiap field secara konsisten, termasuk:

* nama attribute;
* fungsi;
* tipe data konseptual;
* required/optional;
* contoh nilai;
* catatan penggunaan.

Database belum perlu dibuat sebelum Data Dictionary cukup stabil.
