# Case Study - Decoder & Encoder

> Pembuat Soal: NZ

```
Name    : Firefly
NPM     : 1234567890
```

## Catatan
- Jika ada pertanyaan, silakan tanya asisten lab yang hadir (selama sesi) atau di Discord (di luar waktu sesi). 
- Referensi tidak diperlukan untuk studi kasus ini.  

## Scenario (40 poin)
Hari tenang tak selamanya ada, Magus mendapatkan tugas dari Prof.Vergil untuk membuat sebuah pemecah kode atau memetakan sebuah pesan yang ter-enkripsi dengan angka-angka, lalu beri bobot setiap angka yang direpresentasikan. Bantulah Magus merancang alat ini. Prof.Vergil pun memberi clue sebagai berikut.

Rancangan memiliki 4 input (A,B,C,D) yang masing masing merepresentasikan:
- A: Golden Ratio 
- B: Logaritmik 
- C: Percentile 
- D: Round Number 

Ketentuan dari rangkaian ini adalah:
- Decoder memiliki lebar 4 bit dengan angka maksimal adalah angka 9, dengan output dalam bentuk BCD.
- Golden Ratio memiliki bobot sebesar 4 poin
- Logaritmik dan Percentile masing-masing memiliki bobot sebesar 2 poin
- Round Number memiliki bobot sebesar 1 poin

Buatlah custom decoder untuk membantu Magus yang sesuai dengan spesifikasi di atas

### Truth Table (10 Poin)
| A   | B   | C   | D   | D3  | D2  | D1  | D0  |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 0   | 0   | 0   | 0   |     |     |     |     |
| 0   | 0   | 0   | 1   |     |     |     |     |
| 0   | 0   | 1   | 0   |     |     |     |     |
| 0   | 0   | 1   | 1   |     |     |     |     |
| 0   | 1   | 0   | 0   |     |     |     |     |
| 0   | 1   | 0   | 1   |     |     |     |     |
| 0   | 1   | 1   | 0   |     |     |     |     |
| 0   | 1   | 1   | 1   |     |     |     |     |
| 1   | 0   | 0   | 0   |     |     |     |     |
| 1   | 0   | 0   | 1   |     |     |     |     |
| 1   | 0   | 1   | 0   |     |     |     |     |
| 1   | 0   | 1   | 1   |     |     |     |     |
| 1   | 1   | 0   | 0   |     |     |     |     |
| 1   | 1   | 0   | 1   |     |     |     |     |
| 1   | 1   | 1   | 0   |     |     |     |     |
| 1   | 1   | 1   | 1   |     |     |     |     |

### KMAP (10 Poin)

**D3**
| AB/CD | 00  | 01  | 11  | 10  |
| ----- | --- | --- | --- | --- |
| 00    |     |     |     |     |
| 01    |     |     |     |     |
| 11    |     |     |     |     |
| 10    |     |     |     |     |

**D2**
| AB/CD | 00  | 01  | 11  | 10  |
| ----- | --- | --- | --- | --- |
| 00    |     |     |     |     |
| 01    |     |     |     |     |
| 11    |     |     |     |     |
| 10    |     |     |     |     |

**D1**
| AB/CD | 00  | 01  | 11  | 10  |
| ----- | --- | --- | --- | --- |
| 00    |     |     |     |     |
| 01    |     |     |     |     |
| 11    |     |     |     |     |
| 10    |     |     |     |     |

**D0**
| AB/CD | 00  | 01  | 11  | 10  |
| ----- | --- | --- | --- | --- |
| 00    |     |     |     |     |
| 01    |     |     |     |     |
| 11    |     |     |     |     |
| 10    |     |     |     |     |

### Foto Rangkaian (20 Poin)
Fotolah setidaknya 1 untuk setiap score (bebas input, tapi score harus sesuai) 

| Score | Foto |
| ----- | ---- |
| 0     |      |
| 1     |      |
| 2     |      |
| 3     |      |
| 4     |      |
| 5     |      |
| 6     |      |
| 7     |      |
| 8     |      |
| 9     |      |

Jika tidak selesai, anda boleh menyusunnya di Proteus. Namun, setiap foto hanya akan mendapatkan 1 poin (yang seharusnya 2)

## Analisis & Teori (60 Poin)

### 5. Analisis IC apa saja yang kalian gunakan untuk rangkaian ini beserta kegunaannya. Kemudian berikanlah analisis kesalahan apabila output tidak sesuai atau jika rangkaian tidak selesai. (20 poin)

### 6. Jika kita ingin mengecek komponen 7 segment rusak atau tidak menggunakan IC 7447 ataupun 7448, terdapat 1 pin yang berguna untuk ini, pin input apa yang harus kita atur? (Tidak boleh menggunakan pin input ABCD) (20 poin)


### 7. Buatlah kesimpulan yang kalian dapatkan dari praktikum kali ini dalam bentuk poin-poin minimal 3 ! (20 poin)

### Bonus (0 poin): Ini modul terakhir yang dibikin oleh saya (NZ). Seberapa lega kalian tutam bukan gw yang bikin? Aakowkoakowkaokw (Maaf telah membikin soal ribet). Tolong berikan kesan pesan saran untuk soal modul yang saya buat (Atau curhatan juga gapapa) agar dapat membuat soal yang lebih bagus kedepannya.

![NZ's wife, Ku biarkan ya gess..](https://hackmd.io/_uploads/SJ09vNhngl.png)
