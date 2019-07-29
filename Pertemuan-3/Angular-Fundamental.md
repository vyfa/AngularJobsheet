### Topik 
-	Pengenalan Dasar Angular

### Tujuan

Mahasiswa diharapkan dapat:
1. Memahami dasar-dasar angular beserta komponennya
2. Membuat komponen menggunakan angular CLI

### Pendahuluan
	
Angular merupakan framework yang memiliki konsep Component Based seperti beberapa framework javascript modern lainnya sehingga diperlukan untuk mengetahui komponen apa aja yang akan dibuat pada angular. Pertama kali yang harus diperhatikan adalah bagaimana membuat file component pertama. Angular CLI akan mengenerate file app.module.ts, app.component.ts, app.component.html, app.component.css dan app.component.spec.ts
Component

Komponen pada Angular merupakan bagian-bagian kecil dari keselurahan aplikasi. Misal pada aplikasi chat terdapat komponent form, button, box-chat, balon chat, dsb tergantung bagaimana anda membagi menjadi kepingan-kepingan dari suatu aplikasi utuh atau sebagai contoh pada gambar 1 desain course dimana ada navbar, sidebar dan isi dari course. Pada angular bagian-bagian tersebut dibuat sebagai sebuah component yang nantinya akan saling terkait sehingga hasilnya seperti pada gambar 2.

### Modules

Angular memiliki root module yang bertanggung jawab untuk melakukan boostraping(sebuah modul kecil yang berfungsi untuk mengaktifasi komponen/program yang lebih komplex dengan menggunakan mekanisme tertentu) yang berguna untuk melaunch aplikasi angular.  Setelah bootstraping maka aplikasi akan ditampilkan dibrowser dan angular akan menghandle user interaction sesuai dengan kode/instruksi yang kita tulis. 
Angular Root Module adalah sistem yang terdapat pada angular dan memiliki fungsi sebagai organisator dari keseluruhan komponen, sehingga root module adalah modul yang mengorganisasi modul-modul lainnya. Aplikasi yang dibangun dengan menggunakan angular akan tersusun dari komponen-komponen kecil. Angular Root Module membantu dalam mengorganisasi komponen-komponen tersebut sehingga dapat saling berinteraksi untuk mencapai tujuan tertentu. Angular rootmodule terletak di app.module.ts

dengan studi kasus course terdapat beberapa modules yang dapat kita buat antara lain module course, module messaging yang berisi perintah-perintah untuk mengirim pesan dll, module instructor, dan module admin.


### Praktikum – Bagian 1: Component Basic

#### Langkah Keterangan
1. Buatlah sebuah componen dengan nama courses dengan cara 
 ng generate component name atau ng g c name
2. Catat hasilnya (soal 1)
3. Buka file app.component.html, lakukan modifikasi code nya menjadi seperti berikut : 

 
4. Kemudian open terminal dan jalan kan perintah ng serve --open, lalu perhatikan pada browser. Catat hasilnya (soal 2)
5. Buka file app.modules.ts dan hapus coursecomponent pada declarations

 
6. kemudian perhatikan hasilnya pada browser. Catat hasil nya (soal 3)
7. Kemudian lakukan inspect pada halaman localhost : 4200 di browser, apa yang terlihat? Berikan penjelasan (soal 4)


### Praktikum – Bagian 2: Templates

#### Langkah Keterangan
1. Buka file courses.component.ts tambahkan property baru dengan nama title

 
2. Kemudian buka browser localhost : 4200. Catat hasilnya (soal 5)
3. Tambahkan string pada binding datanya. Buka file courses.component.html. tambahkan seperti berikut :
 

4. Perhatikan dan catat hasil yang ditampilkan oleh browser (soal 6)
5. Buka file courses.component.ts dan buatlah sebuah method dengan nama getTitle seperti berikut ini :


6. Kemudian buka file courses.component.html, lakukan modifikasi sperti berikut :


7. Perhatikan dan catat hasil yang ditampilkan pada browser (soal 7)

### Praktikum - Bagian 3: Directive

#### Langkah Keterangan
1. Buka file courses.component.ts dan buat property dengan nama course dengan data berupa array

2. Buka file courses.component.html lalu tambahkan directive ngFor dan string interpolation seperti berikut :


3. Perhatikan dan catat hasil yang ditampilkan pada browser (soal 8)

### Praktikum – Bagian 4: Services dan Dependency Injection

#### Langkah Keterangan
1. Buatlah service baru yang bernama courses dengan perintah  : ng generate service courses atau ng g s courses
2. Catat hasilnya (soal 9)
3. Buka file courses.service.ts kemudian tambahkan method getCourse seperti berikut :

 
4. Buka file courses.component.ts, kemudikan lakukan modifikasi codenya seperti berikut :
 
5. Perhatikan dan catat hasil yang ditampilkan pada browser (soal 10)
6. Tambahkan constructor seperti berikut :
 
7. Perhatikan dan catat hasil yang ditampilkan pada browser (soal 11)

### Tugas pertama

1. Buatlah tampilan dibawah ini dengan directive ngFor tanpa service dan dependency injection!


















### Tugas Kedua 

2. Buatlah seperti pada gambar dibawah ini:

 
dengan ketentuan 
- “ini tugas” dan “tanggal” menggunakan binding data dan rata tengah
- nama dan alamat menggunakan binding data
- hobby menggunakan service 
