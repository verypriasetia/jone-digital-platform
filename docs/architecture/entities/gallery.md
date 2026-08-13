# Entity: Galeri

**Status:** Draft

**Versi:** 0.1

---

## Tujuan

Galeri digunakan untuk menghimpun dan menampilkan dokumentasi visual Desa Jone.

---

## Definisi

Galeri adalah kumpulan dokumentasi berupa **gambar dan video** yang berkaitan dengan kegiatan, peristiwa, tempat, atau hal lain yang dianggap penting untuk didokumentasikan oleh Desa Jone.

---

## Contoh

Galeri dapat digunakan untuk:

* Dokumentasi kegiatan desa.
* Dokumentasi pembangunan.
* Dokumentasi kegiatan masyarakat.
* Dokumentasi acara atau peringatan.
* Dokumentasi tempat dan lingkungan desa.
* Dokumentasi lainnya yang layak dipublikasikan.

---

## Bentuk Dokumentasi

Galeri dapat memuat:

* Gambar
* Video

---

## Domain

**Content**

---

## Catatan

Detail pengelolaan gambar dan video, termasuk ukuran file, kompresi, resize, penyimpanan, dan tampilan, akan dibahas pada tahap berikutnya.

| # | Attribute     | Required | Makna                            |
| - | ------------- | -------- | -------------------------------- |
| 1 | `id`          | Ya       | Pengenal unik Media              |
| 2 | `file`        | Ya       | Nama/path file media             |
| 3 | `type`        | Ya       | Jenis media/file                 |
| 4 | `title`       | Ya       | Judul media yang dilihat pembaca |
| 5 | `caption`     | Tidak    | Keterangan singkat media         |
| 6 | `uploaded_by` | Ya       | Siapa yang mengunggah            |
| 7 | `uploaded_at` | Ya       | Kapan media diunggah             |

