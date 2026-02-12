---
title: Case Study - Rangkaian Aritmatika

---

# Case Study - Rangkaian Aritmatika
`Pembuat Soal : NA`
```
Nama  : Benianaus Kenneth Indarwan
NPM   : 2506539920
Rekan Kerja : Benedict Jaysen Riofo Panjaitan
```

## Rangkaian Fisik (50 poin)

Setelah selesai kelas, Magus diberikan tugas oleh Prof. Alden. Kali ini, dia ditantang untuk membuat 4-bit full adder yang ditampilkan menggunakan 5 LED. Magus diperbolehkan menggunakan IC 7483 (Full Adder 4bit) ataupun logic gates lainnya untuk membuat rangkaian ini.

> Opsi alternatif jika IC 7483 Habis : Membuat 2 bit subtractor menggunakan Logic Gates tanpa XOR dengan output ditampilkan menggunakan LED saja.

### Truth Table

#### Jika menggunakan IC 7483:
| A    | B    | C<sub>in</sub> | S (Biner) | C<sub>out</sub> | S (Desimal) |
| ---- | ---- | -------------- | --------- | --------------- | ----------- |
| 0000 | 0000 | 0              | 0000      | 0               | 0           |
| 0001 | 0010 | 0              | 0011      | 0               | 3           |
| 0010 | 0001 | 1              | 0100      | 0               | 4           |
| 0111 | 1000 | 0              | 1111      | 0               | 15          |
| 1000 | 1000 | 0              | 0000      | 1               | 0           |
| 1010 | 1001 | 1              | 0100      | 1               | 4           |
| 1111 | 0001 | 0              | 0000      | 1               | 0           |
| 1111 | 1111 | 0              | 1110      | 1               | 14          |
| 1111 | 1111 | 1              | 1111      | 1               | 15          |

<!-- 
#### Jika Alternatif :
| A   | B   | B<sub>in</sub> | D   | B<sub>out</sub> |
| --- | --- | -------------- | --- | --------------- |
| 0   | 0   | 0              | ?   | ?               |
| 0   | 0   | 1              | ?   | ?               |
| 0   | 1   | 0              | ?   | ?               |
| 0   | 1   | 1              | ?   | ?               |
| 1   | 0   | 0              | ?   | ?               |
| 1   | 0   | 1              | ?   | ?               |
| 1   | 1   | 0              | ?   | ?               |
| 1   | 1   | 1              | ?   | ?               |

#### KMAP untuk D:

![Masukkan screenshot KMAP](public_image_link)

D = ...

#### KMAP untuk B<sub>out</sub>:

![Masukkan screenshot KMAP](public_image_link)

B<sub>out</sub> = ...

Lalu, untuk membuat 2-bit full subtractor, Bagus perlu menghubungkan dua full subtractor 1-bit. Caranya adalah dengan menghubungkan B<sub>out</sub> dari full subtractor pertama ke B<sub>in</sub> dari full subtractor kedua. Bagus pun mulai merancang rangkaian tersebut.
-->

### Screenshot Rangkaian Fisik

| A    | B    | C<sub>in</sub> | Gambar Rangkaian |
| ---- | ---- | -------------- | ---------------- |
| 0000 | 0000 | 0              |![*comp-0](https://hackmd.io/_uploads/Skjj_ot1Wl.jpg)|
| 0001 | 0010 | 0              |![*comp-1](https://hackmd.io/_uploads/r10iOjt1-l.jpg)|
| 0010 | 0001 | 1              |![*comp-2](https://hackmd.io/_uploads/r19nusYJZe.jpg)|
| 1111 | 1111 | 1              |![*comp-3](https://hackmd.io/_uploads/B1Za_jtyWe.jpg)|
| 0111 | 1000 | 0              |![*comp-4](https://hackmd.io/_uploads/H1OTdsK1Wg.jpg) ![*comp-5](https://hackmd.io/_uploads/H1OTuitJZe.jpg)|
| 1000 | 1000 | 0              |![*comp-6](https://hackmd.io/_uploads/HyhT_iKyWl.jpg)|
| 1010 | 1001 | 1              |![*comp-7](https://hackmd.io/_uploads/S1g0OoKyWg.jpg)|
| 1111 | 0001 | 0              |![*comp-8](https://hackmd.io/_uploads/S1r0OiKkbe.jpg)|
| 1111 | 1111 | 0              |![*comp-9](https://hackmd.io/_uploads/Bk30dsFy-x.jpg)|

Urutan LED (dari kiri ke kanan)= C<sub>out</sub>, S4, S3, S2, S1

### Analisis Rangkaian 7483 (50 poin)

#### 1. Jelaskan apakah rangkaian dengan 7483 tersebut bekerja dengan input/output unsigned atau signed atau dua-duanya? Adakah kondisi tertentu yang mengakibatkan rangkaian jadi tidak bekerja? Lampirkan juga bukti screenshot dari rangkaian tersebut yang mendukung jawabanmu! (10 poin)

Rangkaian dengan IC 7483 bisa digunakan untuk input signed/unsigned dan output signed/unsigned. Untuk input signed, digunakan metode 2's complement untuk mengubah angka menjadi angka negatif. Keterbatasannya jika input 4 bit adalah angka negatif di atas angka 8, karena akan membutuhkan 5 bit untuk merepresentasikannya. Contohnya pada `15 + (-15)`, tidak bisa menggunakan IC 7483 karena ia 5 bit. Hasil dari `C-OUT` dapat digunakan sebagai bit ke 5 pada hasil jika inputnya keduanya unsigned. Apabila salah satu input signed, maka hasilnya juga akan signed, maka harus diperhatikan untuk dikonversi. Jika ada yang unsigned, maka hasil `C-OUT` tidak perlu diperhatikan. 

*Jika hasil outputnya adalah hasil Input_1 + Input_2, maka lampirkan screenshotnya. Jika tidak, tuliskan `-`.

| Input_1 | Input_2 | Output | Screenshot |
| ------- | ------- | ------ | :--------: |
| 15      | 15      | 30     |![image](https://hackmd.io/_uploads/r1cRrV5kbe.png)|
| 15      | -15     | 0      | -          |
| 7       | 16      | 23     |![image](https://hackmd.io/_uploads/Hy91iNcJbe.png)|
| 0       | -1      | -1     | ![image](https://hackmd.io/_uploads/rkXwwNq1Wx.png) dengan angka negatif termasuk hasil dalam 2's complement|
| -7      | 5       | -2     | ![image](https://hackmd.io/_uploads/SJ53vV5kWx.png) dengan angka negatif termasuk hasil dalam 2's complement|
| -1      | 1       | 0      | ![image](https://hackmd.io/_uploads/ByVNvN91Zx.png) dengan angka negatif dalam 2's complement|

#### 2. Apakah pin C<sub>out</sub> penting dalam menentukan hasil pertambahan dari dua bilangan biner dalam rangkaian yang telah dibuat? Jelaskan alasanmu! (10 poin)

`C-OUT` penting dalam menentukan hasil penjumlahan, terutama pada bilangan unsigned, karena ia juga dapat berperan sebagai bit ke-5 dari output. Misalkan jika hasilnya adalah 23 (10111), maka S akan menghasilkan `0111` dan Carry akan menghasilkan `1`. Jika kita menaruh hasil carry di depan S, maka akan didapatkan `10111`, dimana itu adalah BIN dari 23.

#### 3. Berapa angka positif tertinggi dan angka negatif terendah yang bisa dihasilkan dari 4-bit full adder yang dibuat? (10 poin)

Menggunakan 4-bit full adder, angka positif tertinggi yang bisa dihasilkan adalah jika semua output dan carry bernilai 1, yaitu `11111`, atau 31 dalam DEC. Sedangkan, angka negatif tertinggi yang dapat dihasilkan adalah signed 2's complement `1000` atau 8 dalam DEC.

## Analisis & Kesimpulan (20 poin)

**Analisis Keseluruhan:**  

Rangkaian yang dibuat adalah rangkaian 4-bit full adder yang dibuat dengan menggunakan IC 7483. IC ini bisa digunakan untuk unsigned number dan juga signed number menggunakan format 2's complement. Hasil output dari IC ini adalah 4 bit Sum + 1 bit Carry yang dimana dapat digunakan di awal sebagai bit ke-5 (apabila unsigned). Signed number yang dimasukkan ke IC akan menghasilkan signed number juga di outputnya.

**Kesimpulan: (minimal 3)**

- Signed number dan Unsigned number dapat digunakan pada IC ini untuk dioperasikan.
- Apabila menggunakan salah satu angka Signed number, maka hasilnya akan Signed juga.
- Carry-OUT dapat digunakan sebagai bit ke-5 di depan SUM (MSB) jika Unsigned. Apabila Signed, Carry-OUT tidak dipedulikan, hanya melihat SUM saja.
- IC ini memiliki limit apabila terdapat 2 angka di atas 4 bit (Carry-IN hanya ada 1), apabila menggunakan angka Signed di atas 1000 (8); kondisi ini tidak bisa digunakan karena tidak bisa diinput ke dalam IC.