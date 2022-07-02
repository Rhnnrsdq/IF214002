# Ide Solusi : Sistem Penjualan Sepatu berMerk Original Trusted

## Deskripsi

Aplikasi ini berupaya untuk mempermudah dan terpercaya bagi orang yang ingin membeli sepatu bermerk namun original secara online. Aplikasi ini memiliki fitur utama seperti:
- Menampilkan sepatu bermerk dengan kualitas original bukan fake
- Mempermudah pembelian sepatu secara online dan realtime
- Menambah dan menghapus barang berdasarkan stok

## DDL
### Create Table
```sql
CREATE TABLE users (
  	id_user int DEFAULT 0 not null,
	nama Varchar(255) Not null,
  	email Varchar(255) not null,
  	pass Varchar(255) not null,
  	alamat Varchar(255) not null,
  	no_hp Varchar(15),
  	PRIMARY KEY(id_user)
);
```
```sql
CREATE TABLE barang (
  	id_barang int DEFAULT 0 not null,
	nama_barang Varchar(255) Not null,
  	harga int(11) not null,
  	stok int(11) not null,
  	keterangan Varchar(255) not null,
  	gambar text(11),
  	PRIMARY KEY(id_barang)
);
```
```sql
CREATE TABLE pesanan (
  	id_pesanan int DEFAULT 0 not null,
	id_user int(11) Not null,
  	tanggal_pesan date not null,
  	status_pesan varchar(255) not null,
  	kode_pembayaran int(11) not null,
  	jumlah_harga int(11),
  	PRIMARY KEY(id_pesanan)
);
```
```sql
CREATE TABLE pesanan_details (
  	id_pesanan_detail int DEFAULT 0 not null,
	id_barang int(11) Not null,
  	id_pesanan int(11) not null,
  	jumlah_beli int(11) not null,
  	jumlah_harga int(11),
  	PRIMARY KEY(id_pesanan)
);
```

## DML
```sql
insert into users (id_user, nama, email, pass, alamat, no_hp) values (1, 'Raihan Nur Sidiq', 'raihansidiq19@gmail.com', '123456', 'Komp. Abdi Negara II', '+82 123 456 781');
```
```sql
insert into barang (id_barang, nama_barang, harga, stok, keterangan, gambar) values (1, 'Nike Air Jordan 1 High Chameleon', '5000000', '12', 'Sepatu Original', '/Users/rans/Downloads/jordan.jpeg');
```
```sql
insert into pesanan (id_pesanan, id_user, tanggal_pesan, status_pesan, kode_pembayaran, jumlah_harga) values (1, '1', '2021-05-19', 'belum dibayar', '656', '5000002');
```
```sql
insert into pesanan_details (id_pesanan_detail, id_barang, id_pesanan, jumlah_beli, jumlah_harga) values (1, '1', '1', '1', '5000002');
```

## DQL
```sql
SELECT pesanan.`id_pesanan`,users.`id_user` AS nama_pembeli, barang.`harga`,pesanan_details.`jumlah_harga`
FROM pesanan,users,barang,pesanan_details
where users.`id_user` = pesanan.`id_user` && pesanan_details.`id_pesanan_detail` = pesanan.`id_pesanan`
```
