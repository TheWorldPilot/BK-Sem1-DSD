---
title: Case Study 1 - Rangkaian Sequential (Latch & Flip-Flop)

---

# Case Study - Rangkaian Sequential (Latch & Flip-Flop)

###### Pembuat Soal : KZ

```
Nama  : 
NPM   : 
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
| 1 | 0 | 0 | 1              | Q sebelumnya (biasanya diawal 0) |      |             |
| 0 | 0 | 0 | Q sebelumnya   | Q sebelumnya (biasanya diawal 0) |      |             |
| 1 | 0 | 1 | 1              | Toggle           |                 |             |
| 0 | 1 | 1 | 0              | Toggle           |                 |             |

---

## Analisis dan Kesimpulan (50 Poin)

### 1. Jelaskan proses pembuatan T Flip-Flop dari D Flip-Flop secara detail! (10 Poin)
> jelaskan bagaimana D Flip-Flop dibuat dari gerbang logika dasar, cara mengubah D Flip-Flop menjadi T Flip-Flop menggunakan feedback dan XOR gate, dan konfigurasi tersebut dapat menghasilkan fungsi toggle. Perbedaan hasil rangkaian Anda dengan teori (jika ada)

**Jawab Disini**

---

### 2. Buatlah tabel-tabel berikut: (30 Poin)

a) **Excitation Table** untuk:
   - D Flip-Flop
   - T Flip-Flop (hasil konversi dari D Flip-Flop)
   
b) **Truth Table SR Latch** yang Anda buat

c) **Truth Table lengkap sistem Smart Parking** dengan kolom:
   - Input: S, R, T, Clock
   - Output: Q latch, Q flipflop, Status Gerbang

---

### 3. Kesimpulan (10 Poin)
>Berikan minimal **3 poin kesimpulan** dari praktikum ini 

**Jawab Disini**