# Sehatin — Interactive Health App Prototype

Prototype aplikasi kesehatan **Sehatin** dengan desain mobile dan fitur interaktif berbasis HTML/CSS/JavaScript murni (tanpa framework, tanpa build step) — cocok untuk deployment langsung ke GitHub Pages.

## ✨ Fitur
- Splash screen
- **Login & Register dengan validasi form** (email, password min. 6 karakter, konfirmasi password)
- Akun demo satu-klik untuk mempermudah proses penilaian/demo
- Dashboard / Home dengan ringkasan status kesehatan terakhir
- Bottom navigation
- Health Check (BMI + skor kesehatan) — **hasil otomatis tersimpan ke Riwayat**
- Pencarian dan filter dokter berdasarkan spesialisasi, dengan **empty state** saat tidak ada hasil
- Detail dokter + ulasan pasien + pilihan jadwal praktik
- **Chat konsultasi interaktif** dengan dokter (balasan otomatis simulasi, riwayat chat tersimpan per dokter)
- Riwayat kesehatan — **bisa tambah & hapus catatan sendiri**
- Pengingat obat — **tambah, aktif/nonaktifkan, dan hapus** pengingat dengan waktu kustom
- **Edit profil** (nama, umur, status)
- Notifikasi tes menggunakan Browser Notification API (dengan fallback toast)
- Light/Dark mode (tersimpan, tetap aktif setelah reload)
- **Semua data disimpan di `localStorage`** — akun, riwayat, pengingat, chat, dan preferensi tetap ada setelah refresh/tutup browser
- Reset data demo (untuk keperluan pengujian ulang)
- Toast feedback & modal konfirmasi di seluruh alur

## 📁 Struktur
```text
Sehatin/
├── index.html
├── README.md
├── .gitignore
└── assets/
    ├── design/
    │   └── design_tokens.json
    └── *.svg
```

## 🚀 Menjalankan secara lokal
Cara paling mudah: buka `index.html` di browser.

Untuk hasil yang lebih mirip deployment web, jalankan local server:
```bash
python -m http.server 8000
```
Lalu buka `http://localhost:8000`.

**Akun demo:** email `alip@sehatin.id`, password `sehatin123` (atau tekan tombol "Gunakan Akun Demo" di halaman login).

## 🌐 Deploy dengan GitHub Pages
1. Buat repository baru di GitHub, misalnya `Sehatin`.
2. Upload seluruh isi folder project ini.
3. Pastikan `index.html` berada di root repository.
4. Buka **Settings → Pages**.
5. Pada **Build and deployment**, pilih **Deploy from a branch**.
6. Pilih branch `main` dan folder `/ (root)`.
7. Simpan dan tunggu proses deployment.
8. GitHub akan memberikan URL Pages untuk prototype.

## 🎨 File desain
Folder `assets/` berisi screen SVG yang bisa diimpor ke Figma dan diedit sebagai vector.

## 💡 Ide pengembangan lanjutan (opsional, untuk nilai tambah)
- Ganti localStorage dengan backend sungguhan (mis. Firebase/Supabase) agar data tersinkron antar perangkat
- Tambahkan grafik tren kesehatan (Chart.js) di halaman Riwayat
- Integrasi push notification asli untuk pengingat obat sesuai jadwal
- Autentikasi dengan Google/OAuth sungguhan

> Catatan: project ini adalah prototype web interaktif, bukan APK native dan bukan file `.fig` native Figma.
