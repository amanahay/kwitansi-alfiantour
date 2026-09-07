# Kwitansi Alfian Tour (PWA)

Aplikasi Web Progresif (PWA) untuk pembuatan, pengelolaan, dan pencetakan Kwitansi Pembayaran Haji dan Umroh **PT. Alfian Sejahtera Abadi**.

Aplikasi ini dapat berjalan langsung di browser, diinstal di HP/Desktop layaknya aplikasi native, dan dapat digunakan secara offline tanpa koneksi internet.

---

## ✨ Fitur Utama

- **Progressive Web App (PWA):** Dapat diinstal di Android (Chrome/Edge), iOS (Safari - *Add to Home Screen*), maupun Desktop.
- **Offline Mode:** Menggunakan Service Worker untuk caching asset statis sehingga aplikasi tetap berfungsi walau tanpa internet.
- **Penyimpanan Lokal (CRUD):** Simpan, ubah, buka kembali, dan hapus draft kwitansi langsung di browser via `localStorage`.
- **Perhitungan Otomatis:** Menghitung total, sisa tagihan/pelunasan, serta konversi angka ke terbilang otomatis.
- **Cetak & Export PDF:** Template ukuran cetak kwitansi standar A4/format faktur yang rapi dan siap cetak.
- **Stempel canvas:** Tambahkan beberapa stempel transparan, geser ke seluruh area halaman, dan ubah ukurannya dengan handle.
- **Export/Import JSON:** Manajemen dapat mengirim file JSON; penerima dapat mengimpor dan melihat dokumen dalam mode hanya lihat.
- **Preview WhatsApp / Open Graph:** Dilengkapi metadata Open Graph dan image preview (`og-image.jpg`) saat tautan dibagikan via WhatsApp atau media sosial.

---

## 📁 Struktur Berkas

```text
├── index.html              # Halaman utama aplikasi, template cetak, dan logika CRUD
├── sw.js                   # Service Worker untuk dukungan mode offline
├── manifest.webmanifest    # Metadata instalasi PWA
├── icon-192.png            # Ikon aplikasi (192x192 px)
├── icon-512.png            # Ikon aplikasi (512x512 px)
├── og-image.jpg            # Gambar banner preview Open Graph / WhatsApp (1200x630 px)
├── stamp-transparent.png   # Stempel Alfian Tour dengan latar transparan
├── README.txt              # Catatan panduan penggunaan dasar
└── README.md               # Dokumentasi proyek
```

---

## 🚀 Cara Menjalankan & Deployment

### 1. Menjalankan secara Lokal
Cukup buka berkas `index.html` langsung di browser favorit Anda, atau jalankan menggunakan local server (misalnya VS Code Live Server, `npx serve`, atau Python `http.server`):
```bash
npx serve .
# atau
python -m http.server 8080
```

### 2. Deploy ke Hosting Gratis (HTTPS Diperlukan untuk PWA)
Agar fitur PWA (instalasi & offline cache) dan link preview WhatsApp dapat berjalan optimal, upload ke hosting dengan protokol HTTPS:
- **GitHub Pages:** Masuk ke *Settings* repository > *Pages* > pilih branch `main` / root folder.
- **Cloudflare Pages / Netlify / Vercel:** Hubungkan repo ini atau seret folder untuk deployment instan.

> **Catatan Penting:**
> - Fitur preview WhatsApp hanya bekerja ketika website diakses via URL publik HTTPS (bukan file lokal `file://`).
> - Setelah hosting aktif, Anda dapat memperbarui tag `<link rel="canonical" href="...">` dan `og:url` di `index.html` sesuai domain Anda.

---

## 📄 Lisensi
Hak cipta © PT. Alfian Sejahtera Abadi.
