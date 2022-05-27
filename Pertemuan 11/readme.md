
# DDL
## Create Table
### Karyawan
```sql
CREATE TABLE karyawan (
  	id_karyawan int DEFAULT 0 not null,
	nama_karyawan Varchar(255) Not null,
  	alamat_karyawan Varchar(255) not null,
  	no_hp Varchar(15),
  	PRIMARY KEY(id_karyawan)
);
```
### registrasi_arsip
```sql
CREATE TABLE registrasi_arsip (
  	no_reg int DEFAULT 0 not null,
	id_arsip int(10) Not null,
  	kode_rak Int(10) not null,
  	PRIMARY KEY(no_reg),
);
```
### arsip
```sql
CREATE TABLE arsip (
	id_arsip int DEFAULT 0 not null,
  	judul_arsip varchar(255) not null,
  	tahun_arsip DATE not null,
  	tgl_pengadaan DATE not null,
  	jumlah_arsip Varchar(10) not null,
  	PRIMARY KEY (id_arsip)
);
```
### rak
```sql
CREATE TABLE rak (
	lokasi_arsip InT DEFAULT 0 not null,
  	kode_rak int(10) not null,
  	PRIMARY KEY (lokasi_arsip)
);
```
```sql
ALTER TABLE registrasi_arsip ADD FOREIGN KEY (id_arsip) REFERENCES arsip(id_arsip);
```
# DML
### karyawan
```sql
insert into karyawan (id_karyawan, nama_karyawan, alamat_karyawan, no_hp) values (1, 'Raihan Nur Sidiq', 'Komp.Abdi Negara II', '+82 123 456 7891');
insert into karyawan (id_karyawan, nama_karyawan, alamat_karyawan, no_hp) values (2, 'Jajang Maulana', 'Permata Biru', '+81 231 654 9876');
insert into karyawan (id_karyawan, nama_karyawan, alamat_karyawan, no_hp) values (3, 'Harris Repen', 'Ujung Berung', '+81 342 353 5342');
```
### registrasi_arsip
```sql
insert into registrasi_arsip (no_reg, id_arsip, kode_rak) values (1, '1', '1');
insert into registrasi_arsip (no_reg, id_arsip, kode_rak) values (2, '2', '2');
insert into registrasi_arsip (no_reg, id_arsip, kode_rak) values (3, '3', '3');
```
### arsip
```sql
insert into arsip (id_arsip, judul_arsip, tahun_arsip, tgl_pengadaan, jumlah_arsip) values (1, 'Surat Keluar', '2016', '2015', '1');
insert into arsip (id_arsip, judul_arsip, tahun_arsip, tgl_pengadaan, jumlah_arsip) values (2, 'Buku Kendali', '2017', '2017', '1');
insert into arsip (id_arsip, judul_arsip, tahun_arsip, tgl_pengadaan, jumlah_arsip) values (3, 'SPK Kegiatan Penyelenggaraan Admin', '2019', '2018', '5');
```
### rak
```sql
insert into rak (lokasi_arsip, kode_rak) values (1, 'b3', '2');
insert into rak (lokasi_arsip, kode_rak) values (2, 'b1', '1');
insert into rak (lokasi_arsip, kode_rak) values (3, 'b1', '3');
```
# DQL
