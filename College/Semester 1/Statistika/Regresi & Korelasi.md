# Regresi Linear Sederhana
## Persamaan
$$\begin{align}
b = \frac{\Sigma (x-\bar{x})(y-\bar{y})}{\Sigma(x-\bar{x})^2}\\
a = \bar{y}-b\bar{x}\\
\\
\hat{y} = a+bx
\end{align}$$

## Korelasi & Eror
$$\begin{align}
JKT = \Sigma (y-\bar{y})^2 = JKR + JKG\\
JKR = \Sigma (\hat{y}-\bar{y})^2\\
JKG = \Sigma (y-\hat{y})^2\\
\\
S_{\epsilon} = \sqrt{\frac{JKG}{n-2}}\\
r^2 = 1-\frac{JKG}{JKT}=\frac{JKR}{JKT}
\end{align}$$
- Nilai determinasi $(r^2)$ menentukan seberapa "linear" suatu persamaan
- Nilai eror $(r)$ menentukan jangkauan / *range* nilai dari $(\hat{y})$, alias $\hat{y} \pm r$

## Tingkat Hubungan
| $r$        | Tingkat Hubungan |
| ---------- | ---------------- |
| $0-0.19$   | Sangat Rendah    |
| $0.2-0.39$ | Rendah           |
| $0.4-0.59$ | Sedang           |
| $0.6-0.79$ | Kuat             |
| $0.8-1.0$  | Sangat Kuat      |

## Tabel
Berikut adalah header tabel yang akan digunakan:

| $n$      | $x$ | $y$ | $(x-\bar{x})$ | $(y-\bar{y})$ | $(x-\bar{x})(y-\bar{y})$ | $(x-\bar{x})^2$ | $(y-\bar{y})$ |
| -------- | --- | --- | ------------- | ------------- | ------------------------ | --------------- | ------------- |
| ...      | ... | ... | ...           | ...           | ...                      | ...             | ...           |
| $\Sigma$ |     |     |               |               |                          |                 |               |

# Regresi Linear Ganda
Regresi Linear, namun terdapat 2 variabel yang memengaruhi hasil akhir

## Persamaan
$$\begin{align}
na + b_1\Sigma x_1 + b_2\Sigma x_1 = \Sigma y\\
a\Sigma x_1 + b_1 \Sigma x_1^2 + b_2 \Sigma x_1x_2 = \Sigma yx_1\\
a\Sigma x_2 + b_1 \Sigma x_1x_2 + b_2 \Sigma x_2^2 = \Sigma yx_2\\
\\
\hat{y} = a + b_1X_1 + b_2X_2
\end{align}$$
## Korelasi Berganda
$$\begin{align}
r_{yx_1} = \frac{\Sigma yx_1}{\sqrt{\Sigma x_1^2}\sqrt{\Sigma y^2}}\\
r_{yx_2} = \frac{\Sigma yx_2}{\sqrt{\Sigma x_2^2}\sqrt{\Sigma y^2}}\\
r_{x_1x_2} = \frac{\Sigma x_1x_2}{\sqrt{\Sigma x_1^2}\sqrt{\Sigma x_2^2}}\\
\\
r_{yx_1x_2}^2 = \frac{r_{yx_1}^2+r_{yx_2}^2 - 2r_{yx_1}r_{yx_2}}{1-r_{x_1x_2}}
\end{align}$$

## Korelasi Parsial
Berbeda dengan korelasi & korelasi berganda, korelasi parsial mencari besar efek suatu variabel ke variabel lain, jika variabel lain merupakan konstanta

$$\begin{align}
r_{yx_1.x_2} = \frac{r_{yx_1}-r_{yx_2}r_{x_1x_2}}{\sqrt{1-r_{yx_2}^2}\sqrt{1-r_{x_1x_2}^2}}\\
r_{yx_2.x_1} = \frac{r_{yx_2}-r_{yx_1}r_{x_1x_2}}{\sqrt{1-r_{yx_1}^2}\sqrt{1-r_{x_1x_2}^2}}\\
r_{x_1x_2.y} = \frac{r_{x_1x_2}-r_{yx_1}r_{yx_2}}{\sqrt{1-r_{yx_1}^2}\sqrt{1-r_{yx_2}^2}}\\
\end{align}$$

## Tabel
Berikut adalah header tabel yang digunakan dalam kalkulasi ini:

| $y$      | $x_1$ | $x_2$ | $yx_1$ | $yx_2$ | $x_1x_2$ | $y^2$ | $x_1^2$ | $x_2^2$ |
| -------- | ----- | ----- | ------ | ------ | -------- | ----- | ------- | ------- |
| ...      | ...   | ...   | ...    | ...    | ...      | ...   | ...     | ...     |
| $\Sigma$ |       |       |        |        |          |       |         |         |
