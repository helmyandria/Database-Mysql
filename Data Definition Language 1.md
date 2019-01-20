# Introduction
Pada halaman ini berisi informasi mengenai :
- Mengelola database
- Mengelola tabel
- Relationship

**Mengelola database :**
1. Login\
`mysql -u root -p`
2. Membuat database\
`CREATE DATABASE [nama database];`\
Contoh :\
`CREATE DATABASE BELAJARSQL;`
3. Melihat database\
`SHOW DATABASES;`
4. Menghapus database\
`DROP DATABASE [nama database];`\
Contoh :\
`DROP DATABASE BELAJARSQL;`

**Mengelola tabel :**
1. Login\
`mysql -u root -p`
2. Gunakan database\
`use [nama database];`\
Contoh :\
`use BELAJARSQL;`
3. Membuat tabel
```
CREATE TABLE [nama tabel] (
[nama kolom1] [tipe data] ([ukuran]) [atribut],
[nama kolom2] [tipe data] ([ukuran]) [atribut],
PRIMARY KEY (nama kolom primary)
);
```
Contoh :
```
CREATE TABLE mahasiswa (
nrp varchar (10) not null,
nama varchar (25) not null,
jk char (1) not null,
email varchar (25) null,
PRIMARY KEY (nrp)
);
```
4. Membuat foreign key \
`FOREIGN KEY ([nama field]) REFERENCES [nama tabel referensi]([nama field pada tabel referensi]);`\
Contoh :\
`FOREIGN KEY (nrp) REFERENCES mahasiswa(nrp);`

**Back up & Restore :**
1. Back up \
`Mysqldump –u [username] -p [password] [nama database] > [namafile.sql]`\
Contoh :\
`Mysqldump –u helmy -p BELAJARSQL > BELAJARSQL.sql`
2. Restore \
`Mysqldump –u [username] -p [password] [nama database] < [namafile.sql]`\
Contoh :\
`Mysqldump –u helmy -p BELAJARSQL < BELAJARSQL.sql`
