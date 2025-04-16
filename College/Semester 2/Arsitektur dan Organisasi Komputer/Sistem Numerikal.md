Manusia biasanya menggunakan sistem hitung berbasis 10 / desimal. Artinya, terdapat 10 angka untuk menghitung (0-10). Namun, di dunia komputer, terdapat beberapa sistem lain:

# Biner / Binary / Base 2
Merupakan sistem di mana angka yang digunakan adalah 0 dan 1

## Biner -> Base 10
### Integer
Misalkan terdapat biner $(1101)_2$. Cara mencari angka desimal adalah:
1. Mulai dari nomor paling **kanan**
2. Ingat lokasi nomor yang sekarang dicek (dihitung dari kanan, mulai dari 0)
3. Jika nomor yang dicek = 0, pindah ke kiri
4. Jika nomor yang dicek = 1, maka tambahkan $2^n$ ke hasil akhir, di mana $n$ adalah posisi nomor yang dicek sekarang; lalu pindah ke kiri lagi

Berdasarkan langkah-langkah tersebut, didapatkan:
$2^3 + 2^2 + 0 + 2^0 = 8 + 4 + 0 + 1 = 13$

### Pecahan
$n$ di kanan titik / koma mulai dari $-1$. Misalkan $(0.1011)_2$, maka
$$\begin{align}
(1\cdot 2^{-1}) + (0\cdot 2^{-2}) + (1\cdot 2^{-3}) + (1\cdot 2^{-4})\\
= 0.5 + 0 + 0.125 + 0.0625 = 0.6875
\end{align}$$
## Base 10 -> Biner
### Integer
Misalkan terdapat $(133)_{10}$. Cara mencari angka biner adalah:
1. Bagi nomor desimal dengan 2, lalu catat sisanya.
2. Lakukan sampai bilangan desimal menjadi 1
3. Catat 1 di paling akhir.
4. Baca sisa dari bawah ke atas

Berdasarkan langkah-langkah tersebut, didapatkan:
$$\begin{align}
133/2 = 66\ [1]\\
66/2 = 33\ [0]\\
33/2 = 16\ [1]\\
16/2 = 8\ [0]\\
8/2 = 4\ [0]\\
4/2 = 2\ [0]\\
2/2 = 1\ [0]\\
1/2 = 0\ [1]\\
\end{align}$$
Maka, bilangan biner adalah $(10000101)_2$

### Pecahan
Untuk pecahan,
1. Untuk angka sebelum titik/koma, gunakan cara biasa
2. Untuk angka setelah titik/koma, kalikan dengan 2; lihat apakah jawaban >1
3. Jika jawaban >1, tulis sisa = 1 dan kurangi angka sekarang dengan 1, lanjut
4. Jika jawaban <1, tulis sisa = 0, lanjut
5. Jawaban adalah sisa **dari atas ke bawah**

Misalkan terdapat $(0.8125)_{10}$:
1. $0.8125\cdot 2 = 1.625 [1]$
2. $0.625\cdot 2 = 1.25 [1]$
3. $0.25\cdot 2 = 0.5 [0]$
4. $0.5\cdot 2 = 1.0 [1]$

Maka, jawaban adalah $(0.1101)_2$
# Oktal / Octal / Base 8
Sistem penomoran dengan 8 digit: 0-7

## Oktal -> Base 10
1. Mulai dari digit paling kanan
2. Perhatikan juga lokasi digit dari kanan
3. Kalikan digit dengan $8^n$, di mana $n$ adalah lokasi dari kanan, mulai dari 0
4. Tambahkan ke hasil akhir, kemudian pindah ke kiri

Misal terdapat $(105)_8$:
1. $5\cdot 8^0 = 5$
2. $0\cdot 8^1 = 0$
3. $1\cdot 8^2 = 64$
4. $5 + 0 + 64 = 69$

## Base 10 -> Oktal
1. Bagi nomor Desimal dengan 8, perhatikan juga sisanya
2. Lakukan sampai hasil pembagian 0
3. Lihat dari atas sampa bawah

Misal terdapat $(1792)_{10}$. Maka angka oktalnya adalah:
1. $1792\div 8 = 224 [0]$
2. $224\div 8 = 28 [0]$
3. $28\div 8 = 3 [4]$
4. $3\div 8 = 0 [3]$
Maka, angka oktalnya adalah $(3400)_8$

# Heksadesimal / Hexadecimal / Base 16
Sistem penomoran dengan 16 digit: 0-9 dan A-F.
A = 10
B = 11
C = 12
D = 13
E = 14
F = 15

## Heksadesimal -> Base 10
1. Mulai dari digit paling kanan
2. Perhatikan juga lokasi digit dari kanan
3. Kalikan digit dengan $16^n$, di mana $n$ adalah lokasi dari kanan, mulai dari 0
4. Tambahkan ke hasil akhir, kemudian pindah ke kiri

Misalkan terdapat $(7CF)_{16}$, maka
1. F = 15. $(15\cdot 16^0) = 15$
2. C = 12. $(12 \cdot 16^1) = 192$
3. 7 = 7. $(7\cdot 16^2) = 1792$
4. $15+192+1792 = 1999$

## Base 10 -> Heksadesimal
Misal terdapat $(960)_{10}$, maka bilangan heksadesimalnya adalah:
1. Bagi digit dengan 16, perhatikan sisanya
2. Ulangi hingga hasilnya > 1
3. Lihat sisanya, baca dari bawah ke atas, kemudian lihat tabel konversi nomor di atas

Berdasarkan langkah tersebut, berikut adalah jawaban kita:
$$\begin{align}
960\div 16 = 60 [0]\\
60\div 16 = 3 [12]\\
3 \div 16 = 0 [3]\\
\\
3, 12, 0 \rightarrow 3C0
\end{align}$$
