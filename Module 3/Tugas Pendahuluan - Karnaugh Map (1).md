# Tugas Pendahuluan - Karnaugh Map

Penulis Soal: NZ

```
Nama: Stefanus Josenbergh [Ganti dengan nama kalian]
NPM: 220901293402 [Ganti dengan NPM kalian]
```

### Catatan

  - Jika ada pertanyaan yang kurang jelas, silahkan bertanya di server Discord Digilab.
  - Referensi harus dalam format IEEE (Anda dapat menggunakan [https://www.mybib.com/tools/ieee-citation-generator](https://www.mybib.com/tools/ieee-citation-generator) untuk mempermudah). Sertakan minimal 2 referensi.

## **Teori (40 poin)**

## 1. Apa itu K-MAP? Apa saja kegunaannya? (10 poin)

[Jawaban Anda]

Referensi :
- [1]Author, “Example,” Website_Name, Jun. 22, 2022. https://ilovedigilab.example.url (accessed May 15, 2024).

## 2. Kapan kita menggunakan K-MAP dibandingkan dengan metode aljabar boolean lainnya? (5 poin)

[Jawaban Anda]

Referensi :
- [1]Author, “Example,” Website_Name, Jun. 22, 2022. https://ilovedigilab.example.url (accessed May 15, 2024).

## 3. Jelaskan format kotak-kotak K-MAP dan aturan untuk mengelompokkannya (mana yang bisa dikelompokkan dan mana yang tidak)! (15 poin)

[Jawaban Anda]

Referensi :
- [1]Author, “Example,” Website_Name, Jun. 22, 2022. https://ilovedigilab.example.url (accessed May 15, 2024).

## 4. Apa arti dari kondisi X/Don't Care? Apa perbedaan antara X dan 0? (10 poin)

[Jawaban Anda]

Referensi :
- [1]Author, “Example,” Website_Name, Jun. 22, 2022. https://ilovedigilab.example.url (accessed May 15, 2024).

## Pre-CS (60 poin)

Setelah keluar dari labirin, Magus menjumpai sebuah buku, tiba-tiba buku itu terbuka dan dari dalamnya muncul roh abstrak bernama K-Maph.
Roh itu bergemuruh:

`Aku adalah ekspresi rumit yang tak terbaca! Jika kau tak bisa menyederhanakan aku, aku akan menggandakan diriku menjadi 1024 versi dan memenuhi seluruh kampus!`


Peta misterius muncul seketika di lantai, membentuk kotak-kotak Karnaugh Map. Magus harus menyusun blok demi blok untuk menyederhanakan mantra Boolean itu. Setiap penyederhanaan membuat roh itu semakin lemah… hingga akhirnya ia bisa disegel kembali.

* Orbium, Sigil, Aurum tidak tersedia untuk dipakai. Resonator tersedia. 
* Orbium, Sigil, Resonator tidak tersedia. Aurum tersedia. 
* Orbium, Resonator, dan Aurum tidak tersedia. Sigil tersedia. 
* Sigil, Resonator, dan Aurum tidak tersedia. Orbium tersedia. 
* Orbium dan Aurum tidak tersedia. Sigil dan Resonator tersedia. 
* Orbium dan Resonator tidak tersedia. Sigil dan Aurum tersedia. 
* Sigil dan Aurum tidak tersedia. Orbium dan Resonator tersedia. 
* Sigil dan Resonator tidak tersedia. Orbium dan Aurum tersedia. 
* Aurum dan Resonator tidak tersedia. Orbium dan Sigil tersedia. 
* Aurum tidak tersedia. Orbium, Sigil, dan Resonator tersedia. 
* Resonator tidak tersedia. Orbium, Sigil, dan Aurum tersedia. 
* Semua artefak tersedia.

Pernyataan-pernyataan diatas perlu Magus Sederhanakan dalam waktu 1 hari dan menulis aljabar Boolean untuk setiap kondisi akan menciptakan sirkuit yang rumit yang membutuhkan banyak gerbang logika. Untungnya Magus punya Anda, sebuah teman extradimensional. Bantulah Magus menyederhanakan pernyataan-pernyataan diatas. Gunakan K-MAP untuk mendapatkan ekspresi Boolean sesederhana mungkin yang merepresentasikan fungsi yang lebih sederhana dan melemahkan roh K-Maph.

### Truth Table

`Petunjuk: Ketika artefak tersedia, nilainya TINGGI/1. Ketika artefak tidak tersedia, nilainya RENDAH/0`
`Contoh: Orbium, Sigil, Aurum tidak tersedia untuk dipakai. Resonator tersedia. Ekspresi Boolean: O'S'A'R`
| O   | S   | A   | R   | OUTPUT |
| --- | --- | --- | --- | --- |
| 0   | 0   | 0   | 0   |     |
| 0   | 0   | 0   | 1   |     |
| 0   | 0   | 1   | 0   |     |
| 0   | 0   | 1   | 1   |     |
| 0   | 1   | 0   | 0   |     |
| 0   | 1   | 0   | 1   |     |
| 0   | 1   | 1   | 0   |     |
| 0   | 1   | 1   | 1   |     |
| 1   | 0   | 0   | 0   |     |
| 1   | 0   | 0   | 1   |     |
| 1   | 0   | 1   | 0   |     |
| 1   | 0   | 1   | 1   |     |
| 1   | 1   | 0   | 0   |     |
| 1   | 1   | 0   | 1   |     |
| 1   | 1   | 1   | 0   |     |
| 1   | 1   | 1   | 1   |     |

### Fungsi Boolean berdasarkan Truth Table (Sebelum penyederhanaan K-MAP)

F(O,S,A,R) = ?

### K-MAP

| OS\\AR | 00  | 01  | 11  | 10  |
| ----- | --- | --- | --- | --- |
| 00    |     |     |     |     |
| 01    |     |     |     |     |
| 11    |     |     |     |     |
| 10    |     |     |     |     |

### Peta Karnaugh yang Sudah Diselesaikan (Dengan pengelompokan)

### Fungsi Boolean (Setelah penyederhanaan K-MAP)

F = ?

### Buatlah rangkaiannya di Tinkercad dan tangkap layar (screenshot) kombinasi yang menyalakan LED\!

| O   | S   | A   | R   | Output |
| --- | --- | --- | --- | ------------------------------------------------------- |
| X   | X   | X   | X   |  |

### Link Tinkercad: