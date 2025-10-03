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
     
   - Menampilkan judul "Selamat Datang di Blog LaraPress".
     
   - Struktur HTML yang bersih dan minimal.

   <img width="1917" height="1078" alt="Tampilan Utama LaraPress" src="https://github.com/user-attachments/assets/ea30db62-9012-4b2f-9cad-7e85f08784c8" />
     
3. Halaman Tentang Kami

   - Route: `/about`.
     
   - Menampilkan informasi tentang LaraPress.
     
   - Menjelaskan tujuan proyek sebagai pembelajaran Laravel 12.

   <img width="1919" height="1075" alt="Tentang LaraPress" src="https://github.com/user-attachments/assets/b8059eeb-aab6-422e-8c21-3ab20d7c6149" />

5. Halaman Kontak

   - Route: `/kontak`.
  
   - Menampilkan informasi kontak pengembang.

   <img width="1918" height="1076" alt="Kontak LaraPress" src="https://github.com/user-attachments/assets/ff8d63de-5846-4e5a-a00d-d8e77a2355fb" />

---

📁 Struktur File yang Dimodifikasi

## File yang Dibuat/Dimodifikasi:

### 1. `resources/views/welcome.blade.php`

- Mengubah tampilan default Laravel yang kompleks menjadi struktur HTML sederhana.

- Menampilkan pesan sambutan untuk pengunjung blog.

### 2. `resources/views/about.blade.php` (BARU)

- File view baru untuk halaman "Tentang Kami".

- Berisi informasi tentang LaraPress sebagai proyek pembelajaran.

### 3. `resources/view/contact.blade.php` (BARU)

- File view baru untuk halaman "Kontak".

- Berisi informasi tentang kontak pengembang.

### 4. `routes/web.php`

- Menambahkan route baru `/about` yang mengarah ke view `about.blade.php`.

- Menambahkan route baru `/contact` yang mengarah ke view `contact.blade.php`.

---

## 🛠️ Langkah-Langkah Implementasi

### Step 1: Modifikasi Halaman Welcome

Mengubah file `resources/views/welcome.blade.php` dari tampilan default Laravel (266 baris) menjadi HTML sederhana:

``` resources/views/welcome.blade.php
<!DOCTYPE html>
<html>
<head>
    <title>Selamat Datang di LaraPress</title>
</head>
<body>
    <h1>Selamat Datang di Blog LaraPress</h1>
    <p>Ini adalah halaman utama dari aplikasi blog kita.</p>
    <a href="/tentang-kami">Lihat Halaman Tentang Kami</a>
    <br>
    <a href="/kontak">Lihat Halaman Kontak</a>
</body>
</html>

```

### Step 2: Membuat Route Baru

Menambahkan route baru di `routes/web.php` :

``` routes/web.php
Route::get('/tentang-kami', function () {
    return view('about'); // Kita akan menampilkan view bernama 'about'
});

Route::get('/kontak', function () {
    return view('kontak'); // Kita akan menampilkan view bernama 'kontak'
});

```

### Step 3: Membuat View About

Membuat file baru `resources/views/about.blade.php` :

``` resources/views/about.blade.php
<!DOCTYPE html>
<html>
<head>
    <title>Tentang Kami - LaraPress</title>
</head>
<body>
    <h1>Tentang LaraPress</h1>
    <p>LaraPress adalah sebuah proyek blog sederhana yang dibuat untuk mempelajari dasar-dasar framework Laravel 12.</p>
    <a href="/kontak">Lihat Halaman Kontak</a>
    <br>
    <a href="/">Kembali ke Halaman Utama</a>
</body>
</html>

```

### Step 4: Membuat View Kontak

Membuat file baru `resources/views/contact.blade.php` :

``` resources/views/contact.blade.php
<!DOCTYPE html>
<html>

<head>
    <title>Kontak Kami - LaraPress</title>
</head>

<body>
    <h1>Kontak LaraPress</h1>
    <p>Nama : Revalina Adelia</p>
    <p>NPM  : 4523210091</p>
    <p>Mata Kuliah : Prak. Pemrograman Berbasis Web (A)</p>
    <p>Email : revalina4523091@univpancasila.ac.id</p>
    <a href="/tentang-kami">Lihat Halaman Tentang Kami</a>
    <br>
    <a href="/">Kembali ke Halaman Utama</a>
</body>

</html>

```
---

## 🌐 Endpoint yang Tersedia

| Route      | Method | Deskripsi                              |
|------------|--------|----------------------------------------|
| `/`        | GET    | Halaman utama LaraPress                |
| `/about`   | GET    | Halaman tentang LaraPress              |
| `/contact` | GET    | Halaman tentang kontak pengembang      |

---

## 💻 Teknologi yang Digunakan

- Framework: Laravel 12

- PHP Version: 8.x

- Database: MySQL

- Frontend: Blade Template Engine, HTML, CSS

- Build Tool: None
