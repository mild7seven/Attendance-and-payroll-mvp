# Attendance & Payroll PWA

PWA offline-first untuk pencatatan kehadiran dan simulasi payroll personal.

## Jalankan lokal
Jalankan static server pada folder ini (service worker tidak berjalan di `file://`), misalnya:
```bash
python -m http.server 8080
```
Lalu buka `http://localhost:8080`.

## Deploy GitHub Pages
Unggah isi folder ke repository, aktifkan GitHub Pages dari branch/folder yang sesuai, lalu buka URL Pages melalui HTTPS.

## Fitur
- Profil pekerja; basic salary input manual.
- Periode payroll 21–20.
- Shift pagi, sore, malam.
- Attendance Log dan edit/hapus.
- Aturan lembur Sabtu: pagi/sore 2.5 jam termasuk 7 jam efektif; malam tanpa lembur otomatis.
- Ketidakhadiran unpaid pada siklus Senin–Sabtu memicu pengecualian Sabtu pagi/sore (implementasi awal; cocokkan roster aktual sebelum produksi).
- Meal allowance, BPJS Kesehatan, JHT, JP, unpaid leave.
- Payroll preview, print-to-PDF, CSV export, JSON backup/restore.
- Penyimpanan localStorage.

## Batasan penting
Ini MVP lokal satu perangkat, bukan sistem payroll multi-user. Formula uang lembur dimasukkan manual sebagai tarif per jam; belum memodelkan formula legal/statutory lengkap. Evaluasi siklus lembur menggunakan minggu Senin–Sabtu sebagai pendekatan awal, sehingga harus dikonfirmasi terhadap roster perusahaan. Data tidak tersinkronisasi ke server. Proteksi akses dan enkripsi data belum diimplementasikan.

## QA
Gunakan data dummy terlebih dahulu. Periksa hitungan, backup/restore, periode 21–20, dan aturan Sabtu sebelum memasukkan data gaji nyata.
