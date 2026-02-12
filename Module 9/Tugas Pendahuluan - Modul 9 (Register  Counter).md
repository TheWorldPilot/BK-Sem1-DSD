---
title: Tugas Pendahuluan - Modul 9 (Register & Counter)

---

# Tugas Pendahuluan - Modul 9 (Register & Counter)
Pembuat Soal: DY
```
Nama  : IsThisRealChat?
NPM   : 250xxxxxxx
```
## Teori (40 Poin)

### 1. Kedua konsep modul ini (register dan counter) relatif mirip dengan flip-flop dan latch. Jika ditinjau dari cara kerja mereka, mengapakah demikian? (10 poin)

[your answer here]

### Referensi:


---
### 2. Apa saja perbedaan antara counter synchronous dan asynchronous? Jabarkan perbedaan keduanya dari segi alur, kelebihan/kelemahan, dan aplikasi. (15 poin)

[your answer here]

### Referensi:


---
### 3. PIPO, SISO, PISO, SIPO. Apa yang membedakan jenis-jenis register tersebut, dan bagaimana cara mereka menyimpan/mengeluarkan data? (15 poin)

[your answer here]

### Referensi:


---

## Pre-CS (60 Poin)
~~Sangat berasa~~ Tak terasa waktu untuk berkuliah untuk satu semester hampir habis, Anda dan Magus sudah melalui banyak sekali rintangan dan ujian baik yang normal ataupun alomani. Sebagai persiapan untuk akhir yang menyenangkan (LIBUR), Magus ingin membuat sebuah alat yang bisa menyimpan kenangan dan peristiwa selama ini dan peristiwanya memiliki kode untuk nanti ditampilkan secara berulang yaitu 
`9 -> 6 -> 3 -> 1 -> 0 -> 9 -> 6 -> 3 -> .....`
Namun ia kesulitan untuk membuatnya, Anda yang tahu hal ini (Tahu lah ya kan Anda Omniscent) berinisiatif untuk membantunya (Teknik SOLID). Seperti yang Anda ketahui, untuk menyimpan sesuatu data/memori pada sebuah alat dibutuhkan sebuah `Register` dan sebuah `Counter` untuk menunjukkan sebuah angka yang bergilir. Bantulah Magus merancang ini di sebuah rancangan menggunakan alat MAGIS yang bernama Proteus.

### 4. Dalam Proteus 8, buat sebuah 4-bit Register (jenis SIPO) menggunakan D Flip-Flop. Lalu, `screenshot` fungsionalitas "menyimpan data" dan "mereset data" dari register tersebut! (25 poin)
`Note : Mereset artinya membuat outputnya kembali ke 0 (0000)`
`Note 2 : Untuk nomor ini dan selanjutnya, gunakan 7-Segment untuk menampilkan output`

Menyimpan Data:
![Alamak](https://hackmd.io/_uploads/SJ1RXvSxbe.gif)

Mereset Data:
![meninBLACK-Forgor Tools](https://hackmd.io/_uploads/BkMRXPSxbg.gif)


### 5. Buat sebuah 4-bit Synchronous Down Counter menggunakan JK flip-flop. Akan tetapi, outputnya akan mengikuti siklus seperti berikut:
`Siklus (desimal) : 9 -> 6 -> 3 -> 1 -> 0 -> 9 -> ... (ulang)`
### Setelah itu, screenshot tiap output! (35 poin)
`Hint: Coba manfaatkan K-Map dan tabel transisi untuk memodifikasi Synchronous Down Counter standar`

|Output |Screenshot|
|-------|----------|
|       |          |
|       |          |
|...    |...       |

![Sneak Peak Finpro DSD, Tapi gak meledak hanya panas wkwkw](https://hackmd.io/_uploads/ByReVPrx-e.gif)