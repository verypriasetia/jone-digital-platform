# JDP Module Map

**Status:** Draft

**Versi:** 0.2

---

## Tujuan

Dokumen ini memberikan gambaran sederhana mengenai modul utama Jone Digital Platform (JDP).

Module Map digunakan sebagai peta arsitektur tingkat tinggi dan akan berkembang mengikuti kebutuhan JDP.

---

# Struktur Utama

```text
JDP
│
├── Content
│
└── Core
```

---

# Content

Content berisi informasi yang ditampilkan kepada masyarakat melalui website JDP.

```text
Content
│
├── Berita
├── Pengumuman
├── Agenda
├── Galeri
├── Dokumen
└── Halaman
```

### Berita

Mendokumentasikan kejadian atau kegiatan yang **sudah terjadi**.

### Pengumuman

Menyampaikan informasi mengenai sesuatu yang **akan terjadi atau masih berlaku**.

Pengumuman dapat memiliki tanggal mulai dan tanggal berakhir.

### Agenda

Mencatat **rencana kegiatan** yang akan dilakukan.

### Galeri

Menghimpun dokumentasi visual berupa:

* Gambar
* Video

### Dokumen

Mengelola produk resmi Kantor Desa yang dapat digunakan untuk:

* Informasi satu arah kepada masyarakat.
* Kebutuhan pelayanan atau proses yang membutuhkan respons/feedback dengan standar tertentu.

### Halaman

Menyediakan informasi yang bersifat:

* Baku
* Mendasar
* Tidak temporer

Halaman digunakan sebagai informasi profil atau informasi dasar Desa.

---

# Core

Core berisi fungsi dasar untuk mengelola JDP.

```text
Core
│
├── Operator
├── Role
├── Permission
├── Settings
├── Media Library
└── Audit Log
```

### Operator

Pengelola JDP yang dipercaya dan bertanggung jawab kepada Kantor Desa.

JDP memungkinkan terdapat beberapa Operator.

Setiap Operator memiliki akun sendiri.

Operator menjadi jalur resmi pengelolaan dan publikasi informasi JDP.

### Role

Menentukan kelompok kewenangan Operator.

Role awal:

```text
Administrator
Editor
```

Role merupakan kewenangan di dalam sistem dan bukan jabatan seseorang di Kantor Desa.

### Permission

Menentukan tindakan yang dapat dilakukan berdasarkan Role.

Permission dasar:

* Melihat
* Membuat
* Mengubah
* Menghapus
* Mempublikasikan

Editor dapat mengelola dan mempublikasikan konten secara langsung.

### Settings

Menyediakan pengaturan dasar JDP.

Detail Settings belum ditentukan.

### Media Library

Menyediakan pengelolaan aset media yang digunakan JDP.

Detail Media Library belum ditentukan.

### Audit Log

Mencatat tindakan penting Operator yang berdampak terhadap data.

Pada tahap awal mencatat:

* Membuat data
* Mengubah data
* Menghapus data
* Mempublikasikan data

Aktivitas yang hanya melihat atau membaca data tidak dicatat.

---

# Prinsip Dasar

## Satu Jalur Publikasi

Informasi yang dipublikasikan melalui JDP tetap melalui Operator sebagai jalur resmi publikasi Kantor Desa.

Hal ini berlaku meskipun informasi berasal dari Kades, Sekdes, perangkat desa, atau pihak lain di lingkungan desa.

---

## Beberapa Operator

JDP dapat memiliki beberapa Operator.

Semua Operator bekerja dalam satu sistem dan mengikuti standar publikasi yang sama.

---

## Akun Operator Bersifat Individual

Setiap Operator memiliki akun sendiri.

Akun tidak digunakan bersama oleh beberapa orang.

---

## Masyarakat sebagai Pengguna Website

Masyarakat merupakan pengguna website publik yang memanfaatkan informasi dan layanan yang tersedia.

Masyarakat tidak harus memiliki akun untuk mengakses informasi publik.

---

## Role Bukan Jabatan

Role JDP merupakan kewenangan teknis di dalam sistem.

Role tidak secara otomatis mengikuti jabatan seseorang di Kantor Desa.

---

## Status Arsitektur

Dokumen ini masih berstatus **Draft**.

Struktur modul dapat berubah apabila ditemukan kebutuhan baru atau keputusan arsitektur yang lebih baik.
