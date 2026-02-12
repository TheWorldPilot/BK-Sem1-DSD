---
title: Case Study Multiplexer & Demultiplexer

---

# Case Study - Modul 6 "MUX&DEMUX"
`Pembuat Soal : NA`
```
Nama: Takahiro Sakurai [Ganti dengan Nama Kalian]
NPM: 13061974 [Ganti dengan NPM Kalian]
Kelompok : 
Rekan Kerja : 
```

## Rangkaian (50 Poin)

Sekarang Magus mendapatkan tugas tambahan dari Prof.Randy yang serupa dengan yang lalu. Namun sekarang terdapat list logika yang berbeda.
List logika cepat:
1. OR
2. NOR
3. AND
4. NAND

Dengan ketentuan:
- Terdapat 4 Input yaitu A,B,C dan D dan 2 Bit Selector yaitu s0 dan s1 untuk memilih pasangan variabel.
- Terdapat 4 pasangan Variabel yaitu A dengan B, B dengan C, C dengan D dan D dengan A.
- Gunakan 74153 untuk menghasilkan logika cepat.

### 1. Buatlah rangkaian secara fisiknya untuk membantu Magus sesuai spesifikasi yang diminta di atas.
***Hint 1 : Saat suatu pasangan dipilih, maka input diluar pasangan dianggap dont care***
***Hint 2 : Pelajari datasheet 74153***

Truth Table 

Pasangan 1 (s1|s0 = 00)
| A | B | OR | NOR | AND| NAND |
| - | - | --- | -- | ----- | ----- |
| 0 | 0 | ?   | ?  | ?     | ?     |
| 0 | 1 | ?   | ?  | ?     | ?     |
| 1 | 0 | ?   | ?  | ?     | ?     |
| 1 | 1 | ?   | ?  | ?     | ?     |

Pasangan 2 (s1|s0 = 01)
| B | C | OR | NOR | AND| NAND |
| - | - | --- | -- | ----- | ----- |
| 0 | 0 | ?   | ?  | ?     | ?     |
| 0 | 1 | ?   | ?  | ?     | ?     |
| 1 | 0 | ?   | ?  | ?     | ?     |
| 1 | 1 | ?   | ?  | ?     | ?     |

Pasangan 3 (s1|s0 = 10)
| C | D | OR | NOR | AND| NAND |
| - | - | --- | -- | ----- | ----- |
| 0 | 0 | ?   | ?  | ?     | ?     |
| 0 | 1 | ?   | ?  | ?     | ?     |
| 1 | 0 | ?   | ?  | ?     | ?     |
| 1 | 1 | ?   | ?  | ?     | ?     |

Pasangan 4 (s1|s0 = 11)
| D | A | OR | NOR | AND| NAND |
| - | - | --- | -- | ----- | ----- |
| 0 | 0 | ?   | ?  | ?     | ?     |
| 0 | 1 | ?   | ?  | ?     | ?     |
| 1 | 0 | ?   | ?  | ?     | ?     |
| 1 | 1 | ?   | ?  | ?     | ?     |

Screenshot Rangkaian : 
![Im out!](https://hackmd.io/_uploads/BJGMgrUagg.gif)


### *Jika Anda tidak sempat menyelesaikan rangkaian atau rangkaian bermasalah, Anda dapat melanjutkan pengerjaan di Proteus dengan maksimal poin 40.

## Analisis & Teori (50 Poin)

### 2. Analisis IC apa saja yang kalian gunakan untuk rangkaian ini beserta kegunaannya. Kemudian berikanlah analisis kesalahan apabila output tidak sesuai atau jika rangkaian tidak selesai. (20 poin)

### 3. Jika ingin membuat sebuah opsi lanjutan yaitu memilih output yang ingin diambil, IC apa yang bisa dipakai untuk hal ini?Jelaskan alasan kalian! (20 poin)

### 4. Buatlah kesimpulan yang kalian dapatkan dari praktikum kali ini dalam bentuk poin-poin minimal 3 ! (20 poin)

-
-
-