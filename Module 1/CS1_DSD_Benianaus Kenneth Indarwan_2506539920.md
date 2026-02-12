---
title: Case Study - Introduction to Digital Circuits

---

# Case Study - Introduction to Digital Circuits

Name: Benianaus Kenneth Indarwan  
NPM: 2506539920

## Instruksi
1. Gunakan 1 rangkaian tinkercad baru untuk keseluruhan Case Study modul 1 ini, **jangan memakai yang anda gunakan di TP**  (Tugas Pendahuluan).
2. Sertakan **SCREENSHOT** dan **LINK** ke simulasi Tinkercad Anda di tempat yang sudah disediakan.
3. Ubah nama file/rangkaian tinkercad anda ke `CS_DSD[ModuleNumber]_NamaLengkap_NPM`.
4. Pastikan link tinkercadnya **Shared Link**.
5. Untuk pengerjaan Case Study **tidak perlu** membutuhkan **REFERENSI**
6. Berikan **Jawaban** anda pada **TEMPAT YANG SUDAH DISEDIAKAN**
7. Penting! untuk soal nomor 1, **Ambil tangkapan screenshot rangkaian Tinkercad Anda di setiap langkahnya** 

## 1. Ambil tangkapan screenshot rangkaian Tinkercad Anda di setiap langkah di bawah ini serta jawab pertanyaan yang disediakan bila ada! (50 poin)
1. Buka rangkaian baru di Tinkercad. Tambahkan breadboard small, baterai 9V, LED, dan 7404 ke breadboard. (Jangan hubungkan dulu)
2. Sekarang hubungkan semuanya, hubungkan baterai 9V ke breadboard dengan cara menyambungkan pin `Positive` dan `Negative` pada baterai ke bagian `+` dan `-` pada breadboard. Hubungkan pin Anoda LED (yang lebih panjang) ke bagian `+` dan pin Katoda (yang lebih pendek) ke `-` pada breadboard. Kemudian hubungkan bagian `+` pada breadboard ke pin `Power` (Pin Pojok Kanan Atas) pada 7404 dan bagian `-` pada breadboard ke pin `Ground` (Pin Pojok Kiri Bawah) pada 7404. Yang terakhir, hubungkan bagian `+` pada breadboard ke pin `Input 1` dari 7404. 
**HINT** = Untuk mengetahui nama pin atau bagian pada komponen baik itu lampu,baterai,maupun IC,dll. Anda hanya perlu meng-hover mouse/kursor anda ke bagian pada komponen yang ingin anda ketahui nama pin-nya, contoh : 

![image](https://hackmd.io/_uploads/B1X3HFC9ex.png)

3. Klik "Start Simulation." Apa yang terjadi pada rangkaian, dan kira-kira mengapa?
4. Sekarang tambahkan komponen resistor 1K ohm ke LED . Klik "Start Simulation" lagi. Apa yang terjadi pada rangkaian sekarang? Bagaimana resistor mempengaruhi rangkaian?
5. Ganti baterai 9V dengan power supply. Klik "Start Simulation" lagi. Bagaimana power supply dapat membantu rangkaian anda?
6. **Untuk sesi lab berikutnya, Anda akan menggunakan Arduino sebagai sumber daya**. Sekarang ganti power supply dengan menggunakan Arduino. hubungkan pin `5v` dan `GND` pada arduino (ada di bagian POWER) ke bagian `+` (5V) dan `-`(GND) pada breadboard seperti yang sudah anda lakukan dengan menggunakan power supply dan baterai sebelumnya.
7. Sekarang coba tukar pin LED (hubungkan pin Anoda ke `-` dan pin Katoda ke `+` pada breadboard). Apa yang terjadi, dan mengapa?
8. Kemudian, coba tukar pin 7404 (hubungkan pin Power ke `-` dan pin Ground ke `+` pada breadboard). Apa yang terjadi, dan mengapa?
9. Sekarang perbaiki rangkaian anda kembali persis seperti dalam kondisi sebelum nomer 7. Setelah itu, hubungkan bagian `+` pada breadboard ke pin `Output 1` dari 7404. Apa yang terjadi pada rangkaian, dan mengapa?

Pastikan screenshot mencakup seluruh window dan menyoroti kesalahan dari rangkaian. Contoh : 
<img src="https://hackmd.io/_uploads/SkHqFecnR.png" alt="dsd" width="700" />

Jangan lupa untuk mengubah nama file tinkercad anda ke :
`CS_DSD[ModuleNumber]_NamaLengkap_NPM`

---
| Step  | Screenshot  |
| ----- | ----------- |
| 1     |<img src="https://hackmd.io/_uploads/H1lip3ysxe.png" width="700" /> |
| 2     |<img src="https://hackmd.io/_uploads/rkClk6kjxg.png" width="700" /> |
| 3     |<img src="https://hackmd.io/_uploads/B1CucTysll.png" width="700" /> <img src="https://hackmd.io/_uploads/SkTcc61jee.png" width="700" /> |
| 4     |<img src="https://hackmd.io/_uploads/SkYzj6yoxe.png" width="700" /> |
| 5     |<img src="https://hackmd.io/_uploads/SkfNUakile.png" width="700" /> |
| 6     |<img src="https://hackmd.io/_uploads/HJWk8pyogg.png" width="700" /> |
| 7     |<img src="https://hackmd.io/_uploads/By4kU61sex.png" width="700" /> |
| 8     |<img src="https://hackmd.io/_uploads/B1IkUakile.png" width="700" /> <img src="https://hackmd.io/_uploads/rkVio61olg.png" />
 |
| 9     |<img src="https://hackmd.io/_uploads/SkbehT1jex.png" width="700" /> |

### Jawaban untuk Pertanyaan 3  
IC dan LED akan meledak. LED meledak karena langsung dihubungkan dengan baterai, sehingga kuat arusnya melebihi batas LED. Sedangkan, IC meledak karena tegangannya melebihi batas IC.

### Jawaban untuk Pertanyaan 4  
Sekarang LED menyala. Pengaruh resistor terhadap rangkaian adalah resistor menambah hambatan pada LED sehingga arus yang masuk ke LED tidak lagi berlebih dan lampu bisa menyala tanpa rusak. Tetapi, tegangan yang masuk ke dalam IC melebihi sebelumnya, sehingga IC tetap meledak.

### Jawaban untuk Pertanyaan 5  
Power supply dapat membantu rangkaian karena dengan menggunakan power supply, bisa diatur secara manual tegangannya, yang juga akan mempengaruhi kuat arusnya.

### Jawaban untuk Pertanyaan 7  
LED tidak lagi menyala. Arus positif yang masuk akan masuk ke pin negatif LED sehingga tidak bisa tersalurkan arusnya.

### Jawaban untuk Pertanyaan 8  
Ketika pin `+` dan `-` dibalik maka IC akan meledak. Hal ini karena tegangan yang masuk menjadi `-5 V`, dimana batas IC adalah `-500 mV` dan `7 V`, sehingga tidak sesuai dengan batas dan spesifikasi IC

### Jawaban untuk Pertanyaan 9  
LED akan kembali menyala dengan normal, tetapi IC akan rusak. IC rusak karena kuat arus rangkaian melebihi spesifikasi IC. Hal ini karena IC 7404 adalah IC untuk Hex-Inverter, sehingga ketika arus masuk ke `Input 1`, maka `Output 1` akan mengeluarkan inversenya, yang masuk kembali ke pin positif dan menambah kuat arus listrik.


## 2. Berikan analisis dan kesimpulan untuk percobaan praktikum kali ini! Analisis harus dalam bentuk paragraf, dan kesimpulan harus disajikan dalam bentuk poin (minimal 3 poin). Serta berikan screenshot keseluruhan rangkaian tinkercad (Kondisi pada step 9) anda beserta linknya! (50 poin)

### Screenshot:  
<img src="https://hackmd.io/_uploads/SkbehT1jex.png" width="700" />

### Link:  
https://www.tinkercad.com/things/1WWUYhrh9fT-csdsd1benianaus-kenneth-indarwan2506539920?sharecode=CUC3fQ1VZwWOoaKZlj9RjKl0JyPdXUJpBhZUAgd9RFQ

### Analisis:  
Dalam rangkaian listrik, kita harus memastikan agar arus dan tegangan dalam rangkaian tidak melebihi spesifikasi atau limit dari setiap komponen. Arus `+` dan `-` juga tidak boleh terbalik, karena ada komponen seperti LED yang tidak akan menyala, atau komponen seperti IC yang ketika positif negatifnya terbalik, maka IC akan meledak. 

Untuk memastikan agar arus dan tegangan tidak berlebihan, kita bisa memakai Power Supply sebagai alternatif baterai, karena Power Supply dapat diatur secara manual tegangannya. Atau menggunakan power supply dari Arduino yang hanya 5V. Kemudian, IC 7404 (Hex-Inverter) juga bisa menambahkan arus listrik yang berlebih ketika mengambil input dari rangkaian dan di output di rangkaian itu lagi. Hal ini juga dapat membuat IC meledak. Atau kita bisa menambahkan resistor yang menambah hambatan dan mengurangi arus pada suatu komponen, seperti LED.

Oleh karena itu, dalam merangkai rangkaian penting sekali untuk memastikan bahwa semua komponen, power supply, dan lain-lain terhubung dengan benar dan pastikan bahwa tegangan dari baterai tidak melebihi batas komponennya.

### Kesimpulan:  
- Dalam merangkai rangkaian penting untuk dicek apakah semua koneksi sudah benar dan tegangannya sudah sesuai.
- Tegangan dan kuat arus dapat diatur dengan menggunakan Power Supply yang bisa diatur, atau dengan menambahkan resistor untuk mengurangi kuat arus.
- Ketika `+` dan `-` pada rangkaian dibalik, maka komponen komponen tidak akan menyala atau bahkan meledak. Dalam kasus LED, akan tidak menyala saja; tapi untuk IC akan meledak karena tegangannya tidak sesuai dengan spesifikasi IC.
- IC 7404 dapat membuat arus berlebih ketika IC diinput dari rangkaian dan output dari IC dimasukkan kembali ke dalam rangkaian.