# PRAKTIKUM 3: LARAPRESS - APLIKASI BLOG SEDERHANA

# 📃 Identitas Diri

- **Nama**             : Revalina Adelia
- **NPM**              : 4523210091
- **Mata Kuliah**      : Pemrograman Berbasis Web (A)
- **Dosen Pengampu**   : Adi Wahyu Pribadi, S.Si., M.Kom.

---
# 📋 Tentang Proyek

LaraPress adalah aplikasi blog sederhana berbasis **Laravel 12** yang dikembangkan untuk mendukung proses pembelajaran mata kuliah **Pemrograman Berbasis Web**. Proyek ini dirancang untuk membantu mahasiswa memahami **konsep fundamental Laravel**, meliputi instalasi, konfigurasi, routing, view, hingga penerapan alur kerja dasar **MVC (Model-View, Controller)**.

<img width="1917" height="1078" alt="image" src="https://github.com/user-attachments/assets/05fa5a19-7d12-4fb4-b89c-8525f490af44" />

---

# 🎯 Latar Belakang dan Tujuan

Laravel dikenal sebagai salah satu framework PHP modern yang mendukung pengembangan aplikasi web dengan cepat, terstruktur, dan maintainable. Melalui proyek **LaraPress**, mahasiswa diharapkan dapat:

1. Menjalankan proyek Laravel 12 baru menggunakan Composer.
2. Menjalankan server development lokal menggunakan `php artisan serve`.
3. Memahami struktur folder esensial untuk memulai.
4. Mendefinisikan rute (Route) sederhana di `routes/web.php`.
5. Membuat dan memodifikasi file tampilan (View) menggunakan Blade.
6. Memahami alur kerja fundamental Laravel: **Request -> Route -> View -> Response**.
   
# 🚀 Fitur yang Sudah Diimplementasikan

## 1. Halaman Utama (Welcome Page (`/`))

   - Mengubah tampilan default Laravel menjadi halaman sederhana.
     
   - Menampilkan judul "Selamat Datang di Blog LaraPress".
     
   - Struktur HTML yang bersih dan minimal.

   - Navigasi menuju halaman "**Tentang Kami**" dan "**Kontak**".

   <img width="1917" height="1078" alt="Tampilan Utama LaraPress" src="https://github.com/user-attachments/assets/ea30db62-9012-4b2f-9cad-7e85f08784c8" />
     
## 2. Halaman Tentang Kami (`/tentang-kami`)

   - Route: `/about`.
     
   - Menampilkan informasi tentang LaraPress.
     
   - Menjelaskan tujuan proyek sebagai pembelajaran Laravel 12.

   - Menyediakan tautan kembali ke **Home** dan menuju **Kontak**.

   <img width="1919" height="1075" alt="Tentang LaraPress" src="https://github.com/user-attachments/assets/b8059eeb-aab6-422e-8c21-3ab20d7c6149" />

## 3. Halaman Kontak (`/kontak`)

   - Route: `/kontak`.
  
   - Menampilkan identitas pengembang (nama, NPM, mata kuliah, dan email).

   - Menyediakan tautan kembali ke **Home** maupun **Tentang Kami**.

   <img width="1918" height="1076" alt="Kontak LaraPress" src="https://github.com/user-attachments/assets/ff8d63de-5846-4e5a-a00d-d8e77a2355fb" />

---

# 🛠️ Instalasi dan Konfigurasi

## 1. Persyaratan Lingkungan

- **XAMPP** terinstal dan aktif (Apache dan MySQL).

- **Composer** sudah tersedia pada sistem operasi.

- **PHP** minimal versi 8.x.

- **Editor:** VS Code.

- **Browser:** Google Chrome atau lainnya yang setara.

## 2. Proses Instalasi Laravel

Buka terminal (CMD/PowerShell) pada folder `c:\xampp\htdocs`, kemudian jalankan:

`composer create-project laravel/laravel LaraPress`

Perintah ini akan membuat folder **LaraPress** berisi instalasi Laravel terbaru.

## 3. Menjalankan Server

Masuk ke direktori proyek, lalu jalankan:

`cd LaraPress`
`phhp artisan serve`

Aplikasi ini dapat diakses melalui browser: `http://127.0.0.1:8000`

--- 

# 📁 Struktur File yang Dimodifikasi

LaraPress/
├── routes/
│   └── web.php         # Definisi route aplikasi
└── resources/
    └── views/
        ├── welcome.blade.php   # Halaman utama
        ├── about.blade.php     # Halaman Tentang Kami
        └── contact.blade.php   # Halaman Kontak

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

**Keterangan:**

- Teks sambutan ditampilkan melalui tag `<h1>`.

- Terdapat hyperlink menuju halaman **Tentang Kami** dan **Kontak**.
  
### Step 2: Membuat Route Baru

Menambahkan route baru di `routes/web.php` :

``` routes/web.php
?php

use Illuminate\Support\Facades\Route;

Route::get('/', function () {
    return view('welcome');
});

Route::get('/tentang-kami', function () {
    return view('about'); // Kita akan menampilkan view bernama 'about'
});

Route::get('/kontak', function () {
    return view('kontak'); // Kita akan menampilkan view bernama 'kontak'
});

```

**Keterangan:**

- `Route::get('/url', function(){...})` digunakan untuk mendefinisikan alamat URL yang dapat diakses melalui metode GET.

- Fungsi `return view('...')` akan memanggil file tampilan (Blade) yang sesuai di folder `resources/views/`.

- Pada proyek ini terdapat 3 rute: `/` (halaman utama), `/tentang-kami`, dan `/kontak`.
  
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

**Keterangan:**

- Berisi deskripsi singkat mengenai proyek LaraPress.

- Disertai tautan navigasi kembali ke **Home** atau menuju **Halaman Kontak**.
  
### Step 4: Membuat View Kontak

Membuat file baru `resources/views/kontak.blade.php` :

``` resources/views/kontak.blade.php
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

**Keterangan:**

- Menampilkan identitas pengembang berupa nama, NPM, mata kuliah, dan email.

- Dilengkapi navigasi antar halaman agar user tidak terjebak dalam satu tampilan.

---

## 🔄 Alur Kerja

1. Pengguna mengakses URL tertentu melalui browser.
   
2. Laravel mencari **route** yang sesuai di `routes/web.php`.
   
3. Route tersebut memanggil file view **Blade (welcome, about, kontak)**.
   
4. View dikembalikan sebagai **response** ke browser.
   
---

## 🌐 Endpoint yang Tersedia

| Route             | Method | Deskripsi                              |
|-------------------|--------|----------------------------------------|
| `/`               | GET    | Halaman utama LaraPress                |
| `/tentang-kami`   | GET    | Informasi tentang LaraPress            |
| `/kontak`         | GET    | Informasi kontak pengembang            |

---

## 💻 Teknologi yang Digunakan

- **Framework** : Laravel 12

- **PHP Version** : 8.x

- **Database** : MySQL

- **Frontend** : Blade Template Engine, HTML, CSS

- **Build Tool** : None
