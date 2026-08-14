# Entity: Operator

**Status:** Draft

**Versi:** 0.1

---

## Tujuan

Operator adalah pengelola yang dipercaya dan bertanggung jawab kepada Kantor Desa untuk mengendalikan isi dan pengelolaan Jone Digital Platform (JDP).

Operator menjadi jalur resmi pengelolaan dan publikasi informasi yang mewakili Kantor Desa secara online.

---

## Definisi

Operator adalah pengguna internal yang memiliki akses untuk masuk ke panel pengelolaan JDP dan menjalankan kewenangan sesuai Role yang dimilikinya.

JDP memungkinkan terdapat beberapa Operator dalam satu sistem.

---

## Akun Operator

Setiap Operator **wajib memiliki akun sendiri**.

Akun tidak boleh digunakan bersama oleh beberapa orang.

Dengan demikian, setiap tindakan yang dilakukan di dalam sistem dapat dikaitkan dengan Operator yang melakukannya.

---

## Kewenangan

Kewenangan Operator ditentukan oleh Role.

Role awal JDP:

* Administrator
* Editor

Satu Operator memiliki satu Role.

---

## Prinsip Pengelolaan

* Operator merupakan jalur resmi publikasi JDP.
* Informasi dari berbagai pihak di lingkungan desa tetap melalui Operator sebelum dipublikasikan.
* Setiap Operator menggunakan akun pribadi.
* Beberapa Operator dapat bekerja dalam satu sistem.
* Setiap Operator bekerja sesuai Role yang diberikan.
* Operator bertanggung jawab menjaga konsistensi dan representasi informasi resmi desa.

---

## Catatan

Pengaturan hak akses secara lebih rinci akan dibahas pada Permission.

Pencatatan aktivitas Operator akan dibahas pada Audit Log.

Mekanisme autentikasi dan keamanan akun akan dibahas pada tahap implementasi.

Struktur database belum dibahas dalam dokumen ini.

| # | Attribute  | Required | Makna                                      |
| - | ---------- | -------- | ------------------------------------------ |
| 1 | `id`       | Ya       | Pengenal unik Operator bagi sistem         |
| 2 | `name`     | Ya       | Nama orang yang dikenali manusia           |
| 3 | `username` | Ya       | Nama unik untuk berinteraksi dengan sistem |
| 4 | `password` | Ya       | Kredensial untuk autentikasi               |
| 5 | `role_id`  | Ya       | Role yang melekat pada Operator            |
