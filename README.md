# PRAKTIKUM 3: LARAPRESS - APLIKASI BLOG SEDERHANA

# 📃 Identitas Diri

- **Nama**             : Revalina Adelia
- **NPM**              : 4523210091
- **Mata Kuliah**      : Pemrograman Berbasis Web (A)
- **Dosen Pengampu**   : Adi Wahyu Pribadi, S.Si., M.Kom.

---

LaraPress adalah aplikasi blog sederhana yang dibangun menggunakan Laravel 12 untuk tujuan pembelajaran dan pengembangan keterampilan web development.

<img width="1917" height="1078" alt="image" src="https://github.com/user-attachments/assets/05fa5a19-7d12-4fb4-b89c-8525f490af44" />

---

# 📋 Tentang Proyek

Proyek ini dibuat sebagai bagian dari pembelajaran Laravel framework. LaraPress mendemonstrasikan konsep-konsep dasar Laravel seperti routing, views, dan struktur MVC.

# 🚀 Fitur yang Sudah Diimplementasikan

1. Halaman Utama (Welcome Page)

   - Mengubah tampilan default Laravel menjadi halaman sederhana.
     
   - Menampilkan judul "Selamat Datang di LaraPress".
     
   - Struktur HTML yang bersih dan minimal.
     
3. Halaman Tentang Kami

   - Route: `/about`.
     
   - Menampilkan informasi tentang LaraPress.
     
   - Menjelaskan tujuan proyek sebagai pembelajaran Laravel 12.
     
5. Halaman Kontak

   - Route: `/contact`.
  
   - Menampilkan informasi kontak pengembang.

---

📁 Struktur File yang Dimodifikasi

## File yang Dibuat/Dimodifikasi:

### 1. resources/views/welcome.blade.php

- Mengubah tampilan default Laravel yang kompleks menjadi struktur HTML sederhana.

- Menampilkan pesan sambutan untuk pengunjung blog.

### 2. resources/views/about.blade.php (BARU)

- File view baru untuk halaman "Tentang Kami".

- Berisi informasi tentang LaraPress sebagai proyek pembelajaran.

### 3. resources/view/contact.blade.php (BARU)

- File view baru untuk halaman "Contact".

- Berisi informasi tentang kontak pengembang.

### 4. routes/web.php

- Menambahkan route baru `/about` yang mengarah ke view `about.blade.php`.

- Menambahkan route baru `/contact` yang mengarah ke view `contact.blade.php`.

---

## 🛠️ Langkah-Langkah Implementasi

### Step 1: Modifikasi Halaman Welcome

Mengubah file `resources/views/welcome.blade.php` dari tampilan default Laravel (266 baris) menjadi HTML sederhana:

<img width="616" height="317" alt="resources views welcome blade php" src="https://github.com/user-attachments/assets/c61e50aa-11f4-4332-ba78-52ba52c425a2" />

### Step 2: Membuat Route Baru

Menambahkan route baru di `routes/web.php` :

<img width="721" height="198" alt="routes web php" src="https://github.com/user-attachments/assets/cb244947-9e3c-4669-acb2-8cecc7b3427b" />

### Step 3: Membuat View About

Membuat file baru `resources/views/about.blade.php` :

<img width="1175" height="318" alt="resources views about blade php" src="https://github.com/user-attachments/assets/c97c15b6-ce80-4919-b4b1-db05a2e28159" />

### Step 4: Membuat View Contact

Membuat file baru `resources/views/contact.blade.php` :

<img width="592" height="466" alt="resources viewscontact blade php" src="https://github.com/user-attachments/assets/f37636c4-5cf4-4054-b636-32ef1884eb35" />

---

## 🌐 Endpoint yang Tersedia


---

## 💻 Teknologi yang Digunakan

- Framework: Laravel 12

- PHP Version: 8.x

- Database: MySQL

- Frontend: Blade Template Engine, HTML, CSS

- Build Tool: None

## 📸 Dokumentasi

### Halaman Utama 










