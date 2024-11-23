Dalam statistika, kita mengambil sampel untuk merepresentasikan sebuah populasi. Namun, biasanya ada data yang tidak kita ketahui. Upaya untuk menghitung / mendekati nilai tersebut dinamai **estimasi / pendugaan**.

# Estimasi Titik
Estimasi titik adalah di mana penaksiran menghasilkan 1 hasil diskrit. Contohnya menghitung rata-rata populasi dari sampel.

## Contoh Estimasi Titik
1. Diambil 20 sampel dari suatu pabrik dan dihasilkan data berikut:
   170 165 169 157 172
   168 157 166 160 164
   176 156 161 160 170
   163 159 162 168 157
   
   Hitunglah rata-rata produksi!
   
   $$\begin{align}
   \bar{x} = \frac{\Sigma_{n=1}^{20}(X_n)}{n} = \frac{3280}{20} = 164
   \end{align}$$

# Estimasi Interval
Kenyataannya, kita lebih sering mengestimasikan suatu *range* dengan konfidensi (keyakinan) tertentu. Konfidensi ini direpresentasikan oleh $\alpha$ yang menandakan kemungkinan "gagal".

![[Ilustrasi konfidensi Distribusi Normal.svg]]

Jika $\sigma$ tidak diketahui, namun $n > 30$, disarankan memisalkan $s = \sigma$

## Estimasi Rataan
Dari sebuah sampel, kita dapat mengestimasikan rata-rata sebuah populasi:

### Standar deviasi populasi ($\sigma$) diketahui
$$\begin{align}
\bar{x} - Z_{0.5\alpha}\frac{\sigma}{\sqrt{n}} \lt \mu \lt  \bar{x} + Z_{0.5\alpha}\frac{\sigma}{\sqrt{n}}
\end{align}$$
### Standar deviasi populasi tidak diketahui
$$\begin{align}
\bar{x} - t_{0.5\alpha;v}\frac{s}{\sqrt{n}} \lt \mu \lt \bar{x} + t_{0.5\alpha;v}\frac{s}{\sqrt{n}}\\
\\
v = n-1
\end{align}$$
## Estimasi Selisih 2 Rataan
Misal terdapat 2 sampel yang merepresentasikan 2 populasi yang berbeda, kita dapat menghitung selisih rata-rata kedua populasi tersebut:

### Standar deviasi populasi diketahui
$$\begin{align}
(\bar{x}_A - \bar{x}_B) - Z_{0.5\alpha}\sqrt{\frac{\sigma_A^2}{n_A}+\frac{\sigma_B^2}{n_B}} \lt \mu_A - \mu_B \lt (\bar{x}_A - \bar{x}_B) + Z_{0.5\alpha}\sqrt{\frac{\sigma_A^2}{n_A}+\frac{\sigma_B^2}{n_B}}
\end{align}$$

### Standar deviasi populasi tidak diketahui, namun dianggap sama
$$\begin{align}
(\bar{x}_A - \bar{x}_B)-t_{0.5\alpha;v} \cdot S_P \cdot \sqrt{\frac{1}{n_A}+\frac{1}{n_B}} \lt \mu_A - \mu_B \lt (\bar{x}_A - \bar{x}_B)+t_{0.5\alpha;v} \cdot S_P \cdot \sqrt{\frac{1}{n_A}+\frac{1}{n_B}}\\
\\
S_P^2 = \frac{(n_A -1)S_A^2 + (n_B - 1)S_B^2}{n_A+n_B-2}\\
\\
v = n_A + n_B -2
\end{align}$$

### Standar deviasi populasi tidak diketahui, dan dianggap berbeda
$$\begin{align}
(\bar{x}_A - \bar{x}_B)-t_{0.5\alpha}\sqrt{\frac{s_A^2}{n_A}+\frac{s_B^2}{n_B}} \lt \mu_A - \mu_B \lt (\bar{x}_A - \bar{x}_B)+t_{0.5\alpha}\sqrt{\frac{s_A^2}{n_A}+\frac{s_B^2}{n_B}}\\
\\
v = \frac{(\frac{s_A^2}{n_A}+\frac{s_B^2}{n_B})^2}{(\frac{(\frac{s_A^2}{n_A})^2}{n_A-1})+(\frac{(\frac{s_B^2}{n_B})^2}{n_B-1})}
\end{align}$$
### Rata-rata observasi berpasangan
$$\begin{align}
\bar{d} - t_{0.5\alpha}\frac{s_d}{\sqrt{n}}\lt \mu_1 - \mu_2 \lt \bar{d} + t_{0.5\alpha}\frac{s_d}{\sqrt{n}}
\end{align}$$

## Estimasi proporsi
**hanya dipakai jika** $np \ge 5$ **, n besar, dan p tidak ekstrim**
Misal $\hat{p}$ adalah kemungkinan sukses sebuah sampel, maka bisa dicari proporsi $p$ populasi:

$$\begin{align}
\hat{p} - Z_{0.5\alpha}\sqrt{\frac{\hat{p}\hat{q}}{n}}\lt p < \hat{p}+Z_{0.5\alpha}\sqrt{\frac{\hat{p}\hat{q}}{n}}
\end{align}$$
## Estimasi selisih proporsi
**hanya dipakai jika** $np \ge 5$ **, n besar, dan p tidak ekstrim**
Misal $\hat{p}_A$ dan $\hat{p}_B$ masing-masing merepresentasikan kemungkinan sukses sampel A dan B, maka bisa dicari selisih  $p_A$ dengan $p_B$:
$$\begin{align}
(\hat{p}_A - \hat{p}_B) - Z_{0.5\alpha}\sqrt{\frac{\hat{p}_A \hat{q}_A}{n_A}+\frac{\hat{p}_B \hat{q}_B}{n_B}} \lt p_A - p_B \lt (\hat{p}_A - \hat{p}_B) + Z_{0.5\alpha}\sqrt{\frac{\hat{p}_A \hat{q}_A}{n_A}+\frac{\hat{p}_B \hat{q}_B}{n_B}}
\end{align}$$

## Eror
Sampel tentunya tidak bisa merepresentasikan keseluruhan populasi secara tepat 100%. Eror bisa didefinisikan sebagai selisih dari $\mu$ dengan $\bar{x}$. Jika tidak ada selisih, alias $\mu = \bar{x}$, maka tidak ada eror. Namun seringkali kedua nilai tersebut berbeda

$$\begin{align}
\epsilon \le Z_{0.5\alpha}\frac{\sigma}{\sqrt{n}}
\end{align}$$

## Kecukupan data
Misal kita memiliki $\bar{x}$ dan ingin eror untuk tidak melebihi $e$, maka $n$ yang diperlukan sebaiknya lebih dari sama dengan:
$$\begin{align}
n = (\frac{Z_{0.5\alpha}\sigma}{n})^2
\end{align}$$

Misal kita memiliki $\hat{p}$:
$$\begin{align}
n = \frac{Z_{0.5\alpha}^2 \cdot \hat{p}\hat{q}}{e^2}
\end{align}$$

## Interval Prediksi
Rumus interval di atas menghitung suatu parameter, namun interval prediksi menghitung interval observasi selanjutnya, alias interval nilai jika kita mengambil sampel lagi

### Standar deviasi populasi diketahui
$$\begin{align}
\bar{x} - Z_{0.5\alpha} \cdot \sigma \cdot\sqrt{1+\frac{1}{n}} \lt x_0 \lt \bar{x}+Z_{0.5\alpha}\cdot \sigma \cdot \sqrt{1+\frac{1}{n}}
\end{align}$$
### Standar deviasi populasi tidak diketahui
$$\begin{align}
\bar{x}-t_{0.5\alpha;v}\cdot s\cdot \sqrt{1+\frac{1}{n}} \lt x_0 \lt \bar{x}+t_{0.5\alpha;v}\cdot s \cdot \sqrt{1+\frac{1}{n}}\\
\\
v = n-1
\end{align}$$
## Batas Toleransi
Batas toleransi jika distribusi normal, mean populasi tidak diketahui, dan standar deviasi populasi tidak diketahui adalah 
$$\begin{align}
TL = \bar{x}\pm ks\\
\\
k = 100-\gamma \% \\
\text{Untuk k, cari persen gamma \& alfa, n, kemudian cari di tabel "A7"}
\end{align}$$

## Estimasi Varians
### Varians tunggal
Misal terdapat $s^2$, maka bisa diestimasikan $\sigma^2$:
$$\begin{align}
\frac{(n-1)s^2}{\chi_{0.5\alpha^2}}\lt \sigma^2 \lt \frac{(n-1)s^2}{\chi_{1-0.5\alpha}^2}
\end{align}$$

### Rasio Varians
Misal $s_A^2$ dan $s_B^2$ adalah varians sampel populasi A dan B, maka dapat dihitung rasio varians populasi:
$$\begin{align}
\frac{s_A^2}{s_B^2}\cdot \frac{1}{f_{0.5\alpha;v_1;v_2}} \lt \frac{\sigma_A^2}{\sigma_B^2} \lt \frac{s_A^2}{s_B^2}f_{0.5\alpha;v_1;v_2}
\end{align}$$

## Contoh Soal Estimasi Interval
1. **Konfidensi rata-rata dengan standar deviasi**
   Suatu biro pariwisata mengadakan sebuah penelitian di mana 25 sampel turis asing diambil dari populasi yang banyaknya dianggap $\infty$. Dari hasil wawancara, diketahui rata-rata pengeluaran mereka $800. Jika dimisalkan standar deviasi populasi turis $120, buatlah interval konfidensi 95% rata-rata pengeluaran para wisatawan!
   
   $$\begin{align}
   n = 25\\
   \bar{x} = 800\\
   \sigma = 120\\
   \alpha = 5\% = 0.05 \rightarrow \frac{\alpha}{2} = 0.025 \rightarrow 1-0.025 = 0.975\\
   \\
   Z_{0.975} = 1.96\\
   \\
   \bar{x} \pm Z_{0.5\alpha} \frac{\sigma}{\sqrt{n}}\\
   800 \pm 1.96 \cdot \frac{120}{\sqrt{25}}\\
   = 800 \pm 47.04\\
   = 752.96 < \mu < 847.04
   \end{align}$$
   Dari cerita & data di atas, kita dapat 95% yakin rata-rata wisatawan mengeluarkan uang sebanyak $752.96 - $847.04

2. **Konfidensi rata-rata tanpa standar deviasi**
   Misalkan cerita nomor 1, namun standar deviasi populasi tidak diketahui dan standar deviasi sampel $120!
   
   $$\begin{align}
   n = 25\\
   \bar{x} = 800\\
   \sigma = 120\\
   \alpha = 5\% = 0.05\rightarrow \frac{\alpha}{2} = 0.025\\
   v = n-1 = 24\\
   \\
   t_{0.025;24} = 2.391\\
   \\
   \bar{x}\pm t_{0.5\alpha}\cdot \frac{s}{\sqrt{n}}\\
   =800\pm2.391\cdot \frac{120}{\sqrt{25}}\\
   =800\pm57.384\\
   = 742.616 \lt \mu \lt 857.384
   \end{align}$$
   