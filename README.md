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

Format NIM: `[Tahun][Jalur Masuk]-[Kode Fakultas][Kode Jurusan]-[Nomor Urut]`
Contoh: `25T-A11-0001` → tahun 2025, jalur Tes, Fakultas Sains (A1), Jurusan Matematika (1), nomor urut 0001.

Seluruh isi data dapat dilihat pada file ''

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
