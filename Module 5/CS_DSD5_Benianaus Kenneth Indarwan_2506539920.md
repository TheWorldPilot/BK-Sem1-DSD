# Case Study - Decoder & Encoder

> Pembuat Soal: NZ

```
Name    : Benianaus Kenneth Indarwan
NPM     : 2506539920
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
| 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   |
| 0   | 0   | 0   | 1   | 0   | 0   | 0   | 1   |
| 0   | 0   | 1   | 0   | 0   | 0   | 1   | 0   |
| 0   | 0   | 1   | 1   | 0   | 0   | 1   | 1   |
| 0   | 1   | 0   | 0   | 0   | 0   | 1   | 0   |
| 0   | 1   | 0   | 1   | 0   | 0   | 1   | 1   |
| 0   | 1   | 1   | 0   | 0   | 1   | 0   | 0   |
| 0   | 1   | 1   | 1   | 0   | 1   | 0   | 1   |
| 1   | 0   | 0   | 0   | 0   | 1   | 0   | 0   |
| 1   | 0   | 0   | 1   | 0   | 1   | 0   | 1   |
| 1   | 0   | 1   | 0   | 0   | 1   | 1   | 0   |
| 1   | 0   | 1   | 1   | 0   | 1   | 1   | 1   |
| 1   | 1   | 0   | 0   | 0   | 1   | 1   | 0   |
| 1   | 1   | 0   | 1   | 0   | 1   | 1   | 1   |
| 1   | 1   | 1   | 0   | 1   | 0   | 0   | 0   |
| 1   | 1   | 1   | 1   | 1   | 0   | 0   | 1   |

### KMAP (10 Poin)

**D3**
| AB/CD | 00  | 01  | 11  | 10  |
| ----- | --- | --- | --- | --- |
| 00    | 0   | 0   | 0   | 0   |
| 01    | 0   | 0   | 0   | 0   |
| 11    | 0   | 0   | 1   | 1   |
| 10    | 0   | 0   | 0   | 0   |

![image](https://hackmd.io/_uploads/SkCCujEpll.png)

`F=ABC`

**D2**
| AB/CD | 00  | 01  | 11  | 10  |
| ----- | --- | --- | --- | --- |
| 00    | 0   | 0   | 0   | 0   |
| 01    | 0   | 0   | 1   | 1   |
| 11    | 1   | 1   | 0   | 0   |
| 10    | 1   | 1   | 1   | 1   |

![image](https://hackmd.io/_uploads/B1iU5o46lg.png)

`F=A'BC+AC'+AB'`
`F=A'BC+A(B'+C')`

**D1**
| AB/CD | 00  | 01  | 11  | 10  |
| ----- | --- | --- | --- | --- |
| 00    | 0   | 0   | 1   | 1   |
| 01    | 1   | 1   | 0   | 0   |
| 11    | 1   | 1   | 0   | 0   |
| 10    | 0   | 0   | 1   | 1   |

![image](https://hackmd.io/_uploads/ryJQ9jNalx.png)

`F=BC'+B'C`

**D0**
| AB/CD | 00  | 01  | 11  | 10  |
| ----- | --- | --- | --- | --- |
| 00    | 0   | 1   | 1   | 0   |
| 01    | 0   | 1   | 1   | 0   |
| 11    | 0   | 1   | 1   | 0   |
| 10    | 0   | 1   | 1   | 0   |

![image](https://hackmd.io/_uploads/r1N4cs4aee.png)

`F=D`

### Foto Rangkaian (20 Poin)
Fotolah setidaknya 1 untuk setiap score (bebas input, tapi score harus sesuai) 

| Score | Foto | Proteus |
| ----- | ---- | ------- |
| 0 | <image src="https://hackmd.io/_uploads/BkdjD6Vage.jpg" width=600> | <image src="https://hackmd.io/_uploads/SkeM8gB6xl.png" width=600> |
| 1 | <image src="https://hackmd.io/_uploads/BkhhPaNaxx.jpg" width=600> | <image src="https://hackmd.io/_uploads/SyxeLgSagg.png" width=600> |
| 2 | <image src="https://hackmd.io/_uploads/BkrTva4ple.jpg" width=600> | <image src="https://hackmd.io/_uploads/SJkZIlSagg.png" width=600> |
| 3 | <image src="https://hackmd.io/_uploads/S1sAPaVpgg.jpg" width=600> | <image src="https://hackmd.io/_uploads/HJGQLlBplg.png" width=600> |
| 4 | <image src="https://hackmd.io/_uploads/Hy4JO646ge.jpg" width=600> | <image src="https://hackmd.io/_uploads/rkT4Lxragx.png" width=600> |
| 5 | <image src="https://hackmd.io/_uploads/H1yx_TVagg.jpg" width=600> | <image src="https://hackmd.io/_uploads/rJ1IIeSaxl.png" width=600> |
| 6 | <image src="https://hackmd.io/_uploads/BJaxOa4plx.jpg" width=600> | <image src="https://hackmd.io/_uploads/By38Uxr6xx.png" width=600> |
| 7 | <image src="https://hackmd.io/_uploads/HyN-_T4Txl.jpg" width=600> | <image src="https://hackmd.io/_uploads/ByFvUxHael.png" width=600> |
| 8 | <image src="https://hackmd.io/_uploads/Bk2WOpNaex.jpg" width=600> | <image src="https://hackmd.io/_uploads/Bk7OUxBTle.png" width=600> |
| 9 | <image src="https://hackmd.io/_uploads/rJuzOaEagl.jpg" width=600> | <image src="https://hackmd.io/_uploads/Syj_Ieraxg.png" width=600> |


Jika tidak selesai, anda boleh menyusunnya di Proteus. Namun, setiap foto hanya akan mendapatkan 1 poin (yang seharusnya 2)

## Analisis & Teori (60 Poin)

### 5. Analisis IC apa saja yang kalian gunakan untuk rangkaian ini beserta kegunaannya. Kemudian berikanlah analisis kesalahan apabila output tidak sesuai atau jika rangkaian tidak selesai. (20 poin)

IC yang digunakan adalah IC7404, IC7411, IC7432, IC7408, dan IC7447. IC7404 digunakan sebagai inverter, IC7408 dan IC7411 digunakan sebagai AND gate, IC7432 sebagai OR gate, dan IC7447 sebagai BCD to 7-Segment Decoder. 
Output yang keluar ada yang tidak sesuai, hal ini dapat terjadi karena ada pin yang masih floating, rangkaian yang kurang sesuai, atau kesalahan dalam memasang pin layout. Untuk di rangkaian kami, ini bisa terjadi karena floating pin karena display kadang mengalami flickering karena kabel yang kurang pas.

### 6. Jika kita ingin mengecek komponen 7 segment rusak atau tidak menggunakan IC 7447 ataupun 7448, terdapat 1 pin yang berguna untuk ini, pin input apa yang harus kita atur? (Tidak boleh menggunakan pin input ABCD) (20 poin)
Bisa menggunakan pin 3 atau `Lamp Test`. Pin ini akan menyalakan semua segment dari 7-Segment display, dengan kondisi bahwa pin output dari IC sudah terkoneksi dengan 7-Segment display. Pin ini jika diberikan input `HIGH` akan menyalakan semua segment, sehingga bisa melihat segment mana yang rusak atau tidak bekerja.

### 7. Buatlah kesimpulan yang kalian dapatkan dari praktikum kali ini dalam bentuk poin-poin minimal 3 ! (20 poin)
- Untuk membuat suatu decoder secara manual, pertama kita membuat truth table output BCD, dan membuat K-MAP masing-masing bit.
- 7-Segment display ada 2, Tipe `Common Anode` dan `Common Catthode`. Kedua tipe membutuhkan IC decoder yang berbeda, Untuk tipe `Common Anode` membutuhkan IC7447, dan `Common Catthode` membutuhkan IC 7448. 
- Walaupun sudah terkoneksi semua, terkadang pada 7-Segment display masih terdapat segment yang tiba-tiba mati, hal ini karena koneksi pin yang kurang tepat atau kurang rapat.
- Penting untuk membaca dokumentasi dan datasheet untuk IC atau komponen yang belum dikenal, sehingga akan mengerti dan tidak merusak komponen.

### Bonus (0 poin): Ini modul terakhir yang dibikin oleh saya (NZ). Seberapa lega kalian tutam bukan gw yang bikin? Aakowkoakowkaokw (Maaf telah membikin soal ribet). Tolong berikan kesan pesan saran untuk soal modul yang saya buat (Atau curhatan juga gapapa) agar dapat membuat soal yang lebih bagus kedepannya.

- Soalnya sih aman-aman aja bang, tapi waktu buat ngerjainnya yang bikin ribet, CS aja tadi lama belom ngurusin perkabelan. Ya, gitu lah bang.

![NZ's wife, Ku biarkan ya gess..](https://hackmd.io/_uploads/SJ09vNhngl.png)
