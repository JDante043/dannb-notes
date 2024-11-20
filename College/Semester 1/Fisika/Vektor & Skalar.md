Pergerakan atau pergeseran suatu benda dapat dinyatakan / digambarkan dengan **Besaran Vektor**.
Pergerakan yang tidak memiliki arah disebut dengan **Besaran Skalar**.

# Vektor
Ada 2 tipe vektor, yaitu
- **Vektor Posisi**, di mana Vektor digunakan untuk menggambarkan perpindahan dari satu titik ke titik lain. Contoh: Vektor P adalah perpindahan dari titik A(0,0) ke titik B(3,4)
- **Vektor Satuan**, di mana Vektor tidak memiliki titik tertentu, dan hanya menggambarkan perpindahan. Contoh: Vektor P = $5i + 3j + k$

## Komponen Vektor
![[Vektor 1.excalidraw.svg]]
Lihatlah Vektor A di atas. Vektor tersebut memiliki 2 komponen, yaitu Ax dan Ay.

Komponen sebuah Vektor adalah perpindahan di sumbu X dan sumbu Y. Perpindahan ini dapat diproyeksikan dengan menarik garis dari kepala / akhir Vektor ke sumbu masing-masing (Diilustrasikan dengan garis putus-putus)

Besaran / Resultan vektor dapat ditemukan jika komponen-komponen vektor diketahui:
$A = \sqrt{A_x^2 + A_y^2}$

Sudut vektor dapat ditemukan dengan rumus:
$\tan(\frac{A_y}{A_x})$

Misal $\alpha$ adalah sudut, maka rumus-rumus Trigonometri bisa digunakan:
- $\sin(\frac{A_y}{A})$
- $\cos(\frac{A_x}{A})$ 
- $\tan(\frac{A_y}{A_x})$ 

Ada juga rumus untuk menentukan komponen atau proyeksi dengan sudut dan besaran vektor:
- $A_x = A * cos(\alpha)$
- $A_y = A * \sin(\alpha)$ 

# Operasi Vektor
Operasi pada vektor hanya berlaku untuk sumbu yang sama:
$A(i+j+k) + B(i+j+k) = (A+B)I + (A+B)J + (A+B)K$

## Penjumlahan Vektor
Misal ada Vektor AB dan BC, maka Vektor AC dapat ditemukan dengan menambahkan Vektor AB + Vektor BC.

## Perkalian Vektor
### Dot Product
Dot product adalah hasil perkalian vektor di mana hanya arah yang sama dikalikan, dan hasil akhir dijumlahkan.

$$
\begin{align}
A = 80i + 10j\\
B = 20i + 30j\\
A*B?\\
\\
(80i + 10j)(20i + 30j)\\
(80i * 20i)+(80i * 30j)+(10j * 20i)+(10j * 30j)\\
(1600i) + 0 + 0 + 300j\\
1600 + 300\\
1900
\end{align}
$$
### Cross Product
Cross Product adalah hasil perkalian vektor di mana hasil akhir merupakan vektor baru. Cross Product memerlukan rumus baru, karena tidak dikalikan biasa saja, yaitu:
$$\begin{align}
A\cdot B = C\rightarrow (a_i+a_j+a_k) \cdot (b_i+b_j+b_k) = (a_j b_k-a_kb_j)i + (a_k b_i-a_ib_k)j + (a_ib_j-a_jb_i)k
\end{align}$$

# Vektor Resultan
Untuk menentukan resultan sebuah vektor, kuadratkan, jumlahkan, kemudian carilah hasil dari akar resultan tersebut. Contoh:

1. Misal sebuah partikel bergerak 22km ke arah utara dari titik 0, kemudian 47km ke arah tenggara, dengan sudut 60$\degree$ dari sumbu x.
   ![[Vektor 2.png]]
   $$\begin{align}
   P_{1x} = 0\\
   P_{1y} = 22\\
   P_{2x} = 47km \cdot \cos(60\degree) = 23.5km\\
   P_{2y} = -47km \cdot \sin(60\degree) = -40.7km\\
   \\
   P_x = 0 +  23.5 = 23.5\\
   P_y = 22 + (-40.7) = -18.7\\
   \\
   P = \sqrt{(22)^2 + (-40.7)^2} = 30km\\
   \\
   \tan(\alpha) = \frac{P_y}{P_x} = -0.7957 = -38.51\degree \text{ (dari titik awal ke akhir)}
   \end{align}$$
