# Entity: Agenda

**Status:** Draft

**Versi:** 0.1

---

## Tujuan

Agenda digunakan untuk mencatat rencana kegiatan Desa Jone yang akan dilaksanakan.

---

## Definisi

Agenda adalah informasi mengenai kegiatan yang direncanakan, terutama mengenai **apa kegiatannya, kapan, dan di mana kegiatan tersebut dilaksanakan**.

---

## Contoh

Agenda dapat digunakan untuk:

* Rapat desa.
* Gotong royong.
* Upacara atau kegiatan peringatan.
* Pelatihan masyarakat.
* Kegiatan pelayanan.
* Pertemuan lembaga desa.
* Kegiatan desa lainnya yang telah direncanakan.

---

## Perbedaan dengan Pengumuman

**Agenda** berfokus pada kegiatan yang direncanakan.

**Pengumuman** berfokus pada informasi yang perlu diketahui masyarakat.

Contoh:

> **Agenda:** Rapat Desa — 12 Agustus, pukul 09.00, Balai Desa.

> **Pengumuman:** Pelayanan administrasi desa dimulai pukul 13.00 pada 12 Agustus karena pagi hari digunakan untuk rapat.

Agenda dan Pengumuman dapat berkaitan, tetapi memiliki fungsi yang berbeda.

---

## Domain

**Content**

---

-----------------------------
Attribute	| Required	| Makna
=============================
id	|	Ya	|	Pengenal unik Agenda
judul	|	Ya	|	Judul Agenda yang dibaca orang
deskripsi	|	Ya	|	Gambaran singkat Agenda
tanggal_mulai	|	Ya	|	Tanggal rencana mulai kegiatan
tanggal_selesai	|	Tidak	|	Tanggal rencana selesai kegiatan
lokasi	|	Ya	|	Tempat pelaksanaan kegiatan
status	|	Ya	|	draft, published, cancelled
created_by	|	Ya	|	Siapa yang membuat Agenda
created_at	|	Ya	|	Kapan informasi dibuat
updated_by	|	Tidak*	|	Siapa yang terakhir mengubah
updated_at	|	Tidak*	|	Kapan terakhir diubah
---------------------------------------------


Dengan keputusan penting:

tanggal_mulai → wajib
tanggal_selesai → boleh kosong
status → draft, published, cancelled
updated_by → boleh kosong jika belum pernah diubah
updated_at → boleh kosong jika belum pernah diubah
Media → bukan attribute inti Agenda
