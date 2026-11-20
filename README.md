#  Sistem Basis Data Perpustakaan - SQLite & Data Analysis

Sebuah proyek implementasi sistem basis data relasional untuk manajemen perpustakaan menggunakan **SQLite** di lingkungan Python (Google Colab). Proyek ini juga mencakup ekstraksi data, pemrosesan menggunakan **Pandas**, serta visualisasi data menggunakan **Matplotlib** dan **Seaborn**.

---

##  Informasi Mahasiswa

* **Nama:** Syam Budi Luthfi
* **NIM:** 411231150
* **Semester:** 6
* **Program Studi:** Teknik Informatika
* **Universitas:** Universitas Dian Nusantara

---

##  Tujuan Proyek
Proyek ini dibuat untuk memenuhi tugas mata kuliah sistem basis data dan analisis data, dengan fokus pada:
1. Perancangan skema basis data relasional (DDL).
2. Manipulasi data (DML) seperti penginputan data dummy ke dalam tabel.
3. Penerapan Query SQL yang kompleks termasuk `JOIN` dan `GROUP BY` dengan fungsi agregasi.
4. Eksplorasi Data (EDA) menggunakan pustaka Pandas.
5. Visualisasi distribusi numerik dari hasil query SQL.

---

## ` Skema Database (Entity Relationship)

Sistem ini terdiri dari tiga tabel utama yang saling berelasi:

1. **Tabel `buku`**
   * `id` (Primary Key, Integer, Auto-increment)
   * `judul` (Text)
   * `penulis` (Text)
   * `tahun` (Integer)

2. **Tabel `anggota`**
   * `id` (Primary Key, Integer, Auto-increment)
   * `nama` (Text)
   * `email` (Text)

3. **Tabel `peminjaman`**
   * `id` (Primary Key, Integer, Auto-increment)
   * `id_anggota` (Foreign Key ke tabel `anggota`)
   * `id_buku` (Foreign Key ke tabel `buku`)
   * `tgl_pinjam` (Date)
   * `tgl_kembali` (Date, bernilai `NULL` jika belum dikembalikan)

---

##  Teknologi dan Library yang Digunakan

* **Bahasa Pemrograman:** Python 3.x
* **Lingkungan Kerja:** Jupyter Notebook / Google Colab
* **Database:** SQLite3
* **Data Manipulation:** Pandas
* **Data Visualization:** Matplotlib, Seaborn

---

##  Cara Menjalankan Proyek

1. **Buka di Google Colab:**
   Klik file berformat `.ipynb` di dalam repository ini, lalu klik tombol **"Open in Colab"** jika Anda menggunakan ekstensi browser, atau unduh dan *upload* langsung ke [Google Colab](https://colab.research.google.com/).
2. **Jalankan Sel Kode:**
   Jalankan (*Run*) setiap sel kode secara berurutan dari atas ke bawah.
3. **Hasil yang Diharapkan:**
   * File database `perpustakaan.db` akan terbuat secara otomatis di *local storage* session.
   * Output berupa tabel DataFrame dari Pandas (Daftar Peminjaman Lengkap & Total Buku per Anggota).
   * Muncul dua visualisasi grafik: **Diagram Batang** (distribusi buku per anggota) dan **Histogram** (distribusi durasi peminjaman dalam hari).

---

##  Cuplikan Hasil Analisis

* **Pola Peminjaman:** Sistem mampu mendeteksi secara otomatis buku yang masih dalam masa pinjaman (belum dikembalikan / nilai *NULL* pada tanggal kembali).
* **Visualisasi:** Visualisasi memberikan *insight* langsung mengenai anggota paling aktif meminjam dan rata-rata waktu yang dihabiskan anggota untuk membaca sebuah buku.

---
*Dibuat dengan dedikasi oleh Syam Budi Luthfi (2024)*
