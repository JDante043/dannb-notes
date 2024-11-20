Dalam statistika, terdapat istilah PDF & CDF:
- Probability Mass Function, soal yang menanyakan tentang probabilitas ketika $X = n$ / $X$ adalah suatu nilai.
- Cumulative Distribution Function, soal yang menanyakan tentang probabilitas kumulatif ketika X memiliki beberapa nilai

# Definisi
## Diskrit
### PDF
Fungsi PDF diskrit harus memenuhi semua ketentuan berikut:
- $f(x) \ge 0$, kemungkinan sesuatu terjadi harus ada
- $\Sigma_x f(x)$, jika semua peluang ditambahkan, totalnya harus 1
- $P(X=x) = f(x)$, peluang sesuatu terjadi merupakan produk dari $f(x)$

### CDF
Fungsi CDF adalah kumulatif peluang hingga $x$, bentuk matematis seperti:
$$\begin{align}
P(X\le x) = \Sigma_x f(x)
\end{align}$$

## Kontinu
### PDF
Fungsi PDF kontinu harus memenuhi semua peraturan berikut:
- $f(x) \ge 0$, kemungkinan sesuatu terjadi harus ada
- $\int_{-\infty}^{\infty}f(x)dx = 1$, semua peluang jika ditambahkan = 1
- $P(a\lt X\lt b) = \int_a^b f(x) dx$, kemungkinan a-b terjadi bisa dicari dengan $\int_a^b f(x) dx$

### CDF
Fungsi CDF kontinu merupakan integral terbatas mulai dari $-\infty$ sampai $x$ yang diinginkan:
$$\begin{align}
P(X \le x) = \int_{-\infty}^x f(x)dx
\end{align}$$
# Contoh
## Diskrit
Sebuah koin dilempar 5 kali. Hitunglah:
- **CDF**: Peluang muka koin yang terlihat adalah angka paling banyak 3 kali
$$\begin{align}
P(X<=3)\\
\Sigma_{X=0}^3(\binom{5}{x}(0.5)^x(0.5)^{5-x})\\
\end{align}$$

- **PDF**: Peluang muka koin yang terlihat adalah angka sebanyak 3 kali pas
$$\begin{align}
P(X=3)\\
\binom{5}{3}(0.5)^3(0.5)^{5-3}
\end{align}$$

## Kontinu
1. Misal terdapat sebuah fungsi densitas kontinu:
$$\begin{align}
f(x)=\cases{\frac{x^2}{3},-1\lt x\lt 2\\0,\text{ elsewhere}}
\end{align}$$
	1. Buktikan bahwa fungsi tersebut sebuah fungsi densitas (DF) yang valid!
$$\begin{align}
\int_{-\infty}^\infty \frac{x^2}{3}dx,-1\lt x\lt 2\\
\int_{-\infty}^{-1} \frac{x^2}{3} + \int_{-1}^2\frac{x^2}{3}+\int_2^\infty\frac{x^2}{3}\\
0 + \int_{-1}^2\frac{x^2}{3} +0 \\
=1 \text{ valid}
\end{align}$$
	2. Temukan kemungkinan $P(0\lt x \lt 1)$
$$\begin{align}
\int_0^1\frac{x^2}{3}dx\\
=\frac{1}{9}
\end{align}$$

