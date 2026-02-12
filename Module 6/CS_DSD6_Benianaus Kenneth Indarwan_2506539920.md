---
title: Case Study Multiplexer & Demultiplexer

---

# Case Study - Modul 6 "MUX&DEMUX"
`Pembuat Soal : NA`
```
Nama: Benianaus Kenneth Indarwan
NPM: 2506539920
Kelompok : A27
Rekan Kerja : Benedict Jaysen Riofo Panjaitan
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
| 0 | 0 | 0   | 1  | 0     | 1     |
| 0 | 1 | 1   | 0  | 0     | 1     |
| 1 | 0 | 1   | 0  | 0     | 1     |
| 1 | 1 | 1   | 0  | 1     | 0     |

Pasangan 2 (s1|s0 = 01)
| B | C | OR | NOR | AND| NAND |
| - | - | --- | -- | ----- | ----- |
| 0 | 0 | 0   | 1  | 0     | 1     |
| 0 | 1 | 1   | 0  | 0     | 1     |
| 1 | 0 | 1   | 0  | 0     | 1     |
| 1 | 1 | 1   | 0  | 1     | 0     |

Pasangan 3 (s1|s0 = 10)
| C | D | OR | NOR | AND| NAND |
| - | - | --- | -- | ----- | ----- |
| 0 | 0 | 0   | 1  | 0     | 1     |
| 0 | 1 | 1   | 0  | 0     | 1     |
| 1 | 0 | 1   | 0  | 0     | 1     |
| 1 | 1 | 1   | 0  | 1     | 0     |

Pasangan 4 (s1|s0 = 11)
| D | A | OR | NOR | AND| NAND |
| - | - | --- | -- | ----- | ----- |
| 0 | 0 | 0   | 1  | 0     | 1     |
| 0 | 1 | 1   | 0  | 0     | 1     |
| 1 | 0 | 1   | 0  | 0     | 1     |
| 1 | 1 | 1   | 0  | 1     | 0     |

Screenshot Rangkaian : 

Pasangan 4 (s1|s0 = 11)
| D | A | OR | NOR | AND| NAND | Gambar |
| - | - | --- | -- | ----- | ----- | --- |
| 0 | 0 | 0   | 1  | 0     | 1     |![00](https://hackmd.io/_uploads/rkemCPgkWx.jpg)|
| 0 | 1 | 1   | 0  | 0     | 1     |![10](https://hackmd.io/_uploads/ryW40PxkZl.jpg)|
| 1 | 0 | 1   | 0  | 0     | 1     |![01](https://hackmd.io/_uploads/SkcQ0wlJWe.jpg)|
| 1 | 1 | 1   | 0  | 1     | 0     |![11](https://hackmd.io/_uploads/r154AwxJWg.jpg)|

Keterangan LED:
- Merah = OR
- Hijau = NOR
- Biru = AND
- Kuning = NAND

### *Jika Anda tidak sempat menyelesaikan rangkaian atau rangkaian bermasalah, Anda dapat melanjutkan pengerjaan di Proteus dengan maksimal poin 40.

## Analisis & Teori (50 Poin)

### 2. Analisis IC apa saja yang kalian gunakan untuk rangkaian ini beserta kegunaannya. Kemudian berikanlah analisis kesalahan apabila output tidak sesuai atau jika rangkaian tidak selesai. (20 poin)
IC yang digunakan adalah `IC 7404 (NOT GATE)`, `IC 7432 (OR GATE)`, `IC 7408 (AND GATE)`, dan `IC 74153 (DUAL 4-1 MULTIPLEXER)`. Pertama, input dihubungkan ke `MULTIPLEXER` beserta dengan 2 input selector. 2 Output dari `MULTIPLEXER` kemudian bisa dihubungkan dengan jenis-jenis output yang dapat diinginkan. Dalam CS ini, kedua output dihubungkan dengan `AND` dan `OR`, kemudian output dari kedua gate diinvert menggunakan `NOT` sehingga didapatkan 4 output, yaitu OR, NOR, AND, NAND, dari output `MULTIPLEXER`.


### 3. Jika ingin membuat sebuah opsi lanjutan yaitu memilih output yang ingin diambil, IC apa yang bisa dipakai untuk hal ini? Jelaskan alasan kalian! (20 poin)

IC yang digunakan adalah `IC 74153 (DUAL 4-1 MULTIPLEXER)`. Karena, menggunakan IC ini, kita bisa mengambil 4 output tersebut, kemudian menggunakan 2 input selector, kita bisa memilih output mana yang digunakan. Contohnya, (s1|s0 = 00 OR), (s1|s0 = 01 NOR), (s1|s0 = 10 AND), (s1|s0 = 11 NAND). Hasilnya hanya akan ada 1 output saja.

### 4. Buatlah kesimpulan yang kalian dapatkan dari praktikum kali ini dalam bentuk poin-poin minimal 3 ! (20 poin)

- IC 74153 merupakan Multiplexer, yang bekerja dengan cara mengambil 4 input dan memilih output menggunakan 2 bit selector
- Dengan menggunakan Multiplexer, kita dapat menggabungkan 4 input untuk kombinasi masing-masing 2 input. Tidak perlu membuat 4x4 rangkaian berbeda untuk setiap kombinasi input dan gatenya, tetapi cukup menggunakan Multiplexer dan kombinasi gate.
- Kita membutuhkan 4 output LED untuk membaca 4 output tersebut, tetapi bisa menggunakan tambahan 4 switch selector dan 1 Multiplexer jika hanya ingin 1 output saja
- NAND Gate dan NOR Gate dapat diambil menggunakan 1 IC 7404 (inverter) sehingga akan menghemat 1 IC. Alternatifnya, bisa menggunakan 1 jenis complex gate (NAND/NOR) untuk keempat outputnya
- Penting untuk troubleshoot tidak hanya pada kabel dan lampu, tapi juga melihat apakah kabel power/ground berfungsi