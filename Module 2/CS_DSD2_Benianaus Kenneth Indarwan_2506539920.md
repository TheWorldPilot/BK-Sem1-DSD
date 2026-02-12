---
title: Case Study - Boolean Algebra And Basic Logic Gates

---

# Case Study - Boolean Algebra And Basic Logic Gates

Nama: Benianaus Kenneth Indarwan
NPM: 2506539920
Kelompok : A27
Rekan Kerja : Benedict Jaysen Riofo Panjaitan

## 1. Praktikum - Buatlah rangkaian asli secara fisik yang memenuhi ketentuan sesuai kriteria berikut! (60 Poin)

Pada saat TP, kalian sudah membuat rangkaian digital di tinkercad untuk membantu Magus dalam melewati pintu. Sekarang, setelah masuk pintu pertama, Magus dihadapkan pada pintu kedua yang memerlukan fungsi baru dengan kriteria menjadi : 
- (Tidak **Benar** dan **Huruf**) atau (**Angka** dan Tidak **Benar**)

Bantulah Magus dalam merancang lagi dalam bentuk rangkaian Digital secara FISIK.

### Truth Table (Sesuaikan variabel A, B, C dengan kriteria Angka, Benar, Huruf) :

A: Angka, B: Benar, C: Huruf

|  A  |  B  |  C  | Output |
|-----|-----|-----|--------|
|  0  |  0  |  0  |   0    |
|  0  |  0  |  1  |   1    |
|  0  |  1  |  0  |   0    |
|  0  |  1  |  1  |   0    |
|  1  |  0  |  0  |   1    |
|  1  |  0  |  1  |   1    |
|  1  |  1  |  0  |   0    |
|  1  |  1  |  1  |   1    |

Fungsi Boolean : 
`Contoh : F(A,B,C) = A+B+C (GANTI INI DENGAN JAWABAN ANDA!)`
**F(A,B,C) = (B'C)+(AB')**

### Foto Bukti Rangkaian Fisik per-kombinasi Input : 

`ganti tanda "?" di kolom output pada truth table di bawah  dengan foto rangkaian fisik anda yang menampilkan output , contoh :`
|  A  |  B  |  C  | Output |
|-----|-----|-----|--------|
|  1  |  1  |  1  |![image](https://hackmd.io/_uploads/BJJObBZaC.png)|

`Rangkaian di atas ini cuma contoh`

|  A  |  B  |  C  | Output |
|-----|-----|-----|--------|
|  0  |  0  |  0  |![000](https://hackmd.io/_uploads/HysuDMKixg.jpg)|
|  0  |  0  |  1  |![010](https://hackmd.io/_uploads/rkwFPztiel.jpg)|
|  0  |  1  |  0  |![001](https://hackmd.io/_uploads/ryfKPfKjlx.jpg)|
|  0  |  1  |  1  |![100](https://hackmd.io/_uploads/r1gRFPzYoxl.jpg)|
|  1  |  0  |  0  |![011](https://hackmd.io/_uploads/r1iFwfFiee.jpg)|
|  1  |  0  |  1  |![111](https://hackmd.io/_uploads/B1xsPzFogx.jpg)|
|  1  |  1  |  0  |![101](https://hackmd.io/_uploads/HJX9wGtjlx.jpg)|
|  1  |  1  |  1  |![110](https://hackmd.io/_uploads/HJhqDfYsxl.jpg)|

## 2. Teori - Asumsikan Anda telah berhasil membuat rangkaian ini. Akan tetapi, Anda diminta untuk menyalakan lampu lain untuk setiap output yang bernilai `0` dari fungsi yang Anda buat dan hanya boleh menambah 1 IC yang ada (IC 7408, 7432, 7404), IC apa yang akan Anda tambahkan? dan apa jelaskan alasan Anda menggunakan IC tersebut? (10 poin)


IC yang akan ditambahkan adalah IC 7404 (Hex Inverter). Alasannya untuk mengubah output yang nilainya 0 ke nilai 1, dan dihubungkan dengan lampu kedua. Sehingga lampu kedua akan menyala apabila lampu pertama tidak menyala.

## 3. Teori - Misalkan IC 7408 (AND) dilarang digunakan pada praktikum ini, bagaimana cara Anda untuk berhasil menghasilkan output yang tetap benar sesuai fungsi nya hanya dengan menggunakan IC yang tidak dilarang (IC 7404 dan 7432 saja)? (10 poin)

`HINT = De Morgan's theorem, jangan lupa tulis fungsi baru kalian di bawah`

Berdasarkan De Morgan's theorem, **(XY)' = X'+Y'**
Dari fungsi awal dimana **F(A,B,C) = (B'C)+(AB')**, berubah menjadi fungsi 
F = (B'C)+(AB')
F = ((B'C)')' + ((AB')')'
**F = (B+C')' + (A'+B)'**

## 4. Analisis & Kesimpulan - Berikan analisis dan kesimpulan untuk percobaan praktikum kali ini! Analisis harus dalam bentuk paragraf dan mendeskripsikan apa yang kalian lakukan di praktikum ini beserta tujuannya. Kesimpulan harus disajikan dalam bentuk poin (minimal 3 poin) ! (20 poin)

### Analisis: 
Percobaan praktikum ini bertujuan untuk mengejar mengenai penggunaan kombinasi beberapa IC untuk menguji fungsi boolean yang telah dibuat. Komponen yang diperlukan adalah switch dan LED (bisa diganti dengan *Vulcan*), kabel jumper, *Arduino* sebagai power supply, dan IC 7404, 7408, 7432. Semua komponen tersebut disusun berdasarkan fungsi Boolean yang dibuat dan hasilnya seharusnya sama dengan truth tables di awal.

Kesimpulannya, komponen-komponen harus diatur dengan presisi agar tidak menimbulkan kesalahan pembacaan (*floating*) pada lampu test (LED). Selain itu, juga diperlukan untuk mengetes komponen untuk dapat menentukan apakah komponen atau kabel mengalami malfungsi, karena apabila tidak dites terlebih dahulu akan membuat progress anda sia-sia dan anda harus mengulang lagi. Kita harus berhati-hati dengan komponen terutama pada pinnya karena mudah mengalami kerusakan. 

Selain itu juga diperlukan untuk memastikan kembali karena pada percobaan ini, kami mengalami perbedaan pada truth tables dan foto rangkaian. Hal ini dapat terjadi karena kesalahan pada IC, atau karena rangkaian yang kurang tepat yang bisa disebabkan karena kekurangan waktu atau malfungsi komponen; maka sangat perlu diperhatikan dan dicek dan dites kembali.

### Kesimpulan:
- Perlu mengetes dan memilih komponen yang cocok untuk memastikan agar rangkaian dapat bekerja dengan baik
- Perlu memastikan agar pembacaan tidak dalam kondisi *floating* dengan cara memastikan pin terkoneksi dengan benar
- Untuk mempermudah dapat membuat rangkaian terlebih dahulu di TinkerCad sehingga mengurangi resiko kerusakan komponen
- Harus siap ketika menghadapi komponen yang rusak
- Apabila terdapat perbedaan truth tables dan hasil fisik, perlu dilihat lagi komponen apakah bermasalah atau kesalahan pada rangkaian
