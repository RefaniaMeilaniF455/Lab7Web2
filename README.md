<<<<<<< HEAD
# CodeIgniter 4 Framework

## What is CodeIgniter?

CodeIgniter is a PHP full-stack web framework that is light, fast, flexible and secure.
More information can be found at the [official site](https://codeigniter.com).

This repository holds the distributable version of the framework.
It has been built from the
[development repository](https://github.com/codeigniter4/CodeIgniter4).

More information about the plans for version 4 can be found in [CodeIgniter 4](https://forum.codeigniter.com/forumdisplay.php?fid=28) on the forums.

You can read the [user guide](https://codeigniter.com/user_guide/)
corresponding to the latest version of the framework.

## Important Change with index.php

`index.php` is no longer in the root of the project! It has been moved inside the *public* folder,
for better security and separation of components.

This means that you should configure your web server to "point" to your project's *public* folder, and
not to the project root. A better practice would be to configure a virtual host to point there. A poor practice would be to point your web server to the project root and expect to enter *public/...*, as the rest of your logic and the
framework are exposed.

**Please** read the user guide for a better explanation of how CI4 works!

## Repository Management

We use GitHub issues, in our main repository, to track **BUGS** and to track approved **DEVELOPMENT** work packages.
We use our [forum](http://forum.codeigniter.com) to provide SUPPORT and to discuss
FEATURE REQUESTS.

This repository is a "distribution" one, built by our release preparation script.
Problems with it can be raised on our forum, or as issues in the main repository.

## Contributing

We welcome contributions from the community.

Please read the [*Contributing to CodeIgniter*](https://github.com/codeigniter4/CodeIgniter4/blob/develop/CONTRIBUTING.md) section in the development repository.

## Server Requirements

PHP version 8.1 or higher is required, with the following extensions installed:

- [intl](http://php.net/manual/en/intl.requirements.php)
- [mbstring](http://php.net/manual/en/mbstring.installation.php)

> [!WARNING]
> - The end of life date for PHP 7.4 was November 28, 2022.
> - The end of life date for PHP 8.0 was November 26, 2023.
> - If you are still using PHP 7.4 or 8.0, you should upgrade immediately.
> - The end of life date for PHP 8.1 will be December 31, 2025.

Additionally, make sure that the following extensions are enabled in your PHP:

- json (enabled by default - don't turn it off)
- [mysqlnd](http://php.net/manual/en/mysqlnd.install.php) if you plan to use MySQL
- [libcurl](http://php.net/manual/en/curl.requirements.php) if you plan to use the HTTP\CURLRequest library
=======
# Lab7Web2
```
Refania Meilani Firdos
TI.A2.23
312310173
Langkah-langkah Praktikum
```
# Persiapan
Sebelum memulai menggunakan Framework Codeigniter, perlu dilakukan konfigurasi pada webserver. Beberapa ekstensi PHP perlu diaktifkan untuk kebutuhan pengembangan Codeigniter 4.
Berikut beberapa ekstensi yang perlu diaktifkan:
1. php-json ekstension untuk bekerja dengan JSON;
2. php-mysqlnd native driver untuk MySQL;
3. php-xml ekstension untuk bekerja dengan XML;
4. php-intl ekstensi untuk membuat aplikasi multibahasa;
5. libcurl (opsional), jika ingin pakai Curl.

# Langkah-langkah Pratikum 1-11:
1. Pada bagian extention, hilangkan tanda ; (titik koma) pada ekstensi yang akan diaktifkan. Kemudian simpan kembali filenya dan restart Apache web server. 
![image](https://github.com/user-attachments/assets/e7ab9777-ab80-47e0-b24f-1ca19c081d69)
![image](https://github.com/user-attachments/assets/e7feb6db-a300-4d2b-ae75-5243bb0d488e)

2. Instalasi Codeigniter 4, untuk melakukan instalasi Codeigniter 4 dapat dilakukan dengan dua cara, yaitu cara manual dan menggunakan composer. Pada praktikum ini kita menggunakan cara manual.
```
Unduh Codeigniter dari website https://codeigniter.com/download  
• Extrak file zip Codeigniter ke direktori htdocs/lab11_ci. 
• Ubah nama direktory framework-4.x.xx menjadi ci4. 
• Buka browser dengan alamat http://localhost/lab11_ci/ci4/public/
```
![image](https://github.com/user-attachments/assets/7e9b9960-b6ed-4145-980f-5061a5c9c027)

3. Menjalankan CLI (Command Line Interface), Codeigniter 4 menyediakan CLI untuk mempermudah proses development. Untuk mengakses CLI buka terminal/command prompt.  
![image](https://github.com/user-attachments/assets/3ff09c24-5f7a-44ff-a2d3-090773999761)
4. Untuk memudahkan mengetahui jenis errornya, maka perlu diaktifkan mode debugging dengan mengubah nilai konfigurasi pada environment variable CI_ENVIRINMENT menjadi development.
![image](https://github.com/user-attachments/assets/c8553b06-9765-4098-9ccf-ca36883b1dec)
![image](https://github.com/user-attachments/assets/e9a2e384-7c0e-4b50-adfe-0955fc089131)

5. app/Controller/Home.php hilangkan titik koma pada akhir kode ubah return view > 'Welcome_messege'
![image](https://github.com/user-attachments/assets/1e372547-33a5-451b-828d-2253567abee0)
6. Selanjutnya refresh Kembali browser, maka akan ditampilkan hasilnya yaotu halaman sudah
dapat diakses.
![image](https://github.com/user-attachments/assets/2fc078e5-012b-4986-abce-50960b14f38d)
7. Method ini belum ada pada routing, sehingga cara mengaksesnya dengan menggunakan
alamat: (http://localhost:8080/tos)
![image](https://github.com/user-attachments/assets/64d66bdf-3de8-44b5-9b30-5893e0517cb7)
menambahkan perintah pada routes.php ```$routes->get('/tos', Page::tos');```
8. Membuat ViewSelanjutnya adalam membuat view untuk tampilan web agar lebih menarik. Buat file baru dengan nama about.php pada direktori view (app/view/about.php)
![image](https://github.com/user-attachments/assets/6d6b8db5-f734-4888-b8dc-4c67ed9b4f7a)
9. Tambahkan Buat file css pada direktori public dengan nama style.css (copy file dari praktikum lab4_layout. Kita akan gunakan layout yang pernah dibuat pada praktikum 4.Kemudian buat folder template pada direktori view kemudian buat file header.php dan footer.php. Kemudian ubah file app/view/about.php seperti berikut. Selanjutnya refresh tampilan pada alamat http://localhost:8080/about
![Screenshot 2025-07-03 153840](https://github.com/user-attachments/assets/48f62387-7f39-434c-98bd-7cf22f91d7f1)


10. Membuat Database: Studi Kasus Data Artikel
![image](https://github.com/user-attachments/assets/463378e3-de76-4ebb-acea-ed105c6bde31)
11. Selanjutnya adalah membuat Model untuk memproses data Artikel. Buat file baru pada direktori app/Models dengan nama ArtikelModel.php , Buat direktori baru dengan nama artikel pada direktori app/views, kemudian buat file baru dengan nama index.php.
![image](https://github.com/user-attachments/assets/caaddbd6-9812-450a-af08-640e5d073089)
Selanjutnya buka browser kembali, dengan mengakses url ```http://localhost:8080/artikel```
12. Kemudian coba tambahkan beberapa data pada database agar dapat ditampilkan datanya. Refresh kembali browser, sehingga akan ditampilkan hasilnya.
![image](https://github.com/user-attachments/assets/07a67a8f-fb48-4736-a767-23d3c3d1ab0b)
13. Membuat View Detail Buat view baru untuk halaman detail dengan nama app/views/artikel/detail.php dan Buka Kembali file app/config/Routes.php, kemudian tambahkan routing untuk artikel detail. 
![image](https://github.com/user-attachments/assets/dc35effe-8578-457a-9305-7dba1fd8c230)
![image](https://github.com/user-attachments/assets/e7a4ddb9-7b42-4756-b1d5-e3057a935901)
14. Membuat Menu Admin Menu admin adalah untuk proses CRUD data artikel. Buat method baru pada Controller Artikel dengan nama admin_index().
![image](https://github.com/user-attachments/assets/15e713f1-4d7c-47fe-abe9-ddf5d2b203b2)
Akses menu admin dengan url ```http://localhost:8080/admin/artikel```
15. Menambah Data Artikel Tambahkan fungsi/method baru pada Controller Artikel dengan nama add().
![image](https://github.com/user-attachments/assets/42f15d7e-47b5-486d-8665-270852b6c7fd)
16. Kemudian buat view untuk form tambah dengan nama form_edit.php
![image](https://github.com/user-attachments/assets/4b7aeb66-4107-4681-ab84-6b1e908b3be6)
![image](https://github.com/user-attachments/assets/0648f6e6-8676-4027-b21e-c820e1c1c945)
http://localhost:8080/admin/artikel/edit/1
17. Menghapus Data Tambahkan fungsi/method baru pada Controller Artikel dengan nama delete().
![image](https://github.com/user-attachments/assets/6b807c15-8e43-47ae-9f1a-06d521531a19)
dan ini hasil dari artikel yang sudah di edit
18. Buat folder layout di dalam app/Views/. Buat file main.php di dalam folder layout
19. Membuat Tabel User
![image](https://github.com/user-attachments/assets/4eec7305-5b9c-4977-a85b-2b421abdaf21)
20. Membuat Model User
Selanjutnya adalah membuat Model untuk memproses data Login. Buat file baru pada direktori app/Models dengan nama UserModel.php
21. Membuat Controller User Buat Controller baru dengan nama User.php pada direktori app/Controllers. Kemudian tambahkan method index() untuk menampilkan daftar user, dan method login() untuk proses login.
22. Membuat View Login. Buat direktori baru dengan nama user pada direktori app/views, kemudian buat file baru dengan nama login.php.
23. Membuat Database Seeder Database seeder digunakan untuk membuat data dummy. Untuk keperluan ujicoba modul login, kita perlu memasukkan data user dan password kedaalam database. Untuk itu buat database seeder untuk tabel user. Buka CLI, kemudian tulis perintah berikut:
```php spark make:seeder UserSeeder```
24. Selanjutnya, buka file UserSeeder.php yang berada di lokasi direktori ```/app/Database/Seeds/UserSeeder```. Selanjutnya buka kembali CLI dan ketik perintah berikut:
```php spark db:seed UserSeeder``` Selanjutnya buka url http://localhost:8080/user/login seperti berikut: ![WhatsApp Image 2025-07-05 at 14 25 12_2da8a9a8](https://github.com/user-attachments/assets/51f3a660-7d94-44e3-aba2-d84b6d9dc286)
25. Kemudian ini adalah tampilan ketika saya sduah login
![image](https://github.com/user-attachments/assets/9913e00a-ca8f-41db-b16d-677b3e49db9f)
status user login 1
26. Menambahkan Auth Filter Selanjutnya membuat filer untuk halaman admin. Buat file baru dengan nama Auth.php pada direktori app/Filters.Percobaan Akses Menu Admin Buka url dengan alamat http://localhost:8080/admin/artikel ketika alamat tersebut diakses maka, akan dimuculkan halaman login.
![image](https://github.com/user-attachments/assets/73fec06d-7833-49c5-8768-f47c8c9a1eb3)
27. Tambahkan method logout pada Controller User
28. Untuk membuat pagination, buka Kembali Controller Artikel, kemudian modifikasi kode
pada method admin_index, Kemudian buka file views/artikel/admin_index.php dan deklarasi tabel data.
![image](https://github.com/user-attachments/assets/930400c6-4568-4b12-b3c1-84aa64307ff1)
29. Membuat Pencarian Pencarian data digunakan untuk memfilter data. Untuk membuat pencarian data, buka kembali Controller Artikel, pada method admin_index
![image](https://github.com/user-attachments/assets/075fb201-f0c8-4137-bec1-f663fb6e522d)
30. Buka kembali Controller Artikel pada project sebelumnya, sesuaikan kode pada method add Kemudian pada file views/artikel/form_add.php tambahkan field input file Dan sesuaikan tag form dengan menambahkan ecrypt type Ujicoba file upload dengan mengakses menu tambah artikel.
![image](https://github.com/user-attachments/assets/d1ef2a05-6fe1-4fc1-8e91-a036ee87de53)
31. Membuat Tabel Kategori Kita akan membuat tabel baru bernama `kategori` untuk mengkategorikan artikel. Struktur Tabel `kategori`
32. Tambahkan foreign key `id_kategori` pada tabel `artikel` untuk membuat relasi dengan tabel
`kategori`. Query untuk menambahkan foreign key:
33. Membuat Model Kategori Buat file model baru di `app/Models` dengan nama `KategoriModel.php`:
34. Modifikasi `ArtikelModel.php` untuk mendefinisikan relasi dengan `KategoriModel`: Menambahkan method `getArtikelDenganKategori()` untuk mengambil data artikel beserta nama kategorinya menggunakan join.
35. Modifikasi `Artikel.php` untuk menggunakan model baru dan menampilkan data relasi:
36. Buka folder view/artikel sesuaikan masing-masing view. index.php
37. Hasil dari Output:
   > Pertama akan diarahkan kehalaman logi user terlebih dahulu http://localhost:8080/index.php/user/login
![image](https://github.com/user-attachments/assets/5b62cd1f-f6e1-4712-b906-a657efb40b1a)
   > Setelah login berhasil akan masuk kehalaman http://localhost:8080/admin/artikel
![image](https://github.com/user-attachments/assets/fe99e9f5-b356-4571-afc0-a1435b544bcb)
Kemudian lakukan search judul artikel yang sudah ada
![image](https://github.com/user-attachments/assets/148f1700-c5ed-4c9f-ad8a-78bb62f0dbd0)
   > Lakukan uji coba menambahkan artikel dan memilih kategori
![image](https://github.com/user-attachments/assets/f58815d8-993f-4aab-977d-f88629fde1a0)

> Buka Kembali project sebelumnya, kemudian kita tambahkan Pustaka yang dibutuhkan pada project tersebut.
> Menambahkan Pustaka jQuery. Kita akan menggunakan pustaka jQuery untuk mempermudah proses AJAX. Download pustaka jQuery versi terbaru dari https://jquery.com dan ekstrak filenya. Salin file jquery-3.6.0.min.js ke folder public/assets/js.
> Membuat Model. Menambahkan Pustaka jQuery. Kita akan menggunakan pustaka jQuery untuk mempermudah proses AJAX. Download pustaka jQuery versi terbaru dari https://jquery.com dan ekstrak filenya. Salin file jquery-3.6.0.min.js ke folder public/assets/js.
> Pada modul sebelumnya sudah dibuat ArtikelModel, pada modul ini kita akan memanfaatkan model tersebut agar dapat diakses melalui AJAX.
> Selesaikan programnya sesuai Langkah-langkah yang ada. Tambahkan fungsu untuk tambah dan ubah data. Anda boleh melakukan improvisasi.
![image](https://github.com/user-attachments/assets/6dfa1bf0-f535-4b8e-a1fa-c3b2aad3f7d1)
![image](https://github.com/user-attachments/assets/9d17c47e-669f-43f4-a9fa-89e753df8ab8)
> untuk membuka tampilan klik http://localhost:8080/ajax

38. Testing REST API CodeIgniter Buka aplikasi postman dan pilih create new → HTTP Request Menampilkan Semua Data Pilih method GET dan Lalu, klik Send. Jika hasil test menampilkan semua data artikel dari database, maka pengujian berhasil.
![image](https://github.com/user-attachments/assets/6a7ff03e-738a-4498-9e50-8fd6f4cf6beb)
39. Menampilkan Data Spesifik Masih menggunakan method GET, hanya perlu menambahkan ID artikel di belakang URL Selanjutnya, klik Send. Request tersebut akan menampilkan data artikel yang memiliki ID
nomor 2 di database.
![image](https://github.com/user-attachments/assets/b8e7e4a1-5fc1-4e58-abe6-49ffb3b5ef81)
39. Mengubah Data Untuk mengubah data, silakan ganti method menjadi PUT. Kemudian, masukkan URL artikel yang ingin diubah. Misalnya, ingin mengubah data artikel dengan ID nomor 2, maka masukkan URL
![image](https://github.com/user-attachments/assets/b993bb5e-d1e8-44ad-8fc8-c0f1dffba8e4)

>>>>>>> 91309623be2833914655e81d63303885cb52b3b1
