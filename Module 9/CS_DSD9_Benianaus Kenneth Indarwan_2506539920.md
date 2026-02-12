---
title: Case Study - 9 (Register & Counter)

---

# Case Study - 9 (Register & Counter)
Pembuat Soal: DY
```
Nama: Benianaus Kenneth Indarwan
NPM: 2506539920
Kelompok : A27
Rekan Kerja : Benedict Jaysen Riofo Panjaitan
```

<details>
<summary>Doksli Narasi</summary>
`Note: Jika malas membaca, dan jujur ini narasi cringe banget. Langsung aja ke Komponen Sistem.`

*Libur musim panas telah tiba~*

Rintarou berhasil.

Setelah berhari-hari bimbang, dia akhirnya memberanikan diri. Dan sekarang, dia di sini, di pantai, sesuai dengan rencananya. Matahari sudah terbenam, dan di sampingnya, Kaoruko sedang tertawa sambil menyalakan kembang api.

"Ini indah sekali, Rintarou! Ide bagus!" seru Kaoruko.

![YahTamatDeh](https://hackmd.io/_uploads/H1rvb8QxWx.png)

Jantung Rintarou berdebar kencang. Ini adalah momennya. Dia teringat down counter dari tugas pendahuluan yang terasa seperti hitungan mundur. Sekarang, hitungan itu sudah mencapai nol.

Dia memegang kembang api terakhir.

"Kaoruko," panggil Rintarou, suaranya sedikit bergetar.
"Ya? Ada apa?"

"Tugas praktikum kita kali ini... tentang IC 74193, kan?"
Kaoruko menatapnya bingung. "Hah? Iya... Kenapa tiba-tiba membahas itu?"

"Kita harus memanipulasinya jadi BCD counter," lanjut Rintarou, "Harus menghitung dari 0 sampai 9, lalu reset kembali ke 0 saat menyentuh angka 10."

"Iya, terus?"

Rintarou menyalakan kembang api terakhir.

"Selama ini, aku merasa seperti down counter yang terus menghitung mundur, menunggu waktu yang tepat," katanya. "Tapi sejak aku lebih mengenalmu, perasaanku rasanya seperti up counter BCD itu... terus bertambah dari 0, 1, 2... sampai sekarang, rasanya sudah penuh di angka 9."

Cahaya kembang api itu menerangi wajah mereka.

"Kaoruko... aku tidak mau perasaanku ini reset kembali ke 0 seperti di tugas itu saat menyentuh angka 10"

"Aku... aku suka kamu, Kaoruko."

![Aww](https://hackmd.io/_uploads/rJMIzUQx-l.png)

</details>

Setelah berhasil membuat di alat Magis bernama Proteus, sekarang rancanglah secara nyata. Namun, ternyata Magus mengubah niatnya, yang awalnya 6 -> 3 -> ... sekarang menjadi naik terus dan kembali ke awal saat menyentuh **Angka 10** (0 -> 1 -> 2 -> ... -> 9 -> 0) karena semua pengalaman, kejadian dan ujian-ujian ini pada akhirnya hanyalah sebuah repetisi tanpa akhir selama masih ada manusia (Sheesh jadi filsafat). Cobalah mengikuti alur yang telah magus rencanakan dan rangkailah dengan ketentuan Magus.

## Komponen Sistem

### 1. Counter (IC 74193)
`Note: Minta ke aslab. Balikin ke aslab. Tersedia terbatas.`
Counter IC 74193 adalah counter yang menghitung dari 0 hingga 15 (up) atau sebaliknya (down) secara biner. Kita akan manipulasi karakteristik IC ini agar menjadi `BCD counter (menghitung dari 0 hingga 9 dan sebaliknya)`.
Counter ini bekerja menghitung dari 0 ke 15 dan kembali ke 0 untuk up counter. Dan menghitung dari 15 ke 0 dan kembali ke 15 untuk down counter.

Konfigurasi:
![KonfIC](https://i0.wp.com/makerselectronics.com/wp-content/uploads/2016/08/Pin-Configuration-of-IC74193.png?resize=742%2C429&ssl=1)
- `P0, P1, P2, P3` input data. P0 sebagai LSB.
- `Q0, Q1, Q2, Q3` output counter. Q0 sebagai LSB.
- `MR` master reset untuk mereset counter menjadi 0.
- `PL` adalah enable untuk forward data dari P ke Q. `Aktif LOW`, jika 0 maka input pada P0 s.d. P3 akan langsung masuk ke Q0 s.d. Q3.
- `CPd` adalah clock input untuk `down counter`.
- `CPu` adalah clock input untuk `up counter`.
- `VCC, GND` really ya dunno this bruhh?? 🤨
- `TCd, TCu` output borrow/carry. `Gausah dipeduliin`.

### 2. AND / NAND / NOT gate
Dibebaskan menggunakan `AND` atau `NAND` atau `NOT` atau bahkan `kombinasi` dari mereka untuk membuat `logika reset` untuk up dan down counter. **TIDAK ADA PENILAIAN KHUSUS TERKAIT EFISIENSI RANGKAIAN**, ini bukan psikomotorik. Hasil adalah Hasil.

### 3. Decoder 7 segment (7447/7448)
Bebas mau pake yang mana, sesuaikan dengan 7 segment yang dipilih. Jika common `Kathode pake 7448`. Jika common `Anode pake 7447`. `Boleh cari datasheets konfigurasi pin nya di internet.`

### 4. 7 segment
Pilih salah satu:
- Common Kathode: `SM420`
- Common Anode: `SM410`
`Note: Terdapat 5 pin di setiap sisi, pilih salah satu sisi saja, hubungkan pin tepat tengah nya ke common-nya melalui resistor (tergantung common Kathode/Anode).`
`Boleh cari datasheets konfigurasi pin nya di internet.`

### 5. Satu buah resistor
Resistor ke arah pin tengah common 7 segment, biar ga rusak tuh 7 segment nya.

### 6. Vulcan
Ambil sinyal clock-nya aja. Atau mau manual boleh (bolak-balik pindah GND VCC).

### 7. Jumper, BreadBoard, Arduino

## Cara Kerja Sistem

### 1. Logika Reset Up Counter
- Saat `output` bernilai `1010` atau 10 desimal, maka berikan input `HIGH` untuk `MR`.
- `Hint: Validasi 3 digit terbesar output untuk dijadikan input MR.`
- `Hint lagi: jika output terdeteksi 101 maka berikan input HIGH ke MR.`
- Kira-kira pake apa yh logic gate nya...

### 2. Logika Reset Down Counter
- Berikan `input 1001` atau 9 desimal pada `P0 s.d. P3` sebagai data input ketika counter reset. `Langsung saja hubungkan VCC GND menjadi 1001`.
- Saat `output` bernilai `1111` atau 15 desimal, maka berikan input `LOW` untuk `PL`.
- `Hint: Validasi 2 digit terbesar output untuk dijadikan input PL.`
- Kira-kira pake apa yh logic gate nya...

## Hasil & Analisis

### Foto Rangkaian (80 Poin)
`Note: Jika rangkaian tidak jadi sama sekali atau output sama sekali tidak sesuai, isi tabel berikut dengan rangkaian proteus yang benar.`

`Note: Jika tabel diisi dengan rangkaian proteus, maka maks nilai Foto Rangkaian ini 70.`

| Output | Foto |
|--------|------|
|  0     |![comp-1](https://hackmd.io/_uploads/BkRQRd2lWe.jpg)|
|  1     |![comp-0](https://hackmd.io/_uploads/ry3BCd2eZe.jpg)|
|  2     |![comp-4](https://hackmd.io/_uploads/SyqLCuhgZe.jpg)|
|  3     |![comp-2](https://hackmd.io/_uploads/HyeLRdneZl.jpg)|
|  4     |![comp-3](https://hackmd.io/_uploads/rkSLCd2gZl.jpg)|
|  5     |![comp-5](https://hackmd.io/_uploads/BJbv0unlbx.jpg)|
|  6     |![comp-6](https://hackmd.io/_uploads/HkQwRdngWe.jpg)|
|  7     |![comp-7](https://hackmd.io/_uploads/H1uD0d3eZl.jpg)|
|  8     |![comp-8](https://hackmd.io/_uploads/BycPA_2gWe.jpg)|
|  9     |![comp-9](https://hackmd.io/_uploads/rkTD0unlZl.jpg)|

Down Counter:
<img src="https://hackmd.io/_uploads/rJY2mF2xZx.gif" width="600">

Up Counter:
<img src="https://hackmd.io/_uploads/BJ3WmY2lZe.gif" width="600">



### Analisis (20 Poin)

#### 1. Jelaskan bagaimana cara membuat up counter dan down counter seperti itu secara `Asynchronous` dengan menggunakan `D flip-flop`? (10 Poin)

Menggunakan D Flip-Flop, hanya akan menggunakan 1 clock yang dihubungkan dengan D Flip-Flop pertama. Output dari D Flip-Flop akan masuk menjadi input Clock pada D Flip-Flop selanjutnya, sama untuk D Flip-Flop selanjutnya. Output Q' pada suatu D Flip-Flop menjadi input D di flip flop yang sama. Output BCD diambil dari output Q, dengan flip-flop paling kiri adalah LSB.

Untuk menentukan up counter dan down counter:
- Pada Up Counter, yang dihubungkan ke clock adalah Q'
- Pada Down Counter, yang dihubungkan ke clock adalah Q

![image](https://hackmd.io/_uploads/S1D4sY3lWg.png)


#### 2. Dalam dunia nyata sehari hari, sebutkan `minimal 3` masing-masing penerapan up counter dan down counter tersebut (10 poin)

| No | Up Counter | Down Counter |
| :-:| :--------: | :----------: |
|1|Jam/Stopwatch | Timer
|2|Tracking berapa kali sebuah proses dilaksanakan | Tracking jumlah proses/barang yang tersisa untuk dilakukan
|3|Memastikan delay yang terjadi sesuai dengan yang diinginkan (ex. proses berikutnya terjadi setelah x detik) | Untuk timing sebuah proses/mesin akan berjalan selama waktu yang telah ditentukan (ex. proses yang sudah ditrigger akan berjalan selama x detik)