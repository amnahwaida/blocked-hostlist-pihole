# 🛡️ Pi-hole Blocked Hostlist

[![GitHub](https://img.shields.io/badge/GitHub-amnahwaida-181717?style=flat-square&logo=github)](https://github.com/amnahwaida/blocked-hostlist-pihole)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)
[![Hosts](https://img.shields.io/badge/Total_Domains-25%2C099-red?style=flat-square)]()
[![Lists](https://img.shields.io/badge/Blocklists-18-blue?style=flat-square)]()

Koleksi blocklist yang dikurasi untuk **[Pi-hole](https://pi-hole.net/)** — DNS sinkhole yang melindungi jaringan Anda dari iklan, tracking, malware, dan konten yang tidak diinginkan.

> **Cara pakai:** Salin URL raw file dari GitHub, lalu tambahkan di Pi-hole sebagai **Adlist**.

---

## 📋 Daftar Blocklist

| # | Blocklist | Deskripsi | Jumlah Domain | Raw URL |
|---|-----------|-----------|:-------------:|---------|
| 1 | **ads-tracking** | Iklan & pelacak (Google Ads, Criteo, Taboola, dll) | 138 | [🔗 Link](https://raw.githubusercontent.com/amnahwaida/blocked-hostlist-pihole/main/hosts/ads-tracking) |
| 2 | **ai** | Layanan AI, Chatbots & Generator Gambar (ChatGPT, Claude, dll) | 63 | [🔗 Link](https://raw.githubusercontent.com/amnahwaida/blocked-hostlist-pihole/main/hosts/ai) |
| 3 | **dating-apps** | Aplikasi kencan (MiChat, Tinder, Bumble, Omi, dll) | 52 | [🔗 Link](https://raw.githubusercontent.com/amnahwaida/blocked-hostlist-pihole/main/hosts/dating-apps) |
| 4 | **facebook** | Facebook & layanan Meta | 89 | [🔗 Link](https://raw.githubusercontent.com/amnahwaida/blocked-hostlist-pihole/main/hosts/facebook) |
| 5 | **gambling** | Situs judi & taruhan | 82 | [🔗 Link](https://raw.githubusercontent.com/amnahwaida/blocked-hostlist-pihole/main/hosts/gambling) |
| 6 | **gaming** | Game mobile, PC, web & platform gaming | 468 | [🔗 Link](https://raw.githubusercontent.com/amnahwaida/blocked-hostlist-pihole/main/hosts/gaming) |
| 7 | **instagram** | Instagram & CDN terkait | 117 | [🔗 Link](https://raw.githubusercontent.com/amnahwaida/blocked-hostlist-pihole/main/hosts/instagram) |
| 8 | **malware-phishing** | Malware, cryptominer, phishing | 73 | [🔗 Link](https://raw.githubusercontent.com/amnahwaida/blocked-hostlist-pihole/main/hosts/malware-phishing) |
| 9 | **music-streaming** | Streaming musik (Spotify, Apple Music, Joox) | 65 | [🔗 Link](https://raw.githubusercontent.com/amnahwaida/blocked-hostlist-pihole/main/hosts/music-streaming) |
| 10 | **porn** | Konten dewasa (18+) | 84 | [🔗 Link](https://raw.githubusercontent.com/amnahwaida/blocked-hostlist-pihole/main/hosts/porn) |
| 11 | **snapchat** | Snapchat & Bitmoji | 53 | [🔗 Link](https://raw.githubusercontent.com/amnahwaida/blocked-hostlist-pihole/main/hosts/snapchat) |
| 12 | **social-media** | Semua Sosmed (Termasuk MiChat, Tinder, IG, TikTok, dll) | 7.144 | [🔗 Link](https://raw.githubusercontent.com/amnahwaida/blocked-hostlist-pihole/main/hosts/social-media) |
| 13 | **tiktok** | TikTok & infrastruktur ByteDance | 6.668 | [🔗 Link](https://raw.githubusercontent.com/amnahwaida/blocked-hostlist-pihole/main/hosts/tiktok) |
| 14 | **trading-crypto** | Trading crypto, binary, forex & saham | 122 | [🔗 Link](https://raw.githubusercontent.com/amnahwaida/blocked-hostlist-pihole/main/hosts/trading-crypto) |
| 15 | **twitter** | Twitter/X & layanan terkait | 49 | [🔗 Link](https://raw.githubusercontent.com/amnahwaida/blocked-hostlist-pihole/main/hosts/twitter) |
| 16 | **whatsapp** | WhatsApp messaging | 29 | [🔗 Link](https://raw.githubusercontent.com/amnahwaida/blocked-hostlist-pihole/main/hosts/whatsapp) |
| 17 | **youtube** | YouTube (blok total) | 25 | [🔗 Link](https://raw.githubusercontent.com/amnahwaida/blocked-hostlist-pihole/main/hosts/youtube) |
| 18 | **youtubeAds** | YouTube Ads saja (video tetap jalan) | 16.844 | [🔗 Link](https://raw.githubusercontent.com/amnahwaida/blocked-hostlist-pihole/main/hosts/youtubeAds) |
| 🔰 | **combined** | Semua list digabung (tanpa duplikat) | **25.099** | [🔗 Link](https://raw.githubusercontent.com/amnahwaida/blocked-hostlist-pihole/main/hosts/combined) |

---

## 🚀 Cara Menggunakan

### Langkah 1 — Salin URL Raw

Pilih blocklist yang diinginkan dari tabel di atas, atau gunakan **combined** untuk semuanya sekaligus.

Contoh URL untuk list gabungan:
```
https://raw.githubusercontent.com/amnahwaida/blocked-hostlist-pihole/main/hosts/combined
```

### Langkah 2 — Tambahkan ke Pi-hole

1. Buka **Pi-hole Admin Panel** → `http://<IP_PIHOLE>/admin`
2. Navigasi ke **Group Management** → **Adlists**
3. Paste URL raw di kolom **Address**
4. Klik **Add**
5. Jalankan update:
   ```bash
   pihole -g
   ```

### Langkah 3 — Verifikasi

Cek apakah blocklist berhasil dimuat:
```bash
pihole -g -l
```

---

## 📁 Struktur Project

```
blocked-hostlist-pihole/
├── README.md              # Dokumentasi ini
├── LICENSE                # Lisensi MIT
├── build.sh               # Script untuk generate combined list
├── .gitignore             # Git ignore file
└── hosts/                 # Folder blocklist
    ├── ads-tracking       # Iklan & pelacak
    ├── ai                 # AI bots, ChatGPT, Gemini, dll
    ├── dating-apps        # Aplikasi kencan (MiChat, Tinder, dll)
    ├── facebook           # Facebook/Meta
    ├── gambling           # Judi & taruhan
    ├── gaming             # Game mobile, PC, web
    ├── instagram          # Instagram
    ├── malware-phishing   # Malware & keamanan
    ├── music-streaming    # Spotify, Apple Music, dll
    ├── porn               # Konten dewasa
    ├── snapchat           # Snapchat
    ├── social-media       # Sosmed lain (Reddit, LinkedIn)
    ├── tiktok             # TikTok/ByteDance
    ├── trading-crypto     # Crypto, Binary, Forex
    ├── twitter            # Twitter/X
    ├── whatsapp           # WhatsApp
    ├── youtube            # YouTube (blok total)
    ├── youtubeAds         # YouTube Ads saja
    └── combined           # Gabungan semua (auto-generated)
```

---

## 🔧 Build Script

File `combined` di-generate otomatis menggunakan `build.sh`. Script ini:

- ✅ Menggabungkan semua blocklist ke satu file
- ✅ Menghapus duplikat domain
- ✅ Menambah timestamp generasi
- ✅ Menampilkan statistik

```bash
# Jalankan build script
chmod +x build.sh
./build.sh
```

Output contoh:
```
🔨 Pi-hole Blocklist Builder
============================================
  ✅ ads-tracking (138 entries)
  ✅ ai (63 entries)
  ✅ dating-apps (52 entries)
  ✅ facebook (89 entries)
  ✅ gaming (468 entries)
  ✅ malware-phishing (73 entries)
  ✅ music-streaming (65 entries)
  ✅ snapchat (53 entries)
  ✅ social-media (7144 entries)
  ✅ tiktok (6668 entries)
  ✅ trading-crypto (122 entries)
  ✅ instagram (117 entries)
============================================
📊 Summary:
   Files processed: 18
   Total entries:   32165
   Duplicates:      7066
   Unique entries:  25099
============================================
✨ Done!
```

---

## ⚠️ Peringatan Penting

| Blocklist | Peringatan |
|-----------|------------|
| **facebook** | Akan memblok Facebook Login di situs/aplikasi pihak ketiga |
| **instagram** | Bisa mempengaruhi layanan Facebook (infrastruktur berbagi) |
| **whatsapp** | Memblok SEMUA fungsi WhatsApp termasuk panggilan & pesan |
| **gaming** | Memblok SEMUA platform game termasuk Steam, Discord, dan game online |
| **youtube** | Memblok SEMUA konten YouTube — gunakan `youtubeAds` jika hanya ingin blok iklan |
| **youtubeAds** | YouTube sering mengubah domain iklan, list ini perlu diperbarui secara berkala |

---

## 🎯 Rekomendasi Penggunaan

### 🏠 Rumah dengan Anak (Parental Control)
```
ads-tracking + gambling + gaming + porn + malware-phishing
```

### 🏢 Kantor / Produktivitas
```
ads-tracking + tiktok + instagram + facebook + social-media + twitter + gambling + gaming + trading-crypto + music-streaming
```

### 🎓 Sekolah / Lab Komputer
```
ads-tracking + ai + gaming + porn + gambling + tiktok + instagram + twitter
```

### 🔒 Keamanan Maksimal
```
ads-tracking + malware-phishing + gambling
```

### 🚫 Blok Semuanya
```
combined (semua list dalam satu file)
```

---

## 🤝 Kontribusi

Kontribusi sangat disambut! Cara berkontribusi:

1. **Fork** repository ini
2. Tambahkan domain baru ke file blocklist yang sesuai
3. Pastikan formatnya benar: `0.0.0.0 domain.com`
4. Jalankan `./build.sh` untuk regenerate combined list
5. Buat **Pull Request**

### Format Domain

Setiap baris harus mengikuti format:
```
0.0.0.0 domain.com
```

- Gunakan `0.0.0.0` sebagai prefix (bukan `127.0.0.1`)
- Satu domain per baris
- Komentar diawali dengan `#`
- Tidak ada trailing whitespace

---

## 📄 Lisensi

Project ini dilisensikan di bawah [MIT License](LICENSE).

---

## ⭐ Dukung Project Ini

Jika blocklist ini berguna untuk Anda, berikan ⭐ **star** di GitHub!

---

<p align="center">
  <b>Dibuat dengan ❤️ untuk komunitas Pi-hole Indonesia</b><br>
  <sub>Last updated: 2026-03-29</sub>
</p>