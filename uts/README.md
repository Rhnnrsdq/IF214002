# UTS
1. Basis data relasional dapat langsung dibangun menggunakan perintah SQL di sistem basis data seperti MySQL, dsb tanpa ada perancangan terlebih dahulu. 
Jelaskan apa keuntungan melakukan perancangan basis data terlebih dahulu (menggunakan ERD ataupun Class Diagram) !
- Jawab : 
Keuntungan dari melakukan perancangan basis data terlebih dahulu adalah agar bisa mengelompokkan data dan informasi sehingga lebih mudah dimengerti. Mencegah terjadinya duplikat data maupun inkonsistensi data. Mempermudah proses penyimpanan, akses, pembaharuan, dan menghapus data. Menjaga kualitas data dan informasi yang diakses sesuai dengan yang diinput.

2. Jelaskan bagaimana cara mentransformasikan proses bisnis sebuah organisasi menjadi struktur data di basis data !
- Jawab : - Menentukan tujuan dari pembuatan database
Menentukan tabel yang akan diperlukan
- Menentukan isi atau field dari masing-masing tabel yang diperlukan
- Menentukan tabel yang akan digunakan secara bersamaan
- Identifikasi field yang akan menjadi primary key atau kunci utama
- Cek kembali database yang sudah dibuat
- Memasukan data statis ke dalam database yang sudah dibuat tadi

3. Rancang solusi digital dari satu permasalahan yang ada di sekitar Anda. 
A. Deskripsikan solusi digital tersebut dalam satu paragraf
B. Buat list fitur-fitur yang ada pada solusi digital tersebut
C. Buat ERD notasi Chen dari struktur data yang mewakili fitur2 di solusi digital tersebut
D. Buat ERD notasi Crow Foot dari struktur data logical yang mewakili fitur2 di solusi digital tersebut, lengkap dengan keys, tipe data, dan normalisasi hingga bentuk ke 3
- Jawab :
# Sistem Pendataan Arsip Data Kantor

## Deskripsi

Aplikasi ini berupaya untuk mempermudah pendataan atau pencarian arsip kantor pada gudang arsip. 

## Fitur - Fitur 
Aplikasi ini memiliki fitur utama seperti :
- Mempermudah pencarian data arsip berdasarkan rak
- Mempermudah pencarian data arsip berdasarkan lokasi arsip
- menambah dan menghapus arsip data berdasarkan status

## ERD Chen
![pertemuan2 drawio](https://user-images.githubusercontent.com/100889878/158046828-5821344e-79f1-4533-87cc-4c9021dc5435.png)

## ERD Notasi Crow Foot
![Untitled Diagram drawio](https://user-images.githubusercontent.com/100889878/159740986-ef0e8844-0507-484a-8ddb-fb2d85b09741.png)

## Tabel Database
### Karyawan
|🔑id_karyawan| nama_karyawan | alamat | no_hp |
|---|---|---|---|
| 1 | Raihan | Komp. Abdi Negara II Blok B1 No. 3 | 085157597971 |
| 2 | Rahmat | Komp. Abdi Negara II Blok B1 No. 4 | 085157969690 |

### Arsip
|🔑id_arsip| judul_arsip | tahun_arsip | tgl_pengadaan | jumlah_arsip |
|---|---|---|---|---|
| 1 | Surat Keluar | 2017 | 2016 | 1 | 
| 2 | SPK Kegiatan Penyelenggaran Perkantoran | 2018 | 2018 | 5 | 

### Registrasi Arsip
|🔑no_reg| id_arsip | kode_rak |
|---|---|---|
| 1 | 1 | 10 |
| 2 | 2 | 15 |

### Rak
|🔑lokasi_arsip| kode_rak |
|---|---|
| 1 | 1 |
| 2 | 2 |
