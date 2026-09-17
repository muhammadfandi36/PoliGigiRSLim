# Formulir Rekam Medis Odontogram

Aplikasi web statis (satu berkas HTML) untuk pencatatan odontogram. Semua CSS dan JavaScript sudah menyatu di dalam `index.html`, tanpa dependensi eksternal.

## Cara deploy ke GitHub Pages

### Lewat web (tanpa Git)
1. Buat repository baru di GitHub, misalnya `odontogram`, pilih **Public**.
2. Klik **Add file → Upload files**, unggah `index.html` dan `.nojekyll`, lalu **Commit changes**.
3. Buka **Settings → Pages**.
4. Bagian *Build and deployment*: Source = **Deploy from a branch**, Branch = **main**, folder = **/ (root)**, lalu **Save**.
5. Tunggu 1–2 menit. Situs tersedia di `https://<username>.github.io/odontogram/`.

### Lewat Git (terminal)
```bash
git init
git add .
git commit -m "Formulir odontogram"
git branch -M main
git remote add origin https://github.com/<username>/odontogram.git
git push -u origin main
```
Lalu aktifkan GitHub Pages seperti langkah 3–5 di atas.

## Catatan penting
- Nama berkas **harus** `index.html` agar terbuka otomatis di URL utama.
- Data pasien disimpan di `localStorage` browser masing-masing pengguna — tidak terkirim ke server dan tidak tersinkron antar perangkat. Hapus cache browser = data hilang.
- Karena repository publik dapat diakses siapa saja, jangan menyimpan data pasien asli di dalam kode. Untuk penggunaan klinis, pertimbangkan repository privat (GitHub Pages privat perlu paket berbayar) atau hosting internal rumah sakit.
