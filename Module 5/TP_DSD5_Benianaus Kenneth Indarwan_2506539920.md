---
title: Tugas Pendahuluan - Decoder & Encoder

---

# Tugas Pendahuluan - Decoder & Encoder
> Pembuat Soal: NZ

```
Nama    : Benianaus Kenneth Indarwan
NPM     : 2506539920
```

## Notes
- Jika ada pertanyaan yang kurang jelas, silahkan tanya di server Discord Digital Lab
- Referensi harus dalam format IEEE (Kamu boleh menggunakan https://www.mybib.com/tools/ieee-citation-generator biar lebih gampang). Referensi minimal dua

## Teori (30 Poin)

### 1. Jelaskan apa itu `Decoder` dan `Encoder`, beserta dengan fungsi dan contoh aplikasinya.

Encoder adalah rangkaian kombinasional untuk mengubah beberapa input binary menjadi output dalam format lain. Contohnya, ada input dengan 2<sup>n</sup> bit, artinya ada n bit input. Misalkan ada 8 bit, encoder dapat mengubah 8 input tersebut menjadi hanya 3 output. 
Sementara itu, Decoder adalah kebalikan dari encoder, dimana ia berfungsi untuk mengubah input yang singkat, dan mengembalikannya dalam format binary atau format aslinya.

Contoh pengaplikasian encoder dan decoder pada multiplexer (MUX), Priority Encoder, Signal Processing, dan N Segment Displays.


### Referensi: 
- [1]GeeksforGeeks, “Encoders and Decoders in Digital Logic,” GeeksforGeeks, May 08, 2018. https://www.geeksforgeeks.org/digital-logic/encoders-and-decoders-in-digital-logic/ (accessed Oct. 05, 2025).
- [2]Anonymous, “Different Types of Encoder and Decoder and Its Applications,” WatElectronics.com, Jul. 29, 2019. https://www.watelectronics.com/different-types-encoder-decoder-applications/ (accessed Oct. 05, 2025).
- [3]GeeksforGeeks, “Applications of Decoders,” GeeksforGeeks, May 02, 2024. https://www.geeksforgeeks.org/digital-logic/applications-of-decoders/ (accessed Oct. 05, 2025).

### 2. Sebutkan dan jelaskan perbedaan `Decoder` dan `Encoder` secara komprehensif

Perbedaan utama dari Decoder dan Encoder adalah mereka melakukan hal yang berkebalikan. Encoder mengubah informasi awal menjadi hasil yang diperlukan, sedangkan Decoder mengubah informasi yang sudah diubah Encoder menjadi informasi awal atau input awal.

Perbedaannya:
|Encoder|Decoder|
|----|----|
|Mengkonversi input awal menjadi input yang sudah coded | Mengubah hasil dari input coded menjadi input awal|
|Sinyal yang masuk adalah input asli (binary) | Sinyal yang masuk adalah sinyal yang sudah coded|
|Jumlah input yang masuk adalah 2<sup>n</sup> (binary) | Jumlah input yang masuk adalah `n` input|
|Operasi yang dilakukan lebih sederhana | Operasi yang dilakukan lebih kompleks |
|Rangkaian Encoder dipasang di pengirim sinyal | Rangkaian Decoder dipasang di penerima sinyal|
|Pada dasarnya menggunakan OR gate | Pada dasarnya menggunakan AND dan NOT gate |
|Dipakai untuk mengkompres informasi | Dipakai dalam mikroprosesor untuk mengekstrak informasi |
 
### Referensi: 
- [1]GeeksforGeeks, “Difference Between Encoder and Decoder,” GeeksforGeeks, Oct. 10, 2020. https://www.geeksforgeeks.org/digital-logic/difference-between-encoder-and-decoder/ (accessed Oct. 05, 2025).
- [2]Electrical Technology, “What is the Differences Between Encoder and Decoder?,” ELECTRICAL TECHNOLOGY, Dec. 15, 2022. https://www.electricaltechnology.org/2022/12/difference-between-encoder-decoder.html (accessed Oct. 05, 2025).

### 3. Jelaskan apa itu `Priority Encoder` Sebutkan satu saja contoh praktik/kegunaan dari `Priority Encoder` yang sebenarnya ada di dalam kehidupan sehari-hari/lingkungan sekitar kalian

Priority Encoder adalah encoder yang mengambil beberapa input data secara bersamaan, kemudian mengeluarkan hasil output yang paling diprioritaskan. Priority Encoder bekerja dengan cara pertama menentukan prioritas tiap input pin. Jadi, ia akan melihat input dengan prioritas tertinggi. Semakin tinggi prioritasnya, semakin besar outputnya. 

Contoh Priority Encoder adalah untuk sistem interrupt pada processor, dimana processor menetapkan prioritas input dan akan melaksanakan input dengan prioritas tertinggi terlebih dahulu. 

### Referensi: 
- [1]Anonymous, “Priority Encoder and Digital Encoder Tutorial,” Basic Electronics Tutorials, Aug. 2013. https://www.electronics-tutorials.ws/combination/comb_4.html (accessed Oct. 05, 2025).
- [2]
WatElectronics, “Priority Encoder : Truth Table, Differences & Its Applications,” WatElectronics.com, Jul. 17, 2021. https://www.watelectronics.com/priority-encoder/ (accessed Oct. 05, 2025).

## Intro to Proteus (30 poin)

### 4. Mulai pekan ini dan seterusnya, kalian akan berpindah dari Tinkercad ke Proteus. Dengan menggunakan Proteus, buatlah sebuah rangkaian sederhana yang dapat menyalakan satu lampu LED (warna terserah kalian) menggunakan pin power, ground dan komponen switch. Jangan lupa untuk memberikan Teks berupa Nama_NPM pada rangkaian sesuai video tutorial yang sudah diberikan di Emas3. (10 poin)
`Note Untuk kedepannya, rangkaian pada Proteus harus selalu disertakan dengan teks nama_NPM. Jika tidak ada, maka nilainya akan dikurangi`

**Screenshot Rangkaian:**
![image](https://hackmd.io/_uploads/HJ_TtZlagg.png)


### 5. Buatlah kembali rangkaian yang kalian bikin di CS modul lalu (Modul Complex Logic Gate), namun sekarang gunakan proteus. (20 poin)

**Screenshot Rangkaian:**
![image](https://hackmd.io/_uploads/HyzSK-e6xe.png)




## Praktik (40 Poin)

### 6. Pada CS nanti dan beberapa modul-modul selanjutnya, kalian akan menggunakan salah satu decoder yang paling sering dipakai: BCD to 7-Segment decoder. Buatlah isi dari decoder ini menggunakan IC saja. 

#### Truth Table (15 poin)

| A   | B   | C   | D   | a   | b   | c   | d   | e   | f   | g   |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 0   | 0   | 0   | 0   | 1   | 1   | 1   | 1   | 1   | 1   | 0   |
| 0   | 0   | 0   | 1   | 0   | 1   | 1   | 0   | 0   | 0   | 0   |
| 0   | 0   | 1   | 0   | 1   | 1   | 0   | 1   | 1   | 0   | 1   |
| 0   | 0   | 1   | 1   | 1   | 1   | 1   | 1   | 0   | 0   | 1   |
| 0   | 1   | 0   | 0   | 0   | 1   | 1   | 0   | 0   | 1   | 1   |
| 0   | 1   | 0   | 1   | 1   | 0   | 1   | 1   | 0   | 1   | 1   |
| 0   | 1   | 1   | 0   | 1   | 0   | 1   | 1   | 1   | 1   | 1   |
| 0   | 1   | 1   | 1   | 1   | 1   | 1   | 0   | 0   | 0   | 0   |
| 1   | 0   | 0   | 0   | 1   | 1   | 1   | 1   | 1   | 1   | 1   |
| 1   | 0   | 0   | 1   | 1   | 1   | 1   | 1   | 0   | 1   | 1   |
| 1   | 0   | 1   | 0   | X   | X   | X   | X   | X   | X   | X   |
| 1   | 0   | 1   | 0   | X   | X   | X   | X   | X   | X   | X   |
| 1   | 1   | 0   | 1   | X   | X   | X   | X   | X   | X   | X   |
| 1   | 1   | 0   | 0   | X   | X   | X   | X   | X   | X   | X   |
| 1   | 1   | 1   | 1   | X   | X   | X   | X   | X   | X   | X   |
| 1   | 1   | 1   | 0   | X   | X   | X   | X   | X   | X   | X   |

#### KMAP (15 poin)
>a

| AB/CD | 00  | 01  | 11  | 10  |
| ----- | --- | --- | --- | --- |
| 00    | 1   | 0   | 1   | 1   |
| 01    | 0   | 1   | 1   | 1   |
| 11    | X   | X   | X   | X   |
| 10    | 1   | 1   | X   | X   |

![image](https://hackmd.io/_uploads/rJnseMeTle.png)
F=A+C+BD+A'B'D'

>b

| AB/CD | 00  | 01  | 11  | 10  |
| ----- | --- | --- | --- | --- |
| 00    |1    |1    |1    |1    |
| 01    |1    |0    |1    |0    |
| 11    |X    |X    |X    |X    |
| 10    |1    |1    |X    |X    |

![image](https://hackmd.io/_uploads/ryNRlzeTee.png)
F=A+A'B'+C'D'+CD

>c

| AB/CD | 00  | 01  | 11  | 10  |
| ----- | --- | --- | --- | --- |
| 00    |1    |1    |1    |0    |
| 01    |1    |1    |1    |1    |
| 11    |X    |X    |X    |X    |
| 10    |1    |1    |X    |X    |

![image](https://hackmd.io/_uploads/r1eW-zlaee.png)
F=BC+C'+CD

>d

| AB/CD | 00  | 01  | 11  | 10  |
| ----- | --- | --- | --- | --- |
| 00    |1    |0    |1    |1    |
| 01    |0    |1    |0    |1    |
| 11    |X    |X    |X    |X    |
| 10    |1    |1    |X    |X    |

![image](https://hackmd.io/_uploads/S1enfflpgx.png)

F=A+BC'D+CD'+A'B'C+A'B'D'

>e

| AB/CD | 00  | 01  | 11  | 10  |
| ----- | --- | --- | --- | --- |
| 00    |1    |0    |0    |1    |
| 01    |0    |0    |0    |1    |
| 11    |X    |X    |X    |X    |
| 10    |1    |0    |X    |X    |

![image](https://hackmd.io/_uploads/Syz8-Mgaxl.png)
F=AC'D'+A'B'D'+A'CD'

>f

| AB/CD | 00  | 01  | 11  | 10  |
| ----- | --- | --- | --- | --- |
| 00    |1    |0    |0    |0    |
| 01    |1    |1    |0    |1    |
| 11    |X    |X    |X    |X    |
| 10    |1    |1    |X    |X    |

![image](https://hackmd.io/_uploads/rk9pP7eTge.png)
F=AB'+BC'+C'D'+BCD'

>g

| AB/CD | 00  | 01  | 11  | 10  |
| ----- | --- | --- | --- | --- |
| 00    |0    |0    |1    |1    |
| 01    |1    |1    |0    |1    |
| 11    |X    |X    |X    |X    |
| 10    |1    |1    |X    |X    |

![image](https://hackmd.io/_uploads/H1RFbMxaxl.png)
F=AB'+BC'+A'B'C+CD'

#### Screenshot Rangkaian (10 poin)
![image](https://hackmd.io/_uploads/Bk4Wjmepex.png)


