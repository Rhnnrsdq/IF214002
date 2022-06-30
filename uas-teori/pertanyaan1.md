# Entity Relationship Diagram: Sistem Pendataan Arsip Data Kantor
![Untitled Diagram drawio](https://user-images.githubusercontent.com/100889878/159740986-ef0e8844-0507-484a-8ddb-fb2d85b09741.png)
![pertemuan2 drawio](https://user-images.githubusercontent.com/100889878/158046828-5821344e-79f1-4533-87cc-4c9021dc5435.png)

## Deskripsi

Aplikasi ini berupaya untuk mempermudah pendataan atau pencarian arsip kantor pada gudang arsip. Aplikasi ini memiliki fitur utama seperti :
- Mempermudah pencarian data arsip berdasarkan rak
- Mempermudah pencarian data arsip berdasarkan lokasi arsip
- menambah dan menghapus arsip data berdasarkan status

## Entitas dan Atribut

### Karyawan
- *id_karyawan
- nama_karyawan
- alamat
- no_hp

### Registrasi Arsip
- no_reg
- *id_arsip
- kode_rak

### Arsip
- *id_arsip
- judul_arsip
- tahun_arsip
- tanggal_pengadaan
- jumlah_arsip

### Rak
- *kode_rak
- lokasi_arsip


# DDL
## Create Table
```sql
CREATE TABLE karyawan (
  	id_karyawan int DEFAULT 0 not null,
	nama_karyawan Varchar(255) Not null,
  	alamat_karyawan Varchar(255) not null,
  	no_hp Varchar(15),
  	PRIMARY KEY(id_karyawan)
);
```
```sql
CREATE TABLE registrasi_arsip (
  	no_reg int DEFAULT 0 not null,
	id_arsip int(10) Not null,
  	kode_rak Int(10) not null,
  	PRIMARY KEY(no_reg)
);
```
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
```sql
CREATE TABLE rak (
	lokasi_arsip InT DEFAULT 0 not null,
  	kode_rak int(10) not null,
  	PRIMARY KEY (lokasi_arsip)
);
```
### Alter Tabel
```sql
ALTER TABLE registrasi_arsip ADD FOREIGN KEY (id_arsip) REFERENCES arsip(id_arsip);
```
# DML
```sql
insert into karyawan (id_karyawan, nama_karyawan, alamat_karyawan, no_hp) values (1, 'Raihan Nur Sidiq', 'Komp.Abdi Negara II', '+82 123 456 7891');
insert into karyawan (id_karyawan, nama_karyawan, alamat_karyawan, no_hp) values (2, 'Jajang Maulana', 'Permata Biru', '+81 231 654 9876');
insert into karyawan (id_karyawan, nama_karyawan, alamat_karyawan, no_hp) values (3, 'Harris Repen', 'Ujung Berung', '+81 342 353 5342');
```
```sql
insert into registrasi_arsip (no_reg, id_arsip, kode_rak) values (1, '1', '1');
insert into registrasi_arsip (no_reg, id_arsip, kode_rak) values (2, '2', '2');
insert into registrasi_arsip (no_reg, id_arsip, kode_rak) values (3, '3', '3');
```
```sql
insert into arsip (id_arsip, judul_arsip, tahun_arsip, tgl_pengadaan, jumlah_arsip) values (1, 'Surat Keluar', '2016', '2015', '1');
insert into arsip (id_arsip, judul_arsip, tahun_arsip, tgl_pengadaan, jumlah_arsip) values (2, 'Buku Kendali', '2017', '2017', '1');
insert into arsip (id_arsip, judul_arsip, tahun_arsip, tgl_pengadaan, jumlah_arsip) values (3, 'SPK Kegiatan Penyelenggaraan Admin', '2019', '2018', '5');
```
```sql
insert into rak (lokasi_arsip, kode_rak) values (1, 'b3', '2');
insert into rak (lokasi_arsip, kode_rak) values (2, 'b1', '1');
insert into rak (lokasi_arsip, kode_rak) values (3, 'b1', '3');
```
# DQL
```sql
SELECT karyawan.'id_karyawan', arsip.'id_arsip'
FROM karyawan, arsip
WHERE karyawan.'id_karyawan'= arsip.'id_arsip'
```
