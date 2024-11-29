# Trigonometri
## Integral Trigonometri
$$\begin{align}
\int\sin{(x)}dx = -\cos{(x)}+C\\
\int\cos{(x)}dx = \sin{(x)}+C\\
\int\tan{(x)}dx = -\ln{(|\cos{(x)}|)}+C=\ln{(|\sec{(x)}|)}+C\\
\int\csc{(x)}dx = -\ln{(|\csc{(x)}+\cot{(x)}|)}+C\\
\int\sec{(x)}dx = \ln{(|\sec{(x)}+\tan{(x)}|)}+C=\ln{(|\sec{(x)}+\tan{(x)}|)}+C\\
\int\cot{(x)}dx = \ln{(|\sin{(x)}|)}+C
\end{align}$$
## Trigonometri Berpangkat
$$\begin{align}
\int\sin{(x)}^ndx = -\frac{1}{n}\sin{(x)}^{n-1}\cos{(x)}+\frac{n-1}{n}\int\sin{(x)}^{n-2}dx\\
\int\cos{(x)}^ndx = \frac{1}{n}\cos{(x)}^{n-1}\sin{(x)}+\frac{n-1}{n}\int\cos{(x)}^{n-2}dx\\
\int\tan{(x)}^ndx = \frac{\tan{(x)}^{n-1}}{n-1}-\int\tan({x)}^{n-2}dx\\
\int\sec{(x)}^ndx = \frac{\sec{(x)}^{n-2}\tan{(x)}}{n-1}+\frac{n-2}{n-1}\int\sec{(x)}^{n-2}dx\\
\\

\end{align}$$
## Substitusi dengan Trigonometri
$$\begin{align}
\int\sqrt{a^2+x^2}dx\rightarrow x = a\tan{(\theta)}\\
\int\sqrt{a^2-x^2}dx\rightarrow x = a\sin{(\theta)}\\
\int\sqrt{x^2-a^2}dx\rightarrow x = a\cos{(\theta)}\\
\int\frac{1}{x^2+a^2}dx = \frac{1}{a}\arctan{(\frac{x}{a})}+C\\
\int\frac{1}{\sqrt{a^2-x^2}}dx=\arcsin{(\frac{x}{a})}
\end{align}$$
# Rumus Aljabar lain
$$\begin{align}
\int\frac{1}{\sqrt{a^2+x^2}}dx=\ln{(|x+\sqrt{x^2+a^2)}|)}\\
\int\frac{1}{\sqrt{x^2-a^2}}dx=\ln{(|x+\sqrt{x^2-a^2}|)}\\
\int\frac{1}{x^2-a^2}dx=\frac{1}{2a}\ln{(|\frac{x-a}{x+a}|)}\\
\end{align}$$

# Rumus Dasar
## Sum / Difference Rule
$$\begin{align}
\int f(x) \pm g(x)dx\\
= \int f(x)dx \pm \int g(x)dx
\end{align}$$
## Power Rule (n != -1)
$$\begin{align}
\int x^n dx\\
= \frac{x^{n+1}}{n+1}+C
\end{align}$$
## Product Rule (Integration by Parts)
$$\begin{align}
\int f(x)g(x)dx\\
= f(x)\int g(x)dx - \int f'(x) \cdot \int g(x)dx
\end{align}$$
## Multiplication by Constant
$$\begin{align}
\int cf(x)dx\\
= c\int f(x)dx
\end{align}$$
## Integration by Substitution
$$\begin{align}
\text{Note, hanya bisa dipakai ketika bentuk seperti: }\int f(g(x))g'(x)dx\\
\text{g(x) diubah menjadi u, dan g'(x)dx diubah menjadi du}\int f(g(x))g'(x)dx\\
= \int f(u)du
\end{align}$$