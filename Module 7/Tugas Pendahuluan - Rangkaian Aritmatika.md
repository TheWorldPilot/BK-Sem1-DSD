---
title: Tugas Pendahuluan - Rangkaian Aritmatika

---

# Tugas Pendahuluan - Rangkaian Aritmatika
`Pembuat Soal : NA`
```
Nama  : Calamitas[Ganti dengan nama Anda]
NPM   : 2346000[Ganti dengan NPM Anda]
```

## Teori (40 poin)

### 1. Jelaskan apa itu half adder, half subtractor, full adder, dan full subtractor! Sertakan truth table dan gambar rangkaian masing-masing. (10 poin)

---

[your answer here]

### Referensi:

- Contoh Situs [Online]. Available: https://www.myWebsite.com/ilovedigilab/. [Diakses: 25-Agustus-2024]

---

### 2. Jelaskan perbedaan antara half adder dan full adder! (10 poin)

[your answer here]

### Referensi:

- Contoh Situs [Online]. Available: https://www.myWebsite.com/ilovedigilab/. [Diakses: 25-Agustus-2024]

---

### 3. Jelaskan perbedaan antara half subtractor dan full subtractor! (10 poin)

[your answer here]

### Referensi:

- Contoh Situs [Online]. Available: https://www.myWebsite.com/ilovedigilab/. [Diakses: 25-Agustus-2024]

### 4. Jelaskan perbedaan antara signed magnitude dan 2’s complement! (10 poin)

[your answer here]

### Referensi:

- Contoh Situs [Online]. Available: https://www.myWebsite.com/ilovedigilab/. [Diakses: 25-Agustus-2024]

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
| --- | --- | --- | --- | --- | --- | --- | --|
| 0 | 0 | 0 | 0 | ? | ? | ? | ? |
| 0 | 0 | 0 | 1 | ? | ? | ? | ? |
| 0 | 0 | 1 | 0 | ? | ? | ? | ? |
| 0 | 0 | 1 | 1 | ? | ? | ? | ? |
| 0 | 1 | 0 | 0 | ? | ? | ? | ? |
| 0 | 1 | 0 | 1 | ? | ? | ? | ? |
| 0 | 1 | 1 | 0 | ? | ? | ? | ? |
| 0 | 1 | 1 | 1 | ? | ? | ? | ? |
| 1 | 0 | 0 | 0 | ? | ? | ? | ? |
| 1 | 0 | 0 | 1 | X | X | X | X |
| 1 | 0 | 1 | 0 | X | X | X | X |
| 1 | 0 | 1 | 1 | X | X | X | X |
| 1 | 1 | 0 | 0 | X | X | X | X |
| 1 | 1 | 0 | 1 | X | X | X | X |
| 1 | 1 | 1 | 0 | X | X | X | X |
| 1 | 1 | 1 | 1 | X | X | X | X |

### KMAP untuk D3:  
![Masukkan screenshot KMAP](public_image_link)

D3 = ...

### KMAP untuk D2:  
![Masukkan screenshot KMAP](public_image_link)

D2 = ...

### KMAP untuk D1:  
![Masukkan screenshot KMAP](public_image_link)

D1 = ...

### KMAP untuk D0:  
![Masukkan screenshot KMAP](public_image_link)

D0 = ...

### Screenshot:  
![Masukkan screenshot di sini](public_image_link)

Namun, Prof. Alden memberikan suatu pendekatan berbeda yaitu menggunakan 4-bit Full Adder (7483). Prof. Alden memberikan petunjuk bahwa 2’s complement dapat dicapai dengan **INVERT** semua bit input dan kemudian **DITAMBAH 1** pada hasilnya. Dengan petunjuk ini, Magus segera mengembangkan rangkaian lain berdasarkan pendekatan tersebut. **(15 poin)**

### Screenshot:  
![Masukkan screenshot di sini](public_image_link)

### Analisis:
Jelaskan perbedaan serta kelebihan dan kekurangan antara pendekatan KMAP dan pendekatan Full Adder! **(15 poin)**

[your answer here]