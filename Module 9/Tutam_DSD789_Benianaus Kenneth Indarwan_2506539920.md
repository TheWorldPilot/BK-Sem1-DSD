---
title: Tugas Tambahan - Modul 789 (Register & Counter)

---

---
title: Tugas Tambahan - Modul 789 (Register & Counter)

---

# Tugas Tambahan - Modul 789 (Register & Counter)

Pembuat Soal: DY

```
Nama: Benianaus Kenneth Indarwan
Kelompok: A27
```

**`NOTE: TENANG! KALIAN TIDAK MEMBUAT RANGKAIAN INI DARI AWAL. LANGSUNG GUNAKAN FILE .pdsprj YANG TELAH DISEDIAKAN.`**

## Finite State Machine
`NOTE: Silahkan skip narasi ini jika malas.`

<details>
<summary>Doksli Narasi
    </summary>
Liburan musim panas telah berakhir. Rintarou dan Kaoruko kembali ke kampus, namun kali ini, semuanya terasa berbeda. Mereka tidak lagi berjalan canggung berdampingan; Rintarou kini berjalan di samping Kaoruko, menggenggam tangannya.

Pengakuan di pantai malam itu, disinari cahaya kembang api, berjalan sukses. Perasaan Rintarou yang up-counter-nya telah mencapai '9', ternyata tidak 'reset' kembali ke '0'. Kaoruko menerimanya.

Mereka duduk di perpustakaan untuk mengerjakan tugas tambahan terakhir, mungkin yang terakhir kalinya untuk mata kuliah ini. Rintarou membuka file Proteus yang disediakan.

"Tugas terakhir," kata Rintarou sambil tersenyum. "Lihat ini, tentang `Finite State Machine`."

Kaoruko mendekat untuk melihat layar laptop Rintarou. "Sistem Login? Memverifikasi password?"

"Mirip seperti kita, ya," kata Rintarou.

Kaoruko menatapnya bingung, lalu tersipu. "Hah? Maksudmu?"

Rintarou menunjuk ke daftar state di soal. "Lihat. Sebelum liburan, kita berada di `State: Login (000)`, hanya teman."

"Lalu," lanjutnya, "Di pantai, aku `State: Input Password (001)`."

Kaoruko tertawa pelan. "Dan aku butuh beberapa detik untuk `State: Verifikasi Password (010)...`"

Rintarou tersenyum, menatap mata Kaoruko. "Dan sekarang?"

Kaoruko menunjuk ke baris berikutnya. "Sekarang, kita di `State: Berhasil Login/ACC (011)`."

"Tepat," kata Rintarou. "Dan aku harap kita bisa lanjut ke `State: Save Password (101)`. Menyimpan 'state' baru ini."

"Dasar bodoh," kata Kaoruko sambil tersenyum bahagia. "Ayo selesaikan tugas terakhir kita."
</details>

Finally, Anda berhasil melewati semua permintaan Magus. Namun sudah saatnya, sebuah peristiwa yang sudah ditakdirkan terjadi. Perpisahan antara Anda dan Magus sudah dekat karena liburan yang kalian alami sangat berbeda, serta Portal yang selama ini menghubungkan Anda dengan Magus mulai hilang. 

![Real face MAGUS ðŸ˜±](https://hackmd.io/_uploads/H1nehqOeZg.png)
"Yo kawan, terimakasih untuk semuanya selama ini. Sudah kuduga kau adalah partner terbaik yang pernah ada, tanpa mu mungkin Aku tidak akan sampai titik ini. Libur semester sebentar lagi dan kita akan berpisah, untuk itu ini adalah hadiah dariku, sebuah blueprint dari alat khusus yang ku rancang untuk sistem keamanan, cobalah membuatnya."

## Cara Kerja Sistem
Anda akan membuat sebuah finite state machine yang memiliki beberapa state, yaitu:

### 1. Login (000)
State ini merupakan `Home` atau tampilan awal dari sistem ini.

### 2. Input Password (001)
User melakukan input Password yang ditampilkan pada 7 Segment. Untuk awal saat mesin ini dinyalakan, Password default-nya adalah `0000`.

### 3. Verifikasi Password (010)
Sistem memverifikasi Password. Jika `BENAR` maka akan lanjut ke state `Berhasil Login/ACC`. Jika `SALAH` maka akan kembali ke state `Login`.

### 4. Berhasil Login/ACC (011)
Pada state ini akan menampilkan tulisan `ACC` di 7 segment, menandakan Password benar dan berhasil login.

### 5. Change Password (100)
Jika User menekan `Next` lagi saat berada di `Berhasil Login/ACC`, maka akan langsung memasuki menu `Change Password`. User melakukan input Password baru. Menekan `Next` akan lanjut ke state `Save Password`.

### 6. Save Password (101)
Disini sistem akan memperbarui Password yang tersimpan di register dan kembali ke `Login`.

### 7. Reset
Ini bukan state, ini adalah tombol `HARD_RESET` manual yang terhubung ke `seluruh reset` pada sistem. 

### 8. Clear
Ini bukan state, ini adalah tombol `CLEAR` yang akan menghapus input saat ini.


## State Table

`Note: Q adalah current, Q' adalah next.`

`Note: ACC adalah flag input tambahan ketika Verifikasi Password, selain state tersebut akan Don't Care. Namun agar mudah disederhanakan dengan K-Map, tabel ini akan menjadi 4 input lengkap dari 0000 hingga 1111. Jadi jangan bingung jika ada Next State yang double. Pada Proteus, ACC akan menjadi Q0`

`Note: Input 1100 hingga 1111 outputnya X (Don't Care).`

`Note: Jika edit ini di HackMD, geser pembatas tengah agar tabel terlihat lebih baik.`

<span style="color:green;">**TODO 1 : Lengkapi '?' pada state table berikut sesuai dengan State nya dalam biner.**</span>


|Current State| Q3 | Q2 | Q1 | ACC | Next State  |Q'3 |Q'2 |Q'1 |
|------------ |----|----|----|-----|-------------|----|----|----|
| Login       | 0  | 0  | 0  |  0  | Input Pass  | 0  | 0  | 1  |
| Login       | 0  | 0  | 0  |  1  | Input Pass  | 0  | 0  | 1  |
| Input Pass  | 0  | 0  | 1  |  0  | Verif Pass  | 0  | 1  | 0  |
| Input Pass  | 0  | 0  | 1  |  1  | Verif Pass  | 0  | 1  | 0  |
| Verif Pass  | 0  | 1  | 0  |  0  | Login       | 0  | 0  | 0  |
| Verif Pass  | 0  | 1  | 0  |  1  | ACC         | 0  | 1  | 1  |
| ACC         | 0  | 1  | 1  |  0  | Change Pass | 1  | 0  | 0  |
| ACC         | 0  | 1  | 1  |  1  | Change Pass | 1  | 0  | 0  |
| Change Pass | 1  | 0  | 0  |  0  | Save Pass   | 1  | 0  | 1  |
| Change Pass | 1  | 0  | 0  |  1  | Save Pass   | 1  | 0  | 1  |
| Save Pass   | 1  | 0  | 1  |  0  | Login       | 0  | 0  | 0  |
| Save Pass   | 1  | 0  | 1  |  1  | Login       | 0  | 0  | 0  |
| ...         | 1  | 1  | 0  |  0  | ...         | X  | X  | X  |

## K-Map
<span style="color:green;">**TODO 2 : Lengkapi K-Map untuk mencari Q'1 Q'2 Q'3 untuk menjadi input pada D Flip-Flop.**</span>

### 1. Q'1
| Q3,Q2\Q1,ACC | 00  | 01  | 11  | 10  |
|--------------|-----|-----|-----|-----|
| **00**       |  1  |  1  |  0  |  0  |
| **01**       |  0  |  1  |  0  |  0  |
| **11**       |  X  |  X  |  X  |  X  |
| **10**       |  1  |  1  |  0  |  0  |

![image](https://hackmd.io/_uploads/S1vyCM0eZg.png)

Q'1 = Q1'Q2'+Q1'ACC

### 2. Q'2
| Q3,Q2\Q1,ACC | 00  | 01  | 11  | 10  |
|--------------|-----|-----|-----|-----|
| **00**       |  0  |  0  |  1  |  1  |
| **01**       |  0  |  1  |  0  |  0  |
| **11**       |  X  |  X  |  X  |  X  |
| **10**       |  0  |  0  |  0  |  0  |

![image](https://hackmd.io/_uploads/H1l-0MRgZl.png)

Q'2 = Q1Q2'Q3'+Q1'Q2ACC

### 3. Q'3
| Q3,Q2\Q1,ACC | 00  | 01  | 11  | 10  |
|--------------|-----|-----|-----|-----|
| **00**       |  0  |  0  |  0  |  0  |
| **01**       |  0  |  0  |  1  |  1  |
| **11**       |  X  |  X  |  X  |  X  |
| **10**       |  1  |  1  |  0  |  0  |

![image](https://hackmd.io/_uploads/Hk6MAG0gWl.png)

Q'3 = Q1Q2+Q1'Q3


## Rangkaian Proteus
<span style="color:green;">**TODO 3 : Buat rangkaian proteus.**</span>
Implementasikan hasil persamaan dari K-Map tersebut ke D Flip-Flop pada template proteus.
![BUAT DI BAGIAN INI AJA](https://hackmd.io/_uploads/HkFSATIgWg.png)

![image](https://hackmd.io/_uploads/H1tmIQAe-x.png)



## Link Youtube Penjelasan
<span style="color:green;">**TODO 4 : Bukti keberhasilan, video penjelasan.**</span>
Maksimal 3 menit, berisi:
- Menjelaskan keseluruhan state dari LOGIN sampai SAVE_PASSWORD.
- Memperlihatkan kondisi Password Salah
- Memperlihatkan kondisi Password Benar
- Memperlihatkan Password berhasil diubah

LINK: https://youtu.be/TrwtTZB9CJk

![Tamat....??](https://hackmd.io/_uploads/H1LMA5ug-e.png)