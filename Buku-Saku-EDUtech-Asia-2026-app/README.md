# Buku Saku EDUtech Asia 2026 (aplikasi HP)

Web app statis untuk 4 orang delegasi Eduvizta. Tiap orang memilih profil saat pertama dibuka:
**Dial** (Delegasi 2, dengan target), **Kustian** (Delegasi 1, dengan target), atau **Peserta lain** (tanpa target, isi nama).
Isian tersimpan di HP masing-masing (localStorage) dan aplikasi tetap jalan tanpa internet setelah dibuka sekali.

## Isi folder
- `index.html` — seluruh aplikasi (HTML, CSS, JS dalam satu file)
- `sw.js` — service worker untuk mode offline
- `manifest.webmanifest`, `icon-*.png`, `apple-touch-icon.png` — agar bisa dipasang di layar utama

## Deploy ke GitHub Pages
1. Buat repo baru, mis. `buku-saku-edutech`, lalu upload semua file di folder ini ke root repo.
2. Settings → Pages → Source: **Deploy from a branch** → Branch: `main` / `(root)` → Save.
3. Tunggu 1–2 menit. Link-nya: `https://<username>.github.io/buku-saku-edutech/`

Alternatif: Netlify → Add new site → Deploy manually → seret folder ini. (Perlu login supaya link tidak kedaluwarsa.)

## Pasang di HP (bagikan langkah ini ke tim)
1. Buka link di **Chrome (Android)** atau **Safari (iPhone)**.
2. Pilih profil, isi nama kalau "Peserta lain".
3. Android: ⋮ → **Tambahkan ke layar utama / Instal aplikasi**. iPhone: tombol Share → **Tambah ke Layar Utama**.
4. Buka sekali dari ikon di layar utama selagi ada internet. Setelah itu aplikasi bisa dipakai offline.

## Catatan penting
- Data **hanya ada di HP itu**. Tidak sinkron ke HP/laptop lain. Jangan hapus data browser atau aplikasi.
- Tekan **Rekap hasil akhir** (tab Misi/Rekap) tiap malam lalu kirim file `.txt`-nya ke diri sendiri (WhatsApp/email) sebagai cadangan.
- Ganti profil: ketuk nama di pojok kanan atas. Isian tiap profil disimpan terpisah.
- Kalau mengubah `index.html` setelah dipasang, naikkan nilai `VERSION` di `sw.js` supaya HP mengambil versi baru (buka aplikasi dua kali).
