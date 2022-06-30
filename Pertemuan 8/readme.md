# Ide Solusi : Sistem Penjualan Sepatu berMerk Original

![DIAGRAM-LASHOPED](https://user-images.githubusercontent.com/100889878/176704382-b0bb2dbb-249d-4322-8118-d8cf80bc4661.png)

## Entity Relationship Diagram: Sistem Sepatu berMerk Original
![ERD-LASHOPED](https://user-images.githubusercontent.com/100889878/176704190-c6178c31-3fd8-44dd-a546-0d82681e9393.png)

## Deskripsi

Aplikasi ini berupaya untuk mempermudah dan terpercaya bagi orang yang ingin membeli sepatu bermerk namun original secara online. Aplikasi ini memiliki fitur utama seperti:
- Menampilkan sepatu bermerk dengan kualitas original bukan fake
- Mempermudah pembelian sepatu secara online dan realtime
- Menambah dan menghapus barang berdasarkan stok

## Entitas dan Atribut

### User
- *id_user
- nama
- email
- pass
- alamat
- nohp

### Pesanan
- *id_pesanan
- id_user
- tanggal_pesan
- status_pesan
- kode_pembayaran
- jumlah_harga

### Pesanan Detail
- *id_pesanan_detail
- id_barang
- id_pesanan
- jumlah_beli
- jumlah_harga

### Barang
- *id_barang
- nama_barang
- harga
- stok
- keterangan
- gambar
