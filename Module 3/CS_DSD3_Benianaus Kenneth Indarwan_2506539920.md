# Case Study - Karnaugh Map
Pembuat Soal: NZ

```
Nama : Benianaus Kenneth Indarwan
NPM : 2506539920
Group : A27
Rekan Kerja : Benedict Jaysen Riofo Panjaitan
```

## Catatan
- Jika ada pertanyaan, silakan tanya asisten lab yang hadir (selama sesi) atau di Discord (di luar waktu sesi). 
- Referensi tidak diperlukan untuk studi kasus ini.  

## 1. Praktikum (70 poin)

Magus menghela napas saat bayangan K-Maph akhirnya tersegel di dalam buku tua, Ia sudah merasa lega tapi hanya sebentar.

Dari sela-sela segel muncul kepingan-kepingan cahaya kecil seperti potongan peta Karnaugh yang pecah. Mereka bukan roh K-Maph itu sendiri, melainkan gema-gema (echoes) dari pikirannya. Setiap echoes membawa satu pola kondisi artefak yang tetap harus disederhanakan. Gema-gema itu berputar membentuk lingkaran, dan satu suara halus berbisik kepadanya:

`Sekalipun aku telah disegel, anak muda... aku meninggalkan teka-teki. Sederhanakanlah semuanya—atau kepinganku akan bersatu kembali.`

Di hadapan Magus, lantai kembali menyala, kotak-kotak Karnaugh muncul, kali ini lebih rapat, lebih cepat berubah. Di sampingnya masih berdiri Anda, teman extradimensional, siap membantu memetakan dan menyederhanakan. Di atas papan muncul daftar mantra kondisi potongan-potongan kenyataan tentang ketersediaan artefak kampus yang kini harus diubah menjadi ekspresi Boolean sesederhana mungkin agar segel yang baru tak mudah retak.

- Orbium, Sigil, dan Aurum **tidak tersedia**. Resonator **tersedia**.  
- Orbium, Sigil, dan Resonator **tidak tersedia**. Aurum **tersedia**.  
- Orbium dan Aurum **tidak tersedia**. Sigil dan Resonator **tersedia**.  
- Orbium dan Resonator **tidak tersedia**. Sigil dan Aurum **tersedia**.  
- Sigil dan Aurum **tidak tersedia**. Orbium dan Resonator **tersedia**.  
- Sigil dan Resonator **tidak tersedia**. Orbium dan Aurum **tersedia**.  
- Aurum dan Resonator **tidak tersedia**. Orbium dan Sigil **tersedia**.  
- Resonator **tidak tersedia**. Orbium, Sigil, dan Aurum **tersedia**.  
- Aurum **tidak tersedia**. Orbium, Sigil, dan Resonator **tersedia**.  
- Semua tersedia (semua tersedia).  

---

### Tabel Kebenaran
A = Orbium
B = Sigil
C = Aurum
D = Resonator

| A   | B   | C   | D   | Output |
| --- | --- | --- | --- | ------ |
| 0   | 0   | 0   | 0   |   0    |
| 0   | 0   | 0   | 1   |   1    |
| 0   | 0   | 1   | 0   |   1    |
| 0   | 0   | 1   | 1   |   0    |
| 0   | 1   | 0   | 0   |   0    |
| 0   | 1   | 0   | 1   |   1    |
| 0   | 1   | 1   | 0   |   1    |
| 0   | 1   | 1   | 1   |   0    |
| 1   | 0   | 0   | 0   |   0    |
| 1   | 0   | 0   | 1   |   1    |
| 1   | 0   | 1   | 0   |   1    |
| 1   | 0   | 1   | 1   |   0    |
| 1   | 1   | 0   | 0   |   1    |
| 1   | 1   | 0   | 1   |   1    |
| 1   | 1   | 1   | 0   |   1    |
| 1   | 1   | 1   | 1   |   1    |

---

### Peta Karnaugh

| AB\CD | 00  | 01  | 11  | 10  |
|-------|-----|-----|-----|-----|
| **00**| 0   | 1   | 0   | 1   |
| **01**| 0   | 1   | 0   | 1   |
| **11**| 1   | 1   | 1   | 1   |
| **10**| 0   | 1   | 0   | 1   |

---

### Fungsi Boolean
`F(A,B,C,D) = AB + C'D + CD'` 

### Dengan fungsi boolean ini, buat rangkaian logika yang sesuai, lalu ambil foto dengan input yang dapat menyalakan LED.  
**Catatan:** Tidak boleh menggunakan lebih dari **4 IC**.


| A   | B   | C   | D   | Output                                                  |
| --- | --- | --- | --- | ------------------------------------------------------- |
| 0   | 0   | 0   | 1   |![0001](https://hackmd.io/_uploads/rJBNXSGhxl.jpg)|
| 0   | 0   | 1   | 0   |![0010](https://hackmd.io/_uploads/H1JUQHMnex.jpg)|
| 0   | 1   | 0   | 1   |![0101](https://hackmd.io/_uploads/BJhs_FM2lg.jpg)|
| 0   | 1   | 1   | 0   |![0110](https://hackmd.io/_uploads/By4UXSz3ll.jpg)|
| 1   | 0   | 0   | 1   |![1001](https://hackmd.io/_uploads/r1ILQSMhxg.jpg)|
| 1   | 0   | 1   | 0   |![1010](https://hackmd.io/_uploads/ry_Ymrzhle.jpg)|
| 1   | 1   | 0   | 0   |![1100](https://hackmd.io/_uploads/BykPQrG3lg.jpg)|
| 1   | 1   | 0   | 1   |![1101](https://hackmd.io/_uploads/Sy9D7rM3xx.jpg)|
| 1   | 1   | 1   | 0   |![1110](https://hackmd.io/_uploads/H13tQSzngl.jpg)|
| 1   | 1   | 1   | 1   |![1111](https://hackmd.io/_uploads/r1ZqmHfnge.jpg)|

## 2. Jelaskan bagaimana Anda menyederhanakan persamaan boolean sehingga dapat diimplementasikan menggunakan 3–4 IC! (10 points)
Cara menyederhanakan persamaan boolean adalah dengan metode pengelompokan. Pengolompokan dilakukan pada kotak yang bernilai 1, dengan jumlah 2<sup>n</sup>. Hasil dari pengelompokan tersebut kemudian ditulis dalam bentuk aljabar boolean dimana kotak yang berisi `0` adalah komplemen. Contohnya, pada kelompok dimana seluruh kolom CD dengan nilai `01`, maka hasilnya adalah `C'D`. Semua kelompok kemudian dikumpulkan dan di OR kan. Contoh `F(A,B,C)=AB+AC'`

## 3. Dibandingkan metode aljabar boolean lain (seperti maxterms dan minterms), menurut Anda metode mana yang lebih efisien? Jelaskan alasannya! (10 points)

Menurut saya, metode yang lebih efisien adalah dengan menggunakan K-Map, karena dengan K-Map langsung divisualisasikan. Menggunakan metode minterms dan maxterms, kita harus memastikan bahwa kumpulan variabel terdiri dari semua variabel, sedangkan pada metode K-Map bisa dengan persamaan yang lebih sederhana.

## 4. Tuliskan kesimpulan dari percobaan ini dalam bentuk poin-poin (10 points)
- K-MAP dapat digunakan untuk menyederhanakan input atau truth table yang rumit, dengan cara merepresentasikan data secara visual (tabel).
- Hasil dari fungsi yang telah dibuat dengan cara K-MAP akan mendapatkan output yang sama dengan fungsi sebelum penyederhanaan.
- Penyederhanaan K-MAP membuat rangkaian yang ada lebih sederhana dan lebih singkat dibandingkan jika tidak disederhanakan. Dapat menggunakan lebih banyak IC dan rangkaiannya mungkin tidak cukup dalam breadboard.
- Dapat terdapat perbedaan pada rangkaian TinkerCad dan rangkaian asli yang dibuat karena IC yang bermasalah, koneksi kabel yang kurang rapat, dan faktor lainnya. 

## Bonus: Artefak mana yang tersedia bersamaan paling banyak? Jabarkan jawaban Anda! (10 points) (Nilai Maksimal Tetap 100 ya gesss)
- Dari 4 variabel, maka ada 16 

AB, AC, AD, BC, BD, CD
ABC, BCD, ACD, ABD

- Berdasarkan K-MAP tadi, 

| AB\CD | 00  | 01  | 11  | 10  |
|-------|-----|-----|-----|-----|
| **00**| 0   | 1   | 0   | 1   |
| **01**| 0   | 1   | 0   | 1   |
| **11**| 1   | 1   | 1   | 1   |
| **10**| 0   | 1   | 0   | 1   |

terdapat pasangan seperti AB yang memenuhi satu baris. Maka, AB tersedia bersamaan 4x.
AC tersedia 2x. AD tersedia 2x. BC tersedia 1x. BD tersedia 1x. CD tersedia 1x. 
Sedangkan ABC tersedia 2x. BCD tersedia 1x. ACD tersedia 1x. Dan ABD tersedia 1x.

Maka, artefak yang tersedia bersamaan paling banyak adalah artefak AB, yaitu Orbium dan Sigil.