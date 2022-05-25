
# DDL
## Create Table
```sql
CREATE TABLE karyawan (
  	id_karyawan int DEFAULT 0 not null,
	nama_karyawan Varchar(255) Not null,
  	alamat_karyawan Varchar(255) not null,
  	no_hp Varchar(15),
  	PRIMARY KEY(no_reg)
);

CREATE TABLE registrasi_arsip (
  	no_reg int DEFAULT 0 not null,
	id_arsip int(10) Not null,
  	kode_rak Int(10) not null,
  	PRIMARY KEY(no_reg),
);

CREATE TABLE arsip (
	id_arsip int DEFAULT 0 not null,
  	judul_arsip varchar(255) not null,
  	tahun_arsip DATE not null,
  	tgl_pengadaan DATE not null,
  	jumlah_arsip Varchar(10) not null,
  	PRIMARY KEY (id_arsip)
);

CREATE TABLE rak (
	lokasi_arsip InT DEFAULT 0 not null,
  	kode_rak int(10) not null,
  	PRIMARY KEY (lokasi_arsip)
);

# DML
# DQL
