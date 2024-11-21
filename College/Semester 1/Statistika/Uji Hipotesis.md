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

# Uji Rasio Varians
$$\begin{align}
f = \frac{S_A^2}{S_B^2}
\end{align}$$

| Daerah Kritis                                                     |
| ----------------------------------------------------------------- |
| $f<f_{1-0.5\alpha;vA;vB}$ dan $f>f_{0.5\alpha;vA;vB}$; Two-tailed |
| $f<f_{1-0.5\alpha;vA;vB}$; $\sigma_A^2 <\sigma_B^2$               |
| $f>f_{0.5\alpha;vA;vB}$;$\sigma_A^2 > \sigma_B^2$                 |
# $\chi^2$

(header) Tabel adalah

| $x$ | $O_i$ | $E_i$ | $\frac{(O_i - E_i)^2}{E_i}$ |
| --- | ----- | ----- | --------------------------- |
|     |       |       |                             |
