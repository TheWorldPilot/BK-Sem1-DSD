---
title: Tugas Pendahuluan - Modul 6 "MUX&DEMUX"

---

# Tugas Pendahuluan - Modul 6 "MUX&DEMUX"
`Pembuat Soal : NA`
```
Nama    : Benianaus Kenneth Indarwan
NPM     : 2506539920
```
## Teori (30 poin)

### 1. Jelaskan apa perbedaan antara `Mutliplexer` dengan `Demultiplexer` secara lengkap. Anda bisa menjelaskan dari segi fungsionalitas serta bit input dan output sekaligus IC apa yang dipakai (10 Poin).

`Multiplexer` mengkombinasikan beberapa input untuk menjadi satu output, sedangkan `Demultiplexer` adalah kebalikannya, mengambil satu input yang kemudian disalurkan ke beberapa output. `Multiplexer` mengambil beberapa bit input, dengan bantuan selector, kemudian mengubahnya menjadi 1 output. Untuk `Demultiplexer`, mengambil satu input yang diubah menjadi beberapa bit output dengan bantuan selector. `Multiplexer` menggunakan IC 74153 `(DUAL 4-LINE TO 1-LINE DATA SELECTORS/MULTIPLEXERS)` dan `Demultiplexer` menggunakan IC 74155 `(DUAL 2-LINE TO 4-LINE DECODERS/DEMULTIPLEXERS)`.


### Referensi:

* [1]GeeksforGeeks, “Difference between Multiplexer and Demultiplexer,” GeeksforGeeks, May 05, 2020. https://www.geeksforgeeks.org/gate/difference-between-multiplexer-and-demultiplexer/ (accessed Oct. 24, 2025).
* [2]elprocus, “Multiplexer and Demultiplexer : Types, Differences & Their Applications,” ElProCus - Electronic Projects for Engineering Students, Apr. 14, 2014. https://www.elprocus.com/what-is-multiplexer-and-demultiplexer-types-and-differences/ (accessed Oct. 24, 2025).

### 2. Jelaskan apa yang dimaksud `Active Low` secara singkat beserta contoh komponen yang bisa dikatakan sebagai `Active Low` (10 Poin).

Active Low artinya pin yang harus dihubungkan ke GND untuk menjadi aktif. Artinya, akan ada output `1` ketika sinyal terdeteksi `LOW` atau `0`. Konsep ini mirip dengan konsep `NOT GATE`. Contoh komponennya adalah `Pin Interrupt` dan `IC Komunikasi`. Ketika sinyal tidak ada (0), maka Pin Interrupt akan ditrigger atau dalam IC Komunikasi akan memperbolehkan adanya transfer data

### Referensi:

* [1]bri_huang, “Logic Levels - learn.sparkfun.com,” learn.sparkfun.com. https://learn.sparkfun.com/tutorials/logic-levels/all (accessed Oct. 24, 2025).
* [2]Phidgets Inc, “Digital Input Guide,” Phidgets Support, Jun. 26, 2023. https://www.phidgets.com/docs/Digital_Input_Guide (accessed Oct. 24, 2025).
* [3]E. A. Prastyo, “Perbedaan Active High dan Active Low dalam Kontrol Sinyal,” Arduino.biz.id, Jul. 17, 2025. https://www.arduino.biz.id/2025/07/perbedaan-active-high-dan-active-low-dalam-kontrol-sinyal.html (accessed Oct. 26, 2025).

### 3. Sebutkan satu saja contoh praktik/kegunaan dari `Priority Encoder` yang sebenarnya ada di dalam kehidupan sehari-hari/lingkungan sekitar kalian (10 Poin).

Contoh kegunaan `Priority Encoder` adalah pada keyboard. Ketika beberapa key pada keyboard ditekan bersamaan, tidak bisa ditampilkan semuanya bersamaan. Maka, kegunaan `Priority Encoder` disini adalah untuk mengurutkan key mana yang ditekan terlebih dahulu (prioritas), satu-satu sebelum lanjut ke key berikutnya. 

### Referensi:

* [1]WatElectronics, “Priority Encoder : Truth Table, Differences & Its Applications,” WatElectronics.com, Jul. 17, 2021. https://www.watelectronics.com/priority-encoder/ (accessed Oct. 24, 2025).
* [2]Anonymous, “Priority Encoder and Digital Encoder Tutorial,” Basic Electronics Tutorials, Aug. 2013. https://www.electronics-tutorials.ws/combination/comb_4.html (accessed Oct. 24, 2025).

### Ikuti skenario dibawah ini (70 Poin).

Lain hari, lain cerita. Setelah berhasil menyelesaikan tugas dari Prof.Vergil, Magus lanjut ke mata kuliah Poliformisme bersama Prof.Randy. Di mata kuliah ini, diajarkan sebuah rangkaian yang memiliki output yang berbeda-beda hanya dengan mengubah selector. Prof.Randy memberikan tugas yaitu merangkai rangkaian yang bisa berguna untuk menghasilkan logika cepat tanpa mengubah rangkaiannya.
List logika cepat:
1. AND
2. OR
3. NOT INPUT

Dengan ketentuan:
- Terdapat 4 Input yaitu A,B,C dan D dan 2 Bit Selector yaitu s0 dan s1 untuk memilih pasangan variabel.
- Terdapat 4 pasangan Variabel yaitu A dengan B, B dengan C, C dengan D dan D dengan A.
- Gunakan 74153 untuk menghasilkan logika cepat.

### 4. Buatlah rangkaian proteus untuk membantu Magus sesuai spesifikasi yang diminta di atas. (50 Point)

***Hint 1 : Anda diperbolehkan menggunakan Logic State dan Logic Probe sebagai input/output***
***Hint 2 : Saat suatu pasangan dipilih, maka input diluar pasangan dianggap dont care***
***Hint 3 : Pelajari datasheet 74153***

Truth Table 

Pasangan 1 (s1|s0 = 00)
| A | B | AND | OR | NOT 1 | NOT 2 |
| - | - | --- | -- | ----- | ----- |
| 0 | 0 | 0   | 0  | 1     | 1     |
| 0 | 1 | 0   | 1  | 1     | 0     |
| 1 | 0 | 0   | 1  | 0     | 1     |
| 1 | 1 | 1   | 1  | 0     | 0     |

Pasangan 2 (s1|s0 = 01)
| B | C | AND | OR | NOT 1 | NOT 2 |
| - | - | --- | -- | ----- | ----- |
| 0 | 0 | 0   | 0  | 1     | 1     |
| 0 | 1 | 0   | 1  | 1     | 0     |
| 1 | 0 | 0   | 1  | 0     | 1     |
| 1 | 1 | 1   | 1  | 0     | 0     |

Pasangan 3 (s1|s0 = 10)
| C | D | AND | OR | NOT 1 | NOT 2 |
| - | - | --- | -- | ----- | ----- |
| 0 | 0 | 0   | 0  | 1     | 1     |
| 0 | 1 | 0   | 1  | 1     | 0     |
| 1 | 0 | 0   | 1  | 0     | 1     |
| 1 | 1 | 1   | 1  | 0     | 0     |

Pasangan 4 (s1|s0 = 11)
| D | A | AND | OR | NOT 1 | NOT 2 |
| - | - | --- | -- | ----- | ----- |
| 0 | 0 | 0   | 0  | 1     | 1     |
| 0 | 1 | 0   | 1  | 1     | 0     |
| 1 | 0 | 0   | 1  | 0     | 1     |
| 1 | 1 | 1   | 1  | 0     | 0     |

Screenshot Rangkaian : 
![image](https://hackmd.io/_uploads/S14hb2o0xe.png)


### 5. Sekarang gunakan Multiplexer 74157 untuk memberikan opsi mengambil Output berupa AND Operation atau OR Operation dari rangkaian yang telah dibuat sebelumnya. (20 Point)

Screenshot Rangaian :
![image](https://hackmd.io/_uploads/Skcc8ns0le.png)
![image](https://hackmd.io/_uploads/S1ecw3iRgx.png)
