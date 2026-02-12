# Tugas Tambahan - Karnaugh Map
Pembuat Soal: NZ

```
Nama    : Benianaus Kenneth Indarwan
NPM     : 2506539920
```

### Catatan
- Jika ada pertanyaan, silakan tanyakan di server Discord Digilab.
- Referensi tidak diperlukan untuk tugas tambahan kecuali disuruh.

## Ikuti skenario di bawah ini!

Akhirnya Magus bisa selamat dari kejaran K-Maph. Ternyata hal-hal yang dialami oleh Magus tidaklah biasa dan sangat mengagumkan, oleh karena itu Magus dan Anda ditunjuk untuk menjadi penanggung jawab inventaris artefak IME. Masalah baru pun muncul, yaitu Magus perlu membuat list penggunaan artefak. Anda selaku penanggung jawab juga harus membuat list penggunaan artefak lain. Berikut daftar artefak yang Anda urus.
- Last Prism (A), Meomwre (B), Terrarian \(C), dan Vortex Beater (D).

Namun ternyata ada diantara artefak yang Anda urus adalah palsu, oleh karena itu Ketua Departemen Magis Teknik memberikan Notes W, X, Y dan Z.

Aturan puzzle:

  * Kondisi sebuah **artefak palsu** selalu **SALAH**.
  * Kondisi sebuah **artefak asli** selalu **BENAR**.
  * Diketahui ada **satu atau dua palsu**. Kombinasi lain (0, 3, atau 4 tersangka) **tidak mungkin**. Gunakan **X (Don't Care)** untuk skenario yang tidak mungkin.

Kondisi mereka:

  * **Notes W :** "Terrarian dan Last Prism adalah asli."
  * **Notes X :** "Artefak palsu berjumlah genap."
  * **Notes Y :** "Terrasian asli, Vortex Beater palsu."
  * **Notes Z :** "Tepat hanya ada 1 artefak palsu."

## Jawab pertanyaan berikut!

### 1. Lengkapi tabel kebenaran untuk W, X, Y, dan Z (10 poin)

  * `1` berarti artefak (A, B, C, D) **asli**.
  * `0` berarti artefak (A, B, C, D) **palsu**.
  * Notes W, X, Y, Z bernilai `1` jika kondisi yang dijelaskan **benar**.
  * Notes W, X, Y, Z bernilai `0` jika kondisi yang dijelaskan **salah**.
  * Gunakan `X` untuk kondisi **Don't Care**.

---

### Tabel Kebenaran W
`Notes W :"Terrarian dan Last Prism adalah asli.`
| A   | B   | C   | D   | W   |
| --- | --- | --- | --- | --- |
| 0   | 0   | 0   | 0   | X   |
| 0   | 0   | 0   | 1   | X   |
| 0   | 0   | 1   | 0   | X   |
| 0   | 0   | 1   | 1   | 0   |
| 0   | 1   | 0   | 0   | X   |
| 0   | 1   | 0   | 1   | 0   |
| 0   | 1   | 1   | 0   | 0   |
| 0   | 1   | 1   | 1   | 0   |
| 1   | 0   | 0   | 0   | X   |
| 1   | 0   | 0   | 1   | 0   |
| 1   | 0   | 1   | 0   | 1   |
| 1   | 0   | 1   | 1   | 1   |
| 1   | 1   | 0   | 0   | 0   |
| 1   | 1   | 0   | 1   | 0   |
| 1   | 1   | 1   | 0   | 1   |
| 1   | 1   | 1   | 1   | 1   |

### Tabel Kebenaran X
`Notes X : "Artefak palsu berjumlah genap."`
| A   | B   | C   | D   | X   |
| --- | --- | --- | --- | --- |
| 0   | 0   | 0   | 0   | x   |
| 0   | 0   | 0   | 1   | x   |
| 0   | 0   | 1   | 0   | 0   |
| 0   | 0   | 1   | 1   | 1   |
| 0   | 1   | 0   | 0   | 0   |
| 0   | 1   | 0   | 1   | 1   |
| 0   | 1   | 1   | 0   | 1   |
| 0   | 1   | 1   | 1   | 0   |
| 1   | 0   | 0   | 0   | X   |
| 1   | 0   | 0   | 1   | 1   |
| 1   | 0   | 1   | 0   | 1   |
| 1   | 0   | 1   | 1   | 0   |
| 1   | 1   | 0   | 0   | 1   |
| 1   | 1   | 0   | 1   | 0   |
| 1   | 1   | 1   | 0   | 0   |
| 1   | 1   | 1   | 1   | 0   |

### Tabel Kebenaran Y
`Notes Y : "Terrasian asli, Vortex Beater palsu."`
| A   | B   | C   | D   | Y   |
| --- | --- | --- | --- | --- |
| 0   | 0   | 0   | 0   | X   |
| 0   | 0   | 0   | 1   | X   |
| 0   | 0   | 1   | 0   | 1   |
| 0   | 0   | 1   | 1   | 0   |
| 0   | 1   | 0   | 0   | 0   |
| 0   | 1   | 0   | 1   | 0   |
| 0   | 1   | 1   | 0   | 1   |
| 0   | 1   | 1   | 1   | 0   |
| 1   | 0   | 0   | 0   | X   |
| 1   | 0   | 0   | 1   | 0   |
| 1   | 0   | 1   | 0   | 1   |
| 1   | 0   | 1   | 1   | 0   |
| 1   | 1   | 0   | 0   | 0   |
| 1   | 1   | 0   | 1   | 0   |
| 1   | 1   | 1   | 0   | 1   |
| 1   | 1   | 1   | 1   | 0   |

### Tabel Kebenaran Z
`Notes Z : "Tepat hanya ada 1 artefak palsu."`
| A   | B   | C   | D   | Z   |
| --- | --- | --- | --- | --- |
| 0   | 0   | 0   | 0   | 0   |
| 0   | 0   | 0   | 1   | 0   |
| 0   | 0   | 1   | 0   | 0   |
| 0   | 0   | 1   | 1   | 0   |
| 0   | 1   | 0   | 0   | 0   |
| 0   | 1   | 0   | 1   | 0   |
| 0   | 1   | 1   | 0   | 0   |
| 0   | 1   | 1   | 1   | 1   |
| 1   | 0   | 0   | 0   | 0   |
| 1   | 0   | 0   | 1   | 0   |
| 1   | 0   | 1   | 0   | 0   |
| 1   | 0   | 1   | 1   | 0   |
| 1   | 1   | 0   | 0   | 0   |
| 1   | 1   | 0   | 1   | 1   |
| 1   | 1   | 1   | 0   | 1   |
| 1   | 1   | 1   | 1   | 0   |

### 2. Buat Karnaugh Map untuk setiap output pernyataan dan temukan fungsi boolean sederhananya (10 poin)

#### Karnaugh Map untuk W
Gambar K-MAP :
![image](https://hackmd.io/_uploads/SJfOmcU2eg.png)

Fungsi W :
W = ACD'+AB'C

#### Karnaugh Map untuk X
Gambar K-MAP :
![image](https://hackmd.io/_uploads/H11T758nxe.png)
Fungsi X :
X = AC'D'+AB'C'+A'C'D+A'B'D

#### Karnaugh Map untuk Y
Gambar K-MAP :
![image](https://hackmd.io/_uploads/rkG149I2ee.png)
Fungsi Y :
Y = AC'D'+AB'C'+A'C'D+A'B'D

#### Karnaugh Map untuk Z
Gambar K-MAP :
![image](https://hackmd.io/_uploads/S1K1V5Ihlx.png)
Fungsi Z :
Z = ABC+BCD

### 3. Sebuah Notes KONSISTEN jika artefak dan Notes cocok (artefak asli & Notes benar, atau artefak palsu & Notes salah). Lengkapi tabel kebenaran dan buat fungsi boolean untuk konsistensi! (10 poin)

| A   | W   | Consistent1 |
| --- | --- | ----------- |
| 0   | 0   | 1           |
| 0   | 1   | 0           |
| 1   | 0   | 0           |
| 1   | 1   | 1           |

```
Consistent1 = AW+A'W'
```

| B   | X   | Consistent2 |
| --- | --- | ----------- |
| 0   | 0   | 1           |
| 0   | 1   | 0           |
| 1   | 0   | 0           |
| 1   | 1   | 1           |

```
Consistent2 = BX+B'X'
```

| C   | Y   | Consistent3 |
| --- | --- | ----------- |
| 0   | 0   | 1           |
| 0   | 1   | 0           |
| 1   | 0   | 0           |
| 1   | 1   | 1           |

```
Consistent3 = CY+C'Y'
```

| D   | Z   | Consistent4 |
| --- | --- | ----------- |
| 0   | 0   | 1           |
| 0   | 1   | 0           |
| 1   | 0   | 0           |
| 1   | 1   | 1           |

```
Consistent4 = DZ+D'Z'
```

### 4. Artefak mana saja yang palsu? (10 poin)
`Petunjuk: Solusi adalah kombinasi artefak di mana SEMUA notes konsisten (Konsisten1, Konsisten2, Konsisten3, dan Konsisten4 semuanya 1). Temukan kombinasi valid artefak asli dan palsu yang membuat hal ini terjadi.`

Berikut adalah Truth Table yang sudah disortir untuk setiap keadaan konsisten dengan index.

| Index | A | W | Consistent1 |
|---|---|---|---|
| 3 | 0 | 0 | 1 |
| 5 | 0 | 0 | 1 |
| 6 | 0 | 0 | 1 |
| 7 | 0 | 0 | 1 |
| 10 | 1 | 1 | 1 |
| 14 | 1 | 1 | 1 |
| 15 | 1 | 1 | 1 |

| Index | B | X | Consistent2 |
|---|---|---|---|
| 2 | 0 | 0 | 1 |
| 5 | 1 | 1 | 1 |
| 6 | 1 | 1 | 1 |
| 11 | 0 | 0 | 1 |
| 12 | 1 | 1 | 1 |

| Index | C | Y | Consistent3 |
|---|---|---|---|
| 2 | 1 | 1 | 1 |
| 4 | 0 | 0 | 1 |
| 5 | 0 | 0 | 1 |
| 6 | 1 | 1 | 1 |
| 9 | 0 | 0 | 1 |
| 10 | 1 | 1 | 1 |
| 12 | 0 | 0 | 1 |
| 13 | 0 | 0 | 1 |
| 14 | 1 | 1 | 1 |

| Index | D | Z | Consistent4 |
|---|---|---|---|
| 0 | 0 | 0 | 1 |
| 2 | 0 | 0 | 1 |
| 4 | 0 | 0 | 1 |
| 6 | 0 | 0 | 1 |
| 7 | 1 | 1 | 1 |
| 8 | 0 | 0 | 1 |
| 10 | 0 | 0 | 1 |
| 12 | 0 | 0 | 1 |
| 13 | 1 | 1 | 1 |

Artefak yang konsisten pada setiap fungsi adalah untuk index 6 (0110). 

Maka, artefak yang palsu adalah artefak `A (Last Prism)` dan `D (Vortex Beater)`


### 5. Buat rangkaian Tinkercad berdasarkan fungsi boolean yang Anda temukan! (40 poin)

Persyaratan:
1. Gunakan LED untuk setiap variabel: A, B, C, D, W, X, Y, Z, Konsisten1, Konsisten2, Konsisten3, dan Konsisten4.
2. LED merah untuk A, B, C, D (input artefak).
3. LED hijau untuk W, X, Y, Z (output notes).
4. LED biru untuk Konsisten1, Konsisten2, Konsisten3, dan Konsisten4 (output konsistensi).
5. Gunakan Arduino sebagai sumber daya.
6. Pastikan rangkaian dirancang rapi.
7. Gunakan Notes tool untuk memberi label SETIAP LED dengan nama variabel.
8. Gunakan DIP Switch 4 posisi untuk mewakili input A, B, C, D.
9. Gunakan hanya gerbang logika dasar: AND, OR, NOT.

Screenshot :
![image](https://hackmd.io/_uploads/BkTmmqLhll.png)


### 6. Buat analisis dan kesimpulan untuk tugas ini. Analisis dalam bentuk paragraf, kesimpulan dalam poin! (20 poin)

Link Tinkercad:

https://www.tinkercad.com/things/8HPddcPGetD-tutamdsd3benianaus-kenneth-indarwan2506539920?sharecode=oWNpwdAdv3PVMZZv_MsqYm26OxTaEAVWgjakMbiIebY

Analisis:

Hasil dari tugas ini merupakan hasil kombinasi dari 4 set variabel yang berbeda, yaitu 4 variabel ABCD, 4 variabel hasil WXYZ, dan 4 variabel yang menunjukkan konsistensi (Consistent1, Consistent2, Consistent3, Consistent4). Fungsi-fungsi ini pertama kali disederhanakan dengan menggunakan K-MAP berdasarkan Truth Tables yang telah dibuat. Kemudian, berdasarkan ketentuan-ketentuan lainnya, variabel akan dikombinasikan kembali dengan variabel lain yang juga akan membentuk fungsi baru dan variabel baru. Semua variabel ini berhubungan dan dikontrol hanya dari 4 variabel input ABCD. Jadi, walaupun ada total 12 variabel yang dipakai, hanya 4 variabel ABCD di awal yang dapat dikontrol secara binary.  

Berdasarkan hasil tersebut, maka kita dapat membuat suatu rangkaian berdasarkan fungsi-fungsi yang ditemukan dan dengan logic gates sederhana (NOT, AND, OR). Tentunya dengan keterbatasan tersebut, rangkaian yang dibuat menjadi kompleks dan memerlukan waktu untuk dibuat.

Kesimpulan:

- Penggunaan K-MAP mempermudah penyederhanaan fungsi
- Variabel hasil dapat digunakan kembali bersama dengan variabel awal untuk membuat fungsi baru dengan hasil baru (Fungsi Consistent)
- Fungsi consistent merupakan bentuk contoh dari XNOR, dimana ketika kedua input sama baru akan menghasilkan 1.
- Fungsi XNOR dapat dibuat dengan logic gates sederhana sesuai dengan DeMorgan's Theorem. (F=AB'+A'B)