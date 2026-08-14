# Entity: Pengumuman

**Status:** Draft

**Versi:** 0.1

---

## Tujuan

Pengumuman digunakan untuk menyampaikan informasi resmi Desa Jone mengenai sesuatu yang **akan terjadi atau masih berlaku**.

---

## Definisi

Pengumuman adalah informasi resmi desa yang perlu diketahui masyarakat dalam jangka waktu tertentu.

---

## Contoh

Pengumuman dapat digunakan untuk:

* Jadwal pelayanan desa.
* Perubahan jam pelayanan.
* Jadwal kegiatan yang akan datang.
* Pemberitahuan penutupan kantor.
* Informasi pendaftaran.
* Himbauan kepada masyarakat.
* Informasi lain yang masih berlaku.

---

## Periode Pengumuman

Pengumuman dapat memiliki:

* **Tanggal mulai**
* **Tanggal berakhir**

Contoh:

> Pelayanan kantor desa ditutup pada 10–12 Agustus.

Setelah tanggal berakhir, pengumuman tidak lagi dianggap sebagai pengumuman aktif, tetapi tetap disimpan sebagai arsip.

---

## Batasan

Pengumuman digunakan untuk informasi yang:

* Akan terjadi, atau
* Masih berlaku.

Untuk kejadian yang sudah terjadi dan perlu didokumentasikan, gunakan **Berita**.

### Aturan sederhana

> **Sudah terjadi → Berita**

> **Akan terjadi / masih berlaku → Pengumuman**

---

## Domain

**Content**

---

| #  | Attribute       | Required | Fungsi                                        |
| -- | --------------- | -------- | --------------------------------------------- |
| 1  | `id`            | Ya       | Pengenal unik Announcement                    |
| 2  | `title`         | Ya       | Judul yang dibaca pembaca                     |
| 3  | `isi`           | Ya       | Isi informasi pengumuman                      |
| 4  | `mulai_berlaku` | Ya       | Kapan pengumuman mulai berlaku                |
| 5  | `berakhir`      | Tidak    | Kapan pengumuman tidak berlaku lagi           |
| 6  | `status`        | Ya       | `draft`, `published`, `cancelled`, `archived` |
| 7  | `created_by`    | Ya       | Siapa yang membuat                            |
| 8  | `created_at`    | Ya       | Kapan dibuat                                  |
| 9  | `updated_by`    | Tidak    | Siapa yang terakhir mengubah                  |
| 10 | `updated_at`    | Tidak    | Kapan terakhir diubah                         |


## Catatan

Detail atribut Pengumuman, seperti judul, isi, tanggal mulai, tanggal berakhir, dan status, akan ditentukan pada tahap berikutnya.

Struktur database belum dibahas dalam dokumen ini.
