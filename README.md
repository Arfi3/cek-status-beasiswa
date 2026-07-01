# Cek Status Beasiswa Citra 2026

Halaman web sederhana untuk mengecek status kelayakan (eligibilitas) mahasiswa dalam program Beasiswa Citra 2026, berdasarkan Nomor Induk Mahasiswa (NIM).

**Live demo:** https://arfi3.github.io/cek-status-beasiswa/

## Tampilan

Pengguna memasukkan NIM pada kolom pencarian (lengkap dengan saran otomatis saat mengetik), lalu sistem menampilkan:
- Nama, Angkatan, Fakultas, Jurusan, dan IPK mahasiswa
- Status kelayakan (**Eligible** / **Tidak Eligible**) dalam bentuk badge berwarna
- Pesan konfirmasi sesuai status

## Fitur

- 🔍 Pencarian NIM dengan saran otomatis (autocomplete)
- 🎨 Desain kustom (tanpa framework/template generik)
- ⚡ Tidak butuh backend atau database — seluruh data dan logika berjalan di sisi klien (browser)
- 📱 Responsif untuk perangkat mobile

## Kriteria Eligibilitas

Mahasiswa dinyatakan **Eligible** apabila memenuhi kedua syarat berikut:
1. Mahasiswa Angkatan 25
2. IPK ≥ 2.75
3. Tidak memiliki nilai mata kuliah D atau E (Nilai Terendah bukan D/E)

## Tentang Data

Data pada halaman ini adalah **data dummy/simulasi** (700 mahasiswa dengan NIM, nama, dan nilai yang digenerate secara acak), dibuat untuk keperluan demonstrasi/portofolio. Data tidak merepresentasikan mahasiswa atau institusi nyata mana pun.

Struktur data mengikuti format berikut:

| No | NIM | Nama | Jenis Kelamin | Angkatan | Fakultas | Jurusan | Semester | IPK | Nilai Terendah | Status |
|----|-----|------|----------------|----------|----------|---------|----------|-----|------------------|--------|

**Kode Fakultas dan Jurusan**

| Kode Fakultas | Fakultas | Kode Jurusan | Jurusan |
|:-------------:|----------|:------------:|----------|
| A1 | Sains | 1 | Matematika |
| A1 | Sains | 2 | Statistika |
| A1 | Sains | 3 | Biologi |
| A2 | Teknik | 1 | Teknik Informatika |
| A2 | Teknik | 2 | Teknik Industri |
| A3 | Ekonomi | 1 | Manajemen |
| A3 | Ekonomi | 2 | Akuntansi |
| A3 | Ekonomi | 3 | Ekonomi Pembangunan |
| A4 | Pertanian | 1 | Agroteknologi |
| A4 | Pertanian | 2 | Agribisnis |
| A5 | Ilmu Sosial | 1 | Administrasi Publik |
| A5 | Ilmu Sosial | 2 | Ilmu Komunikasi |
| A5 | Ilmu Sosial | 3 | Sosiologi |

**Kode Jalur Masuk**

| Jalur Masuk | Kode |
|:-----------:|:----:|
| Tes | T |
| Rapor | R |
| Mandiri | M |


Format NIM: `[Tahun][Jalur Masuk]-[Kode Fakultas][Kode Jurusan]-[Nomor Urut]`
Contoh: `25T-A11-0001` → tahun 2025, jalur Tes, Fakultas Sains (A1), Jurusan Matematika (1), nomor urut 0001.

Seluruh isi data dapat dilihat pada file [File Data Mahasiswa](https://github.com/Arfi3/cek-status-beasiswa/blob/main/Data%20Lengkap%20Cek%20Status%20Beasiswa%20Citra%202026.xlsx)

## Tech Stack

- HTML5, CSS3 (custom, tanpa framework)
- Vanilla JavaScript (tanpa library eksternal)
- Data ditanam langsung (embedded) di dalam file — tidak memerlukan server atau koneksi internet untuk berjalan

## Menjalankan Secara Lokal

1. Clone atau download repository ini
2. Buka file `index.html` langsung di browser (double-click), tidak perlu instalasi apa pun

## Deploy ke GitHub Pages

1. Pastikan file HTML bernama `index.html` berada di root repository
2. Buka **Settings → Pages**
3. Pilih branch `main` dan folder `/ (root)` sebagai source
4. Simpan — halaman akan aktif di `https://<username>.github.io/<nama-repo>/` dalam 1–2 menit

## Catatan

Proyek ini dikembangkan dengan bantuan AI (Claude, Anthropic) — mulai dari perancangan UI, penulisan kode, hingga generasi data dummy untuk keperluan demonstrasi.

## Lisensi

Bebas digunakan, dimodifikasi, dan dibagikan untuk keperluan pembelajaran maupun portofolio.
