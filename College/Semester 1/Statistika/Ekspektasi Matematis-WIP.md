# Nilai ekspektasi
Misal $x$ adalah variabel random, dan $f(x)$ adalah sebuah fungsi distribusi probabilitias, nilai ekspektasi / $E(x)$ adalah

- $E(x) = \Sigma_x xf(x)$, jika $x$ diskrit
- $E(x) = \int_{-\infty}^{\infty} xf(x)dx$, jika $x$ kontinu

## Contoh
1. Misal sebuah komponen elektronik memiliki jangka waktu kehidupan yang direpresentasikan oleh fungsi berikut:
   
   $$\begin{align}
   f(x) = 
   \begin{cases}
   \frac{20000}{x^3},\text{ ketika x>100}\\
   0,\text{ lainnya}
   \end{cases}
   \end{align}$$
   Carilah ekspektasi jangka waktu kehidupan komponen tersebut
   
   $$\begin{align}
   
   \end{align}$$

# Varians
Dengan pemisalan yang sama dengan [[#Nilai ekspektasi]], varians / $\sigma^2$ adalah

- $\sigma^2 = E[(X-\mu)^2] = \Sigma_x (x-\mu)^2f(x)$, jika $x$ diskrit
- $\sigma^2 = E[(X-\mu)^2] = \int_{-\infty}^{\infty} (x-\mu)^2 f(x)dx$, jika $x$ kontinu

## Contoh