<h1 align="center">
<br>
  <img src="https://user-images.githubusercontent.com/16473727/120782794-8e48ea00-c554-11eb-8712-a68d91690d2c.png" >
</h1>

<p align="center">
  <a href="#deskripsi-singkat-aplikasi">Deskripsi Singkat Aplikasi</a> •
  <a href="#user-analysis">User Analysis</a> •
  <a href="#spesifikasi-teknis-lingkungan-pengembangan">Spesifikasi Teknis Lingkungan Pengembangan</a> •
  <a href="#konsep-OOP-yang-digunakan">Konsep OOP Yang Digunakan</a> •
  <a href="#tipe-desain-pengembangan-yang-digunakan-(pattern/anti-pattern)">Tipe Desain Pengembangan Yang Digunakan</a> •
  <a href="#pembahasan">Pembahasan</a> •
  <a href="#hasil-implementasi">Hasil Implementasi</a> •
  <a href="#saran">Saran</a> •
  <a href="#developer-dan-jobdesc">Developer dan Job Desc</a> •
  <a href="#lain-lain">Lain-Lain</a> 
</p>

----------


#### Nama Sistem :
Panduan Digital

#### Paralel Praktikum :
Paralel 1 - Kelompok 8

#### Anggota Kelompok :
-   Irlan Fazryana Rahman (G64180004)
-   Rian Reftian Nurochmat (G64180009)
-   Ilham Ghiffari Noorrahmat (G64180012)
-   Pascal Pribadi A. P. (G64180022)
-   Raden Rafly R. F. (G64180033)

# Deskripsi Singkat Aplikasi
[`^ kembali ke atas ^`](#)

Ide yang kami pilih didasari dari **Buku Panduan Program Sarjana IPB** dimana mahasiswa yang ingin mengambil suatu mata kuliah biasanya melihat daftar informasi yang diinginkan dari buku tersebut. Karena hal tersebut, ide yang muncul adalah sebuah aplikasi berbentuk website untuk melihat mata kuliah yang disediakan oleh IPB di setiap jurusannya. Di setiap mata kuliahnya, mahasiswa dapat melihat informasi terkait mata kuliah tersebut, seperti deskripsi mata kuliah, prasyarat, dosen pengajar dan review dari mahasiswa yang sudah mengambil mata kuliah tersebut. Selain itu, terdapat fitur pendataan mahasiswa peserta mata kuliah elektif. Pada rentang waktu tertentu (setelah semester berakhir), mahasiswa IPB semester 3 atau lebih dapat memasukkan/mendata dirinya untuk mahasiswa yang ingin mengikuti suatu mata kuliah elektif tertentu. Untuk melihat mata kuliah elektif yang sedang dipilih, mahasiswa dapat melihat di fitur profil yang berisi daftar mata kuliah elektif yang dipilih.

# User Analysis
[`^ kembali ke atas ^`](#)

-   Sebagai mahasiswa saya ingin mengetahui jumlah mahasiswa yang mengambil suatu matkul elektif supaya saya bisa merencanakan mata kuliah yang akan saya ambil pada semester berikutnya.
-   Sebagai dosen saya ingin melihat jumlah mahasiswa yang mengambil mata kuliah elektif sehingga mata kuliah tersebut dapat dibuka
-   Sebagai mahasiswa saya ingin mengikuti mata kuliah elektif sehingga saya harus menginput nama partisipasi dalam mata kuliah elektif tersebut
-   Sebagai mahasiswa saya ingin mengetahui tentang gambaran umum mata kuliah elektif, sehingga saya tidak salah ambil mata kuliah dan mengambil mata kuliah yang saya senangi.

![Storyboard](https://user-images.githubusercontent.com/16473727/120763684-a9f6c500-c541-11eb-851d-366a1233ad33.jpg)

![Sketsa](https://user-images.githubusercontent.com/16473727/120763709-af540f80-c541-11eb-8051-7d38628b6c4a.jpg)
# Spesifikasi Teknis Lingkungan Pengembangan
[`^ kembali ke atas ^`](#)

- Perangkat Keras
    - Processor : Intel(R) Core(™) i7-8750H CPU@2.20GHz 2.21GHz
    - Memory : 16.0 GB
    - Graphic Card : Nvidia GTX 1070
    - Storage :  HDD 1 TB , SSD 256 GB

- Perangkat Lunak yang digunakan
    
    - Text Editor/IDE :
        - Sublime Text
        - Visual Studio Code
    - Development Management :
        - Github
        - Trello
        - Figma

- Tech Stack :

   - Framework :
       - PHP
       - Material-Ui
       - React JS
   - Database :
        - phpMyAdmin
        - Mysql
        - Laravel 8
   - Testing  :
        - Postman

# Konsep OOP Yang Digunakan
[`^ kembali ke atas ^`](#)


# Tipe Desain Pengembangan Yang Digunakan (Pattern/Anti Pattern)
[`^ kembali ke atas ^`](#)
- Model View Controller
  <br>
  Laravel merupakan framework yang menerapkan MVC untuk pengembangan websitenya. MVC atau Model View Controller adalah sebuah pola desain arsitektur dalam sistem pengembangan website yang terdiri dari:
  <br>
  - Model : Mengelola dan berhubungan langsung dengan database
  - View : Menampilkan informasi pada pengguna
  - Controller : Menghubungkan model dan view dalam setiap proses request dari user.
  <br>
  Alur kerja MVC :
  <br>
  1. Bagian view akan merequest informasi untuk bisa ditampilkan kepada pengguna. <br>
  2. Request tersebut kemudian diambil oleh controller dan diserahkan bagian model untuk diproses. <br> 
  3. Model akan mengolah dan mencari data informasi tersebut di dalam database. <br>
  4. Model memberikan kembali pada controller untuk ditampilkan hasilnya di view. <br>
  5. Controller mengambil hasil olahan yang dilakukan di bagian model dan menatanya di  bagian view. <br>
  
  referensi : [MVC](https://www.niagahoster.co.id/blog/mvc-adalah)

- Repository Pattern
  <br>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Repositori adalah pemisahan antara domain dan <em>persistents layer</em> (pemisah antara menyimpan dan mendapatkan data dari <em>bussiness layer</em>). Repositori menyediakan koleksi <em>Interface</em> untuk mengakses data yang disimpan dalam database, sistem file, atau layanan eksternal. Data dikembalikan dalam bentuk objek. Repository pattern adalah sebuah design pattern yang membuat jembatan antara model dan controller. Design Pattern ini berguna agar model tidak bertanggungjawab untuk berkomunikasi atau mengekstrak data dari database. Model harus berupa objek yang mewakili tabel/dokumen/objek tertentu atau tipe lain apa pun dalam struktur data, dan ini harus menjadi tanggung jawabnya sendiri. Oleh karena itu, untuk menjaga kode Laravel tetap <em>clean</em> dan aman, ada baiknya menggunakan <em>repository</em> untuk memisahkan tanggung jawab yang seharusnya tidak pernah menjadi tanggung jawab model.
  <br>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Repository menyediakan abstraksi data, sehingga aplikasi dapat bekerja dengan abstraksi sederhana yang memiliki <em>Interface</em> yang mendekati <em>collection</em>. Menambah, menghapus, memperbarui, dan memilih item dari <em>collection</em> ini dilakukan melalui serangkaian metode langsung, tanpa perlu berurusan dengan masalah database seperti <em>connections, commands, cursors, or readers</em>.
  <br><br>
 referensi : [Repository Pattern](https://deviq.com/design-patterns/repository-pattern)
 
# Pembahasan
[`^ kembali ke atas ^`](#)

#### Use Case Diagram
![Use Case](https://user-images.githubusercontent.com/16473727/122053751-3aba8400-ce11-11eb-98cb-268b85446203.png)
#### Activity Diagram

 <img src="https://user-images.githubusercontent.com/16473727/120764076-09ed6b80-c542-11eb-9314-08d30ef2b265.png" alt="login" align="center" width="400">
<p float="left">
 <img src="https://user-images.githubusercontent.com/16473727/120764089-0bb72f00-c542-11eb-9b03-eb97788916c4.png" alt="Mendata elektif" width="400">

 <img src="https://user-images.githubusercontent.com/16473727/120764109-11147980-c542-11eb-9e56-0ab59bb4d6fe.png" alt="Melihat mata kuliah" width="400">
</p>
<p float="left">
 <img src="https://user-images.githubusercontent.com/16473727/120764111-11ad1000-c542-11eb-9f56-b07d2ab1c260.png" alt="Membatalkan keikutsertaan elektif" width="400">

 <img src="https://user-images.githubusercontent.com/16473727/120764118-12de3d00-c542-11eb-8060-05930efd920c.png" alt="Menulis Komentar" width="400">
</p>
<p float="left">
 <img src="https://user-images.githubusercontent.com/16473727/120764121-1376d380-c542-11eb-96f3-2d00b8079155.png" alt="Melihat daftar yang tertarik elektif" width="400">

 <img src="https://user-images.githubusercontent.com/16473727/120764123-1376d380-c542-11eb-8fa5-5a062cf8ec2f.png" alt="Melihat dashboard" width="400">
</p>

#### Class Diagram

![CLASS DIAGRAM PANDUAN DIGITAL](https://user-images.githubusercontent.com/60166788/122059566-fb8f3180-ce16-11eb-9ff8-fc73f9d2fc32.png)


#### Entity Relationship Diagram

![Untitled Diagram-Page-2](https://user-images.githubusercontent.com/60166922/122154636-9f1c2880-ce8f-11eb-9539-dcab03694d9f.png)

#### Arsitektur Sistem
<img src="https://user-images.githubusercontent.com/60166788/121908773-81e43e80-cd57-11eb-987e-d3c1e06751bc.png" alt="Melihat dashboard" width="500">

#### Fungsi Utama Yang Dikembangkan
- Tambah data tertarik elektif

#### Fungsi CRUD
- CREATE
  - Membuat komentar
    <br>
    Mahasiswa dapat menuliskan/mengetikkan komentar pada tiap mata kuliah yang tersedia baik Mayor maupun Elektif
  - Mendaftar elektif
    <br>
    Mahasiswa dapat mendata diri sendiri untuk menjadi peserta yang ingin mengikuti mata kuliah Elektif
    
- READ
  - Menampilkan daftar mata kuliah
    <br>
    Aplikasi akan menampilkan mata kuliah sesuai dengan mata kuliah yang tersedia di API IPB
  - Menampilkan daftar komentar
    <br>
    Aplikasi akan menampilkan komentar-komentar yang sudah ditulis/diketik pada tiap mata kuliah yang tersedia baik Mayor maupun Elektif
  - Menampilkan Jumlah elektif tersedia
    <br>
    Aplikasi menampilkan jumlah matakuliah Elektif yang tersedia pada dashboard.
  - Menampilkan Jumlah elektif yang tertarik diikuti
    <br>
    Aplikasi menampilkan jumlah mata kuliah Elektif yang tertarik diikuti pada dashboard.
    
- UPDATE  
  - Mengubah komentar
    <br>
    Mahasiswa dapat mengubah/mengedit komentar yang sudah ditulis/diketikkannya sendiri pada suatu mata kuliah.
    
- DELETE
  - Membatalkan elektif
    <br>
    Mahasiswa dapat membatalkan diri untuk menjadi mahasiswa yang tertarik untuk mengikuti Elektif.
  - Menghapus komentar
    <br>
    Mahasiswa dapat menghapus komentar yang sudah dihapus/diketikkannya sendiri pada suatu mata kuliah.
    

# Hasil Implementasi
[`^ kembali ke atas ^`](#)
- Halaman Login
![image](https://user-images.githubusercontent.com/60166788/122150890-c3c0d200-ce88-11eb-8457-6ba16aacd066.png)
- Halaman Dashboard
![image](https://user-images.githubusercontent.com/60166788/122150928-d4714800-ce88-11eb-9742-c3a603480760.png)
- Halaman Mata Kuliah
![image](https://user-images.githubusercontent.com/60166788/122150946-dd621980-ce88-11eb-8b8f-bbe9a1fb3db6.png)
- Pilih departemen
![image](https://user-images.githubusercontent.com/60166788/122150964-e7841800-ce88-11eb-8e11-3081e7f9bb72.png)
- Halaman Mata Kuliah menampilkan mata kuliah mayor dan elektif
![image](https://user-images.githubusercontent.com/60166788/122151010-f36fda00-ce88-11eb-8cc4-6b16c9ad62d4.png)
- Halaman untuk mata kuliah mayor
![image](https://user-images.githubusercontent.com/60166788/122151027-ff5b9c00-ce88-11eb-9407-27a65eb9f4e9.png)
- Halaman untuk mata kuliah elektif
![image](https://user-images.githubusercontent.com/60166788/122151060-0bdff480-ce89-11eb-81b4-21044b24cc8b.png)


#### Screenshot Sistem
#### Link Aplikasi (jika sudah di deploy)
Front-End: https://quirky-hermann-0d2786.netlify.app/
<br>
Back-End: https://intense-temple-76166.herokuapp.com/

# Saran 
[`^ kembali ke atas ^`](#)
1. Menghandle akun Dosen
2. Menambah Fitur untuk Departemen Lainnya
3. Fitur Komentar hanya bisa digunakan oleh mahasiswa yang sudah mengambil mata kuliah tersebut
4. Melengkapi detail mata kuliah , contoh : prasyarat dan deskripsi

# Developer dan Job Desc
[`^ kembali ke atas ^`](#)

-   Irlan Fazryana Rahman (G64180004) -> BackEnd
-   Rian Reftian Nurochmat (G64180009) -> BackEnd
-   Ilham Ghiffari Noorrahmat (G64180012) -> UI/UX
-   Pascal Pribadi A. P. (G64180022) -> FrontEnd + BackEnd
-   Raden Rafly R. F. (G64180033) -> FrontEnd

# Lain-Lain
[`^ kembali ke atas ^`](#)
- source code Front-end: https://github.com/pascalpap20/panduan-digital
- source code Back-end: https://github.com/pascalpap20/panduan-digital-backend
- Trello : https://trello.com/b/CHrZ9XIN/psbo-2021 

