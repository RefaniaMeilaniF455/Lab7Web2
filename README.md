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
![image](https://github.com/user-attachments/assets/5c7821db-2f94-42a1-83d2-4122d7f11008)
2. Instalasi Codeigniter 4, untuk melakukan instalasi Codeigniter 4 dapat dilakukan dengan dua cara, yaitu cara manual dan menggunakan composer. Pada praktikum ini kita menggunakan cara manual.
```
Unduh Codeigniter dari website https://codeigniter.com/download  
• Extrak file zip Codeigniter ke direktori htdocs/lab11_ci. 
• Ubah nama direktory framework-4.x.xx menjadi ci4. 
• Buka browser dengan alamat http://localhost/lab11_ci/ci4/public/
```





