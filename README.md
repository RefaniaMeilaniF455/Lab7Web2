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

# Langkah-langkah :
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
3. Menjalankan CLI (Command Line Interface), Codeigniter 4 menyediakan CLI untuk mempermudah proses development. Untuk mengakses CLI buka terminal/command prompt.  
![image](https://github.com/user-attachments/assets/3ff09c24-5f7a-44ff-a2d3-090773999761)
4. Untuk memudahkan mengetahui jenis errornya, maka perlu diaktifkan mode debugging dengan mengubah nilai konfigurasi pada environment variable CI_ENVIRINMENT menjadi development.
![image](https://github.com/user-attachments/assets/c8553b06-9765-4098-9ccf-ca36883b1dec)
![image](https://github.com/user-attachments/assets/e9a2e384-7c0e-4b50-adfe-0955fc089131)

5. Ubah nama file env menjadi .env kemudian buka file tersebut dan ubah nilai variable CI_ENVIRINMENT menjadi development.

6. 





