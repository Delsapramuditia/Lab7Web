Nama : Delsa Pramuditia

NIM : 312310019

Kelas : TI.23.C1


# Praktikum 1: PHP Framework (CodeIgniter)
## Langkah-langkah Praktikum
### Langkah 1 : Persiapan awal
- Persiapkan text editor seperti VSCode
- Buat folder baru dengan nama lab11_php_ci pada docroot webserver (htdocs)

### Langkah 2 : Melakukan konfigurasi pada webserver
- Mengaktifkan beberapa ekstensi PHP melalui XAMPP Control Panel pada bagian Apache lalu klik Config lalu php.ini, ekstensi yang perlu diaktifkan diantaranya php-json, php-mysqlnd, php-xml, php-intl, dan libcurl.
- Pada bagian extension hilangkan tanda titik koma (;) di ekstensi yang akan diaktifkan kemudian simpan kembali filenya dan restart Apache webserver.

### Langkah 3 : Melakukan instalasi Codeigniter menggunakan cara manual
- Mengunduh Codeigniter dan ekstrak ke direktori htdocs/lab11_php_ci lalu ubah nama direktori code igniter menjadi ci4
![Laprak - 1](Screenshots/Praktikum%201/Laprak%20(1).png)
- Buka browser dengan alamat http://localhost/lab11_php_ci/ci4/public/
![Laprak - 2](Screenshots/Praktikum%201/Laprak%20(2).png)

### Langkah 4 : Menjalankan Command Line Interface (CLI)
- Buka terminal lalu arahkan direktori sesuai dengan direktori kerja project dibuat (xampp/htdocs/lab11_php_ci/ci4)
![Laprak - 3](Screenshots/Praktikum%201/Laprak%20(3).png)
- Ketik php spark pada terminal untuk menjalankan CLI Codeigniter
![Laprak - 4](Screenshots/Praktikum%201/Laprak%20(4).png)

### Langkah 5 : Mengaktifkan mode debugging
- Ubah nilai konfigurasi pada environment variable CI_ENVIRONMENT menjadi development

![Laprak - 5](Screenshots/Praktikum%201/Laprak%20(5).png)
- Ubah nama file env menjadi .env

![Laprak - 6](Screenshots/Praktikum%201/Laprak%20(6).png)

### Langkah 6 : Membuat router
- buka file app/config/Routes.php lalu membuat route baru untuk mengetahui route yang ditambahkan sudah benar, buka CLI dan jalankan perintah php spark routes selanjutnya akses route yang telah dibuat dengan mengakses url http://localhost:8080/about
![Laprak - 7](Screenshots/Praktikum%201/Laprak%20(7).png)

### Langkah 7 : Membuat controller
- buat file baru dengan nama page.php pada direktori controller lalu isi dengan kode berikut lalu simpan dan buka lagi url http://localhost:8080/about
![Laprak - 8](Screenshots/Praktikum%201/Laprak%20(8).png)
![Laprak - 10](Screenshots/Praktikum%201/Laprak%20(10).png)
![Laprak - 9](Screenshots/Praktikum%201/Laprak%20(9).png)

### Langkah 8 : Membuat auto routing
- tambahkan $routes->setAutoRoute(true); pada file Routes.php dan masukan kode berikut pada Controller page lalu simpan dan buka dengan url http:/localhost:8080/tos
![Laprak - 12](Screenshots/Praktikum%201/Laprak%20(12).png)
![Laprak - 11](Screenshots/Praktikum%201/Laprak%20(11).png)

### Langkah 9 : Membuat views
- buat file baru dengan nama about.php pada direktori views (app/views/) kemudian isi kode berikut lalu simpan
![Laprak - 13](Screenshots/Praktikum%201/Laprak%20(13).png)
- ubah method about pada controller page menjadi seperti berikut kemudian simpan dan buka kembali url http://localhost:8080/about
![Laprak - 14](Screenshots/Praktikum%201/Laprak%20(14).png)
![Laprak - 15](Screenshots/Praktikum%201/Laprak%20(15).png)

### Langkah 10 : Membuat layout web dengan CSS
- buat file dengan nama style.css pada direktori public lalu copy isi dari file css pada praktikum sebelumnya
- buat folder template pada direktori views kemudian buat file header.php dan footer.php dan isi kan dengan kode berikut
![code](Screenshots/Praktikum%201/code.png)
![code2](Screenshots/Praktikum%201/code2.png)
- ubah file app/views/about.php menjadi seperti berikut lalu refresh url http://localhost:8080/about
![code3](Screenshots/Praktikum%201/code3.png)
![Laprak - 16](Screenshots/Praktikum%201/Laprak%20(16).png)
![Laprak - 17](Screenshots/Praktikum%201/Laprak%20(17).png)
![Laprak - 18](Screenshots/Praktikum%201/Laprak%20(18).png)
![Laprak - 19](Screenshots/Praktikum%201/Laprak%20(19).png)


# Praktikum 2: Framework Lanjutan (CRUD)
## Langkah-langkah Praktikum
### Langkah 1 : Membuat database lab_ci4 dan tabel artikel
![Laprak 2 - 1](Screenshots/Praktikum%202/laprak%202%20(1).png)

### Langkah 2 : Mengkonfigurasi file.env untuk koneksi ke database
![Laprak 2 - 2](Screenshots/Praktikum%202/laprak%202%20(2).png)

### Langkah 3 : Membuat file ArtikelModel.php sebagai model
![Laprak 2 - 3](Screenshots/Praktikum%202/laprak%202%20(3).png)

### Langkah 4 : Membuat file Artikel.php sebagai controller
![Laprak 2 - 4](Screenshots/Praktikum%202/laprak%202%20(4).png)

### Langkah 5 : Membuat folder artikel di direktori view lalu buat file indeks.php
![Laprak 2 - 5](Screenshots/Praktikum%202/laprak%202%20(5).png)

### Langkah 6 : Menambahkan data artikel melalui SQL
![Laprak 2 - 6](Screenshots/Praktikum%202/laprak%202%20(6).png)

### Langkah 7 : Menambahkan fungsi baru pada controller Artikel dengan nama view(), membuat file detail.php, dan menambahkan routing baru di file routes.php
![Laprak 2 - 7](Screenshots/Praktikum%202/laprak%202%20(7).png)
![Laprak 2 - 8](Screenshots/Praktikum%202/laprak%202%20(8).png)
![Laprak 2 - 9](Screenshots/Praktikum%202/laprak%202%20(9).png)

### Langkah 8 : Membuat menu admin dengan membuat method baru pada controller Artikel dengan nama admin_index() serta membuat file view baru yang bernama admin_index.php lalu tambahkan routing baru pada file routes.php untuk menu admin
![Laprak 2 - 10](Screenshots/Praktikum%202/laprak%202%20(10).png)
![Laprak 2 - 11](Screenshots/Praktikum%202/laprak%202%20(11).png)
![Laprak 2 - 12](Screenshots/Praktikum%202/laprak%202%20(12).png)

### Langkah 9 : Membuat method baru untuk menambahkan data, buat di controller Artikel dengan nama add() serta membuat file view baru yang bernama form_add.php
![Laprak 2 - 13](Screenshots/Praktikum%202/laprak%202%20(13).png)
![Laprak 2 - 14](Screenshots/Praktikum%202/laprak%202%20(14).png)

### Langkah 10 : Membuat method baru untuk mengedit data, buat di controller Artikel dengan nama edit() serta membuat file view baru yang bernama form_edit.php
![Laprak 2 - 15](Screenshots/Praktikum%202/laprak%202%20(15).png)
![Laprak 2 - 16](Screenshots/Praktikum%202/laprak%202%20(16).png)

### Langkah 11 : Membuat method baru untuk menghapus data, buat di controller Artikel dengan nama delete()
![Laprak 2 - 17](Screenshots/Praktikum%202/laprak%202%20(17).png)

## Improvisasi yang dilakukan
- Menambahkan CSS untuk admin panel
![Laprak 2 - 20](Screenshots/Praktikum%202/laprak%202%20(20).png)
- Menambahkan fitur upload gambar
![Laprak 2 - 22](Screenshots/Praktikum%202/laprak%202%20(22).png)
- Menambahkan fitur pencarian artikel
![Laprak 2 - 21](Screenshots/Praktikum%202/laprak%202%20(21).png)

## Hasil akhir praktikum 2
![Laprak 2 - 23](Screenshots/Praktikum%202/laprak%202%20(23).png)
![Laprak 2 - 18](Screenshots/Praktikum%202/laprak%202%20(18).png)
![Laprak 2 - 19](Screenshots/Praktikum%202/laprak%202%20(19).png)


# Praktikum 3: View Layout dan View Cell
## Langkah-langkah Praktikum
### Langkah 1 : Membuat layout utama
- Membuat folder layout di dalam direktori app/Views dan membuat file main.hp di dalam direktori layout
![Laprak 3 - 1](Screenshots/Praktikum%203/Laprak%203%20(1).png)

### Langkah 2 : Modifikasi file view
- Mengubah file home.php, about.php, contact.php, index.php, detail.php untuk menggunakan layout baru
![Laprak 3 - 2](Screenshots/Praktikum%203/Laprak%203%20(2).png)
![Laprak 3 - 3](Screenshots/Praktikum%203/Laprak%203%20(3).png)
![Laprak 3 - 4](Screenshots/Praktikum%203/Laprak%203%20(4).png)
![Laprak 3 - 5](Screenshots/Praktikum%203/Laprak%203%20(5).png)
![Laprak 3 - 6](Screenshots/Praktikum%203/Laprak%203%20(6).png)

### Langkah 3 : Menambahkan field tanggal pada database
- Menambahkan kolom created_at pada tabel artikel
![Laprak 3 - 7](Screenshots/Praktikum%203/Laprak%203%20(7).png)

### Langkah 4 : Membuat class view cell
- Membuat folder Cells dan buat file ArtikelTerkini.php di dalamnya
![Laprak 3 - 8](Screenshots/Praktikum%203/Laprak%203%20(8).png)

### Langkah 5 : Membuat view untuk view cell
- Membuat folder components dan buat file artikel_terkini.php di dalamnya
![Laprak 3 - 9](Screenshots/Praktikum%203/Laprak%203%20(9).png)

### Langkah 6 : Melakukan improvisasi dengan menambahkan kategori pada artikel
- Menambahkan kolom kategori dan mengimplementasikan filter berdasarkan kategori lalu modifikasi file ArtikelModel.php, ArtikelTerkini.php, artikel_terkini.php, dan main.php.
![Laprak 3 - 10](Screenshots/Praktikum%203/Laprak%203%20(10).png)
![Laprak 3 - 11](Screenshots/Praktikum%203/Laprak%203%20(11).png)
![Laprak 3 - 12](Screenshots/Praktikum%203/Laprak%203%20(12).png)
![Laprak 3 - 13](Screenshots/Praktikum%203/Laprak%203%20(13).png)
![Laprak 3 - 14](Screenshots/Praktikum%203/Laprak%203%20(14).png)
![Laprak 3 - 15](Screenshots/Praktikum%203/Laprak%203%20(15).png)


## Jawaban Pertanyaan
### 1. Apa manfaat utama dari penggunaan View Layout dalam pengembangan aplikasi?
Manfaat utama dari penggunaan View Layout dalam pengembangan aplikasi adalah:
1. **Konsistensi Tampilan**: View Layout memastikan semua halaman memiliki struktur dan tampilan yang konsisten.
2. **Pemisahan Konten dan Layout**: Memisahkan konten spesifik halaman dari struktur layout umum, sehingga kode lebih terorganisir.
3. **Penggunaan Kembali Kode (Reusability)**: Layout yang sama dapat digunakan oleh banyak halaman tanpa perlu menulis ulang kode.
4. **Pemeliharaan yang Lebih Mudah**: Perubahan pada layout cukup dilakukan di satu tempat dan akan berlaku untuk semua halaman yang menggunakannya.
5. **Pengembangan yang Lebih Cepat**: Pengembang dapat fokus pada konten halaman tanpa perlu mengulang-ulang kode layout.

### 2. Jelaskan perbedaan antara View Cell dan View biasa.
Perbedaan antara View Cell dan View biasa:
1. **Fungsi dan Tujuan**:
- **View Biasa**: Digunakan untuk menampilkan halaman lengkap atau bagian dari halaman.
- **View Cell**: Digunakan untuk membuat komponen UI yang dapat digunakan ulang dan bersifat modular.
2. **Cara Pemanggilan**:
- **View Biasa**: Dipanggil dengan `return view('nama_view', $data)` atau `echo view('nama_view', $data)`.
- **View Cell**: Dipanggil dengan `<?= view_cell('Namespace\\Class::method', $params) ?>`.
3. **Logika Bisnis**:
- **View Biasa**: Biasanya tidak memiliki logika bisnis, hanya menerima data dari controller.
- **View Cell**: Dapat memiliki logika bisnis sendiri, seperti mengambil data dari database.
4. **Penggunaan Kembali**:
- **View Biasa**: Dapat digunakan kembali dengan include/extend, tetapi kurang fleksibel.
- **View Cell**: Dirancang khusus untuk komponen yang digunakan berulang kali di berbagai halaman.
5. **Isolasi**:
- **View Biasa**: Berbagi konteks dengan view yang memanggilnya.
- **View Cell**: Memiliki konteks tersendiri, terisolasi dari view yang memanggilnya.

### 3. Ubah View Cell agar hanya menampilkan post dengan kategori tertentu.
- Modifikasi method render() di class ArtikelTerkini untuk menerima parameter kategori:
![Laprak 3 - 16](Screenshots/Praktikum%203/Laprak%203%20(16).png)

- Panggil View Cell dengan parameter kategori di layout:
![Laprak 3 - 17](Screenshots/Praktikum%203/Laprak%203%20(17).png)

## Hasil akhir praktikum 3
![Laprak 3 - 18](Screenshots/Praktikum%203/Laprak%203%20(18).png)


# Praktikum 4: Framework Lanjutan (Modul Login)
## Langkah-langkah Praktikum
### Langkah 1 : Membuat tabel user
- Membuat tabel user di database lab_ci4
![Laprak 4 - 1](Screenshots/Praktikum%204/Laprak%204%20(1).png)

### Langkah 2 : Membuat model user
- Membuat file UserModel.php
![Laprak 4 - 2](Screenshots/Praktikum%204/Laprak%204%20(2).png)

### Langkah 3 : Membuat controller user
- Membuat file User.php
![Laprak 4 - 3](Screenshots/Praktikum%204/Laprak%204%20(3).png)

### Langkah 4 : Membuat view login
- Membuat file login.php di direktori user
![Laprak 4 - 4](Screenshots/Praktikum%204/Laprak%204%20(4).png)

### Langkah 5 : Membuat database seeder
- Membuat UserSeeder untuk data dummy
![Laprak 4 - 5](Screenshots/Praktikum%204/Laprak%204%20(5).png)
![Laprak 4 - 6](Screenshots/Praktikum%204/Laprak%204%20(6).png)
![Laprak 4 - 7](Screenshots/Praktikum%204/Laprak%204%20(7).png)

### Langkah 6 : Membuat Auth Filter
- Membuat file Auth.php di folder Filters
![Laprak 4 - 8](Screenshots/Praktikum%204/Laprak%204%20(8).png)
![Laprak 4 - 9](Screenshots/Praktikum%204/Laprak%204%20(9).png)
![Laprak 4 - 10](Screenshots/Praktikum%204/Laprak%204%20(10).png)

### Langkah 7 : Menambahkan fungsi logout
- Menambahkan tombol logout
![Laprak 4 - 11](Screenshots/Praktikum%204/Laprak%204%20(11).png)

## Improvisasi yang dilakukan
1. Menambahkan halaman register
![Laprak 4 - 12](Screenshots/Praktikum%204/Laprak%204%20(12).png)
![Laprak 4 - 13](Screenshots/Praktikum%204/Laprak%204%20(13).png)
![Laprak 4 - 14](Screenshots/Praktikum%204/Laprak%204%20(14).png)

2. Menambahkan dashboard admin
![Laprak 4 - 15](Screenshots/Praktikum%204/Laprak%204%20(15).png)
![Laprak 4 - 16](Screenshots/Praktikum%204/Laprak%204%20(16).png)
![Laprak 4 - 17](Screenshots/Praktikum%204/Laprak%204%20(17).png)

3. Memperbaiki tampilan dengan CSS
![Laprak 4 - 18](Screenshots/Praktikum%204/Laprak%204%20(18).png)

## Hasil akhir praktikum 4
![Laprak 4 - 19](Screenshots/Praktikum%204/Laprak%204%20(19).png)
![Laprak 4 - 20](Screenshots/Praktikum%204/Laprak%204%20(20).png)
![Laprak 4 - 21](Screenshots/Praktikum%204/Laprak%204%20(21).png)

# Praktikum 5: Pagination dan pencarian
## Langkah-langkah Praktikum
### Langkah 1 : Membuat pagination
- Modifikasi controller artikel dan view admin_index.php
![Laprak 5 - 7](Screenshots/Praktikum%205/Laprak%205%20(7).png)
![Laprak 5 - 6](Screenshots/Praktikum%205/Laprak%205%20(6).png)
![Laprak 5 - 3](Screenshots/Praktikum%205/Laprak%205%20(3).png)

### Langkah 2 : Membuat pencarian
- Modifikasi method admin_index untuk menambahkan fitur pencarian dan link pagination, lalu tambahkan form pencarian di View.
![Laprak 5 - 4](Screenshots/Praktikum%205/Laprak%205%20(4).png)
![Laprak 5 - 8](Screenshots/Praktikum%205/Laprak%205%20(5).png)
![Laprak 5 - 8](Screenshots/Praktikum%205/Laprak%205%20(8).png)
![Laprak 5 - 9](Screenshots/Praktikum%205/Laprak%205%20(9).png)

## Hasil akhir praktikum 5
![Laprak 5 - 1](Screenshots/Praktikum%205/Laprak%205%20(1).png)

# Praktikum 6: Upload File Gambar
## Langkah-langkah Praktikum
### Langkah 1 : Modifikasi method add() pada controller artikel
- Modifikasi controller artikel
![Laprak 6 - 3](Screenshots/Praktikum%206/Laprak%206%20(3).png)

### Langkah 2 : Modifikasi file form_add.php
- Menambahkan field input dan sesuaikan tag form dengan menambahkan ecrypt type.
![Laprak 6 - 1](Screenshots/Praktikum%206/Laprak%206%20(1).png)

## Hasil akhir praktikum 6
![Laprak 6 - 2](Screenshots/Praktikum%206/Laprak%206%20(2).png)

