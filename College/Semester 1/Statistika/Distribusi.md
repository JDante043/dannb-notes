Distribusi dalam statistika adalah cara / bagaimana setiap probabilitas didistribusikan.

# Distribusi Binomial
Distribusi binomial adalah distribusi di mana hasil akhir hanya berupa 2 kemungkinan ("Cacat / Tidak cacat", "Berhasil / Tidak Berhasil", dll.) dan terdapat **pengembalian**.

$$\begin{align}
P = \binom{x}{n}p^x q^{n-x}\\
\mu = xp\\
\sigma^2 = npq
\end{align}$$
$x$ = Berapa kali percobaan dilakukan
$n$ = Berapa kali percobaan "berhasil"
p = Kemungkinan percobaan "berhasil"
q = Kemungkinan percobaan "gagal"
$\mu$ = Rata-rata
$\sigma^2$ = Standard varians

# Distribusi Multinomial
Distribusi multinomial adalah distribusi di mana hasil akhir ada beberapa kemungkinan (Warna HP yang diambil bisa antara merah, biru, hijau, dll.).

$$\begin{align}
P = \frac{N!}{x_1!x_2!x_3!...}p_1^{x_1}p_2^{x_2}p_3^{x_3}...
\end{align}$$
$N$ = Berapa kali percobaan dilakukan
$x_n$ = Berapa kali hasil tipe $n$ berhasil
$p_n$ = Kemungkinan percobaan tipe $n$ berhasil

# Distribusi Hipergeometrik
## Hipergeometrik Dasar
Distribusi hipergeometrik dasar adalah distribusi di mana hasil akhir hanya berupa 2 kemungkinan dan percobaan dilakukan **tanpa pengembalian**. 

$$\begin{align}
P = \frac{\binom{k}{x}\binom{N-k}{n-x}}{\binom{N}{n}}\\
\mu = \frac{nk}{N}\\
\sigma^2 = \frac{N-n}{N-1}\cdot n \cdot (1-\frac{k}{N})
\end{align}$$
$N$ = Total percobaan dilakukan / barang yang ada
$n$ = Berapa kali percobaan "berhasil" / barang yang ingin dilihat / dihitung
$k$ = Total "berhasil" dari keseluruhan $N$ / barang yang "cacat" dari keseluruhan $N$
$x$ = Total "berhasil" dari keseluruhan $n$ / barang yang "cacat" dari keseluruhan $n$
$\mu$ = Rata-rata
$\sigma^2$ = Standard varians

## Hipergeometrik Multivarians
Distribusi Hipergeometrik Multivarians adalah distribusi di mana hasil akhir ada banyak dan percobaan dilakukan **tanpa pengembalian**.

$$\begin{align}
P = \frac{\binom{k_1}{x_1}\binom{k_2}{x_2}...}{\binom{N}{n}}
\end{align}$$
$N$ = Berapa kali percobaan dilakukan
$n$ = Berapa kali percobaan "berhasil"
$k_n$ = Kemungkinan tipe $k$ ke $n$ dari keseluruhan $N$
$x_n$ = Kemungkinan tipe $k$ ke $n$ dari keseluruhan $n$

# Distribusi Poisson
Distribusi Poisson adalah distribusi di mana diketahui kejadian $\mu$ terjadi setiap interval dan ingin kita hitung kemungkinan kejadian terjadi $x$ kali.
$$\begin{align}
P = \frac{e^{-\mu}\mu^x}{x!}
\end{align}$$
# Distribusi Seragam Diskrit
Distribusi Seragam Diskrit adalah distribusi di mana terdapat beberapa kejadian akhir yang mungkin, tetapi **semua hasil akhir memiliki peluang yang sama**.
$$\begin{align}
P = \frac{1}{k}\\
\mu = \frac{\Sigma_{x=1}^k(x)}{k}\\
\sigma^2 = \frac{\Sigma_{x = 1}^k((x - \mu)^2)}{k}
\end{align}$$
$k$ = Banyak kemungkinan yang terjadi
$e$ = Nomor Euler (**Bukan** konstanta Euler) = 2.71828
$\mu$ = Rata-rata
$\sigma^2$ = Standard Varians