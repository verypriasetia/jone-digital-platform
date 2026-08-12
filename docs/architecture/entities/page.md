# Entity: Halaman

**Status:** Draft

**Versi:** 0.1

---

## Tujuan

Halaman digunakan untuk memberikan gambaran dan informasi paling mendasar mengenai Desa Jone.

---

## Definisi

Halaman adalah entity yang mendeskripsikan informasi yang bersifat **baku, mendasar, dan tidak temporer** mengenai suatu profil atau bagian dari Desa.

Halaman menjadi tempat untuk menyampaikan informasi yang diharapkan tetap tersedia dan dapat menjadi rujukan dalam jangka panjang.

---

## Contoh

Halaman dapat digunakan untuk:

- Profil Desa.
- Sejarah Desa.
- Visi dan Misi.
- Gambaran wilayah desa.
- Struktur pemerintahan.
- Informasi dasar desa.
- Informasi profil lainnya yang bersifat mendasar.

---

## Karakteristik

Halaman pada umumnya:

- Bersifat baku.
- Bersifat mendasar.
- Tidak terikat pada suatu kejadian tertentu.
- Tidak memiliki masa berlaku seperti Pengumuman.
- Tidak digunakan untuk mendokumentasikan peristiwa seperti Berita.

---

## Perbedaan dengan Content Lain

**Halaman** → informasi mendasar dan tidak temporer.

**Berita** → informasi mengenai sesuatu yang sudah terjadi.

**Pengumuman** → informasi yang akan terjadi atau masih berlaku.

**Agenda** → rencana kegiatan yang akan dilakukan.

---

## Domain

**Content**

---

## Struktur Atribut V1

Struktur atribut Page V1:

| Attribute | Makna | Required | Tipe Konseptual |
|---|---|---|---|
| `id` | Pengenal unik Page | Ya | Identifier |
| `title` | Judul yang dibaca oleh orang | Ya | Text |
| `slug` | Nama/identitas yang digunakan pada URL halaman | Ya | Text |
| `content` | Isi utama dari sebuah Page | Ya | Text |
| `status` | Keadaan publikasi Page | Ya | Status |
| `created_by` | Operator/User yang membuat Page | Ya | User reference |
| `created_at` | Waktu pembuatan Page | Ya | DateTime |
| `updated_by` | Operator/User yang terakhir mengubah Page | Ya | User reference |
| `updated_at` | Waktu terakhir perubahan Page | Ya | DateTime |

### Status V1

Status Page pada V1:

- `draft`
- `published`

`draft` berarti Page masih disiapkan dan belum ditampilkan kepada masyarakat.

`published` berarti Page telah dipublikasikan dan dapat dilihat oleh masyarakat.

### Catatan Atribut

`created_by` dan `created_at` menunjukkan siapa dan kapan Page dibuat.

`updated_by` dan `updated_at` menunjukkan siapa dan kapan terakhir kali Page diubah.

Atribut tersebut merupakan metadata sistem dan berbeda dari informasi historis atau substansial yang terdapat di dalam `content`.

---

## Catatan

Satu Halaman dapat diperbarui apabila informasi dasarnya berubah. Perubahan tersebut tidak menjadikan Halaman sebagai Berita.

Media yang hanya digunakan di dalam isi Page untuk sementara diperlakukan sebagai bagian dari `content`. Relationship Page–Media khusus belum dibuat pada V1.

Struktur database belum dibahas dalam dokumen ini.
