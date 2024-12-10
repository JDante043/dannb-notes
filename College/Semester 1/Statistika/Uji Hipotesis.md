# Uji Rata-rata
## $\sigma^2$ Diketahui
$$\begin{align}
Z_H = \frac{\bar{x}-\mu_0}{\frac{\sigma}{\sqrt{n}}}
\end{align}$$

| Ketika $H_0$ | Ketika $H_1$   | Daerah Kritikal ($H_0$ Ditolak)                |
| ------------ | -------------- | ---------------------------------------------- |
| $\mu=\mu_0$  | $\mu<\mu_0$    | $Z_H < - Z_{\alpha}$                           |
| $\mu=\mu_0$  | $\mu>\mu_0$    | $Z_H > Z_{\alpha}$                             |
| $\mu=\mu_0$  | $\mu\neq\mu_0$ | $Z_H<-Z_{0.5\alpha}$ dan $Z_H > Z_{0.5\alpha}$ |
## $\sigma^2$ Tidak diketahui
$$\begin{align}
v = n-1\\
t_H = \frac{\bar{x}-\mu_0}{\frac{s}{\sqrt{n}}}
\end{align}$$

| Ketika $H_0$  | Ketika $H_1$   | Daerah Kritikal ($H_0$ Ditolak)                |
| ------------- | -------------- | ---------------------------------------------- |
| $\mu = \mu_0$ | $\mu<\mu_0$    | $t_H<-t_{\alpha}$                              |
| $\mu = \mu_0$ | $\mu>\mu_0$    | $t_H>t_{\alpha}$                               |
| $\mu = \mu_0$ | $\mu\neq\mu_0$ | $t_H<-t_{0.5\alpha}$ dan $t_H > t_{0.5\alpha}$ |

# Uji Selisih Rata-rata
## $\sigma_A^2$ dan $\sigma_B^2$ Diketahui
$$\begin{align}
Z_H = \frac{(\bar{x}_A - \bar{x}_B)-d_0}{\sqrt{\frac{\sigma_A^2}{n_A}+\frac{\sigma_B^2}{n_B}}}
\end{align}$$

| Ketika $H_0$          | Ketika $H_1$             | Daerah Kritikal ($H_0$ Ditolak)                  |
| --------------------- | ------------------------ | ------------------------------------------------ |
| $\mu_A - \mu_B = d_0$ | $\mu_A - \mu_B < d_0$    | $Z_H < -Z_{\alpha}$                              |
| $\mu_A - \mu_B = d_0$ | $\mu_A - \mu_B > d_0$    | $Z_H > Z_{\alpha}$                               |
| $\mu_A - \mu_B = d_0$ | $\mu_A - \mu_B \neq d_0$ | $Z_H < -Z_{0.5\alpha}$ dan $Z_H > Z_{0.5\alpha}$ |

## $\sigma_A^2 = \sigma_B^2$, Tidak Diketahui
$$\begin{align}
v = n_A + n_B -2\\
S_P^2=\frac{(n_A-1)S_A^2+(n_B-1)S_B^2}{n_A+n_B-2}\\
t_H = \frac{(\bar{x}_A - \bar{x}_B)-d_0}{S_P\sqrt{\frac{1}{n_A}+\frac{1}{n_B}}}
\end{align}$$

| Ketika $H_0$          | Ketika $H_1$             | Daerah Kritikal ($H_0$ DItolak)                  |
| --------------------- | ------------------------ | ------------------------------------------------ |
| $\mu_A - \mu_B = d_0$ | $\mu_A - \mu_B < d_0$    | $t_H < -t_{\alpha}$                              |
| $\mu_A - \mu_B = d_0$ | $\mu_A - \mu_B > d_0$    | $t_H > t_{\alpha}$                               |
| $\mu_A - \mu_B = d_0$ | $\mu_A - \mu_B \neq d_0$ | $t_H < -t_{0.5\alpha}$ dan $t_H > t_{0.5\alpha}$ |

## $\sigma_A^2 \neq \sigma_B^2$, Tidak Diketahui
$$\begin{align}
t_H = \frac{(\bar{x}_A - \bar{x}_B)-d}{\sqrt{\frac{S_A^2}{n_A}+\frac{S_
B^2}{n_B}}}\\
\\
v = \frac{(\frac{S_A^2}{n_A}+\frac{S_B^2}{n_B})^2}{\frac{(\frac{S_A^2}{n_A})^2}{n_A-1}+\frac{(\frac{S_B^2}{n_B})^2}{n_B-1}}
\end{align}$$

| Ketika $H_0$          | Ketika $H_1$             | Daerah Kritikal ($H_0$ DItolak)                  |
| --------------------- | ------------------------ | ------------------------------------------------ |
| $\mu_A - \mu_B = d_0$ | $\mu_A - \mu_B < d_0$    | $t_H < -t_{\alpha}$                              |
| $\mu_A - \mu_B = d_0$ | $\mu_A - \mu_B > d_0$    | $t_H > t_{\alpha}$                               |
| $\mu_A - \mu_B = d_0$ | $\mu_A - \mu_B \neq d_0$ | $t_H < -t_{0.5\alpha}$ dan $t_H > t_{0.5\alpha}$ |

# Uji Paired Observations
$$\begin{align}
v=n-1\\
t_H = \frac{\bar{d}-d_0}{\frac{s_d}{\sqrt{n}}}
\end{align}$$

| Ketika $H_0$  | Ketika $H_1$     | Daerah Kritikal ($H_0$ DItolak)                  |
| ------------- | ---------------- | ------------------------------------------------ |
| $\mu_D = d_0$ | $\mu_D < d_0$    | $t_H < -t_{\alpha}$                              |
| $\mu_D = d_0$ | $\mu_D > d_0$    | $t_H > t_{\alpha}$                               |
| $\mu_D = d_0$ | $\mu_D \neq d_0$ | $t_H < -t_{0.5\alpha}$ dan $t_H > t_{0.5\alpha}$ |

# Uji Proporsi
## Sampel kecil

Binomial: $\binom{n}{x}(p)^x (q)^{n-x}$
Daerah kritis saat $P \le \alpha$
### $H_1: P < P_0$
$$\begin{align}
P(X \le x)
\end{align}$$
### $H_1: P > P_0$
$$\begin{align}
P(X \ge x)
\end{align}$$
### $H_1: P\neq P_0$
$$\begin{align}
2P(X\le x);x<np_0\\
2P(X\ge x);x>np_0
\end{align}$$
## Sampel Besar
$$\begin{align}
Z_H = \frac{x-np_0}{\sqrt{np_0q_0}} = \frac{\hat{p}-p_0}{\sqrt{\frac{p_0q_0}{n}}}
\end{align}$$

| Daerah Kritis                                            |
| -------------------------------------------------------- |
| $Z_H<-Z_{0.5\alpha}$ dan $Z_H>Z_{0.5\alpha}$; Two tailed |
| $Z_H<-Z_{\alpha}$; $p<p_0$                               |
| $Z_H > Z_{\alpha}$; $p>p_0$                              |

# Uji 2 Proporsi
$$\begin{align}
\hat{p}_A = \frac{X_A}{n_A}\\
\hat{p}_B = \frac{X_B}{n_B}\\
p = \frac{X_A+X_B}{n_A+n_B}\\
Z_H = \frac{\hat{P}_A - \hat{P}_B}{\sqrt{pq(\frac{1}{n_A}+\frac{1}{n_B})}}
\end{align}$$

| Daerah Kritis                                                    |
| ---------------------------------------------------------------- |
| $Z_H < -Z_{0.5\alpha}$ dan $Z_H > Z_{0.5\alpha}$; $P_A \neq P_B$ |
| $Z_H < -Z_{\alpha}$; $P_A < P_B$                                 |
| $Z_H > Z_{\alpha}$; $P_A > P_B$                                  |

# Uji Varians
$$\begin{align}
v=n-1\\
\chi_H^2 = \frac{(n-1)S^2}{\sigma^2}
\end{align}$$

| Daerah Kritis                                                                     |
| --------------------------------------------------------------------------------- |
| $\chi_H^2 < \chi_{1-0.5\alpha}^2$ dan $\chi_H^2 > \chi_{0.5\alpha}^2$; Two-tailed |
| $\chi_H^2 < \chi_{1-\alpha}^2$; $\sigma^2 < \sigma_0$                             |
| $\chi_H^2 > \chi_{\alpha}^2$; $\sigma^2 > \sigma_0$                               |
# $\chi^2$

(header) Tabel adalah

| $x$ | $O_i$ | $E_i$ | $\frac{(O_i - E_i)^2}{E_i}$ |
| --- | ----- | ----- | --------------------------- |
|     |       |       |                             |

# Uji Rasio Varians
$$\begin{align}
f_H = \frac{S_A^2}{S_B^2}
\end{align}$$

| Daerah Kritis                                                         |
| --------------------------------------------------------------------- |
| $f_H<f_{1-0.5\alpha;vA;vB}$ dan $f_H>f_{0.5\alpha;vA;vB}$; Two-tailed |
| $f_H<f_{1-0.5\alpha;vA;vB}$; $\sigma_A^2 <\sigma_B^2$                 |
| $f_H>f_{0.5\alpha;vA;vB}$;$\sigma_A^2 > \sigma_B^2$                   |
|                                                                       |

# Uji Bartlett / Uji multivarians
Terdapat beberapa langkah untuk melakukan uji Bartlett:

## Menghitung b (daerah kritis)
Terdapat 2 cara menghitung daerah kritis, tergantung dengan ukuran sampel setiap populasi:
### Daerah kritis ketika semua sampel sama besar ($n_A = n_B = ...$)
Lihat tabel, cari $b_{k;\alpha;n}$, di mana:
- $k$ = total / jumlah populasi
- $\alpha$ = konfidensi
- $n$ = jumlah sampel di setiap populasi

### Daerah kritis ketika setiap sampel beda besar ($n_A \neq n_B \neq ...$)
$$\begin{align}
b = \frac{(n_A)(b_{k;\alpha;n_A})+(n_B)(b_{k;\alpha;n_B})+...}{N}
\end{align}$$

## Menghitung $b_H$
$$\begin{align}
S_P^2 = \frac{(n_A-1)S_A^2+(n_B-1)S_B^2+...}{n_A -1 + n_b-1 + ...}\\
\\
b_H = \frac{(S_A^2)^{n_A-1}\cdot (S_B^2)^{n_B-1}\cdot...}{S_P^2}
\end{align}$$

Daerah kritis selalu left-tailed $(b_H < b)$

# Analisis Varians / ANOVA
ANOVA merupakan tes rata-rata yang bisa dipakai ketika populasi lebih dari 2

## Daerah Kritis
Daerah kritis ANOVA selalu $f_H < f$, artinya $H_0$ akan ditolak ketika $f_H$ lebih kecil dari tabel $f$

## ANOVA 1 Faktor
Terdapat beberapa langkah untuk mengerjakan metode ANOVA:
1. Hitung rata-rata setiap sampel ($\bar{x}_A, \bar{x}_B,...$)
2. Hitung varians setiap sampel ($S_A^2, S_B^2, ...$)
3. Hitung rata-rata dari varians sampel ($\bar{x}_{S^2}$)
4. Hitung rata-rata dari rata-rata sampel ($\bar{\bar{x}}$)
5. Hitung varians dari rata-rata sampel dengan rata-rata rata-rata sampel ($\S_{\bar{\bar{x}}}^2$)
6.  Hitunglah $f_H$ dengan: $$\begin{align}
f_H = \frac{n\cdot S_{\bar{\bar{x}}}^2}{\bar{x}_{S^2}}
\end{align}$$

## ANOVA Multifaktor
Untuk mengerjakan ANOVA multifaktor, maka digunakan tabel ANOVA:

| Variasi     | Derajat Kebebasan (V) | Jumlah Kuadrat (SS)                            | Rata-rata Kuadrat (MS) | Statistik F       |
| ----------- | --------------------- | ---------------------------------------------- | ---------------------- | ----------------- |
| Faktor A    | $N_A -1$              | $N_B \cdot \Sigma (\bar{x}_A-\bar{\bar{x}})^2$ | $\frac{SSA}{V_A}$      | $\frac{MSA}{MSE}$ |
| Faktor B    | $N_B -1$              | $N_A\cdot \Sigma(\bar{x}_B - \bar{\bar{x}})^2$ | $\frac{SSB}{V_B}$      | $\frac{MSB}{MSE}$ |
| Faktor Eror | $(N_A -1)(N_B -1)$    | $\Sigma_A \Sigma_B (x_{AB}-\bar{\bar{x}})$     | $\frac{SSE}{V_E}$      |                   |
| Total       | $b(k-1)$              | $\Sigma SS$                                    |                        |                   |
# Sign Test
Uji Sign adalah uji rata-rata ketika distribusi soal tidak diketahui (bukan distribusi normal).

Uji ini melihat selisih setiap data dari suatu target, kemudian menggunakan nilai kumulatif distribusi binomial untuk melihat jika suatu sampel mencapai target tersebut.

## Daerah Kritis
| $H$                                                            | Tolak $H_0$ jika:                                                |
| -------------------------------------------------------------- | ---------------------------------------------------------------- |
| $$\begin{align}H_0: \mu = \mu_0\\H_1:\mu\neq\mu_0\end{align}$$ | $$\begin{align}x<B_{0.5\alpha}\\ x> B_{1-0.5\alpha}\end{align}$$ |
| $$\begin{align}H_0:\mu=\mu_0\\H_1: \mu<\mu_0 \end{align}$$     | $x<B_{\alpha}$                                                   |
| $$\begin{align}H_0: \mu=\mu_0\\H_1: \mu>\mu_0\end{align}$$     | $x>B_{a-\alpha}$                                                 |
Dimana:
$x =$ jumlah nilai yang lebih besar dari / mencapai nilai yang diinginkan
$B =$ nilai $n$ pada tabel kumulatif distribusi binomial yang maksimal sebelum melebihi $\alpha$

## Prosedur
- Buatlah tabel semua sampel
- Bandingkan sampel, dengan sebuah target yang diinginkan
- Jika sampel tidak mencapai target, *tag* dengan tanda `-`, jika mencapai, *tag* dengan tanda `+`.
- Setelah semua sampel dicek, carilah nilai $n$ kumulatif binomial pada peluang $0.5$ yang paling tinggi, tapi tidak melebihi nilai $\alpha$
- Nilai $n$ tersebut adalah batas daerah kritis, lihat tabel penolakan $H_0$
# Wilcoxon Test
Merupakan tes yang dilakukan untuk mengecek sampel yang berasal dari populasi yang sama

## Sampel kecil $(n\le 15)$
### Daerah Kritis
Gunakan tabel peringkat Wilcoxon untuk mencari titik kritis

| Jika $H_1$:      | Carilah:        | Tolak $H_0$ jika: |
| ---------------- | --------------- | ----------------- |
| $\mu < \mu_0$    | $W^+$           | $W^+ \le T$       |
| $\mu > \mu_0$    | $W^-$           | $W^- \le T$       |
| $\mu \neq \mu_0$ | $\min(W^+,W^-)$ | $W \le T$         |

### Prosedur
- Buatlah tabel semua sampel
- Bandingkan sampel, dengan sebuah target yang diinginkan
- Jika sampel tidak mencapai target, *tag* dengan tanda `-`, jika mencapai, *tag* dengan tanda `+`.;
- Jumlahkan semua yang bertanda `-` dan `+`, masing-masing namanya $W^-$ dan $W^+$.
- Gunakan tabel daerah kritis untuk mencari kesimpulan

## Sampel Besar
###

# Kruskal-Wallis Test
Uji Kruskal-Wallis adalah uji rata-rata 3 populasi atau lebih, **ketika ukuran populasi tidak sama**
## Daerah Kritis
$H_0$ akan selalu ditolak ketika $K > \chi_{\alpha;m-1}^2$.
## Prosedur
Untuk melakukan uji Kruskal-Wallis, diperlukan beberapa langkah:
- Buatlah tabel keseluruhan populasi, beserta sampel mereka
- Buatlah ranking setiap nilai populasi, mulai dari yang terkecil - besar
	- Jika ada sampel yang sama, rata-ratakan mereka **setelah** proses ranking selesai
- Jumlahkan ranking masing-masing sampel, kemudian gunakan rumus

$K=\frac{12}{N(N+1)}[\frac{R_{A}^2}{n_A} + \frac{R_{B}^2}{n_B}+...]-3(N+1)$
Dimana:
$N =$ Jumlah semua sampel
$n =$ ukuran sampel sebuah populasi
$R =$ Jumlah ranking suatu populasi