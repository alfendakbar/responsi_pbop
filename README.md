# 5230411195 - Alfenda Maulana Akbar

# Deskripsi Aplikasi
Program ini adalah aplikasi manajemen produk dan transaksi berbasis GUI (Graphical User Interface) yang dibuat menggunakan Python dengan library Tkinter untuk interface dan MySQL sebagai database. Program ini memiliki dua tab utama:
- Tab Produk: Untuk menambahkan, mengedit, menghapus, dan melihat daftar produk.
- Tab Transaksi: Untuk mencatat transaksi berdasarkan produk yang tersedia, menghitung total harga otomatis, dan mengelola daftar transaksi

# Cara Menjalankan Aplikasi
1. Buat database dengan nama sistemretail_db.
2. Import file sistemretail_db.sql ke dalam database tersebut.
3. Jalankan Kode Python-nya

# Struktur Tabel
Tabel produk
| Nama Kolom   | Tipe Data     | Keterangan                      |
|--------------|---------------|----------------------------------|
| id_produk    | INT           | Primary Key, Auto Increment     |
| nama_produk  | VARCHAR(255)  | Nama produk                     |
| harga_produk | DECIMAL(10,2) | Harga satuan produk             |

Tabel transaksi
| Nama Kolom        | Tipe Data     | Keterangan                       |
|-------------------|---------------|-----------------------------------|
| id_transaksi      | INT           | Primary Key, Auto Increment      |
| id_produk         | INT           | Foreign Key dari tabel `produk`  |
| jumlah_produk     | INT           | Jumlah produk yang dibeli        |
| total_harga       | DECIMAL(10,2) | Total harga transaksi            |
| tanggal_transaksi | DATE          | Tanggal transaksi                |
