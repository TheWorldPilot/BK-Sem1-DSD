---
title: Tugas Pendahuluan - Modul 6 "MUX&DEMUX"

---

# Tugas Pendahuluan - Modul 6 "MUX&DEMUX"
`Pembuat Soal : NA`
```
Nama    : Hideo Kojima [Ganti dengan Nama Kalian]
NPM     : 24081963 [Ganti dengan NPM Kalian]
```
## Teori (30 poin)

### 1. Jelaskan apa perbedaan antara `Mutliplexer` dengan `Demultiplexer` secara lengkap. Anda bisa menjelaskan dari segi fungsionalitas serta bit input dan output sekaligus IC apa yang dipakai(10 Poin).

[Jawaban Kalian Disini]

### Referensi:

* Contoh Website [Online]. Available: [https://www.myWebsite.com/ilovedigilab/](https://www.myWebsite.com/ilovedigilab/). [Accessed: 25-Aug-2024]
* Contoh Website [Online]. Available: [https://www.myWebsite.com/ilovedigilab/](https://www.myWebsite.com/ilovedigilab/). [Accessed: 25-Aug-2024]

### 2. Jelaskan apa yang dimaksud `Active Low` secara singkat beserta contoh komponen yang bisa dikatakan sebagai `Active Low`(10 Poin).

[Jawaban Kalian Disini]

### Referensi:

* Contoh Website [Online]. Available: [https://www.myWebsite.com/ilovedigilab/](https://www.myWebsite.com/ilovedigilab/). [Accessed: 25-Aug-2024]
* Contoh Website [Online]. Available: [https://www.myWebsite.com/ilovedigilab/](https://www.myWebsite.com/ilovedigilab/). [Accessed: 25-Aug-2024]

### 3. Sebutkan satu saja contoh praktik/kegunaan dari `Priority Encoder` yang sebenarnya ada di dalam kehidupan sehari-hari/lingkungan sekitar kalian(10 Poin).

[Jawaban Kalian Disini]

### Referensi:

* Contoh Website [Online]. Available: [https://www.myWebsite.com/ilovedigilab/](https://www.myWebsite.com/ilovedigilab/). [Accessed: 25-Aug-2024]
* Contoh Website [Online]. Available: [https://www.myWebsite.com/ilovedigilab/](https://www.myWebsite.com/ilovedigilab/). [Accessed: 25-Aug-2024]

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
| 0 | 0 | ?   | ?  | ?     | ?     |
| 0 | 1 | ?   | ?  | ?     | ?     |
| 1 | 0 | ?   | ?  | ?     | ?     |
| 1 | 1 | ?   | ?  | ?     | ?     |

Pasangan 2 (s1|s0 = 01)
| B | C | AND | OR | NOT 1 | NOT 2 |
| - | - | --- | -- | ----- | ----- |
| 0 | 0 | ?   | ?  | ?     | ?     |
| 0 | 1 | ?   | ?  | ?     | ?     |
| 1 | 0 | ?   | ?  | ?     | ?     |
| 1 | 1 | ?   | ?  | ?     | ?     |

Pasangan 3 (s1|s0 = 10)
| C | D | AND | OR | NOT 1 | NOT 2 |
| - | - | --- | -- | ----- | ----- |
| 0 | 0 | ?   | ?  | ?     | ?     |
| 0 | 1 | ?   | ?  | ?     | ?     |
| 1 | 0 | ?   | ?  | ?     | ?     |
| 1 | 1 | ?   | ?  | ?     | ?     |

Pasangan 4 (s1|s0 = 11)
| D | A | AND | OR | NOT 1 | NOT 2 |
| - | - | --- | -- | ----- | ----- |
| 0 | 0 | ?   | ?  | ?     | ?     |
| 0 | 1 | ?   | ?  | ?     | ?     |
| 1 | 0 | ?   | ?  | ?     | ?     |
| 1 | 1 | ?   | ?  | ?     | ?     |

Screenshot Rangkaian : 
![KJ FOGGY](https://hackmd.io/_uploads/HynFoVLTle.png)


### 5. Sekarang gunakan Multiplexer 74157 untuk memberikan opsi mengambil Output berupa AND Operation atau OR Operation dari rangkaian yang telah dibuat sebelumnya. (20 Point)

Screenshot Rangaian :
![Shussh](https://hackmd.io/_uploads/B1OQpEU6lg.gif)