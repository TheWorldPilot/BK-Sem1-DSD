---
title: Tugas Pendahuluan - Modul 9 (Register & Counter)

---

---
title: Tugas Pendahuluan - Modul 9 (Register & Counter)

---

# Tugas Pendahuluan - Modul 9 (Register & Counter)
Pembuat Soal: DY
```
Nama  : Benianaus Kenneth Indarwan
NPM   : 2506539920
```
## Teori (40 Poin)

### 1. Kedua konsep modul ini (register dan counter) relatif mirip dengan flip-flop dan latch. Jika ditinjau dari cara kerja mereka, mengapakah demikian? (10 poin)

Register dan counter mirip dengan konsep flip-flop dan latch karena register dan counter merupakan gabungan dari beberapa flip-flop yang bekerja bersamaan untuk membentuk register atau counter. Register menyimpan beberapa bit data dengan bantuan flip-flop, dan counter menggunakan logika flip-flop untuk mengubah data setiap clocknya.

### Referensi:
- [1]Anonymous, “Flip-Flops and Registers: Everything You Need to Know When Assessing Flip-Flops and Registers Skills,” Alooba.com, 2024. https://www.alooba.com/skills/concepts/electronics-253/flip-flops-and-registers/ (accessed Nov. 16, 2025).
- [2]Asmamushtaq, “What are the Flip-Flops and Registers in Digital Circuits?,” Medium, Feb. 22, 2024. https://medium.com/@asmamushtaq_45022/what-are-the-flip-flops-and-registers-in-digital-circuits-90612ec23a37 (accessed Nov. 16, 2025).

---
### 2. Apa saja perbedaan antara counter synchronous dan asynchronous? Jabarkan perbedaan keduanya dari segi alur, kelebihan/kelemahan, dan aplikasi. (15 poin)

Perbedaan antara synchronous dan asynchronous counter adalah pada synchronous counter, clock yang dipakai di setiap flip-flop asalnya dari satu clock yang sama; sedangkan pada asynchronous counter, clock di flip-flop akan dipengaruhi oleh output Q dari flip-flop sebelumnya.

|Counter type|Synchronous|Asynchronous|
|:----------:|:---------:|:----------:|
|Input Clock |Satu clock untuk semua flip-flop|Clock setiap flip-flop diambil dari output flip-flop sebelumnya|
|Timing|Tidak ada delay dalam perubahan bit|Ada delay yang muncul|
|Kelebihan| Timing yang predictable, input/control clock yang sederhana, tingkat reliabilitas yang tinggi|Desain yang lebih sederhana, lebih fleksibel, lebih murah| 
|Kekurangan|Desain yang lebih kompleks, lebih mahal|Akurasinya kurang, terdapat delay, operasi lebih lambat.
|Aplikasi|Ring Counter dan Johnson Counter|Ripple Up Counter dan Ripple Down Counter|

### Referensi:
- [1]GeeksforGeeks, “Differences between Synchronous and Asynchronous Counter,” GeeksforGeeks, May 13, 2019. https://www.geeksforgeeks.org/digital-logic/differences-between-synchronous-and-asynchronous-counter/ (accessed Nov. 16, 2025).
- [2]GeeksforGeeks, “Counters in Digital Logic,” GeeksforGeeks, Nov. 02, 2015. https://www.geeksforgeeks.org/digital-logic/counters-in-digital-logic/ (accessed Nov. 16, 2025).

---
### 3. PIPO, SISO, PISO, SIPO. Apa yang membedakan jenis-jenis register tersebut, dan bagaimana cara mereka menyimpan/mengeluarkan data? (15 poin)

Perbedaan jenis-jenis register tersebut adalah dalam cara mereka menginput dan mengoutput data.

- **PIPO (Parallel In, Parallel Out)** mengambil n bit data dan mengoutput n bit data sekaligus. Setiap bit data memiliki flip-flopnya masing-masing sehingga tidak menunggu data diproses lewat flip-flop lain. Membutuhkan 1 clock cycle.
-  **SISO (Serial In, Serial Out)** mengambil 1 bit data dan mengoutput 1 bit data setiap clock. Untuk tipe register ini, hanya ada 1 bit input dan output, sehingga data harus diubah untuk setiap bit input, dan output juga harus dicatat di tempat lain, karena outputnya hanya dalam 1 bit. Membutuhkan 2*n (n=bit input) clock cycle.
-  **PISO (Parallel In, Serial Out)** mengambil n bit data sekaligus, tetapi dioutput dalam 1 bit, sehingga perlu dicatat bit yang keluar secara berurutan. Membutuhkan n clock cycle.
-  **SIPO (Serial In, Parallel Out)** mengambil 1 bit input data, tetapi akan menghasilkan output n bit secara bersamaan. Membutuhkan n clock cycle.

```
Serial = satu-satu secara berurutan
Parallel = bersamaan sekaligus
```

### Referensi:
- [1]GeeksforGeeks, “Shift Registers in Digital Logic,” GeeksforGeeks, Dec. 20, 2017. https://www.geeksforgeeks.org/digital-logic/shift-registers-in-digital-logic/ (accessed Nov. 16, 2025).
- [2]Electronics Tutorials, “Shift Register - Parallel and Serial Shift Register,” Basic Electronics Tutorials, Aug. 30, 2013. https://www.electronics-tutorials.ws/sequential/seq_5.html (accessed Nov. 16, 2025).

---

## Pre-CS (60 Poin)
~~Sangat berasa~~ Tak terasa waktu untuk berkuliah untuk satu semester hampir habis, Anda dan Magus sudah melalui banyak sekali rintangan dan ujian baik yang normal ataupun alomani. Sebagai persiapan untuk akhir yang menyenangkan (LIBUR), Magus ingin membuat sebuah alat yang bisa menyimpan kenangan dan peristiwa selama ini dan peristiwanya memiliki kode untuk nanti ditampilkan secara berulang yaitu 
`9 -> 6 -> 3 -> 1 -> 0 -> 9 -> 6 -> 3 -> .....`
Namun ia kesulitan untuk membuatnya, Anda yang tahu hal ini (Tahu lah ya kan Anda Omniscent) berinisiatif untuk membantunya (Teknik SOLID). Seperti yang Anda ketahui, untuk menyimpan sesuatu data/memori pada sebuah alat dibutuhkan sebuah `Register` dan sebuah `Counter` untuk menunjukkan sebuah angka yang bergilir. Bantulah Magus merancang ini di sebuah rancangan menggunakan alat MAGIS yang bernama Proteus.

### 4. Dalam Proteus 8, buat sebuah 4-bit Register (jenis SIPO) menggunakan D Flip-Flop. Lalu, `screenshot` fungsionalitas "menyimpan data" dan "mereset data" dari register tersebut! (25 poin)
`Note : Mereset artinya membuat outputnya kembali ke 0 (0000)`
`Note 2 : Untuk nomor ini dan selanjutnya, gunakan 7-Segment untuk menampilkan output`

Menyimpan Data:
![image](https://hackmd.io/_uploads/HkIY9PweZx.png)

Mereset Data:
![image](https://hackmd.io/_uploads/HJNqcDvgWe.png)


### 5. Buat sebuah 4-bit Synchronous Down Counter menggunakan JK flip-flop. Akan tetapi, outputnya akan mengikuti siklus seperti berikut:
`Siklus (desimal) : 9 -> 6 -> 3 -> 1 -> 0 -> 9 -> ... (ulang)`
### Setelah itu, screenshot tiap output! (35 poin)
`Hint: Coba manfaatkan K-Map dan tabel transisi untuk memodifikasi Synchronous Down Counter standar`

|Output DEC | Output BIN | Screenshot |
|:---------:|:----------:|:----------:|
|9|1 0 0 1|![image](https://hackmd.io/_uploads/HkDJZuDgWg.png)|
|6|0 1 1 0|![image](https://hackmd.io/_uploads/Bkkl-_vg-x.png)|
|3|0 0 1 1|![image](https://hackmd.io/_uploads/S1wgW_wlWg.png)|
|1|0 0 0 1|![image](https://hackmd.io/_uploads/rkpgZuwx-x.png)|
|0|0 0 0 0|![image](https://hackmd.io/_uploads/BJIZZOvg-e.png)|

![Sneak Peak Finpro DSD, Tapi gak meledak hanya panas wkwkw](https://hackmd.io/_uploads/ByReVPrx-e.gif)