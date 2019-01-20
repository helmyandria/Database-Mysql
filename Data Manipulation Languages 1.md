# Introduction
Pada halaman ini berisi informasi mengenai :
- Memasukkan data (insert)
- Melihat data (select)
- Mengubah data (update)
- Menghapus data (delete)

**Memasukkan data (insert)**\
Cara 1 :\
`insert into [nama tabel] [nama field] values [isi data];`\
Contoh 1 :\
`insert into mhs nama,jk values helmy,L;`\
Cara 2 :\
`insert into [nama tabel] values [isi data];`\
Contoh 2 :\
`insert into mhs nama,jk values 141111056,helmy,L,helmyandria@gmail.com,Jombang;`\
Cara 3 :\
`insert into [nama tabel] values [isi data];`\
Contoh 3 :\
`insert into mhs values 141111056,helmy,L,helmyandria@gmail.com,Jombang;`

**Melihat data (select)**\
Cara 1 :\
`select * from [nama tabel];`\
Contoh 1 :\
`select * from mhs;`\
Cara 2 :\
`select [nama field 1],[nama field 2] from [nama tabel];`\
Contoh 2 :\
`select nama,jk from mhs;`

**Mengubah data (update)**\
`update [nama tabel] set [nama field]="nilai baru" where (kondisi);`\
Contoh :\
`update mhs set nama="memy" where nrp="141111056";`\
Catatan: kondisi bisa menggunakan parameter nama field yang lain selama ada pada tabel tersebut.

**Menghapus data (delete)**\
`delete from [nama tabel] where (kondisi);`\
Contoh :\
`delete from mhs where nrp="141111056";`
