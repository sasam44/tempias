# 🌍 World Clock & Weather — Timer Seluruh Dunia

Web app ceria & penuh warna untuk melihat **waktu real-time di berbagai kota dunia** lengkap dengan **cuaca terkini** dan **prediksi cuaca 7 hari**, dengan **animasi cuaca** (hujan, salju, petir, kabut, awan, dll).

> 🌐 Dibuat khusus dengan dukungan **3 bahasa**: 🇮🇩 Indonesia · 🇬🇧 English · 🇨🇳 中文

## ✨ Fitur

- 🕒 **Jam real-time** untuk **80+ kota** di seluruh dunia (berdasarkan zona waktu masing-masing kota)
- 🗺️ **20+ kota Indonesia** (Jakarta, Surabaya, Bandung, Medan, Makassar, Yogyakarta, Bali, dll.) + kota dunia (Asia, Eropa, Amerika, Oseania, Afrika, Timur Tengah)
- 🕐 **Jam utama besar** yang bisa dipilih dengan mengklik kartu kota
- ⛅ **Cuaca terkini** (suhu, kelembaban, angin, suhu terasa)
- 📈 **Prediksi cuaca per jam** (6 jam ke depan)
- 🗓️ **Prakiraan cuaca 7 hari** (suhu min/max + ikon cuaca)
- 🎨 **Animasi cuaca** langsung di kartu: hujan, salju, petir, kabut, awan melayang
- 🔍 **Pencarian multibahasa**: cari kota pakai nama lokal, Inggris, atau China (mis. ketik "雅加达" → Jakarta, "纽约" → New York)
- 🌐 **Pemilih bahasa** (ID/EN/ZH) — seluruh tampilan dan deskripsi cuaca ikut berubah
- 🌈 **Tampilan ceria penuh warna** dengan blob mengambang, bintang beranimasi, gradien pelangi

## 🚀 Cara Menjalankan

```bash
# Jalankan server statis
npx http-server . -p 8080
# atau
python -m http.server 8080
```

Lalu buka `http://localhost:8080`.

## 📡 Sumber Data

- **Waktu**: Zona waktu standar (IANA tz database) via `Intl.DateTimeFormat`
- **Cuaca**: [**Open-Meteo**](https://open-meteo.com) — API cuaca gratis, open-source, tanpa perlu API key, data dari Met Office, NOAA, dan sumber tepercaya lainnya.

## 🗂️ Struktur

- `index.html` — seluruh aplikasi (HTML + CSS + JS) dalam satu file.

## 🧠 Cara Kerja

1. Aplikasi memuat daftar 80+ kota beserta koordinat, zona waktu, dan nama multibahasa.
2. Untuk setiap kota, memanggil Open-Meteo API untuk data cuaca terkini, per jam, dan harian.
3. Jam diperbarui setiap detik menggunakan zona waktu IANA setiap kota.
4. Kartu kota menampilkan ikon cuaca + animasi sesuai kode cuaca WMO.
5. Klik kartu → modal dengan rincian cuaca & prediksi 7 hari (dalam bahasa terpilih).
6. Pencarian mencocokkan nama kota dalam 3 bahasa + alias (mis. "bali", "纽约", "泗水").

## 🏷️ Ide Judul Lain

- **TimeSync — World Clock & Weather**
- **Tempias 🌧️ — Jam & Cuaca Dunia**
- **EarthTime — Global Clock & Forecast**
- **Chronos 🌍 Real-Time World Time**
- **Cuaca Bumi — Earth Weather & Clock**
- **GlobeTick — Waktu & Cuaca Dunia**
