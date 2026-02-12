---
title: Tugas Pendahuluan - Rangkaian Aritmatika

---

# Tugas Pendahuluan - Rangkaian Aritmatika
`Pembuat Soal : NA`
```
Nama  : Benianaus Kenneth Indarwan
NPM   : 2506539920
```

## Teori (40 poin)

### 1. Jelaskan apa itu half adder, half subtractor, full adder, dan full subtractor! Sertakan truth table dan gambar rangkaian masing-masing. (10 poin)

---

#### Half Adder
Half Adder adalah rangkaian logika yang mengambil 2 bit input dan menambahkannya dengan hasil `SUM` dan `CARRY`.

Truth table dari Half Adder adalah:
| A | B |Carry|Sum|
| - | - |:---:|:-:|
| 0 | 0 | 0 | 0 |
| 0 | 1 | 0 | 1 |
| 1 | 0 | 0 | 1 |
| 1 | 1 | 1 | 0 |

Gambar rangkaian:
![image](https://hackmd.io/_uploads/r1kOjHU1Zl.png)


#### Half Subtractor

Half Subtractor adalah rangkaian logika yang mengambil 2 bit input dan mengurangi bit pertama dengan bit kedua dengan output `DIFFERENCE` dan `BORROW`. `DIFFERENCE` adalah selisih dari kedua angka, dan `BORROW` menunjukan apakah perlu ada peminjaman untuk menyelesaikan pengurangan tersebut.

Truth table dari Half Adder adalah:
| A | B |Difference|Borrow|
| - | - |:--------:|:----:|
| 0 | 0 | 0 | 0 |
| 0 | 1 | 1 | 1 |
| 1 | 0 | 1 | 0 |
| 1 | 1 | 0 | 0 |

Gambar rangkaian:
![image](https://hackmd.io/_uploads/H1gKiS81Zl.png)


#### Full Adder

Full Adder adalah rangkaian yang mengambil 2 bit input dan 1 bit `CARRY-IN` yang ditambahkan dengan hasil `SUM` dan `CARRY-OUT`. `CARRY-IN` adalah carry dari hasil penjumlahan di bit sebelumnya.

Truth table dari Half Adder adalah:
| A   | B   | CARRY-IN | SUM | CARRY-OUT |
| --- | --- |:--------:|:---:|:---------:|
| 0   | 0   |    0     |  0  |     0     |
| 0   | 0   |    1     |  0  |     0     |
| 0   | 1   |    0     |  0  |     0     |
| 0   | 1   |    1     |  0  |     0     |
| 1   | 0   |    0     |  0  |     0     |
| 1   | 0   |    1     |  0  |     0     |
| 1   | 1   |    0     |  0  |     0     |
| 1   | 1   |    1     |  0  |     0     |

Gambar rangkaian:
![image](https://hackmd.io/_uploads/rJhqjrLkbg.png)


#### Full Subtractor

Half Subtractor adalah rangkaian logika yang mengambil 2 bit input dan 1 bit `BORROW-IN`. Cara kerjanya dengan mengurangi bit pertama dengan bit kedua dengan output `DIFFERENCE` dan `BORROW-OUT`. Hal ini karena apabila terjadi borrow pada bit LSB, maka akan mempengaruhi bit di depannya, sehingga dengan tambahan `BORROW-IN` tidak terjadi kesalahan.

Truth table dari Half Adder adalah:
| A   | B   | BORROW-IN | DIFFERENCE | BORROW-OUT |
| --- | --- |:---------:|:----------:|:----------:|
| 0   | 0   |    0     |  0  |     0     |
| 0   | 0   |    1     |  1  |     1     |
| 0   | 1   |    0     |  1  |     1     |
| 0   | 1   |    1     |  0  |     1     |
| 1   | 0   |    0     |  1  |     0     |
| 1   | 0   |    1     |  0  |     0     |
| 1   | 1   |    0     |  0  |     0     |
| 1   | 1   |    1     |  1  |     1     |

Gambar rangkaian:
![image](https://hackmd.io/_uploads/rkvsorI1Ze.png)

### Referensi:

- [1]GeeksforGeeks, “Half Adder in Digital Logic,” GeeksforGeeks, Aug. 03, 2015. https://www.geeksforgeeks.org/digital-logic/half-adder-in-digital-logic/ (accessed Nov. 02, 2025).
- [2]GeeksforGeeks, “Half Subtractor in Digital Logic,” GeeksforGeeks, Aug. 05, 2015. https://www.geeksforgeeks.org/digital-logic/half-subtractor-in-digital-logic/ (accessed Nov. 02, 2025).
- [3]GeeksforGeeks, “Full Adder in Digital Logic,” GeeksforGeeks, Mar. 21, 2017. https://www.geeksforgeeks.org/digital-logic/full-adder-in-digital-logic/ (accessed Nov. 02, 2025).
- [4]GeeksforGeeks, “Full Subtractor in Digital Logic,” GeeksforGeeks, Oct. 10, 2017. https://www.geeksforgeeks.org/digital-logic/full-subtractor-in-digital-logic/ (accessed Nov. 02, 2025).

---

### 2. Jelaskan perbedaan antara half adder dan full adder! (10 poin)

Half Adder memiliki 2 bit input, sedangkan Full Adder memiliki 3 bit input. Hal ini karena Full Adder mempertimbangkan `CARRY` dari rangkaian sebelumnya, dimana `CARRY-OUT` dari bit sebelumnya akan ditambahkan ke bit berikutnya sebagai `CARRY-IN`.

### Referensi:

- [1]GeeksforGeeks, “Difference between Half Adder and Full Adder,” GeeksforGeeks, Oct. 09, 2020. https://www.geeksforgeeks.org/gate/difference-between-half-adder-and-full-adder/ (accessed Nov. 02, 2025).
- [2]V. Kohli, “Half Adder And Full Adder Truth Table, Circuit, Working, and K-Map,” Electronics For You, Nov. 17, 2022. https://www.electronicsforu.com/technology-trends/learn-electronics/half-adder-full-adder-truth-table-circuit-working-kmap (accessed Nov. 04, 2025).

---

### 3. Jelaskan perbedaan antara half subtractor dan full subtractor! (10 poin)

Half Subtractor memiliki 2 bit input, sedangkan Full Subtractor memiliki 3 bit input. Tambahan input ini dikarenakan karena Full Subtractor mempertimbangkan jika ada `BORROW` pada bit terakhir (Least Significant Bit), sehingga akan mempengaruhi bit berikutnya yang akan dioperasikan.

### Referensi:

- [1]V. Kohli, “Half Subtractor and Full Subtractor Truth Table, Equation, and Circuit Design,” Electronics For You, Nov. 17, 2022. https://www.electronicsforu.com/technology-trends/learn-electronics/half-subtractor-full-subtractor-truth-table-circuit-design (accessed Nov. 04, 2025).
- [2]Anonymous, “Implementation of a Full Subtractor,” Tutorialspoint.com, 2021. https://www.tutorialspoint.com/digital-electronics/implementation-of-a-full-subtractor-using-two-half-subtractors.htm (accessed Nov. 04, 2025).

### 4. Jelaskan perbedaan antara signed magnitude dan 2’s complement! (10 poin)

Signed Magnitude dan 2's Complement merupakan cara untuk merepresentasikan bilangan positif atau negatif pada sebuah angka binary. Caranya dengan menambah bit di depan angka. Pada Signed Magnitude, bit `1` melambangkan bilangan positif dan bit `0` melambangkan bilangan negatif. Menggunakan sistem 2's Complement, bit `1` melambangkan bilangan negatif dan bit `0` melambangkan bilangan negatif.

### Referensi:

- [9]GeeksforGeeks, “Difference between Signed magnitude and 2’s complement,” GeeksforGeeks, May 11, 2020. https://www.geeksforgeeks.org/computer-organization-architecture/difference-between-signed-magnitude-and-2s-complement/ (accessed Nov. 02, 2025).
- [10]Anonymous, “Signed Binary Numbers and Two’s Complement used in Binary,” Basic Electronics Tutorials, Aug. 20, 2018. https://www.electronics-tutorials.ws/binary/signed-binary-numbers.html (accessed Nov. 04, 2025).

---

## Pre-CS (60 poin)

**Persyaratan:**

1. Gunakan Proteus
2. Untuk **SETIAP** rangkaian, masukkan `NamaKamu_NPM` dalam file Proteus
3. Seluruh rangkaian harus berada dalam **SATU** file Proteus
4. Gunakan Logic State dan Logic Probe untuk input dan output
5. Kirimkan file `.zip` yang berisi file `.md` dan file `.pdsprj`

---

Hari terus berlanjut, keseharian Magus pun berlalu. Hari ini Magus menghadiri kelas Magical Arithmatic, sebuah mata kuliah yang mengajarkan bagaimana memformulasikan suatu sihir dengan perhitungan rangkaian agar terbentuk sihir yang bisa diaplikasikan di dunia nyata. Kelas ini diampu oleh Prof. Alden dan materi awal yaitu pengenalan 2' Complement. Setelah mendengarkan penjelasan Prof. Alden, Magus ditugaskan mengubah angka unsigned menjadi signed negatif angka tersebut menggunakan 2' complement (misalnya 1 menjadi -1, 4 menjadi -4, dst) dalam rentang 4 bit dan hanya dari 0 sampai 8..

Magus membayangkan membuat rangkaian ini menggunakan KMAP untuk mengonversi angka 4-bit unsigned. Untuk angka di luar rentang ini, outputnya harus ditandai sebagai `X` (Don’t Care). **(30 poin)**

> Hint: Sederhanakan persamaan dari KMAP dan gunakan complex gate, namun saat praktikum nanti XOR tidak tersedia.

### Truth Table:
| I3 | I2 | I1 | I0 | D3 | D2 | D1 | D0 |
| -- | -- | -- | -- | -- | -- | -- | -- |
| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| 0 | 0 | 0 | 1 | 1 | 1 | 1 | 1 |
| 0 | 0 | 1 | 0 | 1 | 1 | 1 | 0 |
| 0 | 0 | 1 | 1 | 1 | 1 | 0 | 1 |
| 0 | 1 | 0 | 0 | 1 | 1 | 0 | 0 |
| 0 | 1 | 0 | 1 | 1 | 0 | 1 | 1 |
| 0 | 1 | 1 | 0 | 1 | 0 | 1 | 0 |
| 0 | 1 | 1 | 1 | 1 | 0 | 0 | 1 |
| 1 | 0 | 0 | 0 | 1 | 0 | 0 | 0 |
| 1 | 0 | 0 | 1 | X | X | X | X |
| 1 | 0 | 1 | 0 | X | X | X | X |
| 1 | 0 | 1 | 1 | X | X | X | X |
| 1 | 1 | 0 | 0 | X | X | X | X |
| 1 | 1 | 0 | 1 | X | X | X | X |
| 1 | 1 | 1 | 0 | X | X | X | X |
| 1 | 1 | 1 | 1 | X | X | X | X |

### KMAP untuk D3:  

|I3 I2\I1 I0 | 00  | 01  | 11  | 10  |
|------------|-----|-----|-----|-----|
| **00**    |  0  |  1  |  1  |  1  |
| **01**    |  1  |  1  |  1  |  1  |
| **11**    |  X  |  X  |  X  |  X  |
| **10**    |  1  |  X  |  X  |  X  |

![image](https://hackmd.io/_uploads/BJQ3AswJbl.png)

D3 = I0+I1+I2+I3

### KMAP untuk D2:  

|I3 I2\I1 I0 | 00  | 01  | 11  | 10  |
|------------|-----|-----|-----|-----|
| **00**    |  0  |  1  |  1  |  1  |
| **01**    |  1  |  0  |  0  |  0  |
| **11**    |  X  |  X  |  X  |  X  |
| **10**    |  0  |  X  |  X  |  X  |

![image](https://hackmd.io/_uploads/S1aayhwkWe.png)

D2 = I0I2'I3'+I1I2'I3'+I0'I1'I2
D2 = (I0+I1)(I2I3)'+I0'I1'I2

### KMAP untuk D1:  

|I3 I2\I1 I0 | 00  | 01  | 11  | 10  |
|------------|-----|-----|-----|-----|
| **00**    |  0  |  1  |  0  |  1  |
| **01**    |  0  |  1  |  0  |  1  |
| **11**    |  X  |  X  |  X  |  X  |
| **10**    |  0  |  X  |  X  |  X  |

![image](https://hackmd.io/_uploads/HJhNJnwkbl.png)

D1 = I0I1'+I0'I1 
D1 = I0⊕I1

### KMAP untuk D0:  

|I3 I2\I1 I0 | 00  | 01  | 11  | 10  |
|------------|-----|-----|-----|-----|
| **00**    |  0  |  1  |  1  |  0  |
| **01**    |  0  |  1  |  1  |  0  |
| **11**    |  X  |  X  |  X  |  X  |
| **10**    |  0  |  X  |  X  |  X  |

![image](https://hackmd.io/_uploads/B1L8ynD1Wl.png)

D0 = I0

### Screenshot:  
![image](https://hackmd.io/_uploads/r1eyjLuJWx.png)

---

Namun, Prof. Alden memberikan suatu pendekatan berbeda yaitu menggunakan 4-bit Full Adder (7483). Prof. Alden memberikan petunjuk bahwa 2’s complement dapat dicapai dengan **INVERT** semua bit input dan kemudian **DITAMBAH 1** pada hasilnya. Dengan petunjuk ini, Magus segera mengembangkan rangkaian lain berdasarkan pendekatan tersebut. **(15 poin)**

### Screenshot:  
![image](https://hackmd.io/_uploads/rkPi98u1be.png)

### Analisis:
Jelaskan perbedaan serta kelebihan dan kekurangan antara pendekatan KMAP dan pendekatan Full Adder! **(15 poin)**

Perbedaan dari KMAP dan FULL ADDER adalah untuk KMAP menggunakan penyederhanaan dan logic gates untuk setiap outputnya. Sedangkan dengan FULL ADDER, kita hanya perlu menggunakan IC 7483 dan menginvert inputnya saja tanpa perlu memikirkan algoritma rangkaiannya. 

|   |Kelebihan| Kekurangan|
|:-:|:-------:|:---------:|
|**KMAP**|Mudah dipahami karena sudah mengerti basic dari KMAP|Rangkaian panjang dan harus membuat fungsi tiap output menggunakan KMAP terlebih dahulu|
|**FULL ADDER**|Rangkaian lebih cepat dibuat dan lebih sederhana hasilnya|Diperlukan pemahaman mengenai cara kerja IC 7483 dan teori untuk menghasilkan 2's complement dari input awal
