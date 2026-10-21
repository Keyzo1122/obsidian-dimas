# Arsitektur Server & Infrastruktur Hermes

Rincian sistem infrastruktur hosting dan otomasi yang menopang operasional bisnis Mas Dimas.

## 1. Spesifikasi Server
- **Platform**: Sumopod VPS (Ubuntu 24.04 LTS, 2 vCPU / 8 GB RAM).
- **Zona Waktu**: WIB (UTC+7).
- **Kapasitas RAM**: Bebas sekitar ~4 GB. *Pencegahan: Hindari beberapa proses render video bersamaan.*

## 2. Jaringan & Domain (Tailscale Private Network)
- **app.keyzo.my.id**: Pusat Kendali Sistem.
- **hermes.keyzo.my.id**: Dasbor Utama Hermes.
- **router.keyzo.my.id**: 9Router (Penyedia perutean model AI).
- **media.keyzo.my.id**: Folder sementara publik untuk Repliz (/srv/media).
- **keyzo.my.id / www**: Website milik Mas Dimas (zona terproteksi).

## 3. Otomasi Distribusi Konten (Repliz)
- **Kredensial**: Dikelola eksklusif oleh **Jay - Production & Publishing Specialist**.
- **Platform Terhubung**: Facebook, TikTok, Instagram, Threads.
- **Prosedur Unggah**: Ken kirim pratinjau -> Mas Dimas setujui -> Ken tugaskan Jay via Kanban -> Jay render JPEG q90 -> salin ke `/srv/media` -> jadwalkan (+2 menit WIB) -> pantau sukses -> bersihkan `/srv/media`.
