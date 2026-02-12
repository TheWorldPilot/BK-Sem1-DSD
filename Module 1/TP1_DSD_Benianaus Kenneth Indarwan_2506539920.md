# Tugas Pendahuluan - Introduction to Digital Circuits

Nama: Benianaus Kenneth Indarwan  
NPM: 2506539920

# Notes
Referensi berformat IEEE style (bisa menggunakan https://www.mybib.com/ untuk kemudahan) dan setidaknya 2 referensi.

## 1. Apa itu breadboard? Dan apa kegunaannya di dalam praktikum ini? (15 poin)

Breadboard adalah board persegi panjang dengan lubang-lubang yang digunakan untuk memasukkan perangkat elektronik. Breadboard bertujuan untuk mengetes atau mencoba desain sirkuit karena mudah untuk dilepas pasang. 
Breadboard terdiri dari casing plastik dan klip-klip yang digunakan untuk menghubungkan dengan perangkat elektronik yang ditancapkan. Di kiri dan kanan breadboard terdapat yang disebut dengan *power rails* yang terkoneksi secara vertikal. Pin pin lainnya terkoneksi secara horizontal.

Kegunaan breadboard dalam praktikum ini adalah untuk *prototyping* atau mendesain sirkuit sederhana, sehingga tidak perlu mendesain dan membuat PCB khusus untuk melakukan tes.

### Referensi: 
- [1]Science Buddies, “How to Use a Breadboard,” Science Buddies, 2019. https://www.sciencebuddies.org/science-fair-projects/references/how-to-use-a-breadboard (accessed September 07, 2025).
- [2]R. Mitchell, “What are Breadboards and Their Uses | Breadboard,” Maker Pro, Sep. 25, 2018. https://maker.pro/breadboard/tutorial/an-introduction-to-breadboards-and-their-uses (accessed September 07, 2025).

## 2. Apa itu VCC dan Ground? Apa yang akan terjadi jika kita tidak sengaja mengganti koneksi VCC dan Ground (VCC ke Ground dan Ground ke VCC)? Coba tunjukkan mana yang VCC dan Ground di breadboard!! (15 poin)

VCC (Voltage Common Collector) adalah pin yang menyediakan tegangan positif dalam perangkat elektronik. Awalnya merujuk pada tegangan suplai dari kolektor transistor. Sekarang, VCC biasanya merujuk pada tegangan positif dari Power Supply atau tegangan masuk (input) ke dalam perangkat atau rangkaian elektronik.

GND (Ground) adalah pin yang merujuk pada titik referensi tegangan 0V dalam rangkaian. Fungsinya sebagai jalur akhir pada arus listrik dan menjadi patokan untuk mengukur tegangan pada komponen dalam rangkaian. GND dapat dibagi menjadi beberapa tipe tergantung jenis rangkaian dan aplikasinya.

Ketika VCC dan GND terbalik maka disebut dengan istilah *Reverse Polarity*.  Ketika ini terjadi, komponen akan mulai panas bahkan bisa tercium bau terbakar. Apabila tidak segera diperbaiki, komponen dapat rusak.

<img src="https://hackmd.io/_uploads/r1bgR-iclx.jpg" alt="dsd" width="800" />

### Referensi: 
- [1]Elga Aris Prastyo, “Apa Itu GND, VCC, dan VIN pada Modul Elektronika?,” Edukasi Elektronika | Electronics Engineering Solution and Education, Sep. 05, 2025. https://www.edukasielektronika.com/2025/05/apa-itu-gnd-vcc-dan-vin-pada-modul-elektronika.html (accessed September 07, 2025).
- [2]Anonymous, “VCC, VDD, VEE, VSS and GND: Meaning of the power supply voltage abbreviations - Jinftry Electronics,” Jinftry.com, 2024. https://www.jinftry.com/news/VCC-VDD-VEE-VSS-and-GND-Meaning-of-the-power-supply-voltage-abbreviations (accessed September 07, 2025).

## 3. Apa kegunaan resistor dalam rangkaian? Bagaimana cara kerja resistor? Apa yang akan terjadi jika kita tidak menggunakan resistor dalam beberapa komponen listrik? (15 poin)

Resistor merupakan perangkat pasif yang digunakan untuk menambahkan hambatan dalam rangkaian. Resistor digunakan untuk mengurangi arus berlebih pada rangkaian.

Cara kerja resistor adalah dengan menempatkan resistor sebelum arus listrik memasuki komponen yang dituju. Resistor dibuat dengan dengan bahan yang memiliki resistansi terhadap arus listrik. Besar hambatannya tergantung dengan jenis bahannya.

Dalam beberapa komponen, contohnya LED, memiliki kuat arus spesifik yang perlu diperhatikan. Apabila arusnya terlalu kecil, LED tidak akan nyala. Tetapi, apabila arusnya terlalu besar, bisa menyebabkan LED *burn out*. Oleh karena itu, biasanya LED ditambahkan resistor untuk mencegah hal seperti itu terjadi. Hal ini juga dapat terjadi pada komponen lainnya yang tidak bisa menerima arus yang terlalu besar.

### Referensi: 
- [1][5]Ø. Nydal Dahl, “What Is A Resistor And What Does It Do?,” Build Electronic Circuits, Oct. 03, 2013. https://www.build-electronic-circuits.com/what-is-a-resistor/ (accessed September 07, 2025).
- [2]EE Power, “What is a resistor? | Resistor fundamentals | Resistor Guide,” eepower.com, 2024. https://eepower.com/resistor-guide/resistor-fundamentals/what-is-a-resistor/ (accessed September 07, 2025).

## 4. Apa itu datasheet? Sebutkan dan jelaskan bagian-bagiannya! Berikan satu contoh datasheet dan jelaskan isinya secara singkat! (Anda dapat mengecek modul 2 pada website learn digilab atau google bagian ini) (15 points)

Datasheet adalah dokumen yang memberikan detail produk, seperti komponen, komputer, atau program. Datasheet digunakan untuk memberikan detail dan informasi spesifik mengenai komponen tersebut.

Bagian-bagian datasheet:
- Date : Tanggal datasheet dibuat
- General Description : Gambaran umum mengenai komponen
- Features : Fitur fitur dan hal yang menjadi poin plus komponen
- Applications : Contoh penggunaan komponen
- Schematic Diagram : Diagram yang menunjukan representasi sirkuit pada komponen.
- Connection Diagram : Diagram yang menunjukan pin layout untuk panduan koneksi
- Ordering Information : Komponen tambahan yang sudah dipaketkan bersama komponen
- Electrical Characteristic : Informasi tentang limit tegangan dan arus listrik
- Performance Charateristic : Grafik mengenai performa komponen
- Applications Information : Cara penggunaan dan contohnya

Contoh Datasheet
<img src="https://techweb.rohm.com/upload/2016/04/7D_dstop2e.gif" alt="dsd" width="800" />
Datasheet ini menjelaskan mengenai komponen Power Supply yang mengubah input 2.7V menjadi 5.5V dengan kuat arus 3A. Datasheet ini memberikan informasi spesifikasi dan limit input, di bagian fitur terdapat beberapa fiturnya, seperti proteksi proteksi yang dimiliki. Aplikasinya untuk microprocessor, storage device, printer, dan lain-lain. Dan dilampirkan sirkuit aplikasinya.

### Referensi: 
- [1]Computer Hope, “What is a Datasheet?,” www.computerhope.com, Jun. 12, 2024. https://www.computerhope.com/jargon/d/datasheet.htm (accessed September 7, 2025).
- [2]G. Lambert, “How to Read Datasheets and Application Notes,” Circuit Basics, Nov. 08, 2021. https://www.circuitbasics.com/how-to-read-datasheets-and-application-notes/ (accessed September 07, 2025).
- [3]Anonymous, “How to Read Power Supply IC Datasheets: Cover, Block Diagram, Absolute Maximum Ratings and Recommended Operating Conditions | TechWeb,” Rohm.com, 2016. https://techweb.rohm.com/product/power-ic/dcdc/1091/ (accessed September 07, 2025).

## 5. Jelaskan definisi dari Integrated Circuit (IC)! Untuk IC berikut, jelaskan fungsi, konfigurasi pin, dan truth tablenya : (15 poin)
1. IC 7432
2. IC 7408
3. IC 7404

---

Integrated Circuit (IC) merupakan kumpulan komponen listrik yang dibuat untuk muat dalam chip kecil. Dalam kata lain, IC merupakan sirkuit yang sudah diminiaturisasi. IC biasanya adalah modul yang digunakan untuk menambah fungsi pada rangkaian sirkuit.

IC 7432
Fungsi : OR Gate dengan 4 set 2 input.

<img src="https://www.futurlec.com/IC7432.gif"/>

Pin 1 : A Input Gate 1
Pin 2 : B Input Gate 1
Pin 3 : Y Output Gate 1
Pin 4 : A Input Gate 2
Pin 5 : B Input Gate 2
Pin 6 : Y Output Gate 2
Pin 7 : GND
Pin 8 : A Input Gate 3
Pin 9 : B Input Gate 3
Pin 10 : Y Output Gate 3
Pin 11 : A Input Gate 3
Pin 12 : B Input Gate 3
Pin 13 : Y Output Gate 3
Pin 14 : VCC

Truth Table
| Input A | Input B | Output Y |
| ------- | ------- | -------- |
|    L    |    L    |     L    |
|    L    |    H    |     H    |
|    H    |    L    |     H    |
|    H    |    H    |     H    |

IC 7408
Fungsi : AND Gate dengan 4 set 2 input.

<img src="https://www.futurlec.com/IC7408.gif"/>

Pin 1 : A Input Gate 1
Pin 2 : B Input Gate 1
Pin 3 : Y Output Gate 1
Pin 4 : A Input Gate 2
Pin 5 : B Input Gate 2
Pin 6 : Y Output Gate 2
Pin 7 : GND
Pin 8 : A Input Gate 3
Pin 9 : B Input Gate 3
Pin 10 : Y Output Gate 3
Pin 11 : A Input Gate 3
Pin 12 : B Input Gate 3
Pin 13 : Y Output Gate 3
Pin 14 : VCC

Truth Table
| Input A | Input B | Output Y |
| ------- | ------- | -------- |
|    L    |    L    |     L    |
|    L    |    H    |     L    |
|    H    |    L    |     L    |
|    H    |    H    |     H    |


IC 7404
Fungsi : Hex Inverter dengan 6 input

<img src="https://www.futurlec.com/IC7404.gif"/>

Pin 1 : A Input Gate 1
Pin 2 : Y Output Gate 1
Pin 3 : A Input Gate 2
Pin 4 : Y Output Gate 2
Pin 5 : A Input Gate 3
Pin 6 : Y Output Gate 3
Pin 7 : GND
Pin 8 : A Input Gate 4
Pin 9 : Y Output Gate 4
Pin 10 : A Input Gate 5
Pin 11 : Y Output Gate 5
Pin 12 : A Input Gate 6
Pin 13 : Y Output Gate 6
Pin 14 : VCC

Truth Table
| Input A | Output Y |
| ------- | -------- |
|    L    |     H    |
|    H    |     L    |

### Referensi: 
- [1]Ø. N. Dahl, “What is an Integrated Circuit (IC)?,” Build Electronic Circuits, Apr. 03, 2023. https://www.build-electronic-circuits.com/integrated-circuit/ (accessed September 07, 2025).
- [2]Anonymous, “7432 Technical Data,” Futurlec.com, 2019. https://www.futurlec.com/74/IC7432.shtml (accessed September 07, 2025).
- [3]Ovaga , “7408 Integrated Circuit Datasheet: Pinout, Pin Diagram, Truth Table - Ovaga Technologies,” Ovaga.com, 2023. https://www.ovaga.com/blog/transistor/7408-integrated-circuit-datasheet-pinout-pin-diagram-truth-table?srsltid=AfmBOor1almJuj8ucAZdxUKF7opaPzcroOmMnFQgKwPQi8cxIC6MjHMY (accessed September 07, 2025).
- [4]Allelco, “IC 7404 Comprehensive Guide - Truth Table, Uses, Pros and Cons, Applications, Pinouts,” Allelco.com. https://www.allelcoelec.com/blog/ic-7404-comprehensive-guide-truth-table,uses,pros-and-cons,applications,pinouts.html (accessed September 07, 2025).

## 6. Follow the scenario below! (25 points)
Magus, seorang mahasiswa baru di Institute Magical Engineering diterima di jurusan Magis Teknis. Hari pertama, ia dipanggil ke ruang kuliah besar oleh dosen eksentrik Prof. Bitwise. Ruangannya penuh gulungan kabel, kristal menyala, dan papan tulis yang menulis sendiri.

Prof. Bitwise Berucap:
`Selamat datang di Magis Teknis. Kalian mungkin berpikir sihir itu soal mantra megah, tapi kenyataannya dunia ini berjalan dengan sirkuit digital! Tegangan, ground, input, output… semua itu adalah jantung dari peradaban magis modern. Hari ini kau akan membuktikannya.`

Tugas pertama Magus: menyalakan Orbium Lamp(LED), sebuah bola cahaya kampus yang hanya bisa hidup bila rangkaian dasarnya benar. Bila salah? Bola itu akan meledak dengan tawa menakutkan dan mengubah rambut mahasiswa jadi antena selamanya dengan menggunakan alat [TinkerCAD](https://www.tinkercad.com), buatlah simulasi untuk menyalakan 3 lampu menggunakan 1 sakelar dengan persyaratan untuk sakelar lampu tersebut adalah sebagai berikut:
1. Lampu harus berwarna putih.
2. Resistor 220 ohm.
3. Warna kabel harus sesuai dengan warna Ground dan VCC.

Sertakan **SCREENSHOT** dan **LINK** ke simulasi Tinkercad.

Pastikan anda sudah membuat akun tinkercad dan mengubah setting privacy tautannya menjadi **PUBLIK**. Berikut caranya:
1. Buka properti sirkuit yang Anda buat dari menu "Your designs".
<img src="https://hackmd.io/_uploads/SJFn--OhA.png" alt="dsd" width="200" />
3. Ubah pengaturan privasi menjadi "public".  
<img src="https://hackmd.io/_uploads/r13aZ-O2A.png" alt="dsd" width="500" />
4. Klik sirkuit Anda.
5. Klik "Copy link".  
<img src="https://hackmd.io/_uploads/Hy-0ZZ_n0.png" alt="dsd" width="500" />

Example: https://www.tinkercad.com/things/4EMnaTkC1Sp-ptdsfds1bryanherdianto2306210885

Pastikan juga bahwa screenshot menangkap seluruh bagian dari window. Contoh:  
<img src="https://hackmd.io/_uploads/r111JMOhR.png" alt="dsd" width="700" />
Format nama yang digunakan untuk rangkaian simulasi tinkercad anda untuk saat ini mengikuti format penamaan TP modul ini yaitu :
**"TP_DSD1_NamaLengkap_NPM"**

---

Screenshot: <img src="https://hackmd.io/_uploads/H1w0zXjcll.png" />

Link: https://www.tinkercad.com/things/9Lr21SWfT0D-tpdsd1benianaus-kenneth-indarwan2506539920?sharecode=iKiffP_QUK0GVpboJ1U06b6-U4m2H5yrPSnqd2pBYFM
