# Entity Relationship Diagram: Sistem Pendataan Arsip Data Kantor
![Untitled Diagram drawio](https://user-images.githubusercontent.com/100889878/159740986-ef0e8844-0507-484a-8ddb-fb2d85b09741.png)

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
