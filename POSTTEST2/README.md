Sistem Pengelolaan Pesanan, Produk dan Stok pada Toko Kaca & Aluminium

1. Deskripsi Program

Program ini merupakan aplikasi sederhana berbasis Python yang digunakan untuk mengelola data produk, pelanggan, stok, dan transaksi pada Toko
Kaca & Aluminium. Program dibuat menggunakan konsep Pemrograman Berorientasi Objek (PBO/OOP), sehingga data dan fungsi yang berkaitan
dikelompokkan ke dalam beberapa class.
Program memiliki tiga class utama, yaitu 'Produk', 'Pelanggan', dan 'Transaksi'. Masing-masing class memiliki atribut dan method yang memiliki tugas yang berbeda.
pada tugas kali ini ditambahkan penerapan relasi UML dan inheritance

2. Tujuan Program

Program dibuat untuk:
    1. Mengelola data produk seperti nama, jenis, stok, dan harga.
    2. Menambah dan mengurangi stok produk.
    3. Mengecek kebutuhan stok.
    4. Mengelola data pelanggan.
    5. Mengubah nomor HP dan alamat pelanggan.
    6. Membuat dan memproses transaksi pembelian.
    7. Menghitung total harga transaksi.
    8. Menampilkan detail transaksi dan mencetak struk.
    9. Menerapkan konsep dasar PBO seperti object, instance method, class method, static method, dan encapsulation melalui getter/setter.


3. Struktur Class

    Program terdiri dari beberapa class, yaitu:

        Produk: mengelola data produk, stok, dan harga.
        ProdukKaca: subclass dari 'Produk' dengan atribut tambahan 'ketebalan'.
        ProdukAluminium: subclass dari 'Produk' dengan atribut tambahan 'ukuran'.
        Pelanggan: mengelola data pelanggan.
        Transaksi: mengelola proses pembelian dan total harga.
        Toko: mengelola kumpulan produk.
        DetailTransaksi: menyimpan detail suatu transaksi.

4. Relasi UML

Relasi yang diterapkan dalam program:
- Asosiasi: 'Transaksi' berhubungan dengan 'Pelanggan' dan 'Produk'.
- Agregasi: 'Toko' memiliki kumpulan 'Produk'.
- Komposisi: 'Transaksi' memiliki 'DetailTransaksi'.

5. inheritance

Class 'Produk' digunakan sebagai superclass, sedangkan 'ProdukKaca' dan 'ProdukAluminium' menjadi subclass.
Kedua subclass menggunakan 'super().__init__()' untuk memanggil constructor dari superclass. Setiap subclass memiliki atribut tambahan yang berbeda, yaitu 'ketebalan' pada 'ProdukKaca' dan 'ukuran' pada 'ProdukAluminium'.
Class 'Produk' juga menggunakan atribut protected '_kode_produk', sedangkan data seperti stok dan harga menggunakan atribut private.

6. pengujian

Pengujian dilakukan dengan membuat object dari setiap class dan menjalankan method yang tersedia. Pengujian mencakup pengelolaan produk, pelanggan, transaksi, relasi antar-class, inheritance, penggunaan 'super()', serta validasi setter dengan data valid dan tidak valid.