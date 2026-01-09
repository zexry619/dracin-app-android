# 📱 Dracin - Short Drama Streaming App

<div align="center">

**Nonton short drama dari berbagai platform dalam satu aplikasi**

[![Download APK](https://img.shields.io/badge/Download-APK-blue.svg?style=for-the-badge)](https://github.com/zexry619/dracin-app-android/releases/latest)
[![Latest Version](https://img.shields.io/badge/version-1.0.19-blue.svg?style=for-the-badge)](https://github.com/zexry619/dracin-app-android/releases)
[![License](https://img.shields.io/badge/License-Proprietary-red.svg?style=for-the-badge)](LICENSE)

</div>

---

## 📖 Tentang Aplikasi

**Dracin** adalah aplikasi Android untuk streaming dan download short drama dari berbagai platform populer. Aplikasi ini mengintegrasikan konten dari **DramaBox**, **Melolo**, dan **NetShort** dalam satu interface yang mudah digunakan.

### ✨ Fitur Utama

#### 🎬 **Multi-Platform Support**
- **DramaBox** - Trending, Latest, VIP, Dubbed Indonesia
- **Melolo** - Drama series dan trending content
- **NetShort** - Explore, For You, dan Trending shorts
- Akses semua platform tanpa perlu install banyak aplikasi

#### 📺 **Video Streaming**
- Video player dengan kontrol kualitas (360p, 480p, 720p, 1080p)
- Auto quality selection berdasarkan koneksi
- Subtitle support (jika tersedia)
- Keep screen awake saat menonton
- Continue watching dari terakhir ditonton

#### 💾 **Download & Offline**
- Download episode untuk ditonton offline
- Batch download (dalam pengembangan)
- Manajemen storage dengan info penggunaan
- Background download dengan notifikasi progress

#### 🔍 **Browse & Discovery**
- Search across semua platform
- Trending & Latest updates
- Filter by category (VIP, Dubbed, dll)
- Random drama suggestion

#### ⭐ **Library Management**
- Favorites - simpan drama favorit
- Watch History - track progress menonton
- Continue Watching - lanjutkan dari episode terakhir
- Library untuk koleksi pribadi

#### � **Auto Update**
- Cek update otomatis dari GitHub Releases
- In-app update notification
- Version comparison dan changelog

---

## 📥 Download & Instalasi

### Download APK Terbaru

<div align="center">

### [📥 Download Latest Release](https://github.com/zexry619/dracin-app-android/releases/latest)

**Current Version: 1.0.19**

</div>

### Cara Instalasi

1. **Download APK** dari link di atas
2. **Enable Unknown Sources**:
   - Buka `Settings` → `Security` → Enable `Unknown Sources` atau `Install Unknown Apps`
3. **Install APK** yang sudah di-download
4. **Buka aplikasi** dan mulai streaming! 🎬

> ⚠️ **Note**: Aplikasi ini tidak tersedia di Google Play Store karena merupakan third-party client.

### System Requirements

- Android 5.0 (Lollipop) atau lebih tinggi
- Minimum 100MB storage untuk aplikasi
- Koneksi internet untuk streaming
- Storage tambahan jika ingin download offline

---

## 🛠️ Tech Stack

Aplikasi ini dibangun dengan teknologi modern:

### Core Framework
- **Flutter 3.4+** - Cross-platform framework
- **Dart 3.4+** - Programming language
- **Riverpod 2.5** - State management

### Key Dependencies
- **dio 5.4** - HTTP client untuk API calls
- **go_router 14.0** - Declarative routing
- **chewie 1.8** - Video player wrapper
- **video_player 2.8** - Video playback engine
- **hive 2.2** - Local NoSQL database untuk downloads
- **cached_network_image 3.3** - Image caching
- **google_fonts 6.2** - Custom typography
- **flutter_local_notifications 17.0** - Download notifications
- **wakelock_plus 1.2** - Keep screen on during playback

### Backend
- **Next.js API** (`https://dracinzek.vercel.app/api`) - Custom backend proxy untuk:
  - DramaBox API integration
  - Melolo API integration  
  - NetShort API integration
  - Video URL processing
  - CORS handling

---

## 🏗️ Arsitektur

Aplikasi menggunakan **Clean Architecture** dengan layer separation:

```
lib/
├── core/
│   ├── constants/     # API endpoints & app constants
│   ├── network/       # Dio client & interceptors
│   ├── router/        # GoRouter configuration
│   ├── services/      # Update service, video proxy
│   ├── theme/         # App theming (dark mode)
│   └── widgets/       # Reusable widgets
│
└── features/
    ├── home/          # Home screen dengan trending
    ├── trending/      # Trending dari semua platform
    ├── category/      # VIP, Dubbed categories
    ├── search/        # Search & search history
    ├── drama_detail/  # Detail drama & episode list
    ├── video_player/  # Video playback & controls
    ├── downloads/     # Download management
    ├── favorites/     # Favorite dramas
    ├── library/       # Personal library
    ├── history/       # Watch history
    └── shorts/        # Short-form content
```

### State Management Pattern
- **Riverpod Providers** untuk dependency injection
- **AsyncNotifier** untuk async state
- **StateNotifier** untuk local state
- Repository pattern untuk data layer

---

## 🎯 Fitur Detail

### Platform Integration

| Platform | Endpoints | Features |
|----------|-----------|----------|
| **DramaBox** | `/dramabox/*` | Trending, Latest, Search, VIP, Dubbed Indonesia, Random |
| **Melolo** | `/melolo/*` | Trending, Latest, Detail, Stream, Search |
| **NetShort** | `/netshort/*` | Explore, Trending, For You, Search, Detail |

### Video Quality Options
- **Auto** - Pilih kualitas otomatis berdasarkan koneksi
- **1080p** - Full HD (jika tersedia)
- **720p** - HD
- **480p** - SD
- **360p** - Low quality untuk koneksi lambat

### Download System
- Menggunakan **Hive** untuk local database
- Support pause/resume downloads
- Background download dengan notification
- Storage management dashboard
- Offline playback dari local storage

---

## 📸 Screenshots

> Screenshots akan ditambahkan setelah release

---

## ❓ FAQ

### Apakah aplikasi ini gratis?
Ya, 100% gratis tanpa biaya berlangganan.

### Apakah aman digunakan?
Ya, source code di-build otomatis via GitHub Actions. Tidak ada tracking atau data collection.

### Kenapa tidak ada di Play Store?
Aplikasi ini adalah third-party client yang mengakses konten dari platform lain, tidak sesuai dengan kebijakan Play Store.

### Bagaimana cara update aplikasi?
Aplikasi akan otomatis cek update dari GitHub Releases dan memberi notifikasi jika ada versi baru.

### Konten tidak bisa diputar / error streaming?
- Pastikan koneksi internet stabil
- Coba ganti quality video ke yang lebih rendah
- Beberapa konten VIP mungkin tidak bisa diakses
- Report bug via GitHub Issues jika masalah persisten

### Aplikasi crash atau force close?
Report bug di [GitHub Issues](https://github.com/zexry619/dracin-app-android/issues) dengan informasi:
- Android version
- App version
- Screenshot error (jika ada)
- Steps untuk reproduce bug

---

## 🚀 Roadmap

- [x] ✅ Multi-platform streaming (DramaBox, Melolo, NetShort)
- [x] ✅ Video quality selection
- [x] ✅ Download & offline playback
- [x] ✅ Favorites & watch history
- [x] ✅ Auto update checker
- [ ] 🔨 Batch download multiple episodes
- [ ] 🔨 Subtitle customization (size, position)
- [ ] 🔨 Picture-in-Picture (PiP) mode
- [ ] 🔨 Chromecast support
- [ ] 🔨 User reviews & ratings
- [ ] 🔨 Cloud sync favorites

---

## � Privacy

- ✅ Tidak ada tracking analytics
- ✅ Tidak ada pengumpulan data pribadi
- ✅ Semua data tersimpan lokal di device
- ✅ Koneksi ke API menggunakan HTTPS
- ✅ Source build public via GitHub Actions

---

## 📞 Support

- **Bug Reports**: [GitHub Issues](https://github.com/zexry619/dracin-app-android/issues)
- **Feature Requests**: [GitHub Issues](https://github.com/zexry619/dracin-app-android/issues)
- **Discussions**: [GitHub Discussions](https://github.com/zexry619/dracin-app-android/discussions)

---

## 📜 License

Copyright © 2026 Dracin. All rights reserved.

Aplikasi ini adalah **proprietary software**. Hanya binary releases (APK) yang dipublikasikan. Source code tetap private.

---

## ⚠️ Disclaimer

Aplikasi ini adalah **third-party client** dan **tidak berafiliasi** dengan DramaBox, Melolo, NetShort, atau platform konten lainnya. 

Semua konten (video, gambar, metadata) adalah properti dari pemilik masing-masing platform. Aplikasi ini hanya menyediakan interface alternatif untuk mengakses konten yang sudah tersedia secara publik.

---

## 🙏 Credits

Built with ❤️ using **Flutter**

Backend API: [dracinzek.vercel.app](https://dracinzek.vercel.app)

---

<div align="center">

**⭐ Star repository ini jika aplikasi ini berguna untuk Anda!**

[Download Latest Release](https://github.com/zexry619/dracin-app-android/releases/latest) • [Report Bug](https://github.com/zexry619/dracin-app-android/issues) • [Request Feature](https://github.com/zexry619/dracin-app-android/issues)

</div>

---

## 📦 Release History

### [v1.0.24](./releases/v1.0.24/) - 2026-01-09
- [Download APK](./releases/v1.0.24/dracin-v1.0.24.apk) (25M)
- [View Changelog](./releases/v1.0.24/CHANGELOG.md)


### [v1.0.24](./releases/v1.0.24/) - 2026-01-08
- [Download APK](./releases/v1.0.24/dracin-v1.0.24.apk) (25M)
- [View Changelog](./releases/v1.0.24/CHANGELOG.md)


### [v1.0.22](./releases/v1.0.22/) - 2026-01-08
- [Download APK](./releases/v1.0.22/dracin-v1.0.22.apk) (25M)
- [View Changelog](./releases/v1.0.22/CHANGELOG.md)


### [v1.0.22](./releases/v1.0.22/) - 2026-01-07
- [Download APK](./releases/v1.0.22/dracin-v1.0.22.apk) (25M)
- [View Changelog](./releases/v1.0.22/CHANGELOG.md)


### [v1.0.22](./releases/v1.0.22/) - 2026-01-06
- [Download APK](./releases/v1.0.22/dracin-v1.0.22.apk) (25M)
- [View Changelog](./releases/v1.0.22/CHANGELOG.md)


### [v1.0.21](./releases/v1.0.21/) - 2026-01-06
- [Download APK](./releases/v1.0.21/dracin-v1.0.21.apk) (25M)
- [View Changelog](./releases/v1.0.21/CHANGELOG.md)


### [v1.0.20](./releases/v1.0.20/) - 2026-01-06
- [Download APK](./releases/v1.0.20/dracin-v1.0.20.apk) (25M)
- [View Changelog](./releases/v1.0.20/CHANGELOG.md)


### [v1.0.20](./releases/v1.0.20/) - 2026-01-06
- [Download APK](./releases/v1.0.20/dracin-v1.0.20.apk) (25M)
- [View Changelog](./releases/v1.0.20/CHANGELOG.md)


### [v1.0.19](./releases/v1.0.19/) - 2026-01-06
- [Download APK](./releases/v1.0.19/dracin-v1.0.19.apk) (25M)
- [View Changelog](./releases/v1.0.19/CHANGELOG.md)


### [v1.0.19](./releases/v1.0.19/) - 2026-01-06
- [Download APK](./releases/v1.0.19/dracin-v1.0.19.apk) (25M)
- [View Changelog](./releases/v1.0.19/CHANGELOG.md)


