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

## Negatif dalam biner
### Sign Magnitude
- Simbol negatif di paling kiri, 0 positif, 1 negatif
- Ada 2 representasi 0
- Bit simbol mempersulit perhitungan
- Paling simpel, namun jarang dipakai

### Two's Complement
- Angka negatif mulai dari $-2^n$ ketika bit paling kiri menjadi 1 dan menghitung ke atas / menuju positif
- $0111 1111 = 127; 1000 0000 = -128; 1000 0001 = -127; 1111 1111 = -1$
- Untuk mengubah positif menjadi negatif, cari komplemen angka, kemudian tambah 1
	- $(91)_{10} = (0101\ 1011)_2$
	- $\neg(0101\ 1011)_2 = (1010\ 0100)_2$
	- $(1010\ 0100)_2 + (1)_2 = (1010\ 0101)_2$
	- $(1010\ 0101)_2 = (-91)_2$
- Untuk membaca angka negatif Two's Complement, hitung 0 sebagai 1 ketika menggunakan $2^n$ dan 1 sebagai 0. Kemudian tambahkan 1 ke hasil terakhir. Kemudian, kalikan dengan $-1$ alias tambahkan tanda negatif ke hasil akhir
	- $(1010\ 0101)_2 = 2^1 + 2^3 + 2^4 + 2^6 = 2 + 8 + 16 + 64 + 1 = 91 \rightarrow -91$

## Negasi
### Two's Complement
1. Cari nomor, misal $(18)_{10} = (00010010)_2$
2. Cari komplemen dari nomor tersebut $= (11101101)_2$
3. Tambahkan $1$ ke komplemen tersebut  $= (11101110)_2 = (-18)_{10}$

#### Kasus khusus
1. Jika 2 angka dengan simbol yang sama ditambahkan (positif + positif / negatif + negatif), jika simbol hasil menjadi lawannya, maka hasil tersebut salah karena overflow
2. Jika 2 angka dengan simbol yang berbeda ditambahkan, overflow tidak dianggap.
3. $128 = -128$

## Pertambahan
- Tinggal ditambah, ingat kasus khusus; overflow tidak dianggap / dipotong
- $(-7)_{10} = (1001)_2;\ (5)_{10} = (0101)_2;\ 1001 + 0101 = 1110 \leftarrow$ Contoh pertambahan normal
- $(-5)_{10} = (1011)_2;\ (-2)_{10} = (1110)_2;\ 1011 + 1110 = 1\ 1001\leftarrow$ Hasil simbol sama (negatif), valid walaupun terjadi overflow
- $(7)_{10} = (0111)_2;\ (7)_{10} = (0111)_2;\ 0111 + 0111 = 1000\leftarrow$ 2 angka positif, hasil negatif. Terjadi overflow, tidak valid
## Perkalian
- Mirip dengan perkalian biasa. Jumlah bit akhir adalah bit angka pertama + bit angka kedua
- $(11)_{10} = (1011)_2;\ (13)_{10} = (1101)_2;\ 1011 \cdot 1101 = (10001111)_2 = (143)_{10}\leftarrow$ Perkalian 2 nomor unsigned
- Untuk anga negatif, kalikan angka positifnya dulu kemudian konversi ke angka negatif
- $(-7)_{10} = (1001)_2;\ (13)_{10} = (1101)_2;\ (7)_{10} = (0111)_2;\ 0111\cdot1101 = (0101\ 1011)_2\rightarrow (1010\ 0101)_2 = (-91)_{10}$
# Gerbang Logika
- AND yang datar
- OR yang melengkung
# Teori CPU
## Struktur

# Parallel Processing
## Tipe
- **SISD (Single instruction, Single Data stream)**: Uniprocessors
- **SIMD (Single instruction, Multiple Data stream**: Vector & Array processors
- **MISD (Multiple Instruction, Single Data stream)**: Not used
- **MIMD (Multiple Instruction, Multiple Data stream**:
	- Distributed memory (Loosely coupled): Clusters
	- Shared memory (Tightly coupled): NUMA & SMP

## Symmetric multiprocessor
Sebuah komputer yang memiliki:
- 2+ unit prosesor yang mirip kemampuannya
- Semua unit prosessor memiliki akses I/O yang sama
- Sistem dikendalikan oleh sebuah sistem operasi internal (membagi tugas, mengatur akses I/O, membagi hasil, dll.)

## Bus organisation
### Positif
- Simpel
- Fleksibel
- Pasif; terandalkan

### Negatif
- Kecepatan dibatasi oleh kecepatan bus
- CPU Cache diperlukan untuk meningkatkan kecepatan
- CPU harus diperingati ketika data dalam bus berubah

## Cache Coherence
Setiap cache di setiap prosessor harus sama (dalam multiprosessor)
### Software based
- Potensi masalah berada dalam compile time, bukan run time
- Namun, harus ada kelonggaran, tidak terlalu efisien

### Hardware based
- Lebih efisien dan transparan
- Terdapat 2 jenis, "directory" dan "snoopy"

### Snoopy Protocol
- Setiap kontroler cache memiliki line dengan cache lain. Setiap ada update di satu cache, cache lain terupdate / cache lain bisa melihat / "snooping" cache lain
- Menggunakan bus
- 2 cara / implementasi:
	- **Write invalidate**: Banyak pembaca, 1 penulis. Cache lain terinvalidasi. Dinamakan "MESI", sesuai dengan status line yang memungkinkan (Modified, Exclusive, Shared, Invalid). Biasa digunakan oleh sistem komersial seperti `x86`
	- **Write update**: Banyak penulis. Satu cache mengupdate data, cache yang lain diberitahu dan mengupdate juga
	- Sistem bisa menggunakan kedua implementasi

### MESI
- Modified, data di cache ini berbeda dengan di cache lain
- Exclusive, data di cache ini tidak terdapat di cache lain
- Shared, data di cache ini same dengan di cache lain
- Invalid, cache ini tidak memiliki data valid

## Multithreading & Multiprosesor
- Performa dapat dilihat dengan banyaknya instruksi yang dieksekusi (frekuensi * instruksi tereksekusi per cycle)
- Untuk meningkatkan performa, dapat menggunakan multithreading untuk meningkatkan instruksi tereksekusi per cycle

### Multithreading
- Thread adalah instruksi yang perlu dieksekusi sementara proses adalah sebuah instansi program di suatu komputer
- Terdapat 2 tipe multithreading
	- **Explisit**: Mengeksekusi beberapa instruksi thread secara bersamaan menggunakan pipeline
	- **Implisit**: Mengeksekusi beberapa thread dari sebuah program sekuensial

## Cluster
- Alternatif SMP
- Beberapa komputer ("Node") bekerjasama menjadi suatu "komputer besar"
- Namun, diperlukan suatu "middleman" untuk menggabungkan semua node

## NUMA (Non-uniform Memory Access)
- SMP berguna karena simpel, Cluster berguna karena scalability yang bagus
- Di NUMA, setiap prosessor memiliki memori lokal sendiri, di mana data di memori tersebut lebih cepat di akses daripada harus mengakses memori terunifikasi yang lebih lambat