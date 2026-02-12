---
title: Tugas Tambahan - Module 456 Kamis

---

# Tugas Tambahan - Module 456 
`Pembuat Soal : NA`
```
Nama: Benianaus Kenneth Indarwan
NPM: 2506539920
```

Terimakasih karena sudah membantu Magus selama dua bulan terakhir ini. Anda telah sukses membantunya mendapatkan Nilai tinggi yang ia selalu impikan di dalam kehidupan kuliah ini. Untuk itu Magus memberikan kalian trick portal wiring dan sebuah hadiah kecil.

Diharapkan trick ini bisa membantu Anda menyelesaikan rangkaian-rangkaian kedepannya serta hadiah yang diberikan bisa membuat Anda semakin bersemangat.

## Rangkaian (100 Poin)

Bukalah file proteus yang sudah diberikan dan kerjakan rangkaian dengan cara melengkapi rangkaian tersebut berdasarkan instruksi dan truth table yang sudah diberikan di dalam file proteus.

### KMAP (Custom Decoder): 

1. Membuat Select Input One-Hot (Encoder)

| i7 | i6 | i5 | i4 | i3 | i2 | i1 | i0 | S2 | S1 | S0 |
| -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- |
| 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 0  | 0  |
| 0  | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 0  | 0  | 1  |
| 0  | 0  | 0  | 0  | 0  | 1  | 0  | 0  | 0  | 1  | 0  |
| 0  | 0  | 0  | 0  | 1  | 0  | 0  | 0  | 0  | 1  | 1  |
| 0  | 0  | 0  | 1  | 0  | 0  | 0  | 0  | 1  | 0  | 0  |
| 0  | 0  | 1  | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 1  |
| 0  | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 1  | 0  |
| 1  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 1  | 1  |

S0 = i1+i3+i5+i7
S1 = i2+i3+i6+i7
S2 = i4+i5+i6+i7


| S2 S1\\S0 | 00 | 01 | 11 | 10 |
| --------- | -- | -- | -- | -- |
| 0         | 0  | 0  | 0  | 1  |
| 1         | 1  | 1  | 0  | 1  |

`A = S1'S2+S0'S1`

| S2 S1\\S0 | 00 | 01 | 11 | 10 |
| --------- | -- | -- | -- | -- |
| 0         | 0  | 0  | 1  | 1  |
| 1         | 0  | 1  | 1  | 1  |

`B = S1+S0S2`

| S2 S1\\S0 | 00 | 01 | 11 | 10 |
| --------- | -- | -- | -- | -- |
| 0         | 0  | 0  | 1  | 1  |
| 1         | 1  | 0  | 1  | 1  |

`C = S1+S0'S1'S2`

| S2 S1\\S0 | 00 | 01 | 11 | 10 |
| --------- | -- | -- | -- | -- |
| 0         | 0  | 0  | 0  | 1  |
| 1         | 1  | 1  | 0  | 1  |

`D = S0'S1+S1'S2`

| S2 S1\\S0 | 00 | 01 | 11 | 10 |
| --------- | -- | -- | -- | -- |
| 0         | 0  | 0  | 0  | 0  |
| 1         | 1  | 1  | 0  | 0  |

`E = S1'S2`

| S2 S1\\S0 | 00 | 01 | 11 | 10 |
| --------- | -- | -- | -- | -- |
| 0         | 0  | 0  | 1  | 0  |
| 1         | 1  | 0  | 0  | 1  |

`F = S0'S1'S2+S0S1S2'+S0'S1S2`

| S2 S1\\S0 | 00 | 01 | 11 | 10 |
| --------- | -- | -- | -- | -- |
| 0         | 0  | 0  | 1  | 1  |
| 1         | 1  | 1  | 0  | 1  |

`G = S1'S2+S1S2'+S0'S1`

### Output 

*masukkan screenshot tampilan 7-Segment Anda untuk masing-masing nilai ini :*

| S2 | S1 | S0 | 7-Segment |
|----|----|----|---|
| 0  | 0  | 0  |![image](https://hackmd.io/_uploads/SkZK9BzkZx.png)|
| 0  | 0  | 1  |![image](https://hackmd.io/_uploads/Syht9BGJWl.png)|
| 0  | 1  | 0  |![image](https://hackmd.io/_uploads/r1v99SMJbg.png)|
| 0  | 1  | 1  |![image](https://hackmd.io/_uploads/SkPo5rGyWl.png)|
| 1  | 0  | 0  |![image](https://hackmd.io/_uploads/HJ9hcBG1Zg.png)|
| 1  | 0  | 1  |![image](https://hackmd.io/_uploads/ryA65Bf1-e.png)|
| 1  | 1  | 0  |![image](https://hackmd.io/_uploads/SJvRcSMJWg.png)|
| 1  | 1  | 1  |![image](https://hackmd.io/_uploads/BkbJoHGyZe.png)|


## Hints Gift 
Silahkan cari sendiri :v , cuman 1 orang tercepat yang bisa dapat hadiahnya ya...
\
\
\
\
\
gLZQoAqkHsDJxRxkbvCrptKFbLnDNuTnKwvzvMQGHVYeyLITewkHZXFCRySvhgztxCTUUBzBaESFwVRILGqpxgPZYmyZnBjUsHdVScQPHQEhTfZAPjUnQFKtVhuRVFMPESvhpVYXzJjQSzHgMBGFYbMxsyRVlwxQtOlwNPmkCmSFXpIxWrtDxOBKhzmpAsUXZdHHAhGtsAyjGzGILumqLvAoHQFnnIuBOhpAdscMZgqHxnHwnYFgWxhHrNzcIbMOsRtZfgrjUCnlJlDAudkdBkdwqYhJkCTFOzgqErVGJfuZcUAXAoxbrIRBkcFpGZvStmKZqIocfsZPjlYcLfFzTAiIqzAyUoUHySTbSKnMkXYYZsRpDgQypsFDZCzzcfRmJcnYsbGKyMnRaoyjcKKWZssVKeYNFOnqMttCGVozKSVzFRpPstRGEefRGMkpzXuwsbIYfhMvgaYNLZHNkLkgzDWGDQUklKZvIDuEPfWyFhbQHMyGxKvYXDrHMuOgUtwbsqgOgKDkWrBPMKwGbyAfqEYWkQhVgDCbciCgdaGlfTbUnCUtRhFSmqlUrwxhISXKnOxnQzbKeWeGGUZqAoItIwaUohcxMdfFLMLNQKZehSXtmkktUXWWUwrCaXZavUSyNWXljDqucAwBgTctkUMjGCDKPsVaVQcfosAahDvgblRaItFOuFbTACiHgWQZJwCrINHbgUqDhuKCrERpOjHdOfhrnvmBLmKUMmlcZazKwSjeGgxJSwiNeqSkToEZNJWXnxGrfThKDUBfYUgoyLgGOYoQxbYUbNDUgHhzFMKWAqMjgNehtJkbhdovcGBGacHaIqZCWApxXQrjEIHQkeHQtrvVBGEKSQkRyULtNxpsFJENuBbsbtIfjAeVbgMWYoAoUtRWhCGHWmvMntNxFrIsxDgGmIMCmcwHcLHeDtnOAnYolFnbkPSwCrXNYlkJWozOzhmjgtNHAbtFpPzgLlqlwCNCVwQZWykmPjbQQngPRRsTjgiMNKIlBLvIEGdWSBcgaRVyRkMQzWwwDTGtsBiAKWQtprFnlByGZLDOZwRvgZLZzFiIuOwYXgfVpoWLmnDGMeqNkcPYseRRlRrHwGNgWWPkvWwAmGfhnLsoAYWSgpXMdLBcpMCuNPoQKZQMdHMtDXRsmZUYXeTEvFCOAoIiGLSIZPTZRhHABeUUSZnRErlLfESc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


```plaintext
Tampilan 7 segment secara urut di tabel
akan melengkapi link ini secara urut dari kiri 
ke kanan :

https://h7.cl/tutamisamazing
```