# Teori Penaksiran
1. Berat rata-rata 200 mesin cuci yang diproduksi oleh PT. Cemerlang adalah 74.5 kg, berasal dari populasi yang memiliki standar deviasi populasi 8.0 kg. Anda diminta untuk mencari estimasi interval konfidensi bagi rata-rata berat mesin cuci tersebut. Gunakan tingkat ketelitian 95 %
$$\begin{align}
\alpha = 0.05\rightarrow 0.5\alpha = 0.025\\
n = 200\\
\sigma = 8\\
\bar{x} = 74.5\\
\\
\bar{x}\pm Z_{0.5\alpha}\frac{\sigma}{\sqrt{n}}\\
= 74.5 \pm 1.96 \frac{8}{\sqrt{200}}\\
= 73.39125657 < \mu < 75.60874343
\end{align}$$

2. Kecepatan rata-rata 12 mesin fotocopy untuk fotocopy dokumen adalah 100 lembar/menit dengan standar deviasi 10 lembar/menit. Anda diminta untuk membuat estimasi interval konfidensi rata-rata kecepatan fotocopy tersebut, bila standar deviasi populasi tidak diketahui. Tingkat ketelitian atau keyakinan yang digunakan 95 %
$$\begin{align}
\alpha = 0.05 \rightarrow 0.5\alpha = 0.025\\
n = 12\\
\bar{x} = 100\\
s = 10\\
\\
\bar{x}\pm t_{0.025;12-1}\frac{s}{\sqrt{n}}\\
=100 \pm 2.201 \frac{10}{\sqrt{12}}\\
= 93.64626029 < \mu < 106.3537397
\end{align}$$

3. Secara random dipilih 70 gelas air minum merek Fresia dari populasi yang memiliki standar deviasi 25 mililiter, dan 75 gelas merek Segar dari populasi yang memiliki standar deviasi 24 mililiter. Setelah dilakukan pengukuran ternyata isi rata-rata air mineral Fresia adalah 510 mililiter dengan standar deviasi 24 mililiter, sedangkan rata-rata merek Segar adalah 518 mililiter dengan standar deviasi 26 mililiter. Hitung estimasi interval konfidensi untuk selisih rata-rata air mineral merek Fresia dan Segar. Gunakan tingkat ketelitian atau keyakinan 95 %
$$\begin{align}
\alpha = 0.05 \rightarrow 0.5\alpha = 0.025\\
n_A = 70\\
\sigma_A = 25\\
\bar{x}_A = 510\\
s_A = 24\\
\\
n_B = 75\\
\sigma_B = 24\\
\bar{x}_B = 518\\
s_B = 26\\
\\
(\bar{x}_a \pm \bar{x}_B)-Z_{0.5\alpha}\sqrt{\frac{\sigma_A^2}{n_A}+\frac{\sigma_B^2}{n_B}}\\
= (510-518)\pm 1.96 \sqrt{\frac{25^2}{70}+\frac{24^2}{75}}\\
=-8 \pm 7.987708558\\
= -15.98770856 < \mu_A - \mu_B < -0.012291442
\end{align}$$

4. cara random dipilih 70 gelas air minum merek Fresia dan 75 gelas merek Segar. Setelah dilakukan pengukuran ternyata isi rata-rata air mineral Fresia adalah 510 mililiter dengan standar deviasi 25 mililiter, sedangkan rata-rata merek Segar adalah 518 mililiter dengan standar deviasi 24 mililiter. Bila diasumsikan bahwa standar deviasi populasi kedua jenis air minum sama, Anda diminta menghitung estimasi interval konfidensi untuk selisih rata-rata air mineral merek Fresia dan Segar. Gunakan tingkat ketelitian atau keyakinan 95 %
$$\begin{align}
n_A = 70\\
\bar{x}_A = 510\\
s = 25\\
\\
n_B = 75\\
\bar{x}_B = 518\\
s = 24\\
\\
\alpha = 0.05\\
\sigma_A = \sigma_B\\
\\
v = n_A + n_B - 2 = 70 + 75 - 2 = 143\\
S_P^2 = \frac{(n_A -1)S_A^2 + (n_B - 1)S_B^2}{n_A+n_B-2} = \frac{69\cdot 25^2 + 74\cdot 24^2}{143} = 599.6433566\\
S_P = \sqrt{599.6433566}=24.48761639\\
t_{0.5\alpha;v}\approx t_{0.025;\infty}=1.96\\
\\
(\bar{x}_A - \bar{x}_B)\pm t_{0.5\alpha;v}\cdot S_P\cdot\sqrt{\frac{1}{n_A}+\frac{1}{n_B}}\\
(510-518)\pm 1.96\cdot 24.48761639\cdot\sqrt{\frac{1}{70}+\frac{1}{75}}\\
= -8\pm 7.8764\\
= -15.9764 < \mu_A - \mu_B < -0.0236\\
\end{align}$$