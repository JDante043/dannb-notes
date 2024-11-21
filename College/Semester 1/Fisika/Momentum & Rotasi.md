# Momentum
$$\begin{align}
P = mv
\end{align}$$
## Impuls
$$\begin{align}
I = F\Delta t = \Delta p = m(v-v_0)
\end{align}$$
### Contoh
Sebuah benda 2KG bergerak secepat 6m/s. Berapa F yang diperlukan untuk menghentikan benda dalam waktu $7\cdot 10^{-4}$ sekon?
$$\begin{align}
I = F\Delta t = m(v-v_0)\\
F(7\cdot10^{-4}) = 2(6-0)\\
F = 1.71\cdot10^4
\end{align}$$
## Hukum Kekekalan Momentum
Ketika 2 benda bertabrakan, misalkan gaya eksternal tidak dihitung, impuls kedua benda dapat dirumuskan seperti:
$$\begin{align}
\Sigma P_{\text{aksi}} = -\Sigma P_{\text{reaksi}}\\
m_1(v'_1 - v_1) = -m_2(v'_2-v_2)
\end{align}$$
Rumus tersebut mengikuti hukum newton kedua, "setiap reaksi dibalas dengan reaksi yang sama besar yang berlawanan arah". Hukum ini juga dapat digunakan untuk menghitung EK:
$$\begin{align}
EK_\text{awal}=EK_\text{akhir}\\
\Sigma \frac{1}{2}mv^2=\Sigma\frac{1}{2}mv^2\\
m_1(v_1^2-v_1^2\prime)=m_2(v_2^2\prime-v_2^2)
\end{align}$$
## Contoh
Misal sebuah kereta 10 ton secepat 24m/s menabrak kereta model sama yang sedang diam. Setelah mereka bertabrakan, kedua kereta menyatu. Hitunglah kecepatan kedua kereta tersebut setelah tabrakan
$$\begin{align}
P_\text{sebelum} = P_\text{sesudah}\\
10000\cdot24+ 10000\cdot 0 = (10000+10000)v'\\
v' = 12m/s
\end{align}$$

# Rotasi
## Persamaan Gerak Rotasi

| Translasi                     | Rotasi                            |
| ----------------------------- | --------------------------------- |
| $v_t = v_0 + at$              | $w_t = w_0 + at$                  |
| $x = v_0t + \frac{1}{2}at^2$  | $\theta = w_0t + \frac{1}{2}at^2$ |
| $v_t^2 = v_0^2 + 2ax$         | $w_t^2 = w_0^2 + 2a\theta$        |
| $\bar{v} = \frac{v_t+v_0}{2}$ | $\bar{w}=\frac{w_t+w_0}{2}$       |
| $x=\bar{v}t$                  | $\theta=\bar{w}t$                 |
## Momen Gaya
$\tau = r\perp F = rF \perp = rF\sin{(\theta)}$
### Contoh
Misal terdapat tangan manusia, di mana otot melekan 5cm dari tulang, dan otot menarik sekuat 700N. Hitunglah torsi jika:
1. Tangan berbentuk siku-siku ($\theta = 90\degree$)
$$\begin{align}
\tau = 0.05\cdot700\cdot\sin{(90\degree)} = 35
\end{align}$$
2. Tangan membuat sudut $30\degree$ dari sumbu x / $60\degree$ dari sumbu y
$$\begin{align}
\tau = 0.05\cdot 700\cdot \sin{(60\degree)} = \frac{35\sqrt{3}}{2}
\end{align}$$

# Momen Inersia
$$\begin{align}
I = mr^2\\
F = mr\alpha\\
\frac{\tau}{r}=mr\alpha\\
\tau = mr^2\alpha=I\alpha
\end{align}$$

# Gerak Kinetik Rotasi
$$\begin{align}
EK_\text{rotasi} = \frac{1}{2}m(rw)^2=\frac{1}{2}Iw^2\\
EK_\text{total} = \frac{1}{2}mv^2+\frac{1}{2}Iw^2\\
W = \tau \theta\\
P = \tau w
\end{align}$$

## Contoh
Sebuah bola menggelinding dari suatu bidang miring. Misal massa m, radius r, ketinggian h, dan bola menggelinding tanpa slip, laju / v?
$$\begin{align}
E_\text{awal}=E_\text{akhir}\\
EK + EP = EK + EP\\
\frac{1}{2}mv^2+\frac{1}{2}Iw^2 + mgh = \frac{1}{2}mv^2+\frac{1}{2}Iw^2 + mgh\\
0 + 0 + mgh = \frac{1}{2}mv^2+\frac{1}{2}Iw^2 + 0\\
mgh = \frac{1}{2}mv^2+\frac{1}{2}Iw^2\\
\\
mgh = \frac{1}{2}mv^2+\frac{1}{2}m(\frac{2}{5}R)^2(\frac{v}{r})^2\\
\end{align}$$

Penjelasan:
- Ikuti hukum kekekalan momentum, bola di atas memiliki total energi mekanik sama dengan ketika dia di bawah.
- Karena EM = EK total + EP total, masukkan rumus
- karena ketika di atas bola tidak bergerak sama sekali, maka tidak ada kecepatan, maupun rotasi
- ketika bola di bawah, EPnya 0
- setelah dapat hasil akhir, rumus kecepatan bola menggelinding adalah $\frac{2}{5}R$ dan karena tidak slip, maka rumus kecepatan sudut adalah $\frac{v}{r}$.

# Momentum sudut
$$\begin{align}
L = Iw\\
F = \frac{dp}{dt}\\
\tau = \frac{dL}{dt}
\end{align}$$
