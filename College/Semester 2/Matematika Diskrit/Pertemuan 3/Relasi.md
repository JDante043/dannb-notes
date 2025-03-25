# Konsep
Misalkan kita ada set $A = \{1,2,3\}$ dan $B = \{4,5,6\}$, maka setiap kemungkinan pasangan / relasi antara kedua set tersebut adalah 
$$\begin{align}
(A\cdot B) = \{(1,4),(1,5),(1,6),\\
(2,4),(2,5),(2,6),\\
(3,4),(3,5),(3,6)\}
\end{align}$$

Kardinalitas / Jumlah elemen $(A\cdot B)$ sudah pasti $|A|\cdot |B|$.

Relasi antara set A dan B disebut relasi biner dan berbentuk $(a,b)$. Misalkan set relasi $R$, maka cara menulis $R$ adalah $R\subset (A\cdot B)$. Di set $R$, $A$ disebut daerah asal / *domain*, sementara $B$ disebut daerah hasil / *codomain*

Misalkan kita ambil relasi asal $(a,b)$;
- Jika relasi tersebut terdapat di dalam set R, maka $(a,b)$ dapat ditulis dengan cara $a\ R\ b$;
- Jika relasi tersebut tidak di dalam set R, maka $(a,b)$ dapat ditulis dengan cara $a\ \cancel{R}\ b$.

Untuk contoh berikutnya, kita misalkan $R = \{(1,4),(2,6),(3,4)\}$; 

# Graf relasi
## Tabel
Relasi biner R dapat dibuat seperti berikut:

| A   | B   |
| --- | --- |
| 1   | 4   |
| 2   | 6   |
| 3   | 4   |
## Graf Berarah
Untuk menggambar graf berarah, maka ambillah setiap elemen $(a,b)$ dan buatlah titik dan panah yang menunjukkan relasi mereka
![[Relasi Berarah.excalidraw.svg]]

# Relasi Invers
Kita lihat set relasi kita tadi: $R = \{(1,4),(2,6),(3,4)\}$.

Relasi invers (ditulis $R^{-1}$) merupakan kebalikan dari $(a,b)$, sehingga menjadi $(b,a)$.

$R^{-1} = \{(4,1),(6,2),(4,3)\}$.

# Mengombinasikan Set / Relasi
Setiap set dapat dikombinasikan. Misalkan:
$A = \{1,2,3\}$ dan $B = \{1,4,5,6\}$.

Maka $A$ dan $B$ dapat dikombinasikan menggunakan operator-operator berikut:
- $A\cap B = \{1\}$
- $A\cup B = \{1,2,3,4,5,6\}$
- $A-B = \{2,3\}$
- $B-A = \{4,5,6\}$
- $A\oplus B = \{2,3,4,5,6\}$

# Komposisi
Misalkan terdapat set:
$$\begin{align}
A = \{1,2,3\}\\
B = \{x,y,z\}\\
C = \{4,5,6\}\\
\\
R_1 = \{(1,x),(1,z),(2,x),(3,z)\}\\
R_2 = \{(x,4),(y,5),(z,6)\}
\end{align}$$
Maka gambaran $R_1$ dan $R_2$: ![[Relasi set.excalidraw.svg]]
Lihat bahwa kita bisa "menghubungkan" $R_1$ dengan $R_2$ sehingga domain $A$ terhubung dengan codomain $C$.

"Penghubungan" ini dapat dituliskan seperti $R_1 \circ R_2 = \{(1,4),(1,6),(2,4),(3,6)\}$.

# Sifat Relasi
## Reflektif
Sebuah relasi dinyatakan reflektif, jika semua $(a,a) \in R$.
Misalkan $A = \{1,2,3\}$, relasi $R_1 = \{(1,1),(1,2),(2,2),(3,3)\}$, dan $R_2 = \{(1,1),(2,2)\}$.

Relasi $R_1$ disebut reflektif sementara $R_2$ tidak reflektif karena $R_2$ tidak mengandung $(3,3)$.

## Symmetric & Antisymmetric
Sebuah relasi dinyatakan simetris jika setiap elemen $(a,b)$ memiliki $(b,a)$.
Sebuah relasi dinyatakan anti simetris jika terdapat elemen $(a,a)$ di mana $a = a$.

Misalkan $A = \{1,2,3\}$, relasi $R_1 = \{(1,1),(1,2),(2,2),(3,3)\}$, dan $R_2 = \{(1,2),(2,1)\}$.

$R_1$ dinyatakan anti-simetris karena: 
- $(1,1); 1=1$
- $(2,2); 2=2$
- $(3,3); 3=3$
 Namun tidak simetris karena mengandung $(1,2)$ namun tidak ada $(2,1)$.

$R_2$ dinyatakan simetris karena mengandung $(1,2)$ dan $(2,1)$; Namun tidak anti-simetris karena $(1,2); 1\neq2$.

## Transitive
Sebuah relasi dibilang transitif jika $(a,b)\in R$ dan $(b,c)\in R$, maka harus ada juga $(a,c)\in R$
Misalkan $A = \{1,2,3,4\}$, $R_1 = \{(1,2),(2,3),(1,3)\}$, dan $R_2 = \{(1,2), (2,4)\}$.

Di contoh ini, $R_1$ transitif sementara $R_2$ tidak transitif


## Setara
Sebuah relasi dinyatakan setara jika memenuhi syarat Reflektif, Simetris, dan Transitif

## Pengurutan Parsial
Sebuah relasi dinyatakan setara jika memenuhi syarat Reflektif, Anti-Simetris, dan Transitif

