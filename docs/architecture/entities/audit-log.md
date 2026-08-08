# Entity: Audit Log

**Status:** Draft

**Versi:** 0.1

---

## Tujuan

Audit Log digunakan untuk mencatat tindakan penting yang dilakukan oleh Operator di dalam Jone Digital Platform (JDP).

---

## Definisi

Audit Log adalah catatan aktivitas Operator yang berkaitan dengan perubahan atau tindakan penting terhadap data di dalam JDP.

Audit Log membantu mengetahui:

* Siapa yang melakukan tindakan.
* Tindakan apa yang dilakukan.
* Data atau objek yang terkena tindakan.
* Kapan tindakan dilakukan.

---

## Tindakan yang Dicatat

Pada tahap awal, Audit Log mencatat tindakan yang:

* Membuat data.
* Mengubah data.
* Menghapus data.
* Mempublikasikan data.

---

## Tindakan yang Tidak Dicatat

Aktivitas yang hanya bersifat melihat atau membaca tidak perlu dicatat sebagai Audit Log.

Contohnya:

* Membuka dashboard.
* Membuka daftar berita.
* Melihat halaman.
* Membaca data.

---

## Contoh

```text
Operator : Ahmad
Tindakan : Mempublikasikan
Objek    : Berita "Gotong Royong Desa"
Waktu    : 8 Agustus 2026, 10:15
```

---

## Prinsip

* Audit Log tidak digunakan sebagai tempat penyimpanan konten.
* Audit Log digunakan sebagai catatan aktivitas penting.
* Catatan Audit Log dikaitkan dengan akun Operator yang melakukan tindakan.
* Audit Log membantu menjaga akuntabilitas pengelolaan JDP.

---

## Domain

**Core**

---

## Catatan

Detail data yang dicatat dalam setiap Audit Log dan mekanisme penyimpanannya akan ditentukan pada tahap implementasi.

Struktur database belum dibahas dalam dokumen ini.
