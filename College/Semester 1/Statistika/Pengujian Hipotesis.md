Hipotesis adalah sebuah pernyataan. Di ilmu statistika, biasanya pernyataan ini merupakan hasil hitung / penaksiran. Namun, tidak semua penaksiran ternyata benar. Di bab ini, kita belajar cara menguji sebuah hipotesis.

- Misalkan ada data dan hipotesisnya, maka hipotesis tersebut akan disingkat menjadi $H_0$. Anti-hipotesis dari hipotesis tersebut adalah $H_1$
- Kedua $H$ bersifat eksklusif, berarti hanya 1 yang benar. Jika $H_0$ benar, maka $H_1$ salah, sebaliknya juga.

# Cara Menentukan Daerah Kritis
Untuk menemukan daerah kritis, bisa dilihat dari $H_0$ dan $Z$. Misal $H_0: \mu > n$, maka daerah kritis adalah ketika $Z_H <= Z$, alias di bagian kiri. Jika ternyata $Z_H = Z$, maka tetap ditolak.

Bisa dibilang Z adalah "batas penerimaan". Jika ternyata $Z_H > Z$, maka hipotesis diterima

# Hipotesis Rata-rata
Misal terdapat sebuah cerita, di mana kita disajikan data dan kesimpulan bahwa $\mu = x$. Maka, hipotesis dari kesimpulan itu adalah $H_0: \mu = x$. Lawanan / anti-hipotesis $H_0$ adalah $H_1: \mu \neq x$.

Untuk menguji $H_0$, diperlukan 2 hal, yaitu daerah kritis dan "Titik Hitung". Jika "titik hitung" berada di luar daerah kritis, maka $H_0$ benar / diterima.

Untuk memudahkan, "titik hitung" akan memiliki *subscript* $_H$ 

## Titik Hitung Rata-rata, $\sigma$ diketahui
$$\begin{align}
Z_H = \frac{\bar{x}-\mu}{\frac{\sigma}{\sqrt{n}}}
\end{align}$$

## Titik Hitung Rata-rata, $\sigma$ tidak diketahui
$$\begin{align}
t_H = \frac{\bar{x}-\mu}{\frac{s}{\sqrt{n}}}\\
v=n-1
\end{align}$$

## Contoh Soal Pengujian Hipotesis Rata-rata
1. Sebuah perusahaan menyatakan bahwa rata-rata lama hidup bohlam yang mereka buat adalah 1600 jam pas, dengan $\alpha = 5\%$ dan $\sigma = 120$. Misal kita ambil 100 sampel dan ternyata rata-rata sampel lama hidupnya 1570 jam dengan standar deviasi 100 jam, apakah hipotesis tersebut benar?
$$\begin{align}
H_0: \mu=1600\\
H_1: \mu \neq 1600\\
---\\
\mu = 1600\\
\alpha = 5\% = 0.05 \rightarrow \frac{\alpha}{2} = 0.025\rightarrow 1-0.025 = 0.975\\
\sigma = 120\\
n = 100\\
\bar{x} = 1570\\
s = 100\\
---\\
Z_H = \frac{1570-1600}{\frac{120}{\sqrt{100}}}=-2.5\\
\\
Z_{0.975} = 1.96\\
Z_{0.025} = -1.96\\
\\
Z_H \neq Z<Z_H<Z\text{, hipotesis ditolak karena }Z_H\text{ berada di daerah kritis}
\end{align}$$
![[Uji Hipotesis 1.svg]]

2. Sebuah perusahaan menyatakan bahwa rata-rata lama hidup bohlam mereka 1500 jam. Namun, pihak lain tidak percaya, dan menyatakan bahwa rata-ratanya lebih kecil dari 1500 jam. Untuk mengecek, diambil 16 sampel yang setelah dihitung memiliki rata-rata 1450 jam dengan standar deviasi 100 jam dan $\alpha = 5\%$. Carilah hipotesis yang benar!
$$\begin{align}
H_0: \mu = 1500\\
H_1: \mu <= 1500\\
---\\
\mu = 1500\\
n = 16\\
\bar{x} = 1450\\
s = 100\\
\alpha = 5\% = 0.05\\
---\\
v = 16-1 = 15\\
t_H = \frac{1450-1500}{\frac{100}{\sqrt{16}}}=-2\\
\\
t_{0.05;15}=1.753\\
\\
Z_H < Z\text{, Karena }Z_H\text{ berada di daerah kritis, maka hipotesis ditolak}
\end{align}$$
![[Uji Hipotesis 2.svg]]


# Hipotesis Selisih Rata-rata
Misal terdapat 2 sampel yang berbeda dan terdapat hipotesis yang membandingkan kedua rata-rata, maka bisa dicari kebenaran hipotesis tersebut

$d$ adalah selisih $\mu_A - \mu_B$, namun opsional dan jika tidak diberi, maka $0$
## Hipotesis Selisih Rata-rata, $\sigma_A$ dan $\sigma_B$ diketahui
$$\begin{align}
Z_H = \frac{(\bar{x}_A - \bar{x}_B)-d}{\sqrt{\frac{\sigma_A^2}{n_A}+\frac{\sigma_B^2}{n_B}}}
\end{align}$$

## Hipotesis Selisih Rata-rata, $\sigma_A = \sigma_B$ namun tidak diketahui
$$\begin{align}
t_H = \frac{(\bar{x}_A - \bar{x}_B)-d}{S_P \sqrt{\frac{1}{n_A}+\frac{1}{n_B}}}\\
v = n_A + n_B-2\\
S_P^2 = \frac{(n_A - 1)S_A^2 + (n_B - 1)S_B^2}{n_A + n_B -2}
\end{align}$$
## Hipotesis Selisih Rata-rata, $\sigma_A \neq \sigma_B$ dan tidak diketahui
$$\begin{align}
t_H = \frac{(\bar{x}_A - \bar{x}_B)-d}{\sqrt{\frac{S_A^2}{n_A}+\frac{_
B^2}{n_B}}}\\
\\
v = \frac{(\frac{S_A^2}{n_A}+\frac{S_B^2}{n_B})^2}{\frac{(\frac{S_A^2}{n_A})^2}{n_A-1}+\frac{(\frac{S_B^2}{n_B})^2}{n_B-1}}
\end{align}$$

## Contoh Soal Hipotesis Selisih Rata-rata
1. Misal terdapat 2 produsen disket: A dan B. Ada klaim bahwa rata-rata usia disket A lebih lama dari B. Maka, dilakukan pengujian, di mana 60 disket A dan 75 disket B dites dengan tingkat keyakinan 95%. Hasil tes tersebut menyatakan rata-rata usia disket A 106 bulan dan disket B 100 bulan. Jika standar deviasi populasi disket A 20 bulan dan disket B 15 bulan, apakah benar hipotesis yang diberikan tadi?
$$\begin{align}
H_0: \mu_A gt \mu_B\\
H_1: \mu_A \le \mu_B\\
---\\
n_A = 60\\
n_B = 75\\
\alpha = 5\% = 0.05\rightarrow 1-0.05 = 0.95\\
\bar{x}_A = 106\\
\bar{x}_B = 100\\
\sigma_A = 20\\
\sigma_b = 15\\
---\\
Z_H=\frac{106-100-0}{\sqrt{\frac{20^2}{60}+\frac{15^2}{75}}}=1.93\\
Z_{0.95} = 1.645\\
\\
Z_H \neq Z_H > Z\text{, hipotesis ditolak}
\end{align}$$
2. Lihat cerita di atas, misalkan $\sigma_A = \sigma_B$, namun tidak diketahui, $s_A = 20$ dan $s_B = 15$, $\bar{x}_A = 100$, $\bar{x}_B = 110$!
$$\begin{align}
H_0: \mu_A \gt \mu_B\\
H_1: \mu_A \le \mu_B\\
---\\
n_A = 10\\
n_B = 12\\
\alpha = 5\% = 0.05\\
\bar{x}_A = 100\\
\bar{x}_B = 110\\
s_A = 20\\
s_B = 15\\
\sigma_A = \sigma_B\\
---\\
S_P^2 = \frac{(10-1)20^2+(12-1)15^2}{10+12-2}= 303.75\\
v = 10+12-2 = 20\\
t_H = \frac{100-110-0}{\sqrt{303.75}\sqrt{\frac{1}{10}+\frac{1}{12}}}=-1.34\\
t_{0.05;20} = -1.724\\
\\
t_H = t_H > t\text{, hipotesis diterima}
\end{align}$$

# Hipotesis Proporsi
Misal kita diberi suatu populasi dan hipotesis mengenai populasi tersebut. Kita juga diberi sampel dan hasil tes sampel tersebut. Maka, kita dapat menguji kebenaran hipotesis proporsi tersebut:

## Sampel Kecil
$$\begin{align}
2\cdot \Sigma_{x=0}^n \binom{n}{x}(p)^x(q)^{n-x}
\end{align}$$
## Sampel Besar
$$\begin{align}
Z = \frac{x-np}{\sqrt{npq}}=\frac{\hat{p}-p}{\sqrt{\frac{pq}{n}}}\\
\hat{p} = \frac{x}{n}
\end{align}$$
## Contoh Soal Hipotesis Proporsi
1. Ada sebuah klaim bahwa 70% rumah memiliki AC. Jika di tes 15 rumah, di mana ternyata 8 memiliki AC, apakah hipotesis tersebut masih valid? Gunakan $\alpha = 10\%$
$$\begin{align}
H_0: p = 0.7\\
H_1: p \neq 0.7\\
---\\
n = 15\\
x = 8/15\\
\alpha = 0.1\\
---\\
P=2\cdot \Sigma_{x=0}^{8} \binom{n}{x}(0.7)^x(0.3)^{15-x} = 2 \cdot 0.1311 = 0.2622\\
P > \alpha\text{, hipotesis diterima}
\end{align}$$
2. Sebuah obat baru diperkirakan maksimal 60% efektif. Dari tes, 70 dari 100 orang mengalami hasil yang bagus. Apakah hipotesis tersebut benar? Gunakan $\alpha = 0.05$.
$$\begin{align}
H_0: p < 0.6\\
H_1: P \ge 0.6\\
---\\
p = 0.6\\
q = 0.4\\
\hat{p} = 0.7\\
\hat{q} = 0.3\\
\alpha = 0.05\rightarrow 1-0.05 = 0.95\\
---\\
\hat{p} = \frac{70}{100} = 0.7\\
Z_H = \frac{0.7-0.6}{\sqrt{\frac{0.6\cdot0.4}{100}}}=2.04\\
Z_{0.95}=1.645\\
\\
Z_H \neq Z_H > Z\text{, hipotesis ditolak}
\end{align}$$
3. 200 batere dicek dan ternyata ada 6 yang rusak. Apakah tes ini menyatakan kerusakan di bawah 5%? gunakan $\alpha = 0.05$
$$\begin{align}
H_0: P < 0.5\\
H_1: P \ge 0.5\\
---\\
p = 5\%\\
q = 0.5\\
\hat{p} = 6/200 = 0.03\\
\hat{p} = 0.97\\
\alpha = 0.05\\
---\\
Z_H = \frac{0.03-0.05}{\sqrt{\frac{0.05\cdot 0.95}{200}}}=-1.29\\
Z_{0.05} = -1.645\\
Z_H > Z\text{, hipotesis diterima}
\end{align}$$
# Hipotesis Dua Proporsi
$$\begin{align}
\hat{p}_A = \frac{x_A}{n_A}\\
\hat{p}_B = \frac{x_B}{n_B}\\
\hat{p} = \frac{x_A+x_B}{n_A+n_B}\\
Z = \frac{\hat{p}_A - \hat{p}_B}{\sqrt{\hat{p}\hat{q}(\frac{1}{n_A}+\frac{1}{n_B})}}
\end{align}$$
## Contoh Soal Hipotesis Dua Proporsi
1. Beberapa desa akan memungut suara untuk persetujuan pembuatan pabrik. Misal 120 dari 200 penduduk desa setuju dan 240 dari 500 penduduk desa sekitar menyetujuinya, apakah proporsi penduduk desa yang setuju lebih tinggi daripada desa sekitar? gunakan $\alpha = 0.05$
$$\begin{align}
H_0: p_A > p_B\\
H_1: p_A \le p_B\\
---\\
\alpha = 0.05\\
\hat{p}_A = 120/200 = 0.6\\
\hat{p}_B = 240/500 = 0.48\\
---\\
\hat{p} = \frac{120+240}{200+500}=0.51\\
Z_H = \frac{0.6-0.48}{\sqrt{0.51\cdot 0.49 (\frac{1}{200}+\frac{1}{500})}}=2.87\\
Z_{0.05} = \pm1.96\\
\\
Z_H \gt Z\text{, hipotesis diterima, penduduk desa lebih menyutujui daripada desa sekitar}
\end{align}$$
# Hipotesis Varians
$$\begin{align}
\chi^2 = \frac{(n-1)S^2}{\sigma^2}
\end{align}$$

## Contoh Soal Hipotesis Varians
1. Sebuah produsen batere mengklaim bahwa batere mereka bersifat distributif normal, dengan standar deviasi 0.9. Dilakukan inspeksi di mana 10 sampel dicek, dan dihasilkan standar deviasi 1.2. Apakah $\sigma \gt 0.9$? gunakan $\alpha = 0.05$
$$\begin{align}
H_0: \sigma > 0.9\\
H_1: \sigma \le 0.9\\
---\\
n = 10\\
\sigma = 0.9\\
S = 1.2\\
\alpha = 0.05\\
---\\
\chi^2_H = \frac{9\cdot 1.2^2}{0.9^2}=16\\
\chi^2_{0.05;10}=18\\
\\
\chi_H^2 < \chi^2\text{, hipotesis diterima}
\end{align}$$

# Hipotesis Selisih / Rasio Varians
## Cek $\sigma_A = \sigma_B$?
$$\begin{align}
f_H = \frac{s_A^2}{s_B^2}
\end{align}$$
Setelah mencari nilai $f_H$, kita bandingkan dengan batas $f_H < f_{1-0.5\alpha;vA;vB} \text{ dan }f > f_{0.5\alpha;vA;vB}$, di mana $v_A = n_A - 1 \text{ dan } v_B = n_B - 2$.

## Cek $\sigma_A > \sigma_B \text{ atau }\sigma_A < \sigma_B$?
Setelah mencari $f_H$:
- $\sigma_A > \sigma_B\rightarrow f_H > f_{\alpha;v1;v2}$
- $\sigma_A < \sigma_B \rightarrow f_H < f_{1-\alpha;v1;v2}$

## Contoh Soal Hipotesis Selisih Varians
1. Sebuah percobaan sosial dilakukan untuk membuktikan bahwa $\sigma_W^2 = \sigma_P^2$. Kita misalkan waktu yang dibutuhkan ber-distribusi normal. Setelah dilakukan percobaan, didapatkanlah hasil seperti berikut:

| Pria      | Wanita    |
| --------- | --------- |
| $n = 11$  | $n = 14$  |
| $S = 6.1$ | $S = 5.3$ |
Misalkan setelah eksperimen, ada yang mengatakan bahwa ternyata $\sigma_W^2 < \sigma_P^2$. Buktikanlah mana yang benar, dengan $\alpha = 0.1$!

$$\begin{align}
H_0: \sigma_W^2 = \sigma_P^2\\
H_1: \sigma_W^2 \neq \sigma_P^2\\
---\\
\text{Misalkan pria = A, wanita = B}\\
n_A = 11\\
S_A = 6.1\\
n_B = 14\\
S_B = 5.3\\
\alpha = 0.05\rightarrow 1-\alpha = 0.95\\
---\\
f_H = \frac{6.1^2}{5.3^2}=1.324\\
f_{0.05;10;13}=2.671\\
f_{1-0.05;10;13}=0.346\\
\\
f_H \neq f_H < f \wedge f_H > f\text{, hipotesis diterima}
\end{align}$$

# Uji $\chi^2$ (Chi-Squared)
Berikut adalah rumus untuk menentukan $\chi_H^2$:
$$\begin{align}
\chi_H^2 = \Sigma_{i=1}^n \frac{(O_i-E_i)^2}{E_i}
\end{align}$$
dengan daerah kritis: $\chi_H^2 < \chi^2$ ($\chi_H^2$ **tidak melebihi** $\chi^2$ agar $H_0$ diterima)

## Pembuatan Tabel
Setiap uji $\chi^2$ memerlukan tabel seperti berikut:

| $n$ | $O_i$ | $E_i$ | $\frac{(O_i-E_i)^2}{E_i}$ |
| --- | ----- | ----- | ------------------------- |
di mana:
- $n$ = jumlah kategori
- $O_i$ = berapa kategori tersebut muncul
- $E_i$ = harapan kategori muncul

## Good of Fit Test
Tipe pertama ujian $\chi^2$, di gunakan untuk memastikan distribusi / peluang dalam cerita adalah benar.
$$\begin{align}
E_i = P\cdot N
\end{align}$$
- Jangan keliru, $N$ adalah berapa kali percobaan dilakukan, sementara $n$ adalah jumlah kategori

## Contoh Soal Good of Fit Test
1. Sebuah dadu dilempar 120 kali. Apakah dadu ini dadu yang adil? Gunakanlah $\alpha = 0.05$!

| $n$ | $O_i$ |
| --- | ----- |
| 1   | 25    |
| 2   | 17    |
| 3   | 15    |
| 4   | 23    |
| 5   | 24    |
| 6   | 16    |

Dari data tersebut, bisa disimpulkan peluang dadu yang adil adalah ketika $E_i = 120\div 6 = 20$, maka:

| $n$ | $O_i$ | $E_i$ | $\frac{(O_i-E_i)^2}{E_i}$ |
| --- | ----- | ----- | ------------------------- |
| 1   | 25    | 20    | 1.25                      |
| 2   | 17    | 20    | 0.45                      |
| 3   | 15    | 20    | 1.25                      |
| 4   | 23    | 20    | 0.45                      |
| 5   | 24    | 20    | 0.8                       |
| 6   | 16    | 20    | 0.8                       |
$\chi_H^2 = \Sigma \frac{(O_i-E_i)^2}{E_i} = 5$

$\chi_{0.05;5} = 11.07$

$\chi_H^2 < \chi^2$, Hipotesis dadu adil diterima

## Uji Kebebasan
Adalah tipe lain dari Good of Fit Test, digunakan ketika terdapat kategori A dan B pada cerita, sehingga terdapat $A\cdot B$ kategori. Hal yang berbeda adalah $\chi^2$, di mana rumusnya berubah menjadi $\chi_{\alpha;vA \cdot vB}^2$.

Karena tabel memiliki kategori yang saling berhubungan, maka $E_i = \frac{n_{An} \cdot n_{Bn} }{N}$

## Contoh Soal Uji Kebebasan
1. Terdapat tabel antara umur dengan minuman seperti berikut, apakah faktor umur memengaruhi selera minum? Gunakan $\alpha = 0.05$!
![[Soal uji kebebasan 1.png]]

![[Soal uji kebebasan 1 - 2.png]]

![[Soal uji kebebasan 1 - 3.png]]

$\chi^2_{0.05;3\cdot 2} = 12.592$

$\chi_H \neq \chi_H < \chi^2$, Hipotesis ditolak

# Uji Liliefors