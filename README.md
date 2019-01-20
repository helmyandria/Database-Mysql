# About Document

Berisi informasi mengenai metode belajar SQL dasar mengggunakan MySQL

**CATATAN**
1. Biasakan menggunakan `huruf kecil` untuk membuat `nama tabel dan nama field` untuk memudahkan meng-query saat di console.
2. Biasakan `konsisten untuk membuat nama tabel dan nama field` untuk memudahkan saat meng-query di console.
2. Setiap tabel hanya boleh mempunyai `1 primary key`.
3. Boleh menggunakan `lebih dari 1 foreign key` di setiap tabel sesuai kebutuhan.
4. Tabel `master` adalah tabel utama yang independen (baca: berdiri sendiri) / tidak ada foreign key di dalamnya.\
Contoh : Tabel Mahasiswa, Pegawai.
5. Tabel `transaksi` adalah tabel yang terbentuk dari hasil transaksi pada suatu form transaksi, terdapat foreign key di dalam tabel tersebut karena tabel transaksi unindependen (baca : tidak dapat berdiri sendiri).\
Contoh : Tabel penjualan -> tabel barang , tabel penyetokan -> tabel barang (baca : membutuhkan).
