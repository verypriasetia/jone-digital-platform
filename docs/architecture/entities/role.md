# Entity: Role

**Status:** Draft

**Versi:** 0.1

---

## Tujuan

Role digunakan untuk menentukan tingkat kewenangan Operator dalam mengelola Jone Digital Platform (JDP).

---

## Definisi

Role adalah kumpulan kewenangan yang menentukan tindakan apa saja yang dapat dilakukan oleh seorang Operator di dalam JDP.

Role merupakan kewenangan teknis di dalam sistem dan **bukan merupakan jabatan seseorang di Kantor Desa**.

---

## Role Awal

JDP pada tahap awal memiliki dua Role:

### Administrator

Administrator memiliki kewenangan untuk mengelola JDP secara keseluruhan.

Kewenangannya meliputi:

* Mengelola Operator.
* Mengatur konfigurasi sistem.
* Mengelola seluruh konten.
* Mengelola kewenangan.
* Melihat catatan aktivitas sistem.

### Editor

Editor berfokus pada pengelolaan isi website.

Kewenangannya meliputi:

* Membuat dan mengelola Berita.
* Membuat dan mengelola Pengumuman.
* Membuat dan mengelola Agenda.
* Mengelola Galeri.
* Mengelola Dokumen.
* Mengelola Halaman.

Editor tidak memiliki kewenangan untuk mengelola Operator atau konfigurasi utama sistem.

---

## Prinsip

* Satu Operator dapat memiliki satu Role.
* Satu Role dapat digunakan oleh beberapa Operator.
* Role dapat dikembangkan sesuai kebutuhan JDP.
* Penambahan Role tidak dilakukan sebelum terdapat kebutuhan yang jelas.

---

## Catatan

Pembagian kewenangan secara lebih rinci akan ditentukan pada tahap Permission.

Struktur database dan mekanisme autentikasi belum dibahas dalam dokumen ini.


| # | Attribute     | Required | Fungsi                                    |
| - | ------------- | -------- | ----------------------------------------- |
| 1 | `id`          | Ya       | Pengenal unik Role bagi sistem            |
| 2 | `name`        | Ya       | Nama Role yang dikenali manusia           |
| 3 | `description` | Ya       | Menjelaskan tugas dan tanggung jawab Role |
