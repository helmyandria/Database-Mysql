#Intro\
Pada halaman ini berisi informasi mengenai :
- Link download bahan
- Cara akses mysql
- Membuat database
- Mengelola user baru

**Bahan :**
- [Xampp](https://www.apachefriends.org/download.html)
- [Power Designer](https://www.sap.com/cmp/syb/crm-xm16-gam-it-dtcpdt/index.html)

**Cara akses :**
1. Buka Xampp
2. Start Mysql
3. Buka terminal atau cmd\
`cd c:\xampp\mysql\bin`
4. Login\
`mysql –u root –p`

**Membuat database :**\
`CREATE DATABASE [nama database];`\
Contoh :\
`CREATE DATABASE BELAJARSQL;`

**Mengelola user baru :**
1. Login mengunakan root\
`mysql –u root –p`
2. Masukkan perintah membuat user baru\
`CREATE USER ‘[nama user]’@’[server]’ IDENTIFIED BY ‘[password]’;`\
Contoh :\
`CREATE USER ‘helmy’@’localhost’ IDENTIFIED BY ‘qwerty12345’;`
3. Berikan hak akses\
`GRANT [tipe hak akses] ON [database].[tabel] TO ‘[nama user]’@'[server]’;`\
dengan tipe hak akses sebagai berikut :
- ALL PRIVILEGE / ALL
- Create
- Drop
- Delete
- Insert
- Select
- Update\
Contoh :\
`GRANT ALL ON BELAJARSQL.* TO ‘helmy’@'localhost’;`\
`GRANT UPDATE ON BELAJARSQL.* TO ‘helmy’@'localhost’;`\
`GRANT UPDATE,SELECT,CREATE ON BELAJARSQL.* TO ‘helmy’@'localhost’;`\
Catatan :
tanda `(*)` menunjukkan semua tabel pada database BELAJARSQL
4. Melihat hak akses user\
`SHOW GRANTS FOR '[nama user]'@'[server]';`\
Contoh :\
`SHOW GRANTS FOR 'helmy'@'localhost';`
5. Menghapus hak akses user\
`REVOKE [tipe hak akses] ON [nama database].[tabel] FROM‘[nama user]’@‘[server]’;`\
Contoh :\
`REVOKE INSERT ON BELAJARSQL.* FROM ‘helmy’@‘localhost’;`
6. Menghapus user\
`DROP USER ‘[nama user]’@‘[server]’;`\
Contoh :\
`DROP USER ‘helmy’@‘localhost’;`
