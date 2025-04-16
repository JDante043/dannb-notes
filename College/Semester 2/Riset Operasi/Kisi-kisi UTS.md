# NOTE
- Gunakan pecahan daripada desimal untuk hasil yang lebih akurat
# Soal Simpleks
1. Maksimumkan $3x_1 + 2x_2$ dengan kendala:
	- $x_1 + 2x_2 \le 20$
	- $3x_1 + x_2 \le 20$
	- $x_1,x_2 \ge 0$

	Kendala bukan persamaan, maka ubah menjadi:
	- $x_1 + 2x_2 + y_1 = 20$
	- $3x_1 + x_2 + y_2 = 20$

	Ubah fungsi awal kita menjadi: $-3x_1 -2x_2 + Z = 0$

	Berikut adalah tabel simpleks kita:

| $x_1$ | $x_2$ | $y_1$ | $y_2$ | $Z$ | C   |       |
| ----- | ----- | ----- | ----- | --- | --- | ----- |
| 1     | 2     | 1     | 0     | 0   | 20  | $y_1$ |
| 3     | 1     | 0     | 1     | 0   | 20  | $y_2$ |
| -3    | -2    | 0     | 0     | 1   | 0   | $Z$   |
**Penyelesaian:**
1. Lihat barisan paling bawah. Koefisien terkecil adalah $-3$. Maka, $x_1$ adalah kolom pivot
2. Lihat kolom C. **Misalkan** setiap sel di kolom C dengan sel sebaris di kolom pivot:

| $x_1$ | $x_2$ | $y_1$ | $y_2$ | $Z$ | C             |       |
| ----- | ----- | ----- | ----- | --- | ------------- | ----- |
| 1     | 2     | 1     | 0     | 0   | $20/1 = 20$   | $y_1$ |
| 3     | 1     | 0     | 1     | 0   | $20/3 = 6.67$ | $y_2$ |
| -3    | -2    | 0     | 0     | 1   | 0             | $Z$   |

3. Dapat dilihat, sel kolom C setelah pembagian yang paling kecil adalah di barisan $y_2$. Barisan $y_2$ setelah 
4. Sel berinterseksi dengan baris dan kolom pivot adalah 3. Sel ini dinamakan sel pivot.
5. Sel pivot harus = 1. Maka bagi seluruh barisan pivot dengan 3:

| $x_1$ | $x_2$         | $y_1$ | $y_2$         | $Z$ | C              |       |
| ----- | ------------- | ----- | ------------- | --- | -------------- | ----- |
| 1     | 2             | 1     | 0             | 0   | $20$           | $y_1$ |
| 1     | $\frac{1}{3}$ | 0     | $\frac{1}{3}$ | 0   | $\frac{20}{3}$ | $y_2$ |
| -3    | -2            | 0     | 0             | 1   | 0              | $Z$   |

6.  Untuk menghabiskan sel di atas sel pivot, maka kalikan seluruh barisan pivot dengan $-1$, lalu tambahkan ke barisan atasnya:

| $x_1$ | $x_2$         | $y_1$ | $y_2$          | $Z$ | C              |       |
| ----- | ------------- | ----- | -------------- | --- | -------------- | ----- |
| 0     | $\frac{5}{3}$ | 1     | $-\frac{1}{3}$ | 0   | $\frac{40}{3}$ | $y_1$ |
| 1     | $\frac{1}{3}$ | 0     | $\frac{1}{3}$  | 0   | $\frac{20}{3}$ | $y_2$ |
| -3    | -2            | 0     | 0              | 1   | 0              | $Z$   |

7. Untuk menghabiskan sel di bawah sel pivot, maka kalikan seluruh barisan pivot dengan $3$, lalu tambahkan ke barisan bawahnya:

| $x_1$ | $x_2$         | $y_1$ | $y_2$          | $Z$ | C              |       |
| ----- | ------------- | ----- | -------------- | --- | -------------- | ----- |
| 0     | $\frac{5}{3}$ | 1     | $-\frac{1}{3}$ | 0   | $\frac{40}{3}$ | $y_1$ |
| 1     | $\frac{1}{3}$ | 0     | $\frac{1}{3}$  | 0   | $\frac{20}{3}$ | $y_2$ |
| 0     | -1            | 0     | 1              | 1   | 20             | $Z$   |

8. Seluruh kolom pivot sudah selesai dimodifikasi (hanya ada elemen pivot yang non 0).
9. Lihat barisan $Z$. Masih ada nilai negatif. Ulangi loop
10. $x_2$ adalah kolom pivot. **Misalkan** seluruh sel di kolom $C$ dibagi dengan sel yang ada di barisan masing-masing di kolom pivot:

| $x_1$ | $x_2$         | $y_1$ | $y_2$          | $Z$ | C                                   |       |
| ----- | ------------- | ----- | -------------- | --- | ----------------------------------- | ----- |
| 0     | $\frac{5}{3}$ | 1     | $-\frac{1}{3}$ | 0   | $\frac{40}{3}\div \frac{5}{3} = 8$  | $y_1$ |
| 1     | $\frac{1}{3}$ | 0     | $\frac{1}{3}$  | 0   | $\frac{20}{3} \div \frac{1}{3} =20$ | $y_2$ |
| 0     | -1            | 0     | 1              | 1   | 20                                  | $Z$   |

11. Dapat dilihat, hasil pembagian paling kecil adalah pada barisan paling atas. Maka, $y_1$ adalah barisan pivot dan $\frac{5}{3}$ adalah elemen pivot.
12. Elemen pivot harus = 1, maka bagikan seluruh barisan pivot dengan $\frac{5}{3}$:

| $x_1$ | $x_2$         | $y_1$         | $y_2$          | $Z$ | C              |       |
| ----- | ------------- | ------------- | -------------- | --- | -------------- | ----- |
| 0     | 1             | $\frac{3}{5}$ | $-\frac{1}{5}$ | 0   | $8$            | $y_1$ |
| 1     | $\frac{1}{3}$ | 0             | $\frac{1}{3}$  | 0   | $\frac{20}{3}$ | $y_2$ |
| 0     | -1            | 0             | 1              | 1   | 20             | $Z$   |
13. Untuk membuat sel di bawah sel pivot pada barisan $y_2$ menjadi 0, kalikan barisan pivot dengan $-\frac{1}{3}$, lalu tambahkan ke barisan tersebut:

| $x_1$ | $x_2$ | $y_1$          | $y_2$          | $Z$ | C   |       |
| ----- | ----- | -------------- | -------------- | --- | --- | ----- |
| 0     | 1     | $\frac{3}{5}$  | $-\frac{1}{5}$ | 0   | $8$ | $y_1$ |
| 1     | 0     | $-\frac{1}{5}$ | $\frac{2}{5}$  | 0   | $4$ | $y_2$ |
| 0     | -1    | 0              | 1              | 1   | 20  | $Z$   |
14. Untuk membuat sel di bawah sel pivot pada barisan $Z$ menjadi 0, kalikan barisan pivot dengan 1, lalu tambahkan ke barisan tersebut:

| $x_1$ | $x_2$ | $y_1$          | $y_2$          | $Z$ | C   |       |
| ----- | ----- | -------------- | -------------- | --- | --- | ----- |
| 0     | 1     | $\frac{3}{5}$  | $-\frac{1}{5}$ | 0   | $8$ | $y_1$ |
| 1     | 0     | $-\frac{1}{5}$ | $\frac{2}{5}$  | 0   | $4$ | $y_2$ |
| 0     | 0     | $\frac{3}{5}$  | $\frac{4}{5}$  | 1   | 28  | $Z$   |
15. Tidak ada lagi elemen negatif di barisan $Z$. Proses sudah selesai
16. Untuk menjawab pertanyaan kita, lihat baris dan kolom di mana variabel awal = 1:

| $x_1$ | $x_2$ | $Z$ | C   |       |
| ----- | ----- | --- | --- | ----- |
| 0     | 1     | 0   | $8$ | $y_1$ |
| 1     | 0     | 0   | $4$ | $y_2$ |
| 0     | 0     | 1   | 28  | $Z$   |
17. Menurut tabel tersebut, fungsi $3x_1 + 2x_2$ dengan kendala tersebut, akan maksimal ketika:
- $x_1 = 4$
- $x_2 = 8$
- Dan hasil maksimalnya adalah 28

2. Sebuah perusahaan membuat 3 jenis produk, yang masing-masing harus
melalui 3 macam proses. Perusahaan tersebut dapat menjual semua
produksinya, tetapi kemampuan produksinya terbatas. Data yang berhubungan
dengan perusahaan tersebut tampak pada tabel di bawah ini. Bagaimana
campuran produksi yang harus dibuat?
![[Contoh soal simpleks.png]]
Soal tersebut adalah soal simpleks dengan rumusan:
Maksimalkan $4A + 8B + 6C$, dengan kendala:
- $A+3B+2C \le 160$
- $3A + 4B + 2C \le 120$
- $2A + B + 2C \le 80$

Berikut adalah bentuk kendala dan rumusan dalam bentuk standar:
Maksimalkan $-4A - 8B - 6C + M = 0$
- $A + 3B + 2C + X = 160$
- $3A + 4B + 2C + Y = 120$
- $2A + B + 2C + Z = 80$

Berikut adalah tabel simpleksnya:

| A   | B   | C   | X   | Y   | Z   | M   | N   |     |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1   | 3   | 2   | 1   | 0   | 0   | 0   | 160 | X   |
| 3   | 4   | 2   | 0   | 1   | 0   | 0   | 120 | Y   |
| 2   | 1   | 2   | 0   | 0   | 1   | 0   | 80  | Z   |
| -4  | -8  | -6  | 0   | 0   | 0   | 1   | 0   | M   |

**Penyelesaian:**
1. Perhatikan baris M. Koefisien terendah adalah $-8$. Maka kolom B adalah kolom pivot.
2. Bagikan koefisien di kolom N dengan koefisien di baris yang sama di kolom B. Hasil pembagian terkecil adalah $120\div 4 = 30$. Maka, Y adalah barisan pivot, dan 4 adalah elemen pivot.
3. Elemen pivot harus = 1. Bagi seluruh barisan pivot dengan 4:

| A             | B   | C             | X   | Y             | Z   | M   | N   |     |
| ------------- | --- | ------------- | --- | ------------- | --- | --- | --- | --- |
| 1             | 3   | 2             | 1   | 0             | 0   | 0   | 160 | X   |
| $\frac{3}{4}$ | 1   | $\frac{1}{2}$ | 0   | $\frac{1}{4}$ | 0   | 0   | 30  | Y   |
| 2             | 1   | 2             | 0   | 0             | 1   | 0   | 80  | Z   |
| -4            | -8  | -6            | 0   | 0             | 0   | 1   | 0   | M   |
5. Untuk menghilangkan 3 di atas elemen pivot, kalikan barisan pivot dengan $-3$, lalu tambahkan ke barisan tersebut:

| A              | B   | C             | X   | Y              | Z   | M   | N   |     |
| -------------- | --- | ------------- | --- | -------------- | --- | --- | --- | --- |
| $-\frac{5}{4}$ | 0   | $\frac{1}{2}$ | 1   | $-\frac{3}{4}$ | 0   | 0   | 70  | X   |
| $\frac{3}{4}$  | 1   | $\frac{1}{2}$ | 0   | $\frac{1}{4}$  | 0   | 0   | 30  | Y   |
| 2              | 1   | 2             | 0   | 0              | 1   | 0   | 80  | Z   |
| -4             | -8  | -6            | 0   | 0              | 0   | 1   | 0   | M   |
6. Untuk menghilangkan 1 di bawah elemen pivot, kalikan barisan pivot dengan $-1$, lalu tambahkan ke barisan tersebut:

| A              | B   | C             | X   | Y              | Z   | M   | N   |     |
| -------------- | --- | ------------- | --- | -------------- | --- | --- | --- | --- |
| $-\frac{5}{4}$ | 0   | $\frac{1}{2}$ | 1   | $-\frac{3}{4}$ | 0   | 0   | 70  | X   |
| $\frac{3}{4}$  | 1   | $\frac{1}{2}$ | 0   | $\frac{1}{4}$  | 0   | 0   | 30  | Y   |
| $\frac{5}{4}$  | 0   | $\frac{3}{2}$ | 0   | $-\frac{1}{4}$ | 1   | 0   | 50  | Z   |
| -4             | -8  | -6            | 0   | 0              | 0   | 1   | 0   | M   |
7. Untuk menghilangkan $-8$ di barisan M, kalikan barisan pivot dengan 8, lalu tambahkan ke barisan tersebut:

| A              | B   | C             | X   | Y              | Z   | M   | N   |     |
| -------------- | --- | ------------- | --- | -------------- | --- | --- | --- | --- |
| $-\frac{5}{4}$ | 0   | $\frac{1}{2}$ | 1   | $-\frac{3}{4}$ | 0   | 0   | 70  | X   |
| $\frac{3}{4}$  | 1   | $\frac{1}{2}$ | 0   | $\frac{1}{4}$  | 0   | 0   | 30  | Y   |
| $\frac{5}{4}$  | 0   | $\frac{3}{2}$ | 0   | $-\frac{1}{4}$ | 1   | 0   | 50  | Z   |
| $2$            | 0   | $-2$          | 0   | 2              | 0   | 1   | 240 | M   |
8. Pilih koefisien terendah lainnya, yaitu $-2$ pada kolom C.
9. Hasil pembagian terkecil adalah $50\div \frac{3}{2} = 33.33$. Maka, barisan pivot adalah barisan Z dan elemen pivot adalah $\frac{3}{2}$.
10. Elemen pivot harus = 1. Kalikan seluruh barisan pivot dengan $\frac{2}{3}$:

| A              | B   | C             | X   | Y              | Z             | M   | N       |     |
| -------------- | --- | ------------- | --- | -------------- | ------------- | --- | ------- | --- |
| $-\frac{5}{4}$ | 0   | $\frac{1}{2}$ | 1   | $-\frac{3}{4}$ | 0             | 0   | 70      | X   |
| $\frac{3}{4}$  | 1   | $\frac{1}{2}$ | 0   | $\frac{1}{4}$  | 0             | 0   | 30      | Y   |
| $\frac{5}{6}$  | 0   | 1             | 0   | $-\frac{1}{6}$ | $\frac{2}{3}$ | 0   | $33.33$ | Z   |
| $2$            | 0   | $-2$          | 0   | 2              | 0             | 1   | 240     | M   |
11. Kalikan barisan pivot dengan $-\frac{1}{2}$, kemudian tambahkan ke barisan X:

| A              | B   | C             | X   | Y              | Z              | M   | N        |     |
| -------------- | --- | ------------- | --- | -------------- | -------------- | --- | -------- | --- |
| $-\frac{5}{3}$ | 0   | 0             | 1   | $-\frac{2}{3}$ | $-\frac{1}{3}$ | 0   | $53.335$ | X   |
| $\frac{3}{4}$  | 1   | $\frac{1}{2}$ | 0   | $\frac{1}{4}$  | 0              | 0   | 30       | Y   |
| $\frac{5}{6}$  | 0   | 1             | 0   | $-\frac{1}{6}$ | $\frac{2}{3}$  | 0   | $33.33$  | Z   |
| $2$            | 0   | $-2$          | 0   | 2              | 0              | 1   | 240      | M   |
12. Kalikan barisan pivot dengan $-\frac{1}{2}$, kemudian tambahkan ke barisan Y:

| A              | B   | C    | X   | Y              | Z              | M   | N        |     |
| -------------- | --- | ---- | --- | -------------- | -------------- | --- | -------- | --- |
| $-\frac{5}{3}$ | 0   | 0    | 1   | $-\frac{2}{3}$ | $-\frac{1}{3}$ | 0   | $53.335$ | X   |
| $\frac{1}{3}$  | 1   | 0    | 0   | $\frac{1}{3}$  | $-\frac{1}{3}$ | 0   | $13.335$ | Y   |
| $\frac{5}{6}$  | 0   | 1    | 0   | $-\frac{1}{6}$ | $\frac{2}{3}$  | 0   | $33.33$  | Z   |
| $2$            | 0   | $-2$ | 0   | 2              | 0              | 1   | 240      | M   |
13. Kalikan barisan pivot dengan 2, lalu tambahkan ke barisan M:

| A              | B   | C   | X   | Y              | Z              | M   | N        |     |
| -------------- | --- | --- | --- | -------------- | -------------- | --- | -------- | --- |
| $-\frac{5}{3}$ | 0   | 0   | 1   | $-\frac{2}{3}$ | $-\frac{1}{3}$ | 0   | $53.335$ | X   |
| $\frac{1}{3}$  | 1   | 0   | 0   | $\frac{1}{3}$  | $-\frac{1}{3}$ | 0   | $13.335$ | Y   |
| $\frac{5}{6}$  | 0   | 1   | 0   | $-\frac{1}{6}$ | $\frac{2}{3}$  | 0   | $33.33$  | Z   |
| $\frac{11}{3}$ | 0   | 0   | 0   | $\frac{5}{3}$  | $\frac{4}{3}$  | 1   | $306.66$ | M   |
14. Sudah tidak ada lagi koefisien negatif di barisan M. Lihat matriks simpleks variabel awal yang nilainya 1, beserta dengan kolom M dan N:

| B   | C   | M   | N        |
| --- | --- | --- | -------- |
| 0   | 0   | 0   | $53.335$ |
| 1   | 0   | 0   | $13.335$ |
| 0   | 1   | 0   | $33.33$  |
| 0   | 0   | 1   | $306.66$ |
15. Dapat dilihat, rumusan $-4A-8B-6C+M$ dengan kendala tersebut akan maksimal jika:
	- $B = 13.335$
	- $A = 0$
	- $C = 33.33$
	Dan hasil akhirnya adalah $306.66$
# Soal Transportasi
1. Berikut adalah sheet logistik sebuah perusahaan distributor dan pabrik. Gunakanlah ketiga metode transportasi untuk mendapatkan jawaban feasible awal! ![[Contoh soal transportasi.png]]

**Penyelesaian:**
**Barat-Laut:**
1. Lihatlah kotak paling atas kiri / paling barat-laut tabel. Antara isi kebutuhan kolom tersebut secara maksimal, atau habiskan kapasitas pabrik.
2. Jika kapasitas pabrik habis, pindah ke pabrik baru / bawah, kemudian coba isi lagi.
3. Jika kebutuhan distributor habis, pindah ke distributor baru / kanan, kemudian coba isi lagi.
4. Isi terus sampai semua kebutuhan tercukupi dan kapasitas habis!

**Termurah:**
1. Carilah kotak dengan harga termurah, kemudian isi kotak itu antara sampai kapasitas pabrik habis atau sampai kebutuhan distributor tercukupi.
2. Kemudian cari kotak termurah kedua, lanjut terus.

**Vogel / VAM:**
1. Untuk setiap kolom DAN baris, cari selisih harga termurah dengan harga termurah kedua di masing masing kolom / baris! (Nilai ini dinamakan penalti)
2. Pilihlah penalti termurah di antara kolom & baris!
3. Di kolom/baris penalti tersebut, carilah nilai termurah, kemudian isi!
4. Jika kapasitas pabrik habis, coret seluruh barisan
5. Jika kebutuhan distributor tercukupi, coret seluruh kolom.
6. Balik ke nomor 1, ulangi sampai semuanya tercukupi


# Soal Penugasan