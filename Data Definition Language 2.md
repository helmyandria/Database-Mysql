# Introduction
Pada halaman ini berisi informasi mengenai :
- Mengubah nama tabel
- Menambah field baru
- Mengubah nama field
- Mengubah tipe data pada field
- Menambah primary key
- Menghapus primary key
- Menambah foreign key
- Menghapus foreign key
- Menghapus tabel

**Mengubah nama tabel :**
1. Login\
`mysql -u root -p`
2. Gunakan database\
`use [nama database];`\
Contoh :\
`use BELAJARSQL;`
3. Ubah nama tabel\
`ALTER TABLE [nama tabel] RENAME TO [nama tabel baru];`\
Contoh :\
`ALTER TABLE mahasiswa RENAME TO mhs;`

**Menambah field baru :**\
`ALTER TABLE [nama tabel] ADD [kolom baru] [attribute field];`\
Contoh :\
`ALTER TABLE mhs ADD alamat varchar (100) not null;`

**Mengubah nama field:**\
`ALTER TABLE [nama tabel] CHANGE [nama field lama] [nama field baru] [attribute field];`\
Contoh :\
`ALTER TABLE mhs CHANGE alamat alamat_mhs varchar (150);`

**Mengubah tipe data pada field:**\
`ALTER TABLE [nama tabel] MODIFY [nama field] [attribute perubahan];`\
Contoh :\
`ALTER TABLE mhs MODIFY alamat_mhs text(250);`

**Menghapus primary key**\
`ALTER TABLE [nama tabel] DROP PRIMARY KEY;`\
Contoh :\
`ALTER TABLE mhs DROP PRIMARY KEY;`

**Menambah primary key**\
`ALTER TABLE [nama tabel] ADD PRIMARY KEY ([nama field]);`\
Contoh :\
`ALTER TABLE mhs ADD PRIMARY KEY (nrp);`

**Menambah foreign key**\
`ALTER TABLE [nama tabel] ADD CONSTRAINT [nama foreign key] FOREIGN KEY ([nama field]) REFERENCES [nama tabel acuan]([nama field acuan]);`\
Contoh :\
`ALTER TABLE ambil_kuliah ADD CONSTRAINT fk_ambilkodemk FOREIGN KEY (kodemk) REFERENCES matakuliah(kodemk);`\
Catatan : Sebelum itu `buatlah 2 tabel baru` dengan nama sbb, [membuat tabel baru](https://github.com/helmyandria/Database-Mysql/blob/master/Data%20Definition%20Language%201.md):\
Tabel `ambil_kuliah`dengan field `ambilkodemk int(11)`.\
Tabel `mata_kuliah` dengan field `kodemk int(11)`.

**Menghapus foreign key**\
`ALTER TABLE [nama tabel] DROP FOREIGN KEY [nama foreign key];`\
Contoh :\
`ALTER TABLE ambil_kuliah DROP FOREIGN KEY fk_ambilkodemk;`

**Menghapus tabel pada database**\
`DROP TABLE [nama tabel];`\
Contoh :\
`DROP TABLE mhs;`
