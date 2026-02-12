---
title: Case Study - Rangkaian Aritmatika

---

# Case Study - Rangkaian Aritmatika
`Pembuat Soal : NA`
```
Nama  : Yharon[Ganti dengan nama Anda]
NPM   : 3182400[Ganti dengan NPM Anda]
Rekan Kerja : Phoenix[Ganti dengan nama rekan Anda]
```

## Rangkaian Fisik (50 poin)

Setelah selesai kelas, Magus diberikan tugas oleh Prof. Alden. Kali ini, dia ditantang untuk membuat 4-bit full adder yang ditampilkan menggunakan 5 LED. Magus diperbolehkan menggunakan IC 7483 (Full Adder 4bit) ataupun logic gates lainnya untuk membuat rangkaian ini.

> Opsi alternatif jika IC 7483 Habis : Membuat 2 bit subtractor menggunakan Logic Gates tanpa XOR dengan output ditampilkan menggunakan LED saja.

### Truth Table

#### Jika menggunakan IC 7483:
| A    | B    | C<sub>in</sub> | S (Biner) | C<sub>out</sub> | S (Desimal) |
| ---- | ---- | -------------- | --------- | --------------- | ----------- |
| 0000 | 0000 | 0              | ????      | ?               | ?           |
| 0001 | 0010 | 0              | ????      | ?               | ?           |
| 0010 | 0001 | 1              | ????      | ?               | ?           |
| 0111 | 1000 | 0              | ????      | ?               | ?           |
| 1000 | 1000 | 0              | ????      | ?               | ?           |
| 1010 | 1001 | 1              | ????      | ?               | ?           |
| 1111 | 0001 | 0              | ????      | ?               | ?           |
| 1111 | 1111 | 0              | ????      | ?               | ?           |
| 1111 | 1111 | 1              | ????      | ?               | ?           |
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

### Screenshot Rangkaian Fisik

![Masukkan screenshot di sini](public_image_link)

### Analisis Rangkaian 7483 (50 poin)

#### 1. Jelaskan apakah rangkaian dengan 7483 tersebut bekerja dengan input/output unsigned atau signed atau dua-duanya? Adakah kondisi tertentu yang mengakibatkan rangkaian jadi tidak bekerja? Lampirkan juga bukti screenshot dari rangkaian tersebut yang mendukung jawabanmu! (10 poin)

Lorem ipsum :+1: .

*Jika hasil outputnya adalah hasil Input_1 + Input_2, maka lampirkan screenshotnya. Jika tidak, tuliskan `-`.

| Input_1 | Input_2 | Output | Screenshot |
| ------- | ------- | ------ | ---------- |
| 15      | 15      | 30     |            |
| 15      | -15     | 0      |            |
| 7       | 16      | 23     |            |
| 0       | -1      | -1     |            |
| -7      | 5       | -2     |            |
| -1      | 1       | 0      |            |

#### 2. Apakah pin C<sub>out</sub> penting dalam menentukan hasil pertambahan dari dua bilangan biner dalam rangkaian yang telah dibuat? Jelaskan alasanmu! (10 poin)

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus quis nunc ac felis fringilla consequat ac nec elit. 

#### 3. Berapa angka positif tertinggi dan angka negatif terendah yang bisa dihasilkan dari 4-bit full adder yang dibuat? (10 poin)

Duis efficitur, magna at pulvinar vulputate, justo ipsum efficitur mauris, id blandit elit magna eget dui. 

## Analisis & Kesimpulan (20 poin)

**Analisis Keseluruhan:**  
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus quis nunc ac felis fringilla consequat ac nec elit. Integer pharetra sagittis libero, eget accumsan eros convallis non. Nullam id dui quis velit pulvinar maximus. Morbi ac magna nec mauris tristique cursus in sit amet mi. Mauris facilisis justo sit amet turpis consequat, at sollicitudin sapien euismod. Duis efficitur, magna at pulvinar vulputate, justo ipsum efficitur mauris, id blandit elit magna eget dui. Proin ultricies turpis ac lorem volutpat tincidunt. Integer porttitor orci id nisl tincidunt dapibus. Pellentesque ac tincidunt metus, non consectetur sem. Sed vulputate venenatis malesuada. Nam euismod, nisi at vulputate vehicula, enim arcu consectetur justo, id feugiat felis nisi ac felis.

**Kesimpulan: (minimal 3)**

- Lorem ipsum dolor sit amet, consectetur adipiscing elit.
- Lorem ipsum dolor sit amet, consectetur adipiscing elit.
- Lorem ipsum dolor sit amet, consectetur adipiscing elit.