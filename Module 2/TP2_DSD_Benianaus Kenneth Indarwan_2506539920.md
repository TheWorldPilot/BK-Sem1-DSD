---
title: Tugas Pendahuluan - Boolean Algebra And Basic Logic Gates

---

# Tugas Pendahuluan - Boolean Algebra And Basic Logic Gates

Nama: Benianaus Kenneth Indarwan
NPM: 2506539920

## 1. Teori - bagaimana cara menghubungkan input `1` atau `0` ke IC pada breadboard? dan bagaimana salah satu cara menunjukkan outputnya? (contohnya salah satu IC saja (7404/7408/7432)) (10 poin)

Cara untuk menghubungkan input `1` ke IC adalah dengan mengambil input dari `VCC (+)`. Sedangkan, jika ingin menghubungkan input `0`, maka mengambil input dari `GND (-)`.
Untuk menunjukkan output salah satu cara yang sederhana adalah menggunakan LED. Jika outputnya `0`, LED mati; jika outputnya `1`, LED menyala.

### Referensi: 
- [1]I. Jayasekara, “Let’s see how can we get the correct output from a Logic IC.,” Medium, Aug. 14, 2021. https://medium.com/@jpisiwarani/lets-see-how-can-we-get-the-correct-output-from-a-logic-ic-42c993f2994d (accessed September 14, 2024).
- [2]Anonymous, “Basic Gate Function | Digital Integrated Circuits | Electronics Textbook,” www.allaboutcircuits.com. https://www.allaboutcircuits.com/textbook/experiments/chpt-7/basic-gate-function/ (accessed Sep. 14, 2025).

## 2. Teori - Selain `0` dan `1`, terdapat satu lagi state di dalam sistem digital yang harus Anda ketahui yaitu `Floating`. Apa yang dimaksud floating dan apa bedanya dengan state `0` ? (10 poin)


Floating state adalah keadaan ketika pin tidak terhubung, tetapi mengeluarkan sinyal `0` dan `1` secara random. Perbedaannya dengan state `0` adalah ketika state `0` berarti data yang dikirimkan benar-benar tidak ada. Sedangkan, pada keadaan floating, sinyal tidak benar-benar hilang dan ada fluksuasi, sehingga tidak bisa terbaca dengan benar.

### Referensi: 
- [1]M. Parks, “Don’t Leave Your Pins Floating | Bench Talk,” Mouser.com, 2018. https://www.mouser.com/blog/dont-leave-your-pins-floating?srsltid=AfmBOopRWcU-1UaU_eJesVDFiXKEfWr8LjMgFLm0VT4lvSBzduMh_4RC (accessed September 14, 2025).
- [2]R. Lee, “Understanding Floating State in Arduino - Ninniku IT Hub,” Ninniku IT Hub, Mar. 05, 2023. https://www.ninniku.tw/understanding-floating-state-in-arduino/ (accessed September 14, 2025).


## 3. PreCS - (80 poin)
Setelah berhasil menyalakan Orbium Lamp, Magus harus masuk ke Labirin Biner. Dinding-dindingnya penuh pintu besi, dan di atasnya tertulis simbol aneh: **AND, OR, NOT**.

Sebuah suara bergema:
`Aku adalah penjaga logika. Jika kau ingin lewat, kau harus membuktikan bahwa dunia bisa dijelaskan hanya dengan benar (1) dan salah (0). Satu ekspresi salah, dan kau akan tersedot ke dimensi ERROR 404.`

Magus harus menuliskan persamaan Boolean yang benar untuk membuka setiap pintu. Suara pintu mengejek tiap kali ia salah. Pintu pertama hanya terbuka jika :
- **Benar** atau (tidak **Angka** dan tidak **Huruf**)

Bantulah Magus merancang untuk melewati tantangan ini dalam bentuk rangkaian Digital (Tinkercad)!

### Fungsi Boolean : 

**`F(A,B,C) = B+(A'C')`**

`HINT : Sebenarnya jawabannya sudah ada di soal. Tinggal kalian ubah saja kata-katanya ke dalam bentuk aljabar boolean`

### Truth Table (Sesuaikan variabel A, B, C dengan kriteria Angka, Benar, Huruf. Misal A = Angka, B = Benar dan C = Huruf, lalu ganti '?' dengan hasil fungsi yang sudah dibuat) :
|  A  |  B  |  C  | Output |
|-----|-----|-----|--------|
|  0  |  0  |  0  |   1    |
|  0  |  0  |  1  |   0    |
|  0  |  1  |  0  |   1    |
|  0  |  1  |  1  |   1    |
|  1  |  0  |  0  |   0    |
|  1  |  0  |  1  |   0    |
|  1  |  1  |  0  |   1    |
|  1  |  1  |  1  |   1    |

### Screenshot Bukti Rangkaian per-kombinasi Input : 

`ganti tanda "?" di kolom output pada truth table di bawah  dengan screenshot rangkaian anda yang menampilkan output , contoh :`
|  A  |  B  |  C  | Output |
|-----|-----|-----|--------|
|  1  |  1  |  1  |![image](https://hackmd.io/_uploads/HJ38U4WaC.png)|

`Rangkaian di atas ini cuma contoh aja yaa, bukan jawaban TP. Rangkaian asli untuk jawaban TP nya beda.`

|  A  |  B  |  C  | Output |
|-----|-----|-----|--------|
|  0  |  0  |  0  |![image](https://hackmd.io/_uploads/B13da-Esxg.png)|
|  0  |  0  |  1  |![image](https://hackmd.io/_uploads/r1HtTW4jlg.png)|
|  0  |  1  |  0  |![image](https://hackmd.io/_uploads/HkAtpZ4oxl.png)|
|  0  |  1  |  1  |![image](https://hackmd.io/_uploads/HkLc6-Vsgl.png)|
|  1  |  0  |  0  |![image](https://hackmd.io/_uploads/SJ-jTW4oxg.png)|
|  1  |  0  |  1  |![image](https://hackmd.io/_uploads/S1_sabNogx.png)|
|  1  |  1  |  0  |![image](https://hackmd.io/_uploads/SkRsp-4sgx.png)|
|  1  |  1  |  1  |![image](https://hackmd.io/_uploads/BkN2p-4jex.png)|

### Link: 
https://www.tinkercad.com/things/cb3DdvcY7p2-cs2dsdbenianaus-kenneth-indarwan2506539920

