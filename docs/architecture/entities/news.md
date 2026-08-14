# Entity: Berita

**Status:** Draft

**Versi:** 0.1

---

## Tujuan

Berita digunakan untuk mendokumentasikan informasi resmi Desa Jone mengenai kejadian, kegiatan, atau peristiwa yang **sudah terjadi**.

---

## Definisi

Berita adalah informasi resmi desa yang menceritakan sesuatu yang telah terjadi dan layak diketahui atau diarsipkan oleh masyarakat.

---

## Contoh

Berita dapat digunakan untuk:

* Kegiatan desa yang telah dilaksanakan.
* Gotong royong yang telah selesai.
* Musyawarah desa yang telah dilaksanakan.
* Pembangunan yang telah dimulai atau selesai.
* Pelatihan atau kegiatan masyarakat yang telah berlangsung.
* Prestasi desa atau warga yang telah terjadi.
* Informasi lain mengenai kejadian yang sudah berlangsung.

---

## Batasan

Berita **bukan** digunakan untuk menyampaikan informasi mengenai sesuatu yang akan terjadi atau pemberitahuan yang masih berlaku.

Untuk kebutuhan tersebut, gunakan **Pengumuman**.

### Aturan sederhana

> **Sudah terjadi → Berita**

> **Akan terjadi / masih berlaku → Pengumuman**

---

## Domain

**Content**

---

## Catatan

Detail atribut Berita, seperti judul, isi, gambar, tanggal, dan penulis, akan ditentukan pada tahap berikutnya.

Struktur database belum dibahas dalam dokumen ini.

| #  | Attribute            | Makna                                         |
| -- | -------------------- | --------------------------------------------- |
| 1  | `id`                 | Pengenal unik News yang digunakan sistem      |
| 2  | `title`              | Judul berita yang dibaca orang                |
| 3  | `isi`                | Berita/informasi yang ingin disampaikan       |
| 4  | `tanggal_kejadian`   | Tanggal terjadinya peristiwa yang diberitakan |
| 5  | `publication_status` | Status berita: draft atau published           |
| 6  | `published_at`       | Waktu berita dipublikasikan                   |
| 7  | `created_by`         | Siapa yang membuat berita                     |
| 8  | `created_at`         | Waktu berita dibuat                           |
| 9  | `updated_by`         | Siapa yang melakukan perubahan, jika ada      |
| 10 | `updated_at`         | Kapan perubahan terakhir terjadi              |

