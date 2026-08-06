# Module Map

> Jone Digital Platform (JDP)
>
> Version : 0.1.0 (Foundation)
>
> Status : Draft
>
> Last Update : 2026-08-06

---

# Tujuan

Dokumen ini mendefinisikan seluruh domain dan modul dalam Jone Digital Platform (JDP).

Module Map menjadi acuan utama sebelum perancangan database, API, antarmuka pengguna, maupun implementasi kode.

Semua fitur baru wajib dipetakan ke dalam domain yang sudah ada sebelum diimplementasikan.

---

# Prinsip

Module Map mengikuti prinsip:

- Single Source of Truth
- Single Publisher
- Content First
- Simplicity First
- Universal by Design
- One Data, Many Views

---

# Layer Architecture

JDP dibagi menjadi empat layer utama.

```
Presentation Layer
        │
Business Layer
        │
Core Layer
        │
Data Layer
```

---

# Domain Overview

| Domain | Tujuan |
|----------|---------|
| Core | Pondasi sistem |
| Content | Pengelolaan informasi publik |
| Village | Data identitas desa |
| Service | Layanan digital desa |

---

# CORE

Core adalah fondasi seluruh platform.

Semua domain lain bergantung pada Core.

## Modul

| Modul | Prioritas | Status |
|---------|-----------|--------|
| Settings | 🟢 | Planned |
| User | 🟢 | Planned |
| Role | 🟢 | Planned |
| Permission | 🟢 | Planned |
| Media Library | 🟢 | Planned |
| Audit Log | 🟢 | Planned |
| Search | 🟡 | Planned |
| Backup | 🟡 | Planned |
| Activity Log | 🔵 | Backlog |

---

# CONTENT

Domain untuk seluruh informasi yang dipublikasikan kepada masyarakat.

## Modul

| Modul | Prioritas | Status |
|---------|-----------|--------|
| Berita | 🟢 | Planned |
| Agenda | 🟢 | Planned |
| Pengumuman | 🟢 | Planned |
| Banner | 🟢 | Planned |
| Galeri | 🟢 | Planned |
| Dokumen | 🟢 | Planned |
| Halaman | 🟢 | Planned |
| FAQ | 🟡 | Backlog |

---

# VILLAGE

Domain identitas resmi Desa Jone.

## Modul

| Modul | Prioritas | Status |
|---------|-----------|--------|
| Profil Desa | 🟢 | Planned |
| Pemerintahan | 🟢 | Planned |
| Perangkat Desa | 🟢 | Planned |
| Dusun | 🟢 | Planned |
| RT/RW | 🟢 | Planned |
| Lembaga | 🟢 | Planned |
| APBDes | 🟢 | Planned |
| Potensi Desa | 🟢 | Planned |
| UMKM | 🟡 | Backlog |
| Wisata | 🔵 | Future |

---

# SERVICE

Domain layanan digital.

Tidak menjadi prioritas pada versi pertama.

## Modul

| Modul | Prioritas | Status |
|---------|-----------|--------|
| Statistik | 🟡 | Planned |
| Surat | 🔵 | Future |
| Pengaduan | 🔵 | Future |
| Tracking | 🔵 | Future |
| Posyandu | 🔵 | Future |
| PKK | 🔵 | Future |
| Karang Taruna | 🔵 | Future |
| BUMDes | 🔵 | Future |

---

# Prioritas Versi

## Version 1.0

Core

Content

Village

---

## Version 1.5

Search

Backup

FAQ

UMKM

Statistik

---

## Version 2.x

Surat

Pengaduan

Tracking

API

Android

TV Informasi

---

# Aturan

1. Semua modul harus berada di dalam satu domain.

2. Tidak boleh ada modul yang berdiri sendiri.

3. Semua data publik berasal dari Domain Content.

4. Semua aset digital berasal dari Media Library.

5. Semua konfigurasi berasal dari Settings.

6. Semua perubahan penting dicatat oleh Audit Log.

---

# Catatan

Module Map merupakan living document.

Perubahan hanya boleh dilakukan apabila terdapat Architecture Decision Record (ADR) yang menjelaskan alasan perubahan tersebut.