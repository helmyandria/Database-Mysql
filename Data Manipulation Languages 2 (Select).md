# Introduction
Pada halaman ini berisi informasi mengenai :
- Select * from where
- Select * from where between / not
- Select * from where like / not
- Select * from where in / not
- Select * from where is null
- Select * from where order by
- Select * from where group by
- Select distinct from
- Select avg / max / min / count / sum

**SELECT - WHERE**\
Cara 1 :\
`SELECT * FROM [nama tabel] where (kondisi);`\
Contoh 1 :\
`SELECT * FROM mhs where jk="L";`

> Digunakan untuk memfilter sesuasi dengan kondisi yang diinginkan.

**SELECT - BETWEEN / NOT BETWEEN**\
Cara 1 :\
`SELECT [nama field] FROM [nama tabel] WHERE [nama field] BETWEEN [value 1] AND [value 2];`\
Contoh 1:\
`SELECT * FROM mhs WHERE nrp BETWEEN '1411110001' AND '141111056';`\
Cara 2 :\
`SELECT [nama field] FROM [nama tabel] WHERE [nama field] NOT BETWEEN [value 1] AND [value 2];`\
Contoh 2:\
`SELECT * FROM mhs WHERE nrp NOT BETWEEN '1411110001' AND '141111056';`

> Digunakan untuk memfilter record berdasarkan range atau diluar range dengan value tertentu.

**SELECT - LIKE / NOT LIKE**\
Cara 1 :\
`SELECT [nama field] FROM [nama tabel] WHERE [nama field] LIKE <‘%karakter / value%’>;`\
Contoh 1 :\
`SELECT * FROM mhs WHERE nama LIKE '%el%';`\
Cara 2 :\
`SELECT [nama field] FROM [nama tabel] WHERE [nama field] NOT LIKE <‘%karakter / value%’>;`\
Contoh 2 :\
`SELECT * FROM mhs WHERE nama NOT LIKE '%el%';`

> Digunakan untuk memfilter record berdasarkan beberapa karakter pada field tertentu atau tidak mengandung karakter tertentu.

**SELECT - IN / NOT IN**\
Cara 1 :\
`SELECT [nama field] FROM [nama tabel] WHERE [nama field] IN ([value 1, value 2]);`\
Contoh 1 :\
`SELECT * FROM mhs WHERE nrp IN ('111110393','101110249');`\
Cara 2 :\
`SELECT [nama field] FROM [nama tabel] WHERE [nama field] NOT IN ([value 1, value 2]);`\
Contoh 2 :\
`SELECT * FROM mhs WHERE nrp NOT IN ('111110393','101110249');`

> Memiliki fungsi hampir sama dengan BETWEEN dan NOT BETWEEN, tetapi difungsikan hanya menggunakan 2 parameter.

**SELECT - NULL / NOT NULL**\
Cara 1 :\
`SELECT [nama field] FROM [nama tabel] WHERE [nama field] IS NULL;`


> Memiliki fungsi menseleksi / menampilkan record yang memiliki field kosong dan sebaliknya.
