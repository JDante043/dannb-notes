Untuk menemukan peluang sesuatu terjadi, bisa menggunakan rumus:
$$P = x_1^n \cdot x_2^n \cdot ...$$
Dimana:
- $P$ adalah total peluang yang bisa terjadi
- $x$ adalah hal yang bisa terjadi
- $n$ adalah berapa kali hal tersebut dilakukan

**Contoh Peluang**
1. 2 buah dadu akan dilempar secara bersamaan. Berapa titik sampel jika dilempar 1x?
$$\begin{align}
6\cdot 6 = 36
\end{align}$$

2. 2 buah dadu akan dilempar secara bersamaan. Berapa titik sampel jika dilempar 2x?
$$\begin{align}
6^2 \cdot 6^2 = 36^2 = 1296 = 6^4
\end{align}$$
3. Di suatu rumah sakit, data pasien mengandung 2 kategori, yaitu tipe darah dan tekanan darah. Ada 8 tipe darah dan 3 klasifikasi tekanan darah. Ada berapa kemungkinan data seseorang?
$$\begin{align}
P = 8 \cdot 3 = 24
\end{align}$$
# Permutasi
Permutasi adalah banyaknya kemungkinan urutan objek, dapat dihitung dengan
$$n! = n \cdot (n-1) \cdot ... \cdot 2 \cdot 1$$
Jika $n$ objek disusun dalam lingkaran, banyaknya kemungkinan susunan / urutan adalah
$$(n-1)!$$
Jika $n$ objek diambil sebanyak $r$ setiap kali pengambilan, maka banyaknya kemungkinan pengambilan adalah
$$_nP_r = \frac{n!}{(n-r)!}$$
Jika $n$ objek diambil secara $k_1$ sebanyak $r_1$ dan  $k_2$ sebanyak $r_2$
$$P = \frac{n!}{r_1!\cdot r_2!}$$
**Contoh Permutasi**
1. 6 orang akan duduk secara melingkar, berapa banyak kemungkinan tempat duduk?
$$P = 6! = 720$$
2. Di sebuah game baseball, satu tim berisi 8 orang yang akan bermain di 5 posisi / role. Berapa banyak kemungkinan susunan pemain?
$$_8P_5 = \frac{8!}{(8-5)!}=5720$$
3. Di sebuah acara kelulusan mahasiswa, terdapat 7 orang mahasiswa yang akan mendapat ruang hotel. 1 ruangan bisa memuat 3 orang, dan 2 ruangan dapat memuat 2 orang. Berapa banyak kemungkinan penempatan mahasiswa?
$$P = \frac{7!}{3!\cdot2(2!)} = 210$$
4. Berapa banyak susunan alfabet yang ada dalam kata "STATISTICS"?
$$\begin{align}
\text{Banyak alfabet:}\\
\text{S = 3}\\
\text{T = 3}\\
\text{I = 2}\\
\text{A = 1}\\
\text{C = 1}\\
\\
\text{Banyak tempat huruf = 10}\\
\\
P = \frac{10!}{3!3!2!1!1!} = 50400
\end{align}$$
5. 6 guru akan mengajar di 4 kelas berbeda. Berapa banyak kemungkinan penugasan?
$$P = \frac{6!}{(6-4)!} = 360$$

# Kombinasi
Kombinasi jika $n$ objek diambil sebanyak $r$ setiap kali pengambilan
$$(^n_r) = _nC_r = \frac{n!}{r!(n-r)!}$$
# Peluang bersyarat
Biasanya, peluang sesuatu terjadi ditulis dengan angka desimal dan jika keseluruhan kejadian ditambahkan, maka akan menghasilkan $1$
$$0<P<1$$

Jika terdapat 2 kejadian yang berbeda, $P(A)$ dan $P(B)$, jika suatu objek mengalami kedua kejadian tersebut, maka probabilitas dapat ditulis dengan:
$$P(A \cap B)$$
$$P(A\cap B) = P(A) \cdot P(B|A) = P(A)\cdot P(B)$$
Jika suatu objek hanya mengalami salah satu dari kejadian tersebut, maka dapat ditulis dengan:
$$P(A\cup B)$$
Dikarenakan $P(A\cup B)$ berarti hanya terjadi $A$ atau $B$, maka
$$P(A\cup B) = P(A) + P(B) - P(A\cap B)$$
Jika diketahui suatu kejadian telah terjadi, dan ditanya kemungkinan sesuatu terjadi, maka bisa menggunakan rumus
$$P(B|A) = \frac{P(A\cap B)}{P(A)}$$