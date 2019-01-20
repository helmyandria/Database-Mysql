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
`ALTER TABLE Mahasiswa RENAME TO Mhs;`

**Menambah field baru :**\
`ALTER TABLE [nama tabel] ADD [kolom baru] [attribute field];`\
Contoh :\
`ALTER TABLE Mhs ADD Alamat varchar (100) not null;`

**Mengubah nama field:**\
`ALTER TABLE [nama tabel] CHANGE [nama field lama] [nama field baru] [attribute field];`\
Contoh :\
`ALTER TABLE Mhs CHANGE Alamat Alamat_mhs varchar (150);`

**Mengubah tipe data pada field:**\
`ALTER TABLE [nama tabel] MODIFY [nama field] [attribute perubahan];`\
Contoh :\
`ALTER TABLE Mhs MODIFY Alamat_mhs text(11);`

**Menghapus primary key**\
`ALTER TABLE [nama tabel] DROP PRIMARY KEY;`\
Contoh :\
`ALTER TABLE 'Mhs' DROP PRIMARY KEY;`

**Menambah primary key**\
`ALTER TABLE [nama tabel] ADD PRIMARY KEY ([nama field]);`\
Contoh :\
`ALTER TABLE Mhs ADD PRIMARY KEY (NRP);`

**Menambah foreign key**\
`ALTER TABLE [nama tabel] ADD CONSTRAINT [nama foreign key] FOREIGN KEY ([nama field]) REFERENCES [nama tabel acuan]([nama field acuan]);`\
Contoh :\
`ALTER TABLE AmbilKuliah ADD CONSTRAINT fk_AmbilKodeMK FOREIGN KEY (KodeMK) REFERENCES MataKuliah(KodeMK);`

**Menghapus foreign key**\
`ALTER TABLE [nama tabel] DROP FOREIGN KEY [nama foreign key];`\
Contoh :\
`ALTER TABLE AmbilKuliah DROP FOREIGN KEY fk_AmbilNRP;`

**Menghapus tabel pada database**\
`DROP TABLE [nama tabel];`\
Contoh :\
`DROP TABLE Mhs;`
