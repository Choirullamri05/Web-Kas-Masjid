# Web Kas Masjid

Sistem Informasi berbasis web sederhana untuk mengelola dan mencatat transaksi kas (pemasukan dan pengeluaran) di lingkungan masjid.

## 🌟 Fitur Utama

* **Manajemen Kas Masuk:** Mencatat setiap transaksi pemasukan dana (misalnya infaq, sedekah, sumbangan).
* **Manajemen Kas Keluar:** Mencatat setiap transaksi pengeluaran dana (misalnya operasional, perbaikan).
* **Rekapitulasi Kas:** Menampilkan ringkasan total kas masuk dan kas keluar.
* **Laporan Keuangan:** Menyediakan laporan kas secara keseluruhan atau per periode.
* **Manajemen Pengguna:** Terdapat dua peran (role) pengguna:
    * **Admin:** Memiliki akses penuh untuk mengelola pengguna dan data master.
    * **Bendahara:** Memiliki akses untuk mengelola transaksi kas masuk dan keluar serta melihat laporan.
* **Dashboard Interaktif:** Menampilkan visualisasi data kas (kemungkinan menggunakan grafik) untuk memudahkan pemantauan.

## 🛠 Teknologi yang Digunakan

Proyek ini dibangun menggunakan tumpukan teknologi berikut:

| Kategori | Teknologi | Keterangan |
| :--- | :--- | :--- |
| **Backend** | PHP | Bahasa pemrograman utama sisi server. |
| **Database** | MySQL / MariaDB | Sistem manajemen basis data untuk penyimpanan data kas dan pengguna. |
| **Frontend** | HTML, CSS, JavaScript, jQuery | Dasar-dasar pengembangan web untuk antarmuka pengguna. |
| **Framework/Template** | SB Admin 2 (Bootstrap) | Template dashboard responsif untuk tata letak dan desain. |
| **Visualisasi** | Chart.js | Library JavaScript untuk menampilkan grafik pada dashboard. |
| **Lain-lain** | Font Awesome, SweetAlert | Iconografi dan notifikasi yang lebih menarik. |

## ⚙️ Prasyarat Instalasi

Pastikan Anda telah menginstal perangkat lunak berikut di lingkungan lokal Anda (misalnya menggunakan **XAMPP**, **WAMPP**, atau **LAMPP**):

1.  **Web Server:** Apache atau Nginx.
2.  **PHP:** Versi 5.x atau 7.x (disarankan).
3.  **Database Server:** MySQL atau MariaDB.

## 🚀 Instalasi

Ikuti langkah-langkah di bawah ini untuk menginstal dan menjalankan proyek:

1.  **Clone Repositori:**
    ```bash
    git clone https://github.com/choirullamri05/web-kas-masjid.git
    ```
2.  **Pindahkan ke Web Server Directory:**
    Salin seluruh folder proyek ke direktori root web server Anda (misalnya `htdocs` untuk XAMPP, atau `www` untuk WAMPP). Ubah nama foldernya menjadi `kasmasjid` (atau nama lain yang Anda inginkan).
3.  **Buat Database:**
    * Buka peramban Anda dan akses `phpMyAdmin` (`http://localhost/phpmyadmin/`).
    * Buat database baru dengan nama: `kasmasjid`.
4.  **Import Database:**
    * Pilih database `kasmasjid` yang baru saja Anda buat.
    * Pilih tab **Import** (Impor).
    * Cari dan unggah file `DATABASE/kasmasjid.sql` dari folder proyek.
5.  **Konfigurasi Koneksi Database:**
    * Buka file koneksi database di `inc/koneksi.php`.
    * Pastikan pengaturan koneksi sesuai dengan konfigurasi database lokal Anda (terutama jika Anda tidak menggunakan *username* `root` dan *password* kosong).

    ```php
    // inc/koneksi.php (Pastikan kredensial Anda sudah benar)
    $koneksi = new mysqli ("localhost","root","","kasmasjid");
    ```
6.  **Akses Aplikasi:**
    Akses aplikasi melalui peramban Anda:
    ```
    http://localhost/kasmasjid/
    ```

## 🔑 Contoh Penggunaan (Default Login)

Setelah instalasi berhasil, Anda dapat login menggunakan kredensial default:

| Role | Username | Password | Halaman Awal |
| :--- | :--- | :--- | :--- |
| **Admin** | `admin` | `admin` | `home/admin.php` |
| **Bendahara** | `bendahara` | `bendahara` | `home/bendahara.php` |

