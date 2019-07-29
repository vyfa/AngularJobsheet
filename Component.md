### Jobsheet-5: Component
Mata Kuliah Pemrograman Web Lanjut 
Pengampu: Tim Ajar Pemrograman Web Lanjut
Februari 2019

### Topik 

-	Building Reusable Component

Tujuan

Mahasiswa mampu memahami Building Reusable Component


Pendahuluan
	
Component
Angular merupakan framework yang memiliki konsep Component Based seperti beberapa framework javascript modern lainnya, jadi salah satu yang perlu kita pelajari adalah bagaimana membuat komponen di Angular.

Component templateUrl dan Template
TemplateUrl pada component adalah salah satu property yang bertipe data string dan optional secara defaultnya. Jika pada saat kita membuat atau menggenerate component yang baru maka secara default pada decorator @component terdapat beberapa property antara lain : selector, templateUrl, styleUrl. Untuk membuat template pada angular ada 2 cara yaitu menggunakan templateUrl atau menggunakan template.

Component styles dan stylesUrl
Angular mempunyai style dengan standart CSS, sehingga kita dapat menggunakan stylesheets CSS pada angular. Untuk menggunakan css kita dapat menggunakan styleUrls dan style.

Component Selector
Selector adalah property yang digunakan sebagai identitas dari sebuah directive dan trigger instansiasi dari directive tersebut.

Component API
Component API adalah kombinasi antara input dan output properties pada component seperti gambar dibawah ini.

 
Input Properties
Input properties adalah sebuah dekorator yang menandai sebuah kelas sebagai properti input dan konfigurasi metadata. Properti input mendeklarasikan data yang terikat dengan Angular sehinga secara otomatis dapat memperbarui data selama terdapat perubahan data.

Aliasing Input Properties
Aliasing input properties digunakan untuk memberikan alias pada decorator input.

Output Properties
Setelah kita belajar tentang Input Properties maka selanjutnya kita akan belajar tentang output properties. Output Properties digunakan unutk menampilkan data dari child Component (component selain app.component) ke parent component (app.component).

Passing Event Data
Ada beberapa cara untuk passing event data, antara lain menggunakan dollar event object, instead pass object dan menggunakan interface.

Templates
Pada component terdapat 2 cara menggunakan property template pada decorator component yaitu menggunakan external template atau menggunakan internal template. Untuk external template menggunakan property templateUrl sedangkan internal template menggunakan property template. 

Styles
Pada component terdapat 2 cara menggunakan property style pada decorator component yaitu menggunakan external styleUrl atau menggunakan internal style. Untuk external style menggunakan property styleUrl sedangkan internal style menggunakan property style.



Praktikum – Bagian 1: Component 

Langkah	Keterangan

1	Buatlah sebuah component baru dengan nama server (ng generate component nama-component) atau ng g c server

 
2	Untuk menampilkan isi dari server.component.html maka buka file app.component.html dan tambahkan code berikut :
 
3	Buka localhost lalu catat hasil nya (soal 1)


Praktikum – Bagian 2: Component templateUrl dan template

Langkah	Keterangan
1	Buatlah juga serbuah component baru dengan nama servers (ng generate component nama-component) atau ng g c servers 
2	Buka file servers.component.ts. Tambahkan kode program berikut ini :

 
3	Buka app.component.html. Rubahlah kode program seperti berikut ini :
 
4	Buka localhost lalu catat hasilnya (soal 2)
5	Buka file app.component.html. tambahkan seperti berikut :
 
6	Buka file server.component.html. tambahkan kode seperti berikut :
 
7	Perhatikan pada localhost dan catat hasil yang ditampilkan pada browser (soal 3)

Praktikum - Bagian 3: Component Styles dan StylesUrl

Langkah	Keterangan
1	Buka file server.component.ts dan tambahkan code berikut :

 

3	Buka file app.component.html dan tambahkan code program berikut :

 

4	Buka app.component.html dan tambahkan code program berikut ini :

 

5	Buka localhost lalu catat hasil nya (soal 4)

 Praktikum – Bagian 4: Component Selector

Langkah	Keterangan
1	Buka server.component.ts. tambahkan [ ] pada bagian selector seperti berikut :
 
2	Cek pada localhost, apa yang terjadi? Lakukan inspect pada browser (soal 5)
3	Jika terjadi error seperti berikut :
 
4	Buka app.component.html, cek apakah ada error di dalam code? Jelaskan apa penyebab nya!
5	Lakukan perubahan seperti dibawah ini :
 
catat hasil yang ditampilkan oleh localhost. (soal 6)
6	Buka file server.component.ts, rubah selector menjadi sebuah class seperti berikut :
 
7	Buka app.component.html, lakukan perubahan seperti berikut :
 
8	Catat hasilnya (soal 7)

Praktikum – Bagian 5: Component API

Langkah	Keterangan
1	Buatlah component baru dengan nama favorite (ng g c favorite)

2	Buka file app.component.ts dan buatlah property dengan nama post seperti berikut :

 
3	Buka file app.component.html dan tambahkan code berikut :
 
4	Install font awesome dan bootstrap :
https://www.npmjs.com/package/angular-font-awesome 
https://www.npmjs.com/package/bootstrap 

5	Buka angular.json dan tambahkan style seperti berikut :
 
6	Favorite.component.html dan tambahkan code berikut :

 
7	Buka file app.component.html dan modifikasi kode nya menjadi berikut :
 
8	Buka file favorite.component.ts lalu tambahkan property, decorator input, dan sebuah function onClick seperti berikut :
 
9	Jalankan localhost dan catat hasil nya. (soal 8)

10	Buka file favorite.componenr.ts dan modifikasi code nya seperti berikut :
 
11	Jalankan localhost dan catat hasilnya (soal 9)
12	Buka file favorite.component.ts, lakukan modifikasi seperti berikut :
 
13	Jalankan localhost dan catat hasilnya (soal 10)

Praktikum – Bagian 6: Aliasing Input Properties

Langkah	Keterangan
1	Buka file favorite.component.ts tambahkan onClickAlias() dan modifikasi code nya menjadi seperti berikut :
 
2	Buka file favorite.component.html

 
3	Buka file app.component.html dang anti input property yang sebelumnya [isFavorite] menjadi [aliasFavorite]

 
4	Jalankan localhostnya, catat hasilnya. (soal 11)

Praktikum – Bagian 7: Output Properties

Langkah	Keterangan
1	Buka file app.component.ts, buatlah function onFavoriteChanged()
 
2	Buka file app.component.html tambahkan output properties
 
3	Jika dijalan, pada localhost tidak akan menampilkan sesuatu. Untuk itu perlu ditambahkan decorator input.
4	Buka favorite.component.ts. tambahkan decorator output dan emitEmitter seperti berikut :

 

5	Buka localhost, lakukan klik pada bintang. Dan lihat apa yang terjadi pada console. 
Catat (soal 12)




Praktikum – Bagian 8: Passing Event Data

Ada beberapa cara untuk passing event data, antara lain menggunakan dollar event object, instead pass object dan menggunakan interface

Langkah	Keterangan
1	Buka file favorite.component.ts, tambahkan seperti berikut :

 
2	Buka file app.component.ts, tambahkan seperti berikut :
 
3	Buka file app.component.html, tambahkan seperti berikut :
 
4	Jalankan localhost, dan klik pada star. Cek console apa yang terjadi. (soal 13)
5	Buka favorite.component.ts, lakukan perubahan seperti berikut :
 
6	Agar app.component dapat menerima value yang diberikan oleh favorite.component.ts maka parameter pada method onFavoriteChanged dirubah menjadi eventArgs (Argument pass with event).
 
7	Catat Hasil pada console. (soal 14)
8	Buka file favorite.component.ts kemudian lakukan export sebuah interface dengan nama FavoriteChangeEventArgs dengan nama property newValue bertipe Boolean.

 
9	Buka app.component.ts tambahkan parameter eventArgs sebuah alias interface dengan nama FavoriteChangeEvent.

 
10	Catat Hasil pada console. (soal 15)

 Praktikum – Bagian 9: Aliasing Output Properties


Langkah	Keterangan
1	Buka favorite.component.ts lalu tambahkan binding property name pada decorator output.

 
2	Buka app.component.html, lalu rubah seperti ini
 
3	Catat Hasil pada console. (soal 16)

Praktikum – Bagian 10: Templates

Pada component terdapat 2 cara menggunakan property template pada decorator component yaitu menggunakan external template atau menggunakan internal template. Untuk external template menggunakan property templateUrl sedangkan internal template menggunakan property template. 

Langkah	Keterangan
1	Buka favorite.component.html, tambahkan kode html berikut ini :

 
2	Buka favorite.component.ts, rubahlah template yang digunakan seperti berikut :
 
3	Catat Hasil pada console. (soal 17)

Praktikum – Bagian 11: Styles

Langkah	Keterangan
1	Buka favorite.component.html, pastikan pada property di decorator component terdapat styleUrl
2	Buka file favorite.component.css. tambahkan code berikut :
 
3	Buka favorite.component.ts. modifikasi seperti berikut :

 
4	Jalankan localhost dan catat hasilnya. (soal 18)