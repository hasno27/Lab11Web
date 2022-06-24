# Lab11Web

# Langkah Praktikum

## 1. Jalankan XAMPP Ubah file php.ini seperti berikut :
![image](https://user-images.githubusercontent.com/83681139/175540804-cc1cdfde-ab26-4443-932b-0969e785a0f2.png)

## 2. Instal Codeigniter 4 dan Buka http://localhost/lab11_php_ci/ci4/public/ , hasilnya :
![image](https://user-images.githubusercontent.com/83681139/175540942-6c0f05e4-7db3-42c1-8c92-293a2a32c9c7.png)

## 3. Buka cmd pada XAMPP Shell lalu buka php spark, untuk menjalankan server ketik "php spark serve" :
+ Hasil error/kesalahan :

![image](https://user-images.githubusercontent.com/83681139/175541104-6bd5ab9b-b4fb-4124-9ab6-351168debe53.png)

## 4. Mengaktifkan mode Debugging dengan mengubah file .env menjadi = development, seperti berikut :
![image](https://user-images.githubusercontent.com/83681139/175541717-d624c8ae-f973-43a8-a419-3d1178faaf10.png)

## 5. Untuk mencoba Error hilangkan tanda ; (titik koma) pada Home.php, seperti berikut :
![image](https://user-images.githubusercontent.com/83681139/175541809-fb387f5a-6898-4646-936a-9cae902452ee.png)

## 6. Struktur Direktori yang tersedia :
![image](https://user-images.githubusercontent.com/83681139/175541994-aa263a64-4b76-4739-8a5e-9d5223e05190.png)

## 7. Mengarahkan router pada controller :
![image](https://user-images.githubusercontent.com/83681139/175542138-39f495c5-23db-47d0-8378-452e7e7db613.png)

## 8. Cek pada CMD dengan memasukan "php spark routes",hasilnya akan seperti berikut :

## 9. Akses route yang telah dibuat dengan http://localhost:8080/about, hasilnya :
![image](https://user-images.githubusercontent.com/83681139/175542273-9dc4c127-f4e5-4e18-b08d-bab93cfa8244.png)

## 10. Membuat Controller Page, dengan membuat file baru bernama page.php seperti berikut :
![image](https://user-images.githubusercontent.com/83681139/175542321-a7bf3abe-e6c7-41c2-a309-7347440d9aa0.png)
+ Hasilnya :

![image](https://user-images.githubusercontent.com/83681139/175542427-b8933a66-e5d0-4c54-929b-a4a660eaf878.png)

## 11. Mengaktifkan AutoRouting dengan men set nilai true/false, jika true maka fungsi akan aktif
![image](https://user-images.githubusercontent.com/83681139/175542822-45791b26-b9b9-4d1b-a953-fbe701cfddc0.png)
+ Akses http://localhost:8080/page/tos karena halaman in belum masuk pada routing, hasilnya :

![image](https://user-images.githubusercontent.com/83681139/175543032-5e860fed-e9f7-4a92-ae71-ca78cac8cf77.png)

## 12. Membuat View, dengan membuat file baru bernama about.php dan masukan kode berikut :
![image](https://user-images.githubusercontent.com/83681139/175546012-0aeeaa25-e733-43f8-8b56-86e2756c8d6f.png)
+ Hasilnya:

![image](https://user-images.githubusercontent.com/83681139/175546082-9b581240-1454-4288-82d7-9946d6725617.png)

## 13. Membuat Layout Web dengan CSS (bisa menggunakan css praktikum sebelumnya Lab4Web) :
![image](https://user-images.githubusercontent.com/83681139/175547313-771c11b6-c573-48bb-949e-6a18539a13db.png)

## 14. Buatlah folder baru dengan nama "template" pada direktori Views, kemudian buat file header dan footer sebagai berikut :
![image](https://user-images.githubusercontent.com/83681139/175547395-893fde52-fdf4-4180-b539-b518d87c4fa9.png)
![image](https://user-images.githubusercontent.com/83681139/175547453-5b8d68e6-dd5b-49f0-a3f9-23e03cbdd7ae.png)

## 15. Kemudian ubah file app/view/about.php seperti berikut :
![image](https://user-images.githubusercontent.com/83681139/175547560-b6390b1f-69d6-495e-8169-d763d005da00.png)

# Praktikum 11 Pertemuan 14 - Pemrograman Web (PHP Framework)

## Laporan Praktikum

## Persiapan

Mengaktifkan beberapa ekstensi php, diantaranya:

+ php-json ekstension untuk bekerja dengan JSON;
+ php-mysqlnd native driver untuk MySQL;
+ php-xml ekstension untuk bekerja dengan XML;
+ php-intl ekstensi untuk membuat aplikasi multibahasa;
+ libcurl (opsional), jika ingin pakai Curl

![image](https://user-images.githubusercontent.com/83681139/175549192-24369510-e7c8-46cf-8179-dc4128e439aa.png)

Hapus tanda ; (titik koma) pada bagian extension yang akan diaktifkan.
![image](https://user-images.githubusercontent.com/83681139/175549293-c9390995-78aa-4a80-b1fc-9ab98b303dd3.png)

## Instalasi CodeIgniter 4
+ Codeigniter dapat didownload dari website https://codeigniter.com/download
+ Extrak file zip Codeigniter ke direktori htdocs/lab11_php_ci.
+ Ubah nama direktory framework-4.x.xx menjadi ci4.
+ Buka browser dengan alamat http://localhost/lab11_php_ci/ci4/public/

Codeigniter menyediakan CLI, untuk mengaksesnya buka terminal lalu arahkan ke direktori project yang akan dibuat. Kemudian jalankan perintah php spark untuk memanggil CLI codeigniter.
![image](https://user-images.githubusercontent.com/83681139/175549600-8d634a5c-dcc3-4a4b-9d45-f9dfd4746179.png)

Codeigniter juga menyediakan mode debugging/development yang dapat menampilkan error/kesalahan dalam kode program. Cara mengaktifkannya dengan mengubah nama file env menjadi .env kemudian buka filenya dan ubah nilai CI_ENVIRONMENT menjadi development.
![image](https://user-images.githubusercontent.com/83681139/175550565-80bb2d78-2537-4c3a-9c6c-02bfb8b323bb.png)

## Langkah 1 - Membuat Route
+ Router terletak pada file app/config/Routes.php

+ Untuk mengetahui route yg ada atau telah berjalan dapat menggunakan perintah php spark routes

![image](https://user-images.githubusercontent.com/83681139/175550955-9d8e253a-4ea4-4180-aa46-25309eb0d76a.png)

+ Selanjutnya mencoba akses route yang telah dibuat dengan mengakses http://localhost:8080/contact

## Langkah 2 - Membuat Controller

+ Membuat file page.php di dalam direktori Controller (/app/Controllers)

![image](https://user-images.githubusercontent.com/83681139/175551502-ff3c6000-6e23-4cd6-804c-c892b4b3ffb5.png)

+ Kemudian refresh browser maka halaman sudah dapat diakses dan menampilkan hasilnya.

+ Menambahkan method baru pada controller page.

+ Method ini dapat diakses dengan menggunakan alamat: http://localhost:8080/page/tos

![image](https://user-images.githubusercontent.com/83681139/175551633-5320b0a6-84fd-440e-9e9d-343369288742.png)

## Langkah 3 - Membuat View

+ Membuat file about.php di dalam direktori View (/app/view/about.php)

![image](https://user-images.githubusercontent.com/83681139/175551774-b89576bf-c981-4329-b18d-e25821e55007.png)

+ Mengubah method about dalam controller page.

![image](https://user-images.githubusercontent.com/83681139/175551831-a43a69a8-ef3e-4ec6-8861-620a992723f1.png)

## Langkah 4 - Membuat Layout Web dengan CSS

+ Buat file css pada direktori public dengan nama style.css (copy file dari praktikum lab4_layout).

![image](https://user-images.githubusercontent.com/83681139/175552033-bc47bfd6-537c-41fd-bba0-b62b83996a0b.png)

+ Kemudian buat folder template pada direktori view, lalu buat file header.php dan footer.php.

![image](https://user-images.githubusercontent.com/83681139/175552110-3203c9cf-99e8-498d-bca5-70341bdf3b86.png)

![image](https://user-images.githubusercontent.com/83681139/175552146-38f0c3dc-c2c8-4ed7-88ce-29919cb85acc.png)

+ Kemudian ubah file about.php (/app/view/about.php) seperti berikut.

<?= $this->include('template/header'); ?>
<h1><?= $title; ?></h1>
<hr>
<p><?= $content; ?></p>
<?= $this->include('template/footer'); ?>

# Laporan Praktikum

## Langkah 1 - Konfigurasi Database

Membuat konfigurasi hubungan ke database server dengan menggunakan file .env.

![image](https://user-images.githubusercontent.com/83681139/175552540-aa03bdd0-9a34-43cb-8f2b-167dfb713dad.png)

## Langkah 2 - Membuat Model

Buat file baru pada direktori /app/Models dengan nama ArtikelModel.php

![image](https://user-images.githubusercontent.com/83681139/175552668-bebfd71c-db0b-4bbe-b9a6-e2ea3b646133.png)

## Langkah 3 - Membuat Controller

Buat Controller baru dengan nama Artikel.php pada direktori /app/Controllers.

![image](https://user-images.githubusercontent.com/83681139/175552809-072e3349-03a0-4b5c-b86b-5fb3ac06575f.png)

## Langkah 4 - Membuat View

Buat direktori baru dengan nama artikel pada direktori /app/Views, kemudian buat file baru dengan nama index.php.

![image](https://user-images.githubusercontent.com/83681139/175552941-ff35563b-bc83-44a8-bf32-5007ff9f2cf4.png)

Lalu buka alamat http://localhost:8080/artikel untuk melihat hasilnya.

## Langkah 5 - Membuat Tampilan Detail Artikel

Tampilan pada saat judul berita di klik maka akan diarahkan ke halaman yang berbeda. Tambahkan sebuah fungsi baru pada Controller Artikel (/app/Controllers/Artikel.php) dengan nama view().

![image](https://user-images.githubusercontent.com/83681139/175553102-e7af8041-e671-4501-955c-46ad774c3567.png)

## Langkah 6 - Membuat View Detail

Buat file baru dalam folder artikel (/app/Views/artikel/) dengan nama detail.php untuk menampilkan halaman detail.

![image](https://user-images.githubusercontent.com/83681139/175553188-49c68861-acf3-485b-b931-afec90800f0d.png)

## Langkah 7 - Membuat Route

Buka file Routes.php dalam folder (/app/Config/) dan tambahkan routing untuk ke halaman detail artikel.
$routes->get('/artikel/(:any)', 'Artikel::view/$1');

![image](https://user-images.githubusercontent.com/83681139/175553325-d46c952c-8581-4221-b692-afe3e8e7bece.png)

## Langkah 8 - Membuat Menu Admin

Menu admin adalah untuk proses CRUD data artikel.
Buat method atau fungsi baru pada Controller Artikel dengan nama admin_index().

![image](https://user-images.githubusercontent.com/83681139/175553471-fcbd76b9-aca9-4a57-9453-ed223b231497.png)

Kemudian buat file admin_index.php dalam folder (/app/Views/artikel/) untuk tampilan halaman admin.

![image](https://user-images.githubusercontent.com/83681139/175553561-5f527695-bb5d-49a0-adb3-bc84959f4cfc.png)

Kemudian tambahkan routing untuk menu admin sebagai berikut:

![image](https://user-images.githubusercontent.com/83681139/175553622-2e3b9988-3f8f-46e9-bbe2-46a2713597f8.png)

## Langkah 9 - Menambah Data Artikel

Tambahkan fungsi/method baru pada Controller Artikel dengan nama add().

![image](https://user-images.githubusercontent.com/83681139/175553755-5dc6e08e-cc4c-4177-859a-b3328bdf8c24.png)

Kemudian buat view untuk form tambah dengan nama form_add.php dalam folder (/app/Views/artikel/).

![image](https://user-images.githubusercontent.com/83681139/175553937-4c1f61d1-c641-4af6-ae4c-b116f65a658b.png)

## Langkah 10 - Mengubah Data

Tambahkan fungsi/method baru pada Controller Artikel dengan nama edit().

![image](https://user-images.githubusercontent.com/83681139/175554094-361e614f-b7d4-4a38-baa9-81950dab5478.png)

Kemudian buat view untuk form tambah dengan nama form_edit.php dalam folder (/app/Views/artikel/).

![image](https://user-images.githubusercontent.com/83681139/175554172-3f66f015-aaa2-4efe-aaea-068813ec6501.png)

## Langkah 11 - Menghapus Data

Tambahkan fungsi/method baru pada Controller Artikel dengan nama delete().

![image](https://user-images.githubusercontent.com/83681139/175554260-96681462-9ddd-4aca-a047-1dfb6ef0cd2b.png)

# Pertanyaan dan Tugas

Selesaikan programnya sesuai Langkah-langkah yang ada. Anda boleh melakukan improvisasi.

# Jawab/Hasil

Saya telah menyelesaikan program diatas agar dapat berjalan dengan semestinya. Seperti membuat file admin_header.php dan admin_footer.php serta CSSnya.
