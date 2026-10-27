Sistem Pengelolaan Pesanan, Produk dan Stok pada Toko Kaca & Aluminium

1. Deskripsi Program

Program ini merupakan aplikasi sederhana berbasis Python yang digunakan untuk mengelola data produk, pelanggan, stok, dan transaksi pembelian pada Toko Kaca & Aluminium. Program dibuat menggunakan konsep Pemrograman Berorientasi Objek (PBO/OOP), sehingga data dan fungsi yang berkaitan dikelompokkan ke dalam beberapa class.

Program memiliki class "Produk", "Kaca", "Aluminium", "Pelanggan", "Transaksi", "Toko", dan "DetailTransaksi". Pada pengembangan kali ini, program menerapkan relasi UML, abstract class, inheritance, dan polimorfisme.

2. Tujuan Program

Program dibuat untuk:
1. Mengelola data produk, termasuk nama, jenis, kode, stok, dan harga.
2. Menambah dan mengurangi stok produk.
3. Mengecek kebutuhan stok.
4. Mengelola data pelanggan serta mengubah nomor HP dan alamat.
5. Memproses transaksi pembelian dan menghitung total harga.
6. Menampilkan detail transaksi dan mencetak struk.
7. Menerapkan encapsulation melalui atribut protected, private, serta getter dan setter.
8. Menerapkan abstraksi dan inheritance pada pengelolaan produk.
9. Menerapkan polimorfisme melalui overriding, duck typing, dan operator overloading.

3. Struktur Class

Program terdiri dari beberapa class berikut:

- Produk: abstract class yang mengelola data umum produk, stok, dan harga. Class ini memiliki dua abstract method, yaitu "tampilkan_spesifikasi()" dan "hitung_nilai_stok()", serta method konkret "info_ringkas()".
- Kaca: subclass dari "Produk" dengan atribut tambahan "ketebalan".
- Aluminium: subclass dari "Produk" dengan atribut tambahan "ukuran".
- Pelanggan: mengelola data pelanggan, nomor HP, dan alamat.
- Transaksi: mengelola pembelian, menghitung total harga, dan menampilkan detail transaksi.
- Toko: mengelola kumpulan objek produk.
- DetailTransaksi: menyimpan informasi produk dan jumlah pembelian dalam transaksi.

4. Relasi UML

Relasi yang diterapkan dalam program meliputi:

- Asosiasi: "Transaksi" berhubungan dengan "Pelanggan" dan "Produk" karena transaksi menggunakan data pelanggan serta produk yang dibeli.
- Agregasi: "Toko" menyimpan kumpulan objek "Produk" yang dibuat secara terpisah. Produk tetap dapat dibuat dan digunakan tanpa harus menjadi bagian dari satu objek toko.
- Komposisi: "Transaksi" memiliki "DetailTransaksi" sebagai bagian dari proses pembelian. Objek detail dibuat ketika pembelian berhasil diproses.

Selain itu, terdapat relasi inheritance dari "Produk" ke "Kaca" dan "Aluminium".

5. Abstraksi dan Inheritance

Class "Produk" menggunakan "ABC" (*Abstract Base Class*) dan memiliki dua abstract method, yaitu "tampilkan_spesifikasi()" dan "hitung_nilai_stok()". Class ini tidak dapat diinstansiasi secara langsung karena abstract method harus diimplementasikan oleh subclass.

Class "Kaca" dan "Aluminium" mengimplementasikan kedua abstract method tersebut dengan perilaku yang sesuai dengan jenis produknya. Kedua subclass menggunakan "super().__init__(...)" untuk memanggil constructor superclass dan memiliki atribut tambahan masing-masing.

Dalam penerapan encapsulation, "_kode_produk" digunakan sebagai atribut protected, sedangkan stok dan harga disimpan menggunakan atribut private.

6. Polimorfisme

Program menerapkan tiga bentuk polimorfisme:

- Polimorfisme melalui pewarisan: method "tampilkan_spesifikasi()" diimplementasikan berbeda pada class "Kaca" dan "Aluminium", kemudian dipanggil melalui satu perulangan.
- Duck typing: fungsi "tampilkan_ringkasan()" dapat digunakan untuk objek "Toko" dan "Transaksi" karena kedua class memiliki method "ringkasan()", meskipun tidak memiliki hubungan inheritance.
- Operator overloading: method "__str__()" pada class "Produk" memungkinkan objek produk ditampilkan menggunakan fungsi "print()".

7. Pengujian

Pengujian dilakukan dengan membuat objek dari subclass dan class lainnya, kemudian menjalankan method yang tersedia. Pengujian meliputi relasi asosiasi, agregasi, dan komposisi; ketidakmampuan menginstansiasi abstract class "Produk"; implementasi abstract method; polimorfisme melalui overriding; duck typing; serta operator overloading.

Pengujian juga mencakup fungsi pengelolaan stok, data pelanggan, transaksi pembelian, perhitungan total harga, dan pencetakan struk.

8. Kesimpulan

Program ini merupakan pengembangan aplikasi pengelolaan produk dan transaksi dengan menerapkan konsep PBO yang lebih lanjut. Selain encapsulation dan inheritance, program menerapkan relasi UML, abstraksi menggunakan abstract class, serta polimorfisme melalui overriding, duck typing, dan operator overloading. Penerapan tersebut membuat struktur program lebih terorganisasi dan memudahkan pengembangan fitur berikutnya.

UML
![alt text](<Diagram Kelas UML Produk dan Transaksi.png>)