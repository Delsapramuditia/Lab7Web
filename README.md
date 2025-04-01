![code](https://github.com/user-attachments/assets/1d9281e1-03fd-441c-a519-fc1d625334e2)Praktikum 1: PHP Framework (Codeigniter)

Nama: Delsa Pramuditia

Nim: 312310019

Kelas: TI.23.C1

Tujuan Praktikum
1. Mahasiswa mampu memahami konsep dasar Framework. 
2. Mahasiswa mampu memahami konsep dasar MVC. 
3. Mahasaswa mampu membuat program sederhana menggunakan Framework Codeigniter4.

Langkah 1 : Persiapan awal
- Persiapkan text editor seperti VSCode
- Buat folder baru dengan nama lab11_php_ci pada docroot webserver (htdocs)

Langkah 2 : Melakukan konfigurasi pada webserver
- Mengaktifkan beberapa ekstensi PHP melalui XAMPP Control Panel pada bagian Apache lalu klik Config lalu php.ini, ekstensi yang perlu diaktifkan diantaranya php-json, php-mysqlnd, php-xml, php-intl, dan libcurl.
- Pada bagian extension hilangkan tanda titik koma (;) di ekstensi yang akan diaktifkan kemudian simpan kembali filenya dan restart Apache webserver.

Langkah 3 : Melakukan instalasi Codeigniter menggunakan cara manual
- Mengunduh Codeigniter dan ekstrak ke direktori htdocs/lab11_php_ci lalu ubah nama direktori code igniter menjadi ci4

![Laprak (1)](https://github.com/user-attachments/assets/8d1629d0-3d48-4a06-a786-c8cf9fc5b49a)

- Buka browser dengan alamat http://localhost/lab11_php_ci/ci4/public/
  
![Laprak (2)](https://github.com/user-attachments/assets/af81506f-1446-45a1-9982-02b11a9e0fbe)


Langkah 4 : Menjalankan Command Line Interface (CLI)
- Buka terminal lalu arahkan direktori sesuai dengan direktori kerja project dibuat (xampp/htdocs/lab11_php_ci/ci4)

![Laprak (3)](https://github.com/user-attachments/assets/b15197f1-6d5d-4314-8e56-8a103f9e4cf4)

- Ketik php spark pada terminal untuk menjalankan CLI Codeigniter

![Laprak (4)](https://github.com/user-attachments/assets/53438db9-950e-45aa-abf6-eec45ee67d3b)


Langkah 5 : Mengaktifkan mode debugging
- Ubah nilai konfigurasi pada environment variable CI_ENVIRONMENT menjadi development

![Laprak (5)](https://github.com/user-attachments/assets/df5dbd1d-a261-446f-ab43-670eacd7df14)

- Ubah nama file env menjadi .env

![Laprak (6)](https://github.com/user-attachments/assets/c4cbd595-da77-4c87-8af6-70fb4559405a)


Langkah 6 : Membuat router
- buka file app/config/Routes.php lalu membuat route baru seperti

$routes->get('/about', 'Page::about'); 

$routes->get('/contact', 'Page::contact'); 

$routes->get('/faqs', 'Page::faqs');

untuk mengetahui route yang ditambahkan sudah benar, buka CLI dan jalankan perintah php spark routes selanjutnya akses route yang telah dibuat dengan mengakses url http://localhost:8080/about

![Laprak (7)](https://github.com/user-attachments/assets/fc007b13-6ea2-4918-9194-03e81b03b9e2)


Langkah 7 : Membuat controller
- buat file baru dengan nama page.php pada direktori controller lalu isi dengan kode berikut lalu simpan dan buka lagi url http://localhost:8080/about

![Laprak (8)](https://github.com/user-attachments/assets/ec24b47c-08fe-42b0-b6b8-ed4c0dbe1f9e)

![Laprak (10)](https://github.com/user-attachments/assets/7f66faee-de7a-4992-b2ad-27ce48209d8a)

![Laprak (9)](https://github.com/user-attachments/assets/922e7393-8c43-4224-baa3-80feb249c316)


Langkah 8 : Membuat auto routing
- tambahkan $routes->setAutoRoute(true); pada file Routes.php dan masukan kode berikut pada Controller page lalu simpan dan buka dengan url http:/localhost:8080/tos

![Laprak (12)](https://github.com/user-attachments/assets/ac61361f-5144-4a4a-b7ef-778469517426)

![Laprak (11)](https://github.com/user-attachments/assets/98af01c9-1f38-4ee9-a2d6-8b0e435d6770)


Langkah 9 : Membuat views
- buat file baru dengan nama about.php pada direktori views (app/views/) kemudian isi kode berikut lalu simpan

![Laprak (13)](https://github.com/user-attachments/assets/45a23f8a-de00-4bc0-b907-f5959de297b3)


- ubah method about pada controller page menjadi seperti berikut kemudian simpan dan buka kembali url http://localhost:8080/about

![Laprak (14)](https://github.com/user-attachments/assets/59cd8fc4-78e4-4a46-809e-f6b521e7f99f)

![Laprak (15)](https://github.com/user-attachments/assets/7a57a022-64d3-471a-9c59-5188b17de75c)

Langkah 10 : Membuat layout web dengan CSS
- buat file dengan nama style.css pada direktori public lalu copy isi dari file css pada praktikum sebelumnya
- buat folder template pada direktori views kemudian buat file header.php dan footer.php dan isi kan dengan kode berikut

![code](https://github.com/user-attachments/assets/eb156ea8-52c1-4cfb-8f7a-0d84d7f55324)

![code2](https://github.com/user-attachments/assets/3666ef1d-b6b7-4f6c-b737-47e7adb4d9e1)

- ubah file app/views/about.php menjadi seperti berikut lalu refresh url http://localhost:8080/about

![code3](https://github.com/user-attachments/assets/0cbedbbc-b9ac-4bb6-9bab-ec01a38c288b)



