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

```sql
CREATE TABLE karyawan (
	id int DEFAULT 0 NOT null,
	nama_karyawan Varchar(255) not null,
	usia Varchar(100) not null,
	jenis_kelamin ENUM("L","P"),
	PRIMARY KEY(id)
);

CREATE TABLE histori_gaji (
  	id_karyawan int DEFAULT 0 not null,
	tanggal_mulai_gaji DATe not null,
  	gaji_bulanan Int(10) not null,
  	PRIMARY KEY(id_karyawan, tanggal_mulai_gaji)
);

CREATE TABLE histori_tempat_tinggal (
	id_karyawan int DEFAULT 0 not null,
  	nama_karyawan varchar(255) not null,
  	alamat varchar(255),
  	PRIMARY KEY (id_karyawan)
);

CREATE TABLE jabatan (
	id_karyawan InT DEFAULT 0 not null,
  	nama_karyawan varchar(255) not null,
  	tanggal_mulai_jabatan Date,
  	jabatan Varchar(100) not null,
  	masa_jabatan int(10)
  	PRIMARY Key(id_karyawan)
);
```
