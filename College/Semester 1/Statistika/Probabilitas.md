# Peluang Pengambilan
## Dengan Pengembalian

$P(X=n) = \binom{N}{n}(\text{Peluang terjadi})^{n}(\text{Peluang tidak terjadi})^{N-n}$

"Jika kita mengambil $N$, **dengan pengembalian**, hitunglah distribusi $n$ terjadi"

### Contoh Soal

1. Kotak berisi 4 bola hitam & 2 bola hijau. Jika 3 bola diambil satu-per-satu dengan pengembalian, hitunglah distribusi probabilitas bola hijau terambil. Misalkan $X$ adalah bola hijau.
   
   $$\begin{align}
   P(X = 0) = \binom{3}{0}(\frac{1}{3})^0(\frac{2}{3})^3\\
   P(X = 1) = \binom{3}{1}(\frac{1}{3})^1(\frac{2}{3})^2\\
   P(X = 2) = \binom{3}{2}(\frac{1}{3})^2(\frac{2}{3})^1\\
   P(X = 3) = \binom{3}{3}(\frac{1}{3})^3(\frac{2}{3})^0\\   
   \end{align}$$
## Tanpa Pengembalian
   
   $P(X = n) = \frac{(\text{C Banyak pengambilan dengan peluang terjadi})(\text{C Sisa barang dengan peluang sisa})}{\text{C Total barang dengan hal yang dicari}}$

### Contoh Soal

1. Kiriman 7 TV ternyata memiliki 2 TV cacat. Sebuah hotel membeli 3 TV secara acak. Jika $X$ adalah TV cacat, temukan distribusi probabilitas $X$
   
   $$\begin{align}
   P(X = 0) = \frac{\binom{3}{0}\binom{4}{2}}{\binom{7}{2}}\\
   P(X = 1) = \frac{\binom{3}{1}\binom{4}{1}}{\binom{7}{2]}}\\
   P(X = 1) = \frac{\binom{3}{2}\binom{4}{0}}{\binom{7}{2}}
   \end{align}$$



# Distribusi Fungsi
## CDF
Sebuah fungsi merupakan CDF jika memenuhi semua syarat berikut:

- $f(x) \ge 0$
- $\begin{align} \sum_{x} f(x) = 1 \end{align}$
- $P(X = x) = f(x)$

## PDF
Sebuah fungsi merupakan PDF jika memenuhi semua syarat berikut:

- $f(x) \ge 0$
- $\int_{- \infty}^{\infty} f(x) dx = 1$
- $P(a \lt X \lt b) = \int_a^b f(x) dx$

## Contoh Soal
1. Sebuah radar kecepatan memiliki interval deteksi per jam dengan fungsi berikut:
   $$\begin{align}
   1-e^{-8x}, x \ge 0\\
   0,x\lt 0
   \end{align}$$
   Berapa peluang menunggu kurang dari 12 menit (0,2 jam) untuk radar itu mendeteksi mobil membalap? Hitunglah menggunakan:
   A. CDF
   (Fungsi tersebut merupakan CDF karena memenuhi semua syarat, langsung di substitusi)
   $1-e^{-8(0.2)} \approx 0.798$
   
   B. PDF
   (Fungsi CDF bisa diubah menjadi PDF dengan cara diturunkan)
   (Untuk mendapat hasil dari PDF, perlu di integralkan dengan batas atas & bawah yang sudah ditentukan)
   
   $\int_0^{0.2} \frac{8}{e^{8x}} dx \approx 0.798$ 