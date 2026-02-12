---
title: Tugas Pendahuluan - Karnaugh Map

---

# Tugas Pendahuluan - Karnaugh Map

Penulis Soal: NZ

```
Nama: Benianaus Kenneth Indarwan
NPM: 2506539920
```

### Catatan

  - Jika ada pertanyaan yang kurang jelas, silahkan bertanya di server Discord Digilab.
  - Referensi harus dalam format IEEE (Anda dapat menggunakan [https://www.mybib.com/tools/ieee-citation-generator](https://www.mybib.com/tools/ieee-citation-generator) untuk mempermudah). Sertakan minimal 2 referensi.

## **Teori (40 poin)**

## 1. Apa itu K-MAP? Apa saja kegunaannya? (10 poin)

K-MAP atau Karnaugh Map adalah sebuah metode untuk menyederhanakan persamaan boolean dengan menggunakan visualisasi, tanpa rumus-rumus kompleks. Kegunaannya adalah untuk menyederhanakan persamaan boolean dengan menggunakan visualisasi data tabel. Visualisasi data ini yang kemudian digunakan untuk mengelompokan data dan mendapatkan fungsi baru yang lebih sederhana.

Referensi :
- [1]J.-P. E. K. Team Hari Ini, “Memahami Peta Karnaugh (1),” JatiTech - Platform Edukasi Kolaboratif, Hari Ini, 2013. https://jati.itda.ac.id/2013/06/memahami-peta-karnaugh-1.html (accessed Sep. 21, 2025).
- [2]R. Sheldon, “What is Karnaugh map (K-map)? - Definition from WhatIs.com,” WhatIs.com, Aug. 2022. https://www.techtarget.com/whatis/definition/Karnaugh-map-K-map (accessed Sep. 21, 2025).

## 2. Kapan kita menggunakan K-MAP dibandingkan dengan metode aljabar boolean lainnya? (5 poin)

K-MAP bisa digunakan ketika terdapat 2-4 variabel. 1 Variabel tidak dapat dibuat K-MAPnya dan diatas 4 variabel juga rumit untuk membuat K-MAPnya. K-MAP juga bisa digunakan untuk menyederhanakan fungsi POS dan SOP.

Referensi :
- [1]GeeksforGeeks, “Applications of Karnaugh map,” GeeksforGeeks, Jul. 17, 2024. https://www.geeksforgeeks.org/electronics-engineering/applications-of-karnaugh-map/ (accessed Sep. 21, 2025).
- [2]Anonymous, “Introduction of K-Map (Karnaugh Map) | GATE Notes,” BYJUS. https://byjus.com/gate/introduction-of-k-map-karnaugh-map-notes/ (accessed Sep. 21, 2025).

## 3. Jelaskan format kotak-kotak K-MAP dan aturan untuk mengelompokkannya (mana yang bisa dikelompokkan dan mana yang tidak)! (15 poin)

Format K-MAP ada untuk 2 variabel, 3 variabel, 4 variabel. Untuk 2 variabel dibuat dalam bentuk kotak 2x2. Untuk 3 variabel dibuat dalam bentuk 2x4. Dan untuk 4 variabel dibuat dalam bentuk 4x4. Untuk aturan pengelompokan, perlu diketahui bahwa pada K-MAP 3 variabel, ujung sebelah kiri dan kanan bisa dihubungkan, dan pada K-MAP 4 variabel, keempat pojok dapat terhubung, begitu juga dengan sisi atas dan bawah, serta kiri kan kanan. Aturan pengelompokannya adalah untuk mengelompokan setiap instansi 1 dengan jumlah 2<sup>n</sup>. Dilakukan pengelompokan dengan jumlah sedikit mungkin dan mengcover semua instansi 1. 

Referensi :
- [1]Sneha H.L, “The Karnaugh Map Boolean Algebraic Simplification Technique,” Allaboutcircuits.com, Jun. 24, 2016. https://www.allaboutcircuits.com/technical-articles/karnaugh-map-boolean-algebraic-simplification-technique/ (accessed Sep. 21, 2025).
- [2]adi, “Tutorial Karnaugh Map (K-Map) Beserta Contohnya,” bisaioti.com, Mar. 17, 2025. https://bisaioti.com/tutorial-karnaugh-map-k-map-beserta-contohnya/ (accessed Sep. 21, 2025).

## 4. Apa arti dari kondisi X/Don't Care? Apa perbedaan antara X dan 0? (10 poin)

Kondisi X/Don't Care Condition adalah konsep un, dimana menyederhanakan rangkaian, dimana kita bisa menganggap satu kotak berisi 0/1 sesuai keadaan yang diperlukan untuk menyederhanakan rangkaian. Contohnya, ketika berhubungan dengan BCD, ada beberapa bit yang diluar range sehingga tidak peduli apa isinya. Perbedaan X dan 0 adalah, `0` adalah bit yang benar-benar nilainya 0, sedangkan `X` dapat berisi 0/1 tergantung situasi yang diperlukan

Referensi :
- [1]Anonymous, “Don’t Care Cells in the Karnaugh Map | Karnaugh Mapping | Electronics Textbook,” www.allaboutcircuits.com. https://www.allaboutcircuits.com/textbook/digital/chpt-8/dont-care-cells-karnaugh-map/ (accessed Sep. 21, 2025).
- [2]GeeksforGeeks, “Don’t Care (X) Conditions in KMaps,” GeeksforGeeks, Oct. 17, 2019. https://www.geeksforgeeks.org/digital-logic/dont-care-x-conditions-in-k-maps/ (accessed Sep. 21, 2025).

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
| --- | --- | --- | --- | ---- |
| 0   | 0   | 0   | 0   | 0    |
| 0   | 0   | 0   | 1   | 1    |
| 0   | 0   | 1   | 0   | 1    |
| 0   | 0   | 1   | 1   | 0    |
| 0   | 1   | 0   | 0   | 1    |
| 0   | 1   | 0   | 1   | 1    |
| 0   | 1   | 1   | 0   | 1    |
| 0   | 1   | 1   | 1   | 0    |
| 1   | 0   | 0   | 0   | 1    |
| 1   | 0   | 0   | 1   | 1    |
| 1   | 0   | 1   | 0   | 0    |
| 1   | 0   | 1   | 1   | 0    |
| 1   | 1   | 0   | 0   | 1    |
| 1   | 1   | 0   | 1   | 1    |
| 1   | 1   | 1   | 0   | 1    |
| 1   | 1   | 1   | 1   | 1    |

### Fungsi Boolean berdasarkan Truth Table (Sebelum penyederhanaan K-MAP)

F(O,S,A,R) = (O'S'A'R)+(O'S'AR')+(O'SA'R')+(O'SA'R)+(O'SAR')+(OS'A'R')+(OS'A'R)+(OSA'R')+(OSA'R)+(OSAR')+(OSAR)

### K-MAP

| OS\\AR | 00  | 01   | 11   | 10   |
| ----- | ---- | ---- | ---- | ---- |
| 00    | 0    | 1    | 0    | 1    |
| 01    | 1    | 1    | 0    | 1    |
| 11    | 1    | 1    | 1    | 1    |
| 10    | 1    | 1    | 0    | 0    |

### Peta Karnaugh yang Sudah Diselesaikan (Dengan pengelompokan)

![image](https://hackmd.io/_uploads/HkK5nY6iel.png)

### Fungsi Boolean (Setelah penyederhanaan K-MAP)

F = O'A + OSA + A'R + SA' + OS'A'

### Buatlah rangkaiannya di Tinkercad dan tangkap layar (screenshot) kombinasi yang menyalakan LED\!

| O   | S   | A   | R   | OUTPUT |
| --- | --- | --- | --- | ---- |
| 0   | 0   | 0   | 1   |![image](https://hackmd.io/_uploads/r1cBc96ogx.png)|
| 0   | 0   | 1   | 0   |![image](https://hackmd.io/_uploads/BJgL596jxx.png)|
| 0   | 1   | 0   | 0   |![image](https://hackmd.io/_uploads/H1o85c6sge.png)|
| 0   | 1   | 0   | 1   |![image](https://hackmd.io/_uploads/rJzD9cpsxl.png)|
| 0   | 1   | 1   | 0   |![image](https://hackmd.io/_uploads/SJwvc56jeg.png)|
| 1   | 0   | 0   | 0   |![image](https://hackmd.io/_uploads/HkQdccpjgl.png)|
| 1   | 0   | 0   | 1   |![image](https://hackmd.io/_uploads/rkud956sxg.png)|
| 1   | 1   | 0   | 0   |![image](https://hackmd.io/_uploads/HJ1K9q6sel.png)|
| 1   | 1   | 0   | 1   |![image](https://hackmd.io/_uploads/rkvK99pjgg.png)|
| 1   | 1   | 1   | 0   |![image](https://hackmd.io/_uploads/ByF95cpoel.png)|
| 1   | 1   | 1   | 1   |![image](https://hackmd.io/_uploads/S1Gq9qaogx.png)|

### Link Tinkercad:
https://www.tinkercad.com/things/2vMbBZLVdPC-tpdsd3benianaus-kenneth-indarwan2506539920?sharecode=BSR5TVcRlXJh2g4CIBZRYcv-BFz4Qf-0YRWQkzhJBwM
