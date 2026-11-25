# Toko Fresh Cimahi

Demo web untuk website pelanggan dan manajemen rantai pasok (SCM) Toko Fresh Cimahi.

## Menjalankan

Tidak perlu memasang paket atau proses build. Buka `index.html` di browser, atau sajikan folder ini sebagai situs statis.

- Masuk admin dari tombol **Masuk Admin**.
- Kata sandi demo: `fresh123`.
- Pilih peran **Pemilik**, **Admin gudang/toko**, **Kasir**, atau **Kurir**.
- Data contoh dan perubahan disimpan di `localStorage` browser.
- Nomor WhatsApp demo bisa diganti di menu **Pengaturan**.
- Form pesanan manual memakai alur keranjang: tambahkan barang satu per satu, atur jumlah, lalu simpan sebagai satu pesanan pelanggan.

Untuk mengulang data contoh, hapus key `toko-fresh-cimahi-v1` dari penyimpanan lokal browser untuk halaman ini, lalu muat ulang.

## Susunan file

- `index.html` adalah kerangka halaman dan memuat stylesheet serta skrip.
- `styles.css` berisi gaya website publik, admin, login, dan responsif.
- `app.js` mengatur navigasi SPA, tampilan modul, data demo, dan aksi aplikasi.
- `assets/` berisi logo.

Halaman login saat ini dirender sebagai bagian dari aplikasi satu halaman (SPA), bukan file HTML terpisah. Pemisahan menjadi modul JavaScript per fitur dapat dilakukan tanpa mengubahnya menjadi PHP. PHP baru dibutuhkan jika nanti aplikasi memakai backend PHP; versi ini berupa situs statis dan dapat berjalan tanpa server aplikasi.

## Deploy

Folder ini dapat diterbitkan sebagai situs statis di Netlify atau Vercel. Atur folder publik ke direktori proyek ini; tidak ada command build.

## Batasan demo

Login hanya simulasi lokal dan bukan autentikasi aman untuk penggunaan produksi. Data tidak tersinkron antarperangkat dan akan mengikuti penyimpanan browser. Sebelum dipakai operasional, hubungkan autentikasi, database, kontrol akses server, serta pencadangan ke layanan backend.
