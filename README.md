# Arisan Tracker

Tool sederhana buat nandain progress setoran arisan mingguan.

## Setup Arisan Ini

- **Total putaran:** 45x
- **Iuran per minggu:** Rp300.000
- **Total pot (jika lunas):** Rp13.500.000
- **Potongan admin:** 1% (Rp135.000)
- **Diterima bersih:** Rp13.365.000

## Cara Pakai

1. Buka file `arisan-tracker.html` di browser (double-click aja, gak perlu internet/install apa-apa).
2. Klik kotak angka minggu yang udah lo bayar → otomatis jadi warna oranye (tertandai).
3. Klik lagi kalau mau batalin tanda (misal salah klik).
4. Statistik di atas grid otomatis update:
   - **Sudah Bayar** — jumlah minggu yang sudah ditandai dari 45
   - **Total Terkumpul** — jumlah minggu tertandai × Rp300.000
   - **Sisa Setoran** — berapa minggu lagi yang belum dibayar
5. Progress bar di bawah statistik nunjukin persentase keseluruhan.
6. Box **Estimasi Perolehan Arisan** di bawah grid nunjukin proyeksi total pot, potongan admin, dan yang diterima bersih di akhir arisan (angka ini fixed, tidak berubah dari progress).

## Penyimpanan Data

- Progress tersimpan otomatis setiap kali lo klik kotak (ada notifikasi kecil "Tersimpan" di pojok kanan bawah).
- Data disimpan secara privat, hanya bisa diakses dari sesi/browser lo sendiri — bukan dibagikan ke orang lain.
- Saat pertama kali dibuka, minggu 1–19 sudah otomatis ditandai (sesuai progress awal saat tool ini dibuat). Setelah itu, progress mengikuti apa yang lo tandai sendiri.

## Reset

Kalau mau mulai ulang dari nol, klik tombol **"Reset semua"** di pojok kiri bawah. Akan ada konfirmasi dulu sebelum semua tanda dihapus.

## Kustomisasi

Kalau ada arisan baru dengan setup beda (jumlah minggu / nominal beda), tinggal ubah 3 baris ini di dalam file `arisan-tracker.html`, di bagian `<script>`:

```js
const TOTAL_WEEKS = 45;        // ganti sesuai jumlah putaran arisan
const WEEKLY_AMOUNT = 300000;  // ganti sesuai iuran per minggu
const ADMIN_FEE_RATE = 0.01;   // ganti sesuai persentase potongan admin
```
