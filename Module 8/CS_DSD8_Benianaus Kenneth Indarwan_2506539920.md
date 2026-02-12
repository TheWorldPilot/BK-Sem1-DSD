---
title: Case Study 1 - Rangkaian Sequential (Latch & Flip-Flop)

---

---
title: Case Study 1 - Rangkaian Sequential (Latch & Flip-Flop)

---

# Case Study - Rangkaian Sequential (Latch & Flip-Flop)

###### Pembuat Soal : KZ

```
Nama  : Benianaus Kenneth Indarwan
NPM   : 2506539920
```
---
## Deskripsi Sistem

Sebuah gedung parkir pintar memiliki sistem kontrol gerbang otomatis yang menggunakan kombinasi latch dan flip-flop. Sistem ini dirancang untuk mengatur status gerbang masuk berdasarkan dua kondisi:

1. **Kartu Akses (menggunakan SR Latch)**
2. **Sensor Kendaraan (menggunakan T Flip-Flop dari D Flip-Flop)**

Gerbang memiliki dua status: **TERTUTUP** dan **TERBUKA**. Gerbang hanya akan terbuka jika kedua kondisi terpenuhi secara bersamaan.

---

### Komponen Sistem

#### 1. **SR Latch untuk Kartu Akses**
- Digunakan untuk memvalidasi kartu akses pengguna
- Diimplementasikan menggunakan gerbang logika **NOR** atau **NAND**
- Input **S (Set)** dihubungkan ke switch yang mewakili "Kartu Valid"
- Input **R (Reset)** dihubungkan ke switch yang mewakili "Kartu Ditolak/Dicabut"
- Ketika switch **Set** ditekan (kartu valid terdeteksi), latch diaktifkan dan status menjadi "Authorized"
- Jika switch **Set** diturunkan, status tetap "Authorized" hingga switch **Reset** ditekan
- **Output Q disambung ke LED**, lalu terhubung ke **gerbang kontrol**

#### 2. **T Flip-Flop dari D Flip-flop untuk Sensor Kendaraan**

![image](https://hackmd.io/_uploads/Sklw-dnJ-e.png)

- Digunakan untuk mendeteksi keberadaan kendaraan di area sensor
- **PENTING**: T Flip-Flop dibuat dari **D Flip-flop**
- D Flip-flop dibuat menggunakan gerbang logika **NAND** atau **NOR** (kalo nemu IC 7474, dan berfungsi boleh aja sih)
- Untuk membuat T Flip-Flop dari D Flip-flop, gunakan gerbang **XOR** untuk menghubungkan output Q dengan input T, kemudian hasil XOR tersebut menjadi input D Flip-flop
- Input **T (Toggle)** disimulasikan dengan switch yang mewakili "Sensor Kendaraan"
- Input **Clock** disimulasikan dengan push button atau clock generator (pake vulcan)
- Setiap kali clock di-trigger dan T=1, status sensor akan toggle (berganti)
- **Output Q dari T Flip-Flop disambung ke LED**, terhubung ke **gerbang kontrol**

#### 3. **Gerbang Kontrol**
- Menggunakan gerbang logika yang sesuai untuk menggabungkan output dari SR Latch dan T Flip-Flop (gunakan AND gate)
- Output akhir terhubung ke LED yang merepresentasikan status gerbang:
  - **LED menyala** = Gerbang TERBUKA
  - **LED mati** atau LED mati = Gerbang TERTUTUP

---

## Ketentuan

1. **SR Latch**: Wajib dibuat menggunakan gerbang logika **NAND** atau **NOR** (pilih salah satu)
2. **D Flip-Flop**: dibuat boleh menggunakan gerbang logika boleh menggunakan IC D Flip-Flop (7474)
3. **T Flip-Flop**: Dibuat dengan menggabungkan D flip-flop yang sudah dibuat dengan gerbang XOR

---

## Tugas Anda

### **Bagian Rangkaian (50 Poin)**

**Buatlah rangkaian lengkap sesuai instruksi di atas dan sertakan:**

1. **Foto rangkaian fisik** yang sudah dirakit di breadboard/project board

2. **Minimal 4 kondisi pengujian** dengan foto yang menunjukkan:
   - Kondisi input (posisi switch S, R, T, dan Clock)
   - Kondisi output (LED dan nilai Q dari masing-masing komponen)
   
   **Contoh kondisi yang harus diuji, secara sekuensial:**
   
| S | R | T | QSR (SR Latch) | QT (T Flip-Flop) | Prediksi Output | Foto rangkaian |
|---|---|---|----------------|------------------|-----------------|-------------|
| 1 | 0 | 0 | 1              | Q sebelumnya (biasanya diawal 0) |0     |![com-0](https://hackmd.io/_uploads/H13FWQXe-g.jpg)             |
| 0 | 0 | 0 | Q sebelumnya   | Q sebelumnya (biasanya diawal 0) |0     |![com-1](https://hackmd.io/_uploads/ry7qWXXgbe.jpg)             |
| 1 | 0 | 1 | 1              | Toggle           | Toggle |![com-2](https://hackmd.io/_uploads/By3qbX7gZg.jpg) ![com-3](https://hackmd.io/_uploads/HJZoWXXlWl.jpg)            |
| 0 | 1 | 1 | 0              | Toggle           | Toggle |![com-4](https://hackmd.io/_uploads/ByyRb7meWx.jpg)![com-5](https://hackmd.io/_uploads/SJMA-QQe-l.jpg) |
| 1 | 1 | 1 | 0              | Toggle           | Toggle |![com-6](https://hackmd.io/_uploads/SJv-MQ7ebe.jpg)![com-7](https://hackmd.io/_uploads/SkFWGmQlbl.jpg) |

```
Keterangan:
Urutan Input (dari kiri) = S, R, T
Urutan Output (dari kiri) = Qsr, Qsr', Qt, (QsrQt)
Input switch S dan R adalah S' dan R' karena menggunakan NAND Gate, di switch terbalik
```

---

## Analisis dan Kesimpulan (50 Poin)

### 1. Jelaskan proses pembuatan T Flip-Flop dari D Flip-Flop secara detail! (10 Poin)
> jelaskan bagaimana D Flip-Flop dibuat dari gerbang logika dasar, cara mengubah D Flip-Flop menjadi T Flip-Flop menggunakan feedback dan XOR gate, dan konfigurasi tersebut dapat menghasilkan fungsi toggle. Perbedaan hasil rangkaian Anda dengan teori (jika ada)

Menggunakan gerbang logika dasar, D Flip-Flop dibuat dengan diagram seperti ini, dengan cara menghubungkan input D dengan salah satu NAND gate, satu lagi di invert. Kemudian kedua output NAND gate dihubungkan ke SR Latch dengan NAND gate. Clock dihubungkan dengan input D di awal.
![image](https://hackmd.io/_uploads/rkHf8N0JZx.png)

Untuk mengubah rangkaian ini menjadi T Flip-Flop, pertama dengan cara menghubungkan input T dengan Output Q dalam XOR gate, kemudian output dari XOR gate akan menggantikan input D pada D Flip-Flop. 
Hasilnya akan menghasilkan output toggle ketika input T adalah `1`, dan ketika input T `0`, akan menyimpan posisi output sebelumnya. Output akan berubah setiap clock berpindah dari posisi OFF ke posisi ON.

---

### 2. Buatlah tabel-tabel berikut: (30 Poin)

a) **Excitation Table** untuk:
   - D Flip-Flop
   
| D | Q | Q<sub>(t+1)</sub> |
|:-:|:-:|:-:|
|0|0|0|
|0|1|0|
|1|0|1|
|1|1|1|
   
   - T Flip-Flop (hasil konversi dari D Flip-Flop)

| T | Q | Q<sub>(t+1)</sub> |
|:-:|:-:|:-:|
|0|0|0|
|0|1|1|
|1|0|1|
|1|1|0|
   
b) **Truth Table SR Latch** yang Anda buat

| S'| R'| Q | Q' |
|:-:|:-:|:-:|:-:|
|1|1|Latch|Latch|
|1|0|0|1|
|0|1|1|0|
|0|0|0|0|

c) **Truth Table lengkap sistem Smart Parking** dengan kolom:
   - Input: S, R, T, Clock
   - Output: Q latch, Q flipflop, Status Gerbang

| S | R | T | Clock | Q<sub>SR</sub> | Q<sub>T(t)</sub> | Q<sub>T(t+1)</sub> | (Q<sub>SR</sub>Q<sub>T</sub>)<sub>(t)</sub> |(Q<sub>SR</sub>Q<sub>T</sub>)<sub>(t+1)</sub> |
|:-:|:-:|:-:|:-----:|:-----:|:-------:|:---------:|:----------------:|:------------------------:|
|0|0|0|0|Latch|0|0|0|0|
|0|0|0|1|Latch|0|1|0|1|
|0|0|1|0|Latch|1|1|1|1|
|0|0|1|1|Latch|1|1|0|0|
|0|1|0|0|0|0|0|0|0|
|0|1|0|1|0|0|1|0|0|
|0|1|1|0|0|1|1|0|0|
|0|1|1|1|0|1|0|0|0|
|1|0|0|0|1|0|0|0|0|
|1|0|0|1|1|0|1|0|1|
|1|0|1|0|1|1|1|1|1|
|1|0|1|1|1|1|0|1|0|
|1|1|0|0|0|0|0|0|0|
|1|1|0|1|0|0|1|0|0|
|1|1|1|0|0|1|1|0|0|
|1|1|1|1|0|1|0|0|0|

---

### 3. Kesimpulan (10 Poin)
>Berikan minimal **3 poin kesimpulan** dari praktikum ini 

- D Flip Flop dapat dibuat dengan mudah menggunakan IC 7474, sehingga tidak memerlukan untuk dibuat rangkaiannya dengan gerbang logika. 
- Pada T Flip-Flop, input akan berubah ketika input T berada di posisi 1 dan pada posisi clock menyala (berubah dari 0 ke 1). Ketika input T di posisi 0, posisi sebelumnya akan tersimpan di output Q. 
- SR Latch bekerja dengan cara sederhana, tetapi penting untuk mengatur posisi switch Reset kembali ke posisi 0 setelah me-reset, karena jika tidak Latch tidak akan bisa berfungsi untuk menyimpan data.
- Tidak selamanya Q dan Q' saling berkebalikan, contohnya pada SR Latch, Q dan Q' bisa bernilai sama ketika Latch baru dinyalakan atau berada dalam kondisi 0 0. 