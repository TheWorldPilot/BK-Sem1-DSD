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
| 0   | 0   | 0   | 0   | ?   |
| 0   | 0   | 0   | 1   | ?   |
| 0   | 0   | 1   | 0   | ?   |
| 0   | 0   | 1   | 1   | ?   |
| 0   | 1   | 0   | 0   | ?   |
| 0   | 1   | 0   | 1   | ?   |
| 0   | 1   | 1   | 0   | ?   |
| 0   | 1   | 1   | 1   | ?   |
| 1   | 0   | 0   | 0   | ?   |
| 1   | 0   | 0   | 1   | ?   |
| 1   | 0   | 1   | 0   | ?   |
| 1   | 0   | 1   | 1   | ?   |
| 1   | 1   | 0   | 0   | ?   |
| 1   | 1   | 0   | 1   | ?   |
| 1   | 1   | 1   | 0   | ?   |
| 1   | 1   | 1   | 1   | ?   |

### Tabel Kebenaran X
`Notes X : "Artefak palsu berjumlah genap."`
| A   | B   | C   | D   | X   |
| --- | --- | --- | --- | --- |
| 0   | 0   | 0   | 0   | ?   |
| 0   | 0   | 0   | 1   | ?   |
| 0   | 0   | 1   | 0   | ?   |
| 0   | 0   | 1   | 1   | ?   |
| 0   | 1   | 0   | 0   | ?   |
| 0   | 1   | 0   | 1   | ?   |
| 0   | 1   | 1   | 0   | ?   |
| 0   | 1   | 1   | 1   | ?   |
| 1   | 0   | 0   | 0   | ?   |
| 1   | 0   | 0   | 1   | ?   |
| 1   | 0   | 1   | 0   | ?   |
| 1   | 0   | 1   | 1   | ?   |
| 1   | 1   | 0   | 0   | ?   |
| 1   | 1   | 0   | 1   | ?   |
| 1   | 1   | 1   | 0   | ?   |
| 1   | 1   | 1   | 1   | ?   |

### Tabel Kebenaran Y
`Notes Y : "Terrasian asli, Vortex Beater palsu."`
| A   | B   | C   | D   | Y   |
| --- | --- | --- | --- | --- |
| 0   | 0   | 0   | 0   | ?   |
| 0   | 0   | 0   | 1   | ?   |
| 0   | 0   | 1   | 0   | ?   |
| 0   | 0   | 1   | 1   | ?   |
| 0   | 1   | 0   | 0   | ?   |
| 0   | 1   | 0   | 1   | ?   |
| 0   | 1   | 1   | 0   | ?   |
| 0   | 1   | 1   | 1   | ?   |
| 1   | 0   | 0   | 0   | ?   |
| 1   | 0   | 0   | 1   | ?   |
| 1   | 0   | 1   | 0   | ?   |
| 1   | 0   | 1   | 1   | ?   |
| 1   | 1   | 0   | 0   | ?   |
| 1   | 1   | 0   | 1   | ?   |
| 1   | 1   | 1   | 0   | ?   |
| 1   | 1   | 1   | 1   | ?   |

### Tabel Kebenaran Z
`Notes Z : "Tepat hanya ada 1 artefak palsu."`
| A   | B   | C   | D   | Z   |
| --- | --- | --- | --- | --- |
| 0   | 0   | 0   | 0   | ?   |
| 0   | 0   | 0   | 1   | ?   |
| 0   | 0   | 1   | 0   | ?   |
| 0   | 0   | 1   | 1   | ?   |
| 0   | 1   | 0   | 0   | ?   |
| 0   | 1   | 0   | 1   | ?   |
| 0   | 1   | 1   | 0   | ?   |
| 0   | 1   | 1   | 1   | ?   |
| 1   | 0   | 0   | 0   | ?   |
| 1   | 0   | 0   | 1   | ?   |
| 1   | 0   | 1   | 0   | ?   |
| 1   | 0   | 1   | 1   | ?   |
| 1   | 1   | 0   | 0   | ?   |
| 1   | 1   | 0   | 1   | ?   |
| 1   | 1   | 1   | 0   | ?   |
| 1   | 1   | 1   | 1   | ?   |

### 2. Buat Karnaugh Map untuk setiap output pernyataan dan temukan fungsi boolean sederhananya (10 poin)

#### Karnaugh Map untuk W
Gambar K-MAP :
![Contoh aja gess](https://hackmd.io/_uploads/Hkt0mDCsgl.png)
Fungsi W :
W = 

#### Karnaugh Map untuk X
Gambar K-MAP :
![Contoh aja gess](https://hackmd.io/_uploads/Hkt0mDCsgl.png)
Fungsi X :
X = 

#### Karnaugh Map untuk Y
Gambar K-MAP :
![Contoh aja gess](https://hackmd.io/_uploads/Hkt0mDCsgl.png)
Fungsi Y :
Y = 

#### Karnaugh Map untuk Z
Gambar K-MAP :
![Contoh aja gess](https://hackmd.io/_uploads/Hkt0mDCsgl.png)
Fungsi Z :
Z = 

### 3. Sebuah Notes KONSISTEN jika artefak dan Notes cocok (artefak asli & Notes benar, atau artefak palsu & Notes salah). Lengkapi tabel kebenaran dan buat fungsi boolean untuk konsistensi! (10 poin)

| A   | W   | Consistent1 |
| --- | --- | ----------- |
| 0   | 0   | ?           |
| 0   | 1   | ?           |
| 1   | 0   | ?           |
| 1   | 1   | ?           |

```
Consistent1 =
```

| B   | X   | Consistent2 |
| --- | --- | ----------- |
| 0   | 0   | ?           |
| 0   | 1   | ?           |
| 1   | 0   | ?           |
| 1   | 1   | ?           |

```
Consistent2 =
```

| C   | Y   | Consistent3 |
| --- | --- | ----------- |
| 0   | 0   | ?           |
| 0   | 1   | ?           |
| 1   | 0   | ?           |
| 1   | 1   | ?           |

```
Consistent3 =
```

| D   | Z   | Consistent4 |
| --- | --- | ----------- |
| 0   | 0   | ?           |
| 0   | 1   | ?           |
| 1   | 0   | ?           |
| 1   | 1   | ?           |

```
Consistent4 =
```

### 4. Artefak mana saja yang palsu? (10 poin)
`Petunjuk: Solusi adalah kombinasi artefak di mana SEMUA notes konsisten (Konsisten1, Konsisten2, Konsisten3, dan Konsisten4 semuanya 1). Temukan kombinasi valid artefak asli dan palsu yang membuat hal ini terjadi.`

[Jawaban kalian disini]

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
![Ganti dengan rangkaian tinkerCAD kalian](https://hackmd.io/_uploads/rJsFvPCseg.gif)


### 6. Buat analisis dan kesimpulan untuk tugas ini. Analisis dalam bentuk paragraf, kesimpulan dalam poin! (20 poin)

Link Tinkercad:

[jawabanmu di sini]

Analisis:

[jawabanmu di sini]

Kesimpulan:

[jawabanmu di sini]