## QUIZ
### Berikan contoh pemanfaatan data historis
- Jawab : Di perusahaan pemasaran produk A. pada suatu hari GM-nya meminta bagian data kearsipan untuk membuat laporan pendataan arsip perusahaan B berdasar dari tanggal pengadaan arsip, dimulai dari 5 tahun lalu hingga sekarang. Laporan tersebut akan digunakan untuk pendaatan data kearsipan di perusahaan dan program customer relation, seperti mencari produk - produk untuk ditampung terlebih dahulu sebelum masa pemesanan.
### Rancang ERD untuk penyimpanan data karyawan dari sebuah perusahaan, lengkap dengan data historis gaji, data historis tempat tinggal, dan data historis jabatan. Selanjutnya, implementasikan ERD tersebut pada basis data relasional (MySQL / PostgreSQL / SQL Server / dll) menggunakan perintah
- Jawab : 

||Karyawan|
|---|---|
|PK|ID|
||Nama|
||Usia|
||Jenis Kelamin|

||Histori Gaji|
|---|---|
|PK|Tanggal Mulai Gaji|
|PK|ID Karyawan|
||Gaji Bulanan|

||Histori Tempat Tinggal|
|---|---|
|PK|ID Karyawan|
||Nama Karyawan|
||Alamat|

||Histori Jabatan|
|---|---|
|PK|ID Karyawan|
||Tanggal Mulai Jabatan|
||Jabatan|
||Masa Jabatan|
