# Overview
- Angka biner, simbol negatif, dan operasi biner
- Logika biner / Aljabar boolean
- Teori Instruksi mesin 
- Teori eksekusi instruksi (pipeline, stream, parallel processing, dll)
- Teori CPU
- Teori GPU

- Note: paling memungkinkan Angka biner & beberapa teori CPU & Instruksi CPU?
# Nomor Biner
- Sistem biner mengandung 3 komponen:
	- Nomor (0 / 1)
	- Tanda (minus / plus)
	- Titik / radik point (koma / titik)

# Negatif dalam biner
## Sign Magnitude
- Simbol negatif di paling kiri, 0 positif, 1 negatif
- Ada 2 representasi 0
- Bit simbol mempersulit perhitungan
- Paling simpel, namun jarang dipakai

## Two's Complement
- Angka negatif mulai dari $-2^n$ ketika bit paling kiri menjadi 1 dan menghitung ke atas / menuju positif
- $0111 1111 = 127; 1000 0000 = -128; 1000 0001 = -127; 1111 1111 = -1$

## Negasi
### Two's Complement
1. Cari nomor, misal $(18)_{10} = (00010010)_2$
2. Cari komplemen dari nomor tersebut $= (11101101)_2$
3. Tambahkan $1$ ke komplemen tersebut  $= (11101110)_2 = (-18)_{10}$

### Kasus khusus
1. Jika 2 angka dengan simbol yang sama ditambahkan (positif + positif / negatif + negatif), jika simbol hasil menjadi lawannya, maka hasil tersebut salah karena overflow
2. Jika 2 angka dengan simbol yang berbeda ditambahkan, overflow tidak dianggap.
3. $128 = -128$

## Pertambahan
- Tinggal ditambah, ingat kasus khusus; overflow tidak dianggap / dipotong
- $(-7)_{10} = (1001)_2;\ (5)_{10} = (0101)_2;\ 1001 + 0101 = 1110 \leftarrow$ Contoh pertambahan normal
- $(-5)_{10} = (1011)_2;\ (-2)_{10} = (1110)_2;\ 1011 + 1110 = 1\ 1001\leftarrow$ Hasil simbol sama (negatif), valid walaupun terjadi overflow
- $(7)_{10} = (0111)_2;\ (7)_{10} = (0111)_2;\ 0111 + 0111 = 1000\leftarrow$ 2 angka positif, hasil negatif. Terjadi overflow, tidak valid
## Perkalian
- Mirip dengan perkalian biasa
- $(11)_{10} = (1011)_2;\ (13)_{10} = (1101)_2;\ 1011 \cdot 1101 = (10001111)_2 = (143)_{10}\leftarrow$ Perkalian 2 nomor unsigned
- 