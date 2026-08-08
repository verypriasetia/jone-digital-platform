# Entity: Permission

**Status:** Draft

**Versi:** 0.1

---

## Tujuan

Permission digunakan untuk menentukan tindakan yang dapat dilakukan oleh setiap Role dalam Jone Digital Platform (JDP).

---

## Definisi

Permission adalah kewenangan terhadap tindakan tertentu di dalam JDP.

Permission berbeda dengan Role.

* **Role** menentukan kelompok kewenangan seorang Operator.
* **Permission** menentukan tindakan yang boleh dilakukan.

---

## Permission Konten

Untuk konten, tindakan dasar yang digunakan pada tahap awal adalah:

* Melihat
* Membuat
* Mengubah
* Menghapus
* Mempublikasikan

---

## Editor

Editor memiliki kewenangan untuk mengelola konten website, meliputi:

* Berita
* Pengumuman
* Agenda
* Galeri
* Dokumen
* Halaman

Editor dapat:

* Melihat konten.
* Membuat konten.
* Mengubah konten.
* Menghapus konten.
* Mempublikasikan konten.

Editor dapat langsung mempublikasikan konten tanpa menunggu persetujuan Administrator.

---

## Administrator

Administrator memiliki kewenangan pengelolaan JDP secara keseluruhan.

Administrator memiliki kewenangan Editor dan tambahan kewenangan untuk:

* Mengelola Operator.
* Mengelola Role dan Permission.
* Mengelola konfigurasi utama sistem.
* Melihat Audit Log.

---

## Prinsip

* Permission diberikan berdasarkan kebutuhan Role.
* Editor tidak memerlukan persetujuan Administrator untuk mempublikasikan konten.
* Pengelolaan konten tetap berada dalam jalur Operator.
* Setiap tindakan Operator dapat dikaitkan dengan akun Operator yang melakukan tindakan tersebut.

---

## Catatan

Rincian Permission per fitur dapat dikembangkan apabila kebutuhan JDP bertambah.

Struktur database dan mekanisme teknis Permission belum dibahas dalam dokumen ini.
