1. Sebuah pabrik ingin mengangkat seorang calon untuk menjadi manager. Calon yang dipilih bisa sukses 60%. Kemudian, diadakan tes sikap, sehingga yang sukses bisa lolos tes 80% dan yang tidak sukses hanya bisa lolos tes 30%.
	1. A. Peluang orang lulus tes?
	   $0.6\cdot 0.8 + 0.4\cdot 0.3 = 0.48 + 0.12 = 0.6$
	   
	2. Misal seseorang lulus tes, berapa kemungkinan dia tidak sukses?
	   $$\begin{align}
	   P(\text{Tidak sukses}|\text{Lulus Tes})= \frac{P(\text{Lulus tes dan tidak sukses)}}{P(\text{Lulus Tes})}\\
	   = \frac{0.3}{0.6} = \frac{1}{2}
	   \end{align}$$

2. Di sebuah perusahaan, kemungkinan seorang pegawai telat masuk dapat dirumuskan seperti berikut:
$$\begin{align}
f(x)=
\begin{cases}
\frac{3}{(4)(50^3)}(50^2-x^2),-50\le x \le 50\\
0, \text{ lainnya}
\end{cases}
\end{align}$$
- Tentukan nilai harapan pegawai terlambat
$$\begin{align}
\int_{-\infty}^{\infty}xf(x)dx\\
=\int_{-\infty}^\infty x \frac{3}{(4)(50^3)}(50^2-x^2)dx\\
=0 + \int_{-50}^{50} x\frac{3}{(4)(50^3)}(50^2-x^2)dx+0\\
=\frac{3}{4(50^3)}\int_{-50}^{50}x(50^2-x^2)dx\\
=\frac{3}{4(50^3)}[\frac{1}{2}50^2x^2-\frac{1}{4}x^4]^{50}_{-50}\\
=0
\end{align}$$

- Tentukan $E(X^2)$
  

- Tentukan Standar Deviasi

3. Menurut peneliti, peluang kelahiran bayi laki-laki dan perempuan sama-sama 0.5. Jika disurvey 100000 keluarga dengan 5 anak, tentukan:
- Jumlah keluarga yang anak laki-laki > anak perempuan
(L,P) = (3,2), (4,1), (5,0)
$$\begin{align}
\Sigma_{x=3}^5 (\binom{5}{x}(0.5)^x(0.5)^{5-x}) = 0.5\\
\\
0.5 \cdot 100000 = 50000
\end{align}$$
- Jumlah keluarga yang anak perempuan <= 2
(L,P) = (5,0),(4,1),(3,2)

(sama saja dengan contoh di atas)

- Tentukan total anak laki-laki dan anak perempuan yang disurvey
(L,P) = (0,5),(1,4),(2,3),(3,2),(4,1),(5,0)
$$\begin{align}
\cdot (0,5) = \binom{5}{0}(0.5)^{0}(0.5)^5 = 0.03125 \cdot 100000 = 3125\\
\cdot (1,4) = \binom{5}{1}(0.5)^1(0.5)^4 = 0.15625 \cdot 100000 = 15625\\
\cdot (2,3) = \binom{5}{3}(0.5)^2(0.5)^3 = 0.3125 \cdot 100000 = 31250\\
\cdot (3,2) = 0.3125 \rightarrow 31250\\
\cdot (4,1) = 0.15625 \rightarrow 15625\\
\cdot (5,0) = 0.03125 \rightarrow 3125\\
\\
\end{align}$$
Hasil perkalian tersebut adalah keluarga dengan komposisi anak di kiri. kalikan anak dengan keluarga, kemudian totalkan.

Cara lain: total anak 500,000 (100,000 keluarga, setiap keluarga 5 anak); peluang antara laki-laki / perempuan 0.5. 500,000 * 0.5 = 250k setiap kelamin.

4. Sebuah negara memiliki pendapatan per kapita $1000 dengan standar deviasi $150 (distribusi normal).
- Persentase keluarga < $800
$$\begin{align}
Z = \frac{800-1000}{150} = -1.33 = 0.0918
\end{align}$$
- Persentase keluarga > $1500 $\rightarrow$ 1 - P<1500
$$\begin{align}
Z = \frac{1500-1000}{150} = 3.33 = 1 - 0.9996 = 0.0004
\end{align}$$
- Misal terdapat 20 juta keluarga, berapa keluarga termasuk kategori $850 < x < $1250
$$\begin{align}
\cdot Z = \frac{850-1000}{150} = -1 = 0.1587\\
\cdot Z = \frac{1250-1000}{150} = 1.66 = 0.9515\\
\\
Z = 0.9515-0.1587 = 0.7928 \cdot 20,000,000 = 15856000 \text{ keluarga}
\end{align}$$
5. Dari 100k komputer, 10k cacat. Carilah peluang 12 unit dari 100 cacat menggunakan distribusi:
- Hipergeometrik
$$\begin{align}
\frac{100!}{88!12!}(0.1)^{12}(0.9)^{88}
\end{align}$$
- Binomial
$$\begin{align}
\binom{100}{12}(0.1)^{12}(0.9)^{88}
\end{align}$$
- Normal
$$\begin{align}
Z = \frac{x-\mu}{\sigma}\\
\mu = 100\cdot0.1=10\\
\sigma = \sqrt{0.1\cdot0.9\cdot100}=3\\
\\
Z = \frac{12-10}{3}=\frac{2}{3} \rightarrow 
\end{align}$$