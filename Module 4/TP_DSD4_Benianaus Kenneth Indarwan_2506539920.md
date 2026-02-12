# Tugas Pendahuluan - Gerbang Logika Kompleks
Pembuat Soal: DY

```
Nama  : Benianaus Kenneth Indarwan
NPM   : 2506539920
```

## Catatan

* Jika ada pertanyaan yang kurang jelas, silakan tanyakan di server Digilab Discord.
* Referensi harus menggunakan gaya IEEE (Anda dapat menggunakan [Mybib](https://www.mybib.com/tools/ieee-citation-generator) untuk mempermudah). Sertakan minimal 2 referensi.

## Teori (50 poin)

### 1. Untuk IC-IC berikut, jelaskan fungsi masing‑masing, konfigurasi pin sesuai datasheet, dan tabel kebenarannya: (10 poin)

1. **IC 7486**
2. **IC 7400**
3. **IC 7402**

---

IC 7486 Quad 2-input XOR gate, merupakan IC untuk gerbang logika Exclusive OR. Artinya output akan `1`, apabila `Input 1` dan `Input 2` berbeda. 

#### Konfigurasi Pin IC 7486
![image](https://hackmd.io/_uploads/B1BdWwK2xx.png)
|Pin Number|  Description    |
|----------|-----------------|
| 1        | A Input Gate 1  |
| 2        | B Input Gate 1  |
| 3        | Y Output Gate 1 |
| 4        | A Input Gate 2  |
| 5        | B Input Gate 2  |
| 6        | Y Output Gate 2 |
| 7        | Gnd             |
| 8        | Y Output Gate 3 |
| 9        | B Input Gate 3  |
| 10       | A Input Gate 3  |
| 11       | Y Output Gate 4 |
| 12       | B Input Gate 4  |
| 13       | A Input Gate 4  |
| 14       | Vcc             |

#### Truth Table IC 7486
| Input A | Input B | Output Y |
| ------- | ------- | -------- |
|    0    |    0    |     0    |
|    0    |    1    |     1    |
|    1    |    0    |     1    |
|    1    |    1    |     0    |

---

IC 7400 Quad 2-input NAND gate, merupakan IC untuk gerbang logika NOT AND. Artinya, gerbang logika ini adalah gerbang `AND` dimana kemudian diinvers lagi hasilnya. Fungsinya untuk mempermudah fungsi apabila dicari fungsi yang mencari hasil `bukan AND`.

#### Konfigurasi Pin IC 7400
![74x00_package-and-pinout](https://hackmd.io/_uploads/HkYEVwYhel.png)
|Pin Number|  Description    |
|----------|-----------------|
| 1        | A Input Gate 1  |
| 2        | B Input Gate 1  |
| 3        | Y Output Gate 1 |
| 4        | A Input Gate 2  |
| 5        | B Input Gate 2  |
| 6        | Y Output Gate 2 |
| 7        | Gnd             |
| 8        | Y Output Gate 3 |
| 9        | B Input Gate 3  |
| 10       | A Input Gate 3  |
| 11       | Y Output Gate 4 |
| 12       | B Input Gate 4  |
| 13       | A Input Gate 4  |
| 14       | Vcc             |

#### Truth Table IC 7400
| Input A | Input B | Output Y |
| ------- | ------- | -------- |
|    0    |    0    |     1    |
|    0    |    1    |     1    |
|    1    |    0    |     1    |
|    1    |    1    |     0    |

---

IC 7402 Quad 2-input NOR gate, merupakan IC untuk gerbang logika NOT OR. Artinya, gerbang logika ini adalah gerbang `OR` yang kemudian diinvers lagi hasilnya. Fungsinya untuk mempermudah fungsi apabila dicari fungsi yang mencari hasil `bukan OR`.

#### Konfigurasi Pin IC 7402
![74x02_package-and-pinout](https://hackmd.io/_uploads/ByV5HvF2el.png)
|Pin Number|  Description    |
|----------|-----------------|
| 1        | A Input Gate 1  |
| 2        | B Input Gate 1  |
| 3        | Y Output Gate 1 |
| 4        | A Input Gate 2  |
| 5        | B Input Gate 2  |
| 6        | Y Output Gate 2 |
| 7        | Gnd             |
| 8        | Y Output Gate 3 |
| 9        | B Input Gate 3  |
| 10       | A Input Gate 3  |
| 11       | Y Output Gate 4 |
| 12       | B Input Gate 4  |
| 13       | A Input Gate 4  |
| 14       | Vcc             |

#### Truth Table IC 7402
| Input A | Input B | Output Y |
| ------- | ------- | -------- |
|    0    |    0    |     1    |
|    0    |    1    |     0    |
|    1    |    0    |     0    |
|    1    |    1    |     0    |

### Referensi:

- [1]Anonymous, “IC 7486 Chip: Datasheet, Pinout and Truth Table,” www.ntchip.com, May 13, 2024. https://www.ntchip.com/electronics-news/ic-7486-chip (accessed Sep. 30, 2025).
- [2]Anonymous, “7400 Series Guide: 74LS00/74HC00 (NAND gates),” Build Electronic Circuits, 2023. https://www.build-electronic-circuits.com/7400-series-integrated-circuits/74hc00-74ls00/ (accessed Sep. 30, 2025).
- [3]Anonymous, “7402 IC Chip: Pin Diagram, Truth table and Datasheet,” Ntchip.com, May 24, 2024. https://www.ntchip.com/electronics-news/7402-ic-chip (accessed Sep. 30, 2025).

---

### 2. Apa saja keuntungan gerbang logika kompleks dibandingkan gerbang logika dasar? (10 poin)

Fungsi dari gerbang kompleks adalah menggabungkan beberapa gerbang logika sederhana. Dengan menggunakan gerbang logika kompleks, maka akan menghemat biaya atau menghemat IC yang digunakan. Selain itu, penggunaan gerbang logika kompleks akan membuat rangkaian terlihat lebih sederhana.

### Referensi:

- [1]Anonymous, “Complex logic gates - Digital data - CCEA - GCSE Digital Technology (CCEA) Revision,” BBC Bitesize. https://www.bbc.co.uk/bitesize/guides/z8qymsg/revision/9 (accessed Sep. 30, 2025).
- [2]GQ, “Mastering the Fundamentals of Logic Gates and Digital Logic Circuits,” Dadao, Feb. 25, 2025. https://dadaoenergy.com/blog/logic-circuit/ (accessed Sep. 30, 2025).

---

### 3. Berikan diagram rangkaian dan jelaskan bagaimana membuat gerbang AND, OR, dan NOT menggunakan: (30 poin)

### a. Hanya gerbang NAND

### b. Hanya gerbang NOR

Anda dapat menggambar secara fisik di kertas lalu memfoto, atau menyediakan tangkapan layar dari aplikasi seperti Logisim/Proteus. Anda **TIDAK** diperbolehkan mengambil tangkapan layar langsung dari internet!
`Petunjuk: Enam diagram adalah NAND→AND, NAND→OR, NAND→NOT, NOR→AND, NOR→OR, NOR→NOT`

#### a. Hanya Gerbang NAND
Dari gerbang NAND, konsep untuk membuat gerbang NOT adalah dengan menggunakan gerbang NAND sendiri, tapi kedua inputnya diambil dari sumber yang sama. Hal ini karena berlaku pada `AB=Y`, `00=1` dan `11=0`. 

Untuk gerbang AND, karena gerbang NAND akan membuat hasilnya terbalik, maka kita invert lagi menggunakan konsep NOT di atas. Untuk gerbang OR, pertama kita harus menginvers input (menggunakan konsep NOT), kemudian hasilnya diinput ke dalam gerbang NAND lagi. 

#### b. Hanya Gerbang NOR
Dari gerbang NOR, konsep untuk membuat gerbang NOT sama seperti pada gerbang NAND; dengan menggunakan gerbang NOR sendiri, tapi kedua inputnya diambil dari sumber yang sama. Hal ini karena berlaku pada `AB=Y`, `00=1` dan `11=0`. Untuk membuat gerbang AND dan OR terbalik dari gerbang NAND. 

Untuk gerbang AND, pertama kita harus menginvers input (menggunakan konsep NOT), kemudian hasilnya diinput ke dalam gerbang NOR lagi. Untuk gerbang OR, karena gerbang NOR akan membuat hasilnya terbalik, maka kita invert lagi menggunakan konsep NOT di atas.

#### c. Diagram 

|       | NAND | NOR |
| ----- | ---- | --- |
|**AND**|![image](https://hackmd.io/_uploads/HysM9wYnlx.png)|![image](https://hackmd.io/_uploads/Sk-MjvY2ee.png)|
|**OR** |![image](https://hackmd.io/_uploads/BypWqDK3xg.png)|![image](https://hackmd.io/_uploads/HJpzowFnee.png)|
|**NOT**|![image](https://hackmd.io/_uploads/HJvmcPY3gl.png)|![image](https://hackmd.io/_uploads/BkDmiDK2xe.png)|

### Referensi:

- [1]GeeksforGeeks, “Implementation of AND Gate from NAND Gate,” GeeksforGeeks, Feb. 14, 2024. https://www.geeksforgeeks.org/digital-logic/implementation-and-from-nand/ (accessed Sep. 30, 2025).
- [2]EngineeringLead, “NOT, AND, OR Gates Using NAND Gates,” Instructables, Dec. 31, 2015. https://www.instructables.com/NOT-AND-OR-Gates-From-NAND-Gates/ (accessed Sep. 30, 2025).
- [3]GeeksforGeeks, “Implementation of AND Gate from NOR Gate,” GeeksforGeeks, Feb. 15, 2024. https://www.geeksforgeeks.org/electronics-engineering/implementation-of-and-gate-from-nor-gate/ (accessed Sep. 30, 2025).
- [4]GeeksforGeeks, “Implementation of OR Gate from NOR Gate,” GeeksforGeeks, Feb. 18, 2024. https://www.geeksforgeeks.org/digital-logic/implementation-of-or-gate-from-nor-gate/ (accessed Sep. 30, 2025).
- [5]GeeksforGeeks, “Implementation of NOT Gate using NOR Gate,” GeeksforGeeks, Feb. 23, 2024. https://www.geeksforgeeks.org/electronics-engineering/implementation-of-not-gate-using-nor-gate/ (accessed Sep. 30, 2025).

---

## Pre-CS (50 poin)

Setelah semua yang dilalui oleh Magus dan Anda, tak terasa kalender Imajineri menunjuk tanggal 26, artinya 2 minggu lagi Magus akan menghadapi ujian tengah semester. Untuk itu, Magus meminta tolong kepada Anda untuk sama-sama brainstorming agar bisa mendapatkan jadwal yang efektif di hari-hari sebelum ujian. Berikut ketentuan jadwalnya.

* Harus ada `Belajar` **ATAU** `Latihan`.
  **DAN**
* Hanya boleh `Bermain` **atau** hanya `Istirahat`, tetapi **tidak boleh keduanya bersamaan**.

Bantu Magus membuat jadwalnya dan rangkailah alat yang bisa menyelesaikan masalah ini di TinkerCad yang sesuai dengan ketentuan jadwal Magus. Bangun 2 rangkaian berbeda, namun dalam file TinkerCad yang sama.

1. Rangkaian pertama tidak boleh menggunakan gerbang kompleks.
2. Rangkaian kedua hanya boleh menggunakan gerbang kompleks.
   `Petunjuk untuk No.2: Gunakan NOR untuk membuat gerbang OR, dan gunakan NAND untuk membuat gerbang AND.`

Sertakan **SCREENSHOT** dan **LINK** ke simulasi Tinkercad. Pastikan link **BERSIFAT SHARE**.

---

### Deskripsi Variabel

A = Belajar
B = Latihan
C = Bermain
D = Istirahat

### Tabel Kebenaran:

| A | B | C | D | Output |
| - | - | - | - | ------ |
| 0 | 0 | 0 | 0 | 0      |
| 0 | 0 | 0 | 1 | 0      |
| 0 | 0 | 1 | 0 | 0      |
| 0 | 0 | 1 | 1 | 0      |
| 0 | 1 | 0 | 0 | 0      |
| 0 | 1 | 0 | 1 | 1      |
| 0 | 1 | 1 | 0 | 1      |
| 0 | 1 | 1 | 1 | 0      |
| 1 | 0 | 0 | 0 | 0      |
| 1 | 0 | 0 | 1 | 1      |
| 1 | 0 | 1 | 0 | 1      |
| 1 | 0 | 1 | 1 | 0      |
| 1 | 1 | 0 | 0 | 0      |
| 1 | 1 | 0 | 1 | 1      |
| 1 | 1 | 1 | 0 | 1      |
| 1 | 1 | 1 | 1 | 0      |

### K-Map:

| AB\CD  | 00 | 01 | 11 | 10 |
| ------ | -- | -- | -- | -- |
| **00** | 0  | 0  | 0  | 0  |
| **01** | 0  | 1  | 0  | 1  |
| **11** | 0  | 1  | 0  | 1  |
| **10** | 0  | 1  | 0  | 1  |

[screenshot/foto penyelesaian pengelompokan Kmap]
![image](https://hackmd.io/_uploads/H1lj-uY2lx.png)

Fungsi = AC'D+ACD'+BC'D+BCD' = A(C'D+CD')+B(C'D+CD')

### Screenshot Rangkaian Gerbang Dasar:

![image](https://hackmd.io/_uploads/rkfyKuFhex.png)


### Screenshot Rangkaian Gerbang Kompleks:

![image](https://hackmd.io/_uploads/BkItxKt3xg.png)


### Link:

https://www.tinkercad.com/things/ggEY1UPrH4q-tpdsd4benianaus-kenneth-indarwan2506539920?sharecode=SUlLmD2EP-xTL65pT74Pkqahp7NJ6_GCCG-CMeEagPE
