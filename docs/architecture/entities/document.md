# Entity: Dokumen

**Status:** Draft

**Versi:** 0.1

---

## Tujuan

Dokumen digunakan untuk mengelola dan menyediakan produk resmi Kantor Desa Jone dalam bentuk dokumen yang dapat dipublikasikan, digunakan, atau menjadi bagian dari proses pelayanan dan komunikasi resmi dengan masyarakat.

---

## Definisi

Dokumen adalah produk resmi Kantor Desa yang memiliki bentuk, isi, atau format tertentu dan digunakan untuk kebutuhan administrasi, informasi, pelayanan, atau proses resmi lainnya.

Dokumen dapat bersifat:

* **Satu arah**, yaitu dokumen yang diterbitkan Desa untuk diketahui atau digunakan oleh masyarakat.
* **Interaktif**, yaitu dokumen yang digunakan dalam proses yang membutuhkan isian, respons, atau feedback dari masyarakat dan memiliki standar tertentu.

---

## Contoh

Dokumen dapat digunakan untuk:

* Peraturan Desa.
* Surat Keputusan.
* Laporan resmi.
* Formulir pelayanan.
* Formulir permohonan.
* Dokumen persyaratan.
* Format isian.
* Dokumen publik lainnya.
* Dokumen resmi lainnya yang digunakan dalam proses administrasi desa.

---

## Arah Penggunaan

### Desa → Masyarakat

Dokumen diterbitkan untuk:

* Dibaca.
* Diketahui.
* Diunduh.
* Digunakan sebagai referensi.

### Desa ↔ Masyarakat

Dokumen digunakan sebagai bagian dari proses yang membutuhkan:

* Isian.
* Respons.
* Feedback.
* Pemenuhan persyaratan tertentu.

---

| # | Attribute     | Required | Makna                                |
| - | ------------- | -------- | ------------------------------------ |
| 1 | `id`          | Ya       | Pengenal unik Document bagi sistem   |
| 2 | `title`       | Ya       | Pengenal/judul Document bagi pembaca |
| 3 | `file_path`   | Ya       | Jalur/lokasi file Document           |
| 4 | `type`        | Ya       | Jenis file Document                  |
| 5 | `description` | Tidak    | Gambaran singkat Document            |
| 6 | `status`      | Ya       | `draft`, `published`, `archived`     |
| 7 | `uploaded_by` | Ya       | Siapa yang mengunggah                |
| 8 | `uploaded_at` | Ya       | Kapan diunggah                       |
