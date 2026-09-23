# Gerakan Beras Umat - PWA

PWA ini adalah wrapper installable untuk Google Apps Script yang Anda kirim.
Frontend asli tetap berada di Google Apps Script; PWA menyediakan ikon, manifest,
mode standalone, splash/theme, dan service worker untuk shell aplikasi.

## 1. Pasang URL Google Apps Script

Buka `index.html`, lalu ganti:

PASTE_URL_WEB_APP_GOOGLE_APPS_SCRIPT_DI_SINI

menjadi URL Web App Google Apps Script Anda, misalnya:
https://script.google.com/macros/s/XXXXX/exec

## 2. Deploy

Cara paling mudah:
1. Upload semua file ke repository GitHub.
2. Aktifkan GitHub Pages dari branch `main` / folder root.
3. Buka URL GitHub Pages tersebut.
4. Di Chrome/Edge akan muncul opsi Install App / Install Gerakan Beras Umat.

## 3. Catatan penting

- Data tetap tersimpan dan diproses oleh Google Apps Script + Google Sheets.
- PWA ini tidak membuat data menjadi offline. Jika internet mati, halaman shell
  masih dapat dibuka, tetapi fungsi yang memanggil `google.script.run` tetap
  membutuhkan koneksi ke Google Apps Script.
- Script backend asli Anda sudah menggunakan `HtmlService.createTemplateFromFile('index')`
  dan Google Sheets, jadi tidak perlu diubah untuk memakai wrapper PWA ini.
