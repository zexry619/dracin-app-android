# 📱 Dracin - Drama & Novel Reader App

<div align="center">

![Dracin Logo](https://via.placeholder.com/150x150/6366f1/ffffff?text=DRACIN)

**Platform Terbaik untuk Membaca Novel dan Menonton Drama Favoritmu**

[![Download APK](https://img.shields.io/badge/Download-APK-blue.svg?style=for-the-badge)](https://github.com/zexry619/dracin-app-android/releases/latest)
[![Latest Version](https://img.shields.io/github/v/release/zexry619/dracin-app-android?style=for-the-badge)](https://github.com/zexry619/dracin-app-android/releases)
[![License](https://img.shields.io/badge/License-Proprietary-red.svg?style=for-the-badge)](LICENSE)

</div>

---

## 📖 Tentang Aplikasi

**Dracin** adalah aplikasi Android yang memungkinkan Anda untuk membaca novel dan menonton drama dengan pengalaman yang lebih baik dan gratis. Aplikasi ini mengintegrasikan konten dari berbagai platform populer seperti DramaBox, ReelShort, dan platform lainnya dalam satu aplikasi yang mudah digunakan.

### ✨ Fitur Utama

#### 📚 **Baca Novel & Drama**
- Akses ke ribuan novel dan drama dari berbagai genre
- Baca semua episode/chapter secara gratis
- Interface yang bersih dan mudah digunakan
- Mode baca yang nyaman untuk mata

#### 🎬 **Tonton Drama Video**
- Streaming drama dalam format video (short drama)
- Kualitas video HD
- Player built-in dengan kontrol penuh
- Download video untuk ditonton offline

#### 🔍 **Pencarian & Eksplorasi**
- Cari konten berdasarkan judul, genre, atau keyword
- Rekomendasi konten populer (Hot/Trending)
- Latest releases - selalu update dengan konten terbaru
- Filter berdasarkan kategori (VIP, Dubbed, dll)

#### ⭐ **Library & Bookmark**
- Simpan konten favorit ke library pribadi
- Bookmark chapter/episode terakhir yang dibaca/ditonton
- History untuk melacak konten yang pernah dibuka
- Sinkronisasi progress membaca

#### 🎨 **Pengalaman Pengguna**
- Dark mode & light mode support
- Customizable reading settings (font, ukuran, spacing)
- Smooth scrolling dan navigation
- Offline reading untuk konten yang sudah di-download

#### 🔔 **Notifikasi**
- Notifikasi untuk episode/chapter baru
- Update berkala untuk konten favorit
- Pengingat untuk melanjutkan membaca

---

## 📥 Download & Instalasi

### Download APK Terbaru

Klik tombol di bawah untuk download versi terbaru:

<div align="center">

### [📥 Download Latest APK](https://github.com/zexry619/dracin-app-android/releases/latest/download/dracin-latest.apk)

</div>

atau lihat [semua versi rilis](https://github.com/zexry619/dracin-app-android/releases)

### Cara Instalasi

1. **Download APK** dari link di atas
2. **Enable Unknown Sources** di pengaturan Android Anda:
   - Buka `Settings` → `Security` → Enable `Unknown Sources` atau `Install Unknown Apps`
3. **Buka file APK** yang sudah di-download
4. **Tap Install** dan tunggu hingga selesai
5. **Buka aplikasi** dan mulai menikmati konten!

> ⚠️ **Catatan**: Aplikasi ini tidak tersedia di Google Play Store. Download hanya melalui GitHub Releases resmi.

---

## 🛠️ Teknologi & Arsitektur

### Tech Stack

- **Framework**: Flutter 3.x
- **Language**: Dart
- **State Management**: Provider / Riverpod / Bloc (sesuai implementasi)
- **Database**: SQLite / Hive untuk local storage
- **Networking**: Dio / http untuk API requests
- **Video Player**: video_player / better_player
- **UI Components**: Material Design 3

### Arsitektur Aplikasi

```
┌─────────────────────────────────────────┐
│         Presentation Layer              │
│  (UI Screens, Widgets, Pages)           │
└──────────────┬──────────────────────────┘
               │
┌──────────────▼──────────────────────────┐
│         Application Layer               │
│  (State Management, BLoC/Provider)      │
└──────────────┬──────────────────────────┘
               │
┌──────────────▼──────────────────────────┐
│          Domain Layer                   │
│  (Business Logic, Use Cases, Models)    │
└──────────────┬──────────────────────────┘
               │
┌──────────────▼──────────────────────────┐
│           Data Layer                    │
│  (API Services, Local DB, Repositories) │
└─────────────────────────────────────────┘
```

### Integrasi API

Aplikasi ini terintegrasi dengan:
- **DramaBox API** - untuk konten drama dan novel
- **ReelShort API** - untuk short drama series
- **Custom Backend API** - untuk fitur tambahan dan caching

---

## 📋 Roadmap & Fitur Mendatang

- [ ] 🎯 Download batch untuk multiple episodes
- [ ] 💬 Kolom komentar dan review
- [ ] 👥 Sistem user profile dan rating
- [ ] 🌐 Multi-language support (EN, ID, CN)
- [ ] 📊 Statistik membaca (total waktu, chapter dibaca, dll)
- [ ] 🎨 Custom themes dan color schemes
- [ ] 🔄 Cloud sync untuk backup data
- [ ] 📱 Tablet optimization dan landscape mode

---

## 🔒 Privacy & Security

- ✅ Tidak mengumpulkan data pribadi pengguna
- ✅ Tidak ada tracking atau analytics pihak ketiga
- ✅ Data lokal tersimpan aman di perangkat Anda
- ✅ Koneksi API menggunakan HTTPS
- ✅ Open source releases untuk transparansi

---

## 📸 Screenshots

<div align="center">

| Home Screen | Library | Reader |
|-------------|---------|--------|
| ![Home](https://via.placeholder.com/250x500/6366f1/ffffff?text=Home) | ![Library](https://via.placeholder.com/250x500/8b5cf6/ffffff?text=Library) | ![Reader](https://via.placeholder.com/250x500/a78bfa/ffffff?text=Reader) |

</div>

---

## ❓ FAQ

### Apakah aplikasi ini gratis?
Ya, aplikasi Dracin 100% gratis dan tidak ada biaya berlangganan.

### Apakah aman untuk digunakan?
Ya, aplikasi ini aman. Kami tidak mengumpulkan data pribadi dan semua releases di-build secara otomatis melalui GitHub Actions.

### Kenapa tidak ada di Play Store?
Aplikasi ini bersifat third-party dan mengakses konten dari platform lain, sehingga tidak memenuhi policy Google Play Store.

### Bagaimana cara update aplikasi?
Cek GitHub Releases secara berkala atau aktifkan notifikasi GitHub untuk repository ini.

### Aplikasi crash atau ada bug, bagaimana cara report?
Silakan buat issue di [GitHub Issues](https://github.com/zexry619/dracin-app-android/issues) dengan detail error dan screenshot.

---

## 📞 Kontak & Support

- **Issues**: [GitHub Issues](https://github.com/zexry619/dracin-app-android/issues)
- **Discussions**: [GitHub Discussions](https://github.com/zexry619/dracin-app-android/discussions)
- **Email**: support@dracin.app (jika ada)

---

## 📜 License

Copyright © 2026 Dracin. All rights reserved.

Aplikasi ini adalah proprietary software. Source code tidak dipublikasikan, hanya distribusi binary (APK) yang tersedia untuk penggunaan pribadi.

---

## 🙏 Credits

Dibuat dengan ❤️ menggunakan Flutter

**Disclaimer**: Aplikasi ini adalah third-party client dan tidak berafiliasi dengan DramaBox, ReelShort, atau platform konten lainnya. Semua konten adalah properti dari pemilik masing-masing.

---

<div align="center">

**⭐ Star repository ini jika Anda merasa aplikasi ini berguna!**

[Download Latest Release](https://github.com/zexry619/dracin-app-android/releases/latest) • [Report Bug](https://github.com/zexry619/dracin-app-android/issues) • [Request Feature](https://github.com/zexry619/dracin-app-android/issues)

</div>
