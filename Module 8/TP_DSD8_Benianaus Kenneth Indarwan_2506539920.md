---
title: Tugas Pendahuluan - Rangkaian Flip-Flop and Latch

---

# Tugas Pendahuluan - Modul 8 (Flip-Flop and Latch)

###### Pembuat Soal : KZ

```
Nama  : Benianaus Kenneth Indarwan
NPM   : 2506539920
```

---

## Teori (50 Poin)

### Pertanyaan 1 (5 Points)
**Jelaskan apa yang kalian pahami tentang modul-modul sebelumnya, menurut kalian rangkaian apa yang digunakan?**

<p style="color:#c62828; font-weight:700;">Soal ini tidak memerlukan referensi</p>

Rangkaian yang digunakan adalah rangkaian kombinasional. Rangkaian ini rangkaian yang menyambungkan input menggunakan logika kemudian hasilnya langsung masuk ke dalam output (bisa berupa Logic State atau LED ataupun output lainnya).

---

### Pertanyaan 2 (15 Points)
**Apa itu rangkaian sekuensial dan kombinasional, jelaskan perbedaannya?**

> *Jelaskan definisi dan kasus nyata penerapan rangkaian sekuensial dan kombinasional*

Rangkaian sekuensial adalah rangkaian yang menggunakan modul memory, sehingga mereka tidak memberikan output berdasarkan input saja, tetapi juga bisa berdasarkan memory sebelumnya. 

Rangkaian kombinasional adalah rangkaian sederhana yang mengambil input dan mengubahnya menjadi output menggunakan gerbang logika. Rangkaian kombinasional tidak memiliki modul memory sehingga output hanya akan dipengaruhi oleh input sekarang dan hasilnya tidak bisa disimpan.

Penerapan dari rangkaian sekuensial adalah pada counter, register, atau data storage. Counter membutuhkan data angka sebelumnya untuk menambahkan 1. Register adalah tempat penyimpanan data sehingga dibutuhkan rangkaian yang mampu menyimpan. Sedangkan rangkaian kombinasional akan ditemui di modul aritmatika, seperti kalkulator. Rangkaian ini akan menampilkan langsung output yang dihasilkan, sedangkan jika perlu menyimpannya akan digunakan rangkaian sekuensial.

#### Referensi
- [1]GeeksforGeeks, “Difference between Combinational and Sequential Circuit,” GeeksforGeeks, Jun. 12, 2018. https://www.geeksforgeeks.org/digital-logic/difference-between-combinational-and-sequential-circuit/ (accessed Nov. 09, 2025).
- [2]Electrical Technology, “Difference Between Combinational & Sequential Logic Circuits,” ELECTRICAL TECHNOLOGY, Jun. 06, 2024. https://www.electricaltechnology.org/2024/06/difference-between-combinational-and-sequential-logic-circuits.html (accessed Nov. 09, 2025).

---

### Pertanyaan 3 (20 Points)
**Apa itu `Latch` dan `Flip-flop`, jelaskan apa perbedaan di antara keduanya!**

> *Sebutkan jenis-jenis `Latch` dan `Flip-flop`, berikan truth table dan gambarkan rangkaiannya*

`LATCH` dan `FLIP-FLOP`, keduanya adalah rangkaian memori yang digunakan dalam rangkaian sekuensial. Masing-masing menyimpan 1 bit memori. Perbedaannya adalah dari bagaimana proses menyimpan datanya.

`LATCH` akan menyimpan data langsung berdasarkan inputnya. Ketika input diubah, maka isi dari `LATCH` juga akan langsung berubah. 
Sedangkan pada `FLIP-FLOP`, konsepnya sama yaitu data akan berubah berdasarkan input, tetapi di sini perubahan terjadi setiap clock (setiap kali ada perubahan clock dari `LOW` ke `HIGH`).

Jenis-jenis `LATCH`:
| Types | Truth Table | Rangkaian |
|:-----:| :---------: | :-------: |
|SR Latch         |![image](https://hackmd.io/_uploads/SkChzNRy-l.png)|![image](https://hackmd.io/_uploads/BJt6G4AJWl.png)|
|Gated SR Latch   |![image](https://hackmd.io/_uploads/B1wk7VAJbe.png)|![image](https://hackmd.io/_uploads/H1TGXV01Zx.png)|
|D Latch          |![image](https://hackmd.io/_uploads/Bkll7NAJWl.png)|![image](https://hackmd.io/_uploads/Bk4QQ4RkZg.png)|
|Gated D Latch    |![image](https://hackmd.io/_uploads/SkixmERJbg.png)|![image](https://hackmd.io/_uploads/B1cQ740J-x.png)|
|JK Latch         |![image](https://hackmd.io/_uploads/B1w-m4AkZl.png)|![image](https://hackmd.io/_uploads/ry7VQN0yZx.png)|
|T Latch          ||![image](https://hackmd.io/_uploads/SJo4XVR1Wx.png)|

Jenis-jenis `FLIP-FLOP`:
| Types | Truth Table | Rangkaian |
|:-----:| :---------: | :-------: |
|SR Flip-Flop  |![image](https://hackmd.io/_uploads/SyEjS4A1Wx.png)|![image](https://hackmd.io/_uploads/H1Mg840Jbe.png)|
|JK Flip-Flop  |![image](https://hackmd.io/_uploads/SkNhr40yZx.png)|![image](https://hackmd.io/_uploads/rJe5-U4RkWx.png)|
|D Flip-Flop   |![image](https://hackmd.io/_uploads/B1qRBNAk-l.png)|![image](https://hackmd.io/_uploads/rkHf8N0JZx.png)|
|T Flip-Flop   |![image](https://hackmd.io/_uploads/BkN1840k-l.png)|![image](https://hackmd.io/_uploads/SJYGU4Rkbx.png)|

#### Referensi
- [1]GeeksforGeeks, “Difference between Flipflop and Latch,” GeeksforGeeks, Mar. 31, 2020. https://www.geeksforgeeks.org/gate/difference-between-flip-flop-and-latch/ (accessed Nov. 09, 2025).
- [2]L. Team, “8 Types of Latches + Working Principle & Applications | Linksemicon,” linqchip, Nov. 19, 2024. https://www.linksemicon.com/blog/types-of-latches/ (accessed Nov. 09, 2025).
- [3]GeeksforGeeks, “FlipFlop types, their Conversion and Applications,” GeeksforGeeks, Jan. 19, 2017. https://www.geeksforgeeks.org/digital-logic/flip-flop-types-their-conversion-and-applications/ (accessed Nov. 09, 2025).
- [4]GeeksforGeeks, “Latches in Digital Logic,” GeeksforGeeks, Sep. 14, 2018. https://www.geeksforgeeks.org/digital-logic/latches-in-digital-logic/ (accessed Nov. 09, 2025).

---

### Pertanyaan 4 (10 Points)
**Apa fungsi Clock pada rangkaian sekuensial?**

Fungsi clock pada rangkaian sekuensial adalah untuk membuat perilaku rangkaian lebih "predictable" karena semuanya akan berjalan dalam waktu yang tetap. Juga untuk mencegah adanya ketidaksinkronan antara satu komponen dengan komponen yang lain agar tidak terjadi kesalahan pada outputnya.

#### Referensi
- [1]GeeksforGeeks, “Synchronous Sequential Circuits in Digital Logic,” GeeksforGeeks, Mar. 08, 2017. https://www.geeksforgeeks.org/digital-logic/synchronous-sequential-circuits-in-digital-logic/ (accessed Nov. 09, 2025).
- [2]eeeguide, “Synchronous Sequential Circuits | Moore Circuit | Mealy Circuit,” EEEGUIDE.COM, Dec. 07, 2021. https://www.eeeguide.com/synchronous-sequential-circuits/ (accessed Nov. 09, 2025).

---

## Pre-CS (50 Poin)

Tak terasa, akhir semester semakin dekat. Magus termenung, bagaimana cara menyimpan suatu kondisi didalam sebuah rangkaian magis, karena ia ingin membangun sebuah rangkaian yang bekerja dengan menggunakan sebuah kondisi tertentu. Anda menyarankan Magus untuk memakai sebuah Flip-flop, namun Magus tidak tahu apa itu Flip-flop, bantulah Magus dengan menjelaskan Flip-Flop, mulai dari penyusunnya yaitu Latch.

### 1. Buatlah SR Latch dan D Latch menggunakan Proteus, dibuat `menggunakan gerbang logika` saja (boleh gerbang kompleks atau sederhana). Kemudian buktikan bahwa Latch bisa `menyimpan nilai` dengan screenshot contoh output Anda beserta Analisisnya

#### A. D Latch
- **Set State**
![image](https://hackmd.io/_uploads/BkjzPSR1We.png)
![image](https://hackmd.io/_uploads/B1dQvr0JWg.png)
![image](https://hackmd.io/_uploads/BJvEwHRybx.png)
![image](https://hackmd.io/_uploads/HJQHPSAJbg.png)

- **Reset State**
![image](https://hackmd.io/_uploads/HkEYIr0JWl.png)
![image](https://hackmd.io/_uploads/S12ZDrCybe.png)

Pada D Latch, ketika Enable berada di posisi 0, maka rangkaian akan menyimpan posisi D sebelumnya. Walaupun D diubah, rangkaian tidak akan terupdate sampai E di posisi 1. 

#### B. SR Latch
- **Set State**
![image](https://hackmd.io/_uploads/HJe5GSS01Ze.png)

- **Reset State**
![image](https://hackmd.io/_uploads/BJ5prHAybg.png)

- **Undefined**
![image](https://hackmd.io/_uploads/SyO9rrCkWx.png)

Menggunakan SR Latch, kita bisa mengubah input S dari 0 ke 1 dan akan terupdate di output. Tetapi, ketika S diubah, output tidak akan terupdate. Output baru akan diupdate ketika rangkaian di-reset oleh Reset switch. 

---

### 2. Buatlah sebuah T Flip Flop dengan menggunakan IC Gerbang Logika juga dan buktikan bahwa rangkaian tersebut bisa `Men-Toggle Nilai`

> *Bebas ingin menggunakan rangkaian SR, JK, atau D Flip Flop untuk diubah menjadi T Flip Flop*
> **Note:** Clock bisa diambil dari components atau direpresentasikan sebuah tombol dengan menggunakan logic state

#### - Hold
![image](https://hackmd.io/_uploads/H1YzW8R1Ze.png)

#### - Toggle
![image](https://hackmd.io/_uploads/S1o7ZIC1Wg.png)

---

## PENTING

**Note:** Jika terdapat error seperti ini

![image](https://hackmd.io/_uploads/BJCmm5oW1g.png)

Tambahkan Switch dan pastikan dia open sebelum simulasi :

![image](https://hackmd.io/_uploads/Sybvm5obye.png)

---