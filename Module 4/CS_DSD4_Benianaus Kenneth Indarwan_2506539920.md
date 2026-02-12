# Case Study - Gerbang Logika Kompleks
Penulis Soal: DY
---

Nama : Benianaus Kenneth Indarwan
NPM : 2506539920
Kelompok: A27
Rekan Kerja : Benedict Jaysen Riofo Panjaitan

## Catatan
- Jika ada pertanyaan, silakan tanyakan pada asisten lab yang sedang bertugas (saat sesi berlangsung) atau di Discord (jika di luar jam sesi).
- Referensi tidak wajib dicantumkan untuk studi kasus ini.

---

## Studi Kasus (50 poin)

Akhirnya jadwal efektif untuk mengisi di hari sebelum ujian selesai. Magus berterimakasih kepadamu karena sudah membantunya. Namun, Anda teringat juga bahwa 2 minggu dari sekarang juga merupakan waktu-waktu ujian untuk dirimu. Untuk itu, Anda menetapkan jadwal baru seperti berikut.

- Harus ada `Latihan` **DAN** `Belajar` bersamaan.  
**ATAU**  
- Ada `Waktu Istirahat` atau `Waktu Bermain`, tapi **tidak boleh keduanya bersamaan**.

Coba petakan jadwal baru ini agar dirimu bisa semakin lebih baik.
**RANGKAIAN HANYA BOLEH MENGGUNAKAN COMPLEX GATES.**  
`Hint: Gunakan NOR untuk membuat OR gate, dan gunakan NAND untuk membuat AND gate.`

---

### Deskripsi Variabel
A = Latihan
B = Belajar  
C = Waktu Istirahat  
D = Waktu Bermain  

### Tabel Kebenaran:
| A   | B   | C   | D   | Output |
| --- | --- | --- | --- | :----: |
| 0   | 0   | 0   | 0   | 0   |
| 0   | 0   | 0   | 1   | 1   |
| 0   | 0   | 1   | 0   | 1   |
| 0   | 0   | 1   | 1   | 0   |
| 0   | 1   | 0   | 0   | 0   |
| 0   | 1   | 0   | 1   | 1   |
| 0   | 1   | 1   | 0   | 1   |
| 0   | 1   | 1   | 1   | 0   |
| 1   | 0   | 0   | 0   | 0   |
| 1   | 0   | 0   | 1   | 1   |
| 1   | 0   | 1   | 0   | 1   |
| 1   | 0   | 1   | 1   | 0   |
| 1   | 1   | 0   | 0   | 1   |
| 1   | 1   | 0   | 1   | 1   |
| 1   | 1   | 1   | 0   | 1   |
| 1   | 1   | 1   | 1   | 1   |

### Peta K-Map:

| AB\CD | 00  | 01  | 11  | 10  |
|:-----:|-----|-----|-----|-----|
| **00**|  0  |  1  |  0  |  1  |
| **01**|  0  |  1  |  0  |  1  |
| **11**|  1  |  1  |  1  |  1  |
| **10**|  0  |  1  |  0  |  1  |

![image](https://hackmd.io/_uploads/rJoTCPjheg.png)

Fungsi = AB+C'D+CD'

### Foto semua kombinasi output:  
| A   | B   | C   | D   | Foto |
| --- | --- | --- | --- | ---- |
| 0   | 0   | 0   | 0   |![0000](https://hackmd.io/_uploads/HyyXCTihlg.jpg)|
| 0   | 0   | 0   | 1   |![0001](https://hackmd.io/_uploads/rJ4KR6j2ll.jpg)|
| 0   | 0   | 1   | 0   |![0010](https://hackmd.io/_uploads/SyBKRajnxe.jpg)|
| 0   | 0   | 1   | 1   |![0011](https://hackmd.io/_uploads/SyHFRTo3gg.jpg)|
| 0   | 1   | 0   | 0   |![0100](https://hackmd.io/_uploads/S14Y0ao2el.jpg)|
| 0   | 1   | 0   | 1   |![0101](https://hackmd.io/_uploads/HkHFRTsnge.jpg)|
| 0   | 1   | 1   | 0   |![0110](https://hackmd.io/_uploads/S1BFCas2eg.jpg)|
| 0   | 1   | 1   | 1   |![0111](https://hackmd.io/_uploads/H1HYCajhgx.jpg)|
| 1   | 0   | 0   | 0   |![1000](https://hackmd.io/_uploads/HJrKCpj2ll.jpg)|
| 1   | 0   | 0   | 1   |![1001](https://hackmd.io/_uploads/rySYC6jhex.jpg)|
| 1   | 0   | 1   | 0   |![1010](https://hackmd.io/_uploads/BkStC6onxe.jpg)|
| 1   | 0   | 1   | 1   |![1011](https://hackmd.io/_uploads/rkStR6ohlx.jpg)|
| 1   | 1   | 0   | 0   |![1100](https://hackmd.io/_uploads/HkSY0pinlg.jpg)|
| 1   | 1   | 0   | 1   |![1101](https://hackmd.io/_uploads/H1HYRTi2le.jpg)|
| 1   | 1   | 1   | 0   |![1110](https://hackmd.io/_uploads/rJAE0aj3xl.jpg)|
| 1   | 1   | 1   | 1   |![1111](https://hackmd.io/_uploads/r1oE06o2lx.jpg)|

---

## Teori (50 poin)

### 1. Gambarlah diagram dan jelaskan bagaimana membangun gerbang XOR menggunakan gerbang logika dasar! (5 poin)
Anda bisa menggambarnya di kertas lalu difoto, atau membuatnya dengan aplikasi seperti Logisim/Proteus.  
Anda `TIDAK` boleh mengambil screenshot langsung dari internet!  

![image](https://hackmd.io/_uploads/B1S7L5o3lx.png)
Untuk membangun gerbang XOR (Exclusive OR), ada 2 kondisi yaitu ketika input sama dan input berbeda. Perbedaannya dengan gerbang OR adalah ketika input `1` dan `1`, pada OR menghasilkan `1`, tetapi pada XOR menghasilkan `0`. Maka, kita bisa menambahkan pengecualian itu dengan menambahkan kondisi input `1 AND 1`, kemudian hasilnya diinverse dan digabungkan dengan output `OR` melalui gerbang `AND`. 

---

### 2. Gambarlah diagram dan jelaskan bagaimana membangun gerbang XNOR menggunakan gerbang logika dasar! (5 poin)
Anda bisa menggambarnya di kertas lalu difoto, atau membuatnya dengan aplikasi seperti Logisim/Proteus.  
Anda `TIDAK` boleh mengambil screenshot langsung dari internet!  

![image](https://hackmd.io/_uploads/HJod_coheg.png)
Untuk membangun gerbang XNOR (Exclusive NOT OR), mirip seperti gerbang XOR, hanya saja outputnya terbalik. Maka, cara mudah untuk membuat gerbang XNOR adalah dengan menambahkan NOT gate di output tadi.

---

### 3. Jika Anda ingin membuat rangkaian validasi password, gerbang logika apa yang paling tepat digunakan? Jelaskan alasannya! (20 poin)  

Untuk rangkaian validasi password, gerbang logika yang cocok untuk digunakan adalah gerbang XNOR. Karena gerbang XNOR adalah gerbang yang digunakan untuk membandingkan; gerbang ini akan mengeluarkan output `1` ketika password cocok dan output `0` ketika password tidak cocok atau tidak sama.

---

### 4. Apa kesimpulan dari percobaan ini? (Gunakan poin-poin!) (20 poin)  

- Fungsi sederhana seperti fungsi tadi, `F=AB+C'D+CD'`, dapat menggunakan gerbang logika dasar atau bisa juga dirangkai dengan gerbang logika kompleks. 
- Ada 2 cara untuk merangkai rangkaian, pertama bisa menggunakan kombinasi IC 7400 dan IC 7402, kemudian selain IC tersebut bisa menggunakan IC 7486 untuk mempermudah. Menggunakan kombinasi IC 7486 dan IC 7400 atau IC 7402 memungkinkan untuk membuat rangkaian hanya dengan total 2 IC.
- Apabila memilih untuk tidak menggunakan IC 7486, maka rangkaian yang dihasilkan akan lebih rumit dan lebih panjang, lebih sulit untuk dianalisis dan diperbaiki.
- Secara teori bisa saja merangkai rangkaian dengan menggunakan satu jenis IC saja, karena IC 7400 dan IC 7402 dapat disusun sedimikian untuk menjadi gerbang NOT, OR, dan AND. 

---

### Bonus (0 poin)
Bagikan keluh kesah atau frustrasi tentang sesi lab DSD sejauh ini.  
- IC terkadang bermasalah
- War kabel (susah dapet kabel yang warnanya bener, kadang kabelnya dapet yang female juga)
- Vulcan, hoki-hokian, bisa dapet yang switchnya bener, kadang dapet yang switchnya 80% gabisa dipake
- Waktu kadang kurang apalagi kalo ga hoki dapet masalah di kabel atau di IC padahal rangkaian udah jadi, bingung troubleshootnya, ternyata masalahnya sama kabel atau ICnya
- Sekian dari saya, terima kasih

![SemangatYahh!! - DY](https://i.pinimg.com/736x/45/10/8c/45108c4c13057e9afdb7a6517bac32c9.jpg)