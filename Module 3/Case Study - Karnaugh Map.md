# Case Study - Karnaugh Map
Pembuat Soal: NZ

```
Nama : 
NPM : 
Group : 
Rekan Kerja :
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
A = ?
B = ?
C = ?
D = ?

| A   | B   | C   | D   | Output |
| --- | --- | --- | --- | ------ |
| 0   | 0   | 0   | 0   |        |
| 0   | 0   | 0   | 1   |        |
| 0   | 0   | 1   | 0   |        |
| 0   | 0   | 1   | 1   |        |
| 0   | 1   | 0   | 0   |        |
| 0   | 1   | 0   | 1   |        |
| 0   | 1   | 1   | 0   |        |
| 0   | 1   | 1   | 1   |        |
| 1   | 0   | 0   | 0   |        |
| 1   | 0   | 0   | 1   |        |
| 1   | 0   | 1   | 0   |        |
| 1   | 0   | 1   | 1   |        |
| 1   | 1   | 0   | 0   |        |
| 1   | 1   | 0   | 1   |        |
| 1   | 1   | 1   | 0   |        |
| 1   | 1   | 1   | 1   |        |

---

### Peta Karnaugh

| AB\CD | 00  | 01  | 11  | 10  |
|-------|-----|-----|-----|-----|
| **00**|     |     |     |     |
| **01**|     |     |     |     |
| **11**|     |     |     |     |
| **10**|     |     |     |     |

---

### Fungsi Boolean
`F(A,B,C,D) =` 

### Dengan fungsi boolean ini, buat rangkaian logika yang sesuai, lalu ambil foto dengan input yang dapat menyalakan LED.  
**Catatan:** Tidak boleh menggunakan lebih dari **4 IC**.


| A   | B   | C   | D   | Output                                                  |
| --- | --- | --- | --- | ------------------------------------------------------- |
| X   | X   | X   | X   |![Goodluck!](https://hackmd.io/_uploads/BkTaNPTixl.gif)|

## 2. Jelaskan bagaimana Anda menyederhanakan persamaan boolean sehingga dapat diimplementasikan menggunakan 3–4 IC! (10 points)

## 3. Dibandingkan metode aljabar boolean lain (seperti maxterms dan minterms), menurut Anda metode mana yang lebih efisien?Jelaskan alasannya! (10 points)

## 4. Tuliskan kesimpulan dari percobaan ini dalam bentuk poin-poin (10 points)
-
-
-

## Bonus: Artefak mana yang tersedia bersamaan paling banyak? Jabarkan jawaban Anda! (10 points) (Nilai Maksimal Tetap 100 ya gesss)