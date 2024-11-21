Limit adalah hasil suatu fungsi ketika x mendekati suatu konstanta (c)

$$
\begin{align}
\lim_{x\rightarrow c}(f(x))
\end{align}
$$
# Limit Aljabar
##  Menemukan Limit
Untuk menemukan limit suatu fungsi, maka ada beberapa langkah yang harus diikuti:

- Substitusikan nilai $x$ di fungsi dengan nilai $c$
- Jika hasil merupakan varian dari $\frac{n}{0}$, maka nilai limit fungsi tersebut **tidak ada**
- Jika hasil **terdefinisi**, maka nilai tersebut merupakan limit fungsi tersebut
- Jika hasil **tidak terdefinisi**, maka fungsi baru bisa difaktorkan / diturunkan

## Contoh

1. Contoh jika $x$ dapat disubstitusikan langsung$$\lim_{x\rightarrow 3}(4x-5)$$
$$
\begin{align}
=4(3)-5\\
=12-5\\
=7
\end{align}
$$
2. Contoh penggunaan metode L'Hôpital $$\lim_{x\rightarrow3}(\frac{x^2-x-6}{x-3})$$
$$
\begin{align}
=[\frac{2x-1}{1}]_{x\rightarrow3}\\
=2(3)-1\\
=6-1\\
=5
\end{align}
$$
3. Contoh dari fungsi yang tidak memiliki limit $$\lim_{x\rightarrow2}(\frac{x^2+3x+2}{x^2-4})$$
$$
\begin{align}
=\frac{(2)^2+3(2)+2}{2^2-4}\\
=\frac{4+6+2}{4-4}\\
=\frac{12}{0}
\end{align}
$$
- Karena setelah $x$ disubstitusikan ternyata hasil merupakan $\frac{n}{0}$, maka **hasil limit tidak ada**

## Sifat-sifat
- $\lim\limits_{x\rightarrow a}(f(x)) = L$
- $\lim\limits_{x\rightarrow a}(f(x) \pm g(x)) = \lim\limits_{x\rightarrow a}(f(x)) \pm \lim\limits_{x\rightarrow a}(g(x))$
- $\lim\limits_{x\rightarrow a}(f(x) * g(x)) = \lim\limits_{x\rightarrow a}(f(x)) * \lim\limits_{x\rightarrow a}(g(x))$
- $\lim\limits_{x\rightarrow a}(\frac{f(x)}{g(x)}) = \frac{\lim\limits_{x\rightarrow a}(f(x))}{\lim\limits_{x\rightarrow a}(g(x))}$


## Limit Kiri dan Limit Kanan
Jika fungsi merupakan gabungan dari beberapa fungsi lain, misal:
$$
f(x)=\begin{cases}
x^2+1\\
2x
\end{cases}
$$
Fungsi tersebut dinamakan *piecewise function* atau fungsi piecewise. Cara menemukan limit dari fungsi $f(x)$ adalah dengan menggunakan limit kiri dan limit kanan.

Limit kiri ($\lim\limits_{x\rightarrow c^+}$) dan limit kanan ($\lim\limits_{x\rightarrow c^-}$) adalah nama lain dari limit untuk fungsi pertama dan kedua $f(x)$.

Contoh di atas:
$$
\begin{align}
\lim_{x\rightarrow c^+}(x^2 + 1)\\
\lim_{x\rightarrow c^-}(2x)\\
\end{align}
$$
Tanda + dan - merupakan penamaan saja dan tidak memengaruhi hasil limit.

Jika hasil limit kiri dan kanan sama, maka limit dari $f(x)$ merupakan hasil tersebut, jika tidak, maka fungsi tersebut tidak memiliki limit

# Limit Trigonometri
Seperti limit aljabar, limit trigonometri dapat diselesaikan dengan cara substitusi, faktor, dan / atau metode L'Hôpital. Namun, metode L'Hôpital bise menyebabkan perhitungan yang sangat panjang, maka tidak disarankan.

## Rumus Dasar
- $\lim\limits_{x\rightarrow 0}(\frac{\sin(ax)}{bx})$
- $\lim\limits_{x\rightarrow 0}(\frac{ax}{\sin(bx)})$
- $\lim\limits_{x\rightarrow 0}(\frac{\sin(ax)}{\sin(bx)})$
- $\lim\limits_{x\rightarrow 0}(\frac{\tan(ax)}{bx})$
- $\lim\limits_{x\rightarrow 0}(\frac{ax}{\tan(bx)})$
- $\lim\limits_{x\rightarrow 0}(\frac{\tan(ax)}{\tan(bx)})$
- $\lim\limits_{x\rightarrow 0}(\frac{\sin(ax)}{\tan(bx)})$
- $\lim\limits_{x\rightarrow 0}(\frac{\tan(ax)}{\sin(bx)})$