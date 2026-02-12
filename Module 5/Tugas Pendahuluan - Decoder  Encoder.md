# Tugas Pendahuluan - Decoder & Encoder
> Pembuat Soal: NZ

```
Nama    : Cyrene
NPM     : 1234567890
```

## Notes
- Jika ada pertanyaan yang kurang jelas, silahkan tanya di server Discord Digital Lab
- Referensi harus dalam format IEEE (Kamu boleh menggunakan https://www.mybib.com/tools/ieee-citation-generator biar lebih gampang). Referensi minimal dua

## Teori (30 Poin)

### 1. Jelaskan apa itu `Decoder` dan `Encoder`, beserta dengan fungsi dan contoh aplikasinya.

[Jawab di sini]

### Referensi: 
- Author, “Title,” Website_Name, publication date. https://exampleURL (accessed date).

### 2. Sebutkan dan jelaskan perbedaan `Decoder` dan `Encoder` secara komprehensif

[Jawab di sini]

### Referensi: 
- Author, “Title,” Website_Name, publication date. https://exampleURL (accessed date).

### 3. Jelaskan apa itu `Priority Encoder` Sebutkan satu saja contoh praktik/kegunaan dari `Priority Encoder` yang sebenarnya ada di dalam kehidupan sehari-hari/lingkungan sekitar kalian

[Jawab di sini]

### Referensi: 
- Author, “Title,” Website_Name, publication date. https://exampleURL (accessed date).

## Intro to Proteus (30 poin)

### 4. Mulai pekan ini dan seterusnya, kalian akan berpindah dari Tinkercad ke Proteus. Dengan menggunakan Proteus, buatlah sebuah rangkaian sederhana yang dapat menyalakan satu lampu LED (warna terserah kalian) menggunakan pin power, ground dan komponen switch. Jangan lupa untuk memberikan Teks berupa Nama_NPM pada rangkaian sesuai video tutorial yang sudah diberikan di Emas3. (10 poin)
`Note Untuk kedepannya, rangkaian pada Proteus harus selalu disertakan dengan teks nama_NPM. Jika tidak ada, maka nilainya akan dikurangi`

**Screenshot Rangkaian:**
![NZ's first wife](https://hackmd.io/_uploads/HJkRIX32el.jpg)

### 5. Buatlah kembali rangkaian yang kalian bikin di CS modul lalu (Modul Complex Logic Gate), namun sekarang gunakan proteus. (20 poin)

**Screenshot Rangkaian:**

![NZ's second wife](https://hackmd.io/_uploads/S1eUP7h2gg.jpg)


## Praktik (40 Poin)

### 6. Pada CS nanti dan beberapa modul-modul selanjutnya, kalian akan menggunakan salah satu decoder ysng paling sering dipakai: BCD to 7-Segment decoder. Buatlah isi dari decoder ini menggunakan IC saja. 

#### Truth Table (15 poin)

| A   | B   | C   | D   | a   | b   | c   | d   | e   | f   | g   |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 0   | 0   | 0   | 0   |     |     |     |     |     |     |     |
| 0   | 0   | 0   | 1   |     |     |     |     |     |     |     |
| 0   | 0   | 1   | 0   |     |     |     |     |     |     |     |
| 0   | 0   | 1   | 1   |     |     |     |     |     |     |     |
| 0   | 1   | 0   | 0   |     |     |     |     |     |     |     |
| 0   | 1   | 0   | 1   |     |     |     |     |     |     |     |
| 0   | 1   | 1   | 0   |     |     |     |     |     |     |     |
| 0   | 1   | 1   | 1   |     |     |     |     |     |     |     |
| 1   | 0   | 0   | 0   |     |     |     |     |     |     |     |
| 1   | 0   | 0   | 1   |     |     |     |     |     |     |     |
| 1   | 0   | 1   | 0   |     |     |     |     |     |     |     |
| 1   | 0   | 1   | 0   |     |     |     |     |     |     |     |
| 1   | 1   | 0   | 1   |     |     |     |     |     |     |     |
| 1   | 1   | 0   | 0   |     |     |     |     |     |     |     |
| 1   | 1   | 1   | 1   |     |     |     |     |     |     |     |
| 1   | 1   | 1   | 0   |     |     |     |     |     |     |     |

#### KMAP (15 poin)
>a

| AB/CD | 00  | 01  | 11  | 10  |
| ----- | --- | --- | --- | --- |
| 00    |     |     |     |     |
| 01    |     |     |     |     |
| 11    |     |     |     |     |
| 10    |     |     |     |     |

>b

| AB/CD | 00  | 01  | 11  | 10  |
| ----- | --- | --- | --- | --- |
| 00    |     |     |     |     |
| 01    |     |     |     |     |
| 11    |     |     |     |     |
| 10    |     |     |     |     |

>c

| AB/CD | 00  | 01  | 11  | 10  |
| ----- | --- | --- | --- | --- |
| 00    |     |     |     |     |
| 01    |     |     |     |     |
| 11    |     |     |     |     |
| 10    |     |     |     |     |

>d

| AB/CD | 00  | 01  | 11  | 10  |
| ----- | --- | --- | --- | --- |
| 00    |     |     |     |     |
| 01    |     |     |     |     |
| 11    |     |     |     |     |
| 10    |     |     |     |     |

>e

| AB/CD | 00  | 01  | 11  | 10  |
| ----- | --- | --- | --- | --- |
| 00    |     |     |     |     |
| 01    |     |     |     |     |
| 11    |     |     |     |     |
| 10    |     |     |     |     |

>f

| AB/CD | 00  | 01  | 11  | 10  |
| ----- | --- | --- | --- | --- |
| 00    |     |     |     |     |
| 01    |     |     |     |     |
| 11    |     |     |     |     |
| 10    |     |     |     |     |

>g

| AB/CD | 00  | 01  | 11  | 10  |
| ----- | --- | --- | --- | --- |
| 00    |     |     |     |     |
| 01    |     |     |     |     |
| 11    |     |     |     |     |
| 10    |     |     |     |     |

#### Screenshot Rangkaian (10 poin)
![NZ'S Wives](https://hackmd.io/_uploads/rJOti72neg.jpg)


