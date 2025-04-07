<!-- 
Resource pembantu: https://math.libretexts.org/Bookshelves/Applied_Mathematics/Applied_Finite_Mathematics_(Sekhon_and_Bloom)/04%3A_Linear_Programming_The_Simplex_Method/4.02%3A_Maximization_By_The_Simplex_Method
 -->

# Bentuk Standar
## Ekspresi aljabar
Berikut adalah bentuk standar ketika menggunakan algoritma simpleks:
> Maksimalkan $ax_1+bx_2+cx_3+...$
> Dengan kendala:
>   $dx_1+ex_2+fx_3 + ... = A_1$
>   $gx_1+hx_2+ix_3 + ... = A_2$
>   $x_1, x_2, x_3, ... >= 0$
>   $A_1, A_2, A_3, ... >= 0$

## Ekspresi Matriks

## Syarat lainnya
- Semua kendala harus berbentuk persamaan. Jika bukan persamaan, maka gunakanlah *variabel slack*
- Ruas kanan tidak boleh negatif

# Contoh
Maksimumkan $x_1+x_2$
Dengan kendala:
- $x_1+5x_2 <= 5$
- $2x_1 + x_2 <= 4$
- $x_1,x_2 >= 0$

Perhatikan bahwa $x_1+5x_2 <= 5$ dan $2x_1 + x_2 <= 4$ bukan berbentuk persamaan. Kita bisa menambahkan variabel baru $x_3$ dan $x_4$ untuk melengkapi ketidak-samaan tersebut agar menjadi persamaan:
- $x_2+5x_2+x_3 = 5$
- $2x_1+x_2+x_4=4$
- $x_1,x_2 >= 0$

Perhatikan juga fungsi maksimum kita hanya mengandung $x_1$ dan $x_2$. Kita akan mengubah fungsi tersebut menjadi:
$MAX(-x_1-x_2+Z = 0)$
Di mana $Z$ melambangkan total dari variabel slack kita.

Karena bentuk sudah standar, kita dapat menggunakan tabel simpleks:

| $x_1$ | $x_2$ | $x_3$ | $x_4$ | Z   | C   |
| ----- | ----- | ----- | ----- | --- | --- |
| 1     | 5     | 1     | 0     | 0   | 5   |
| 2     | 1     | 0     | 1     | 0   | 4   |
| -1    | -1    | 0     | 0     | 1   | 0   |

Penjelasan:
1. Setiap variabel ditaruh di paling atas
2. Setiap kolom melambangkan suatu ekspresi kendala kita
3. Setiap baris berisi koefisien variabel setiap ekspresi
4. $C$ merupakan hasil dari ekspresi
5. Ekspresi MAX() selalu ditaruh dibawah
6. Variabel slack selalu di paling kanan, sebelum $Z$ dan $C$

Penyelesaian:
1. Perhatikan kolom dari mulai variabel slack sampai $C$:

| $x_3$ | $x_4$ | Z | C |
| --- | --- | --- | --- |
| 1 | 0 | 0 | 5 |
| 0 | 1 | 0 | 4 |
| 0 | 0 | 1 | 0 |

2. Misalkan $x_1, x_2 = 0$, maka jika ekspresi diselesaikan, didapatkan $x_3 = 5$, $x_4 = 4$, dan $Z = 0$. Sekarang, tabel kita berbentuk:

| $x_1$ | $x_2$ | $x_3$ | $x_4$ | Z   | C   |       |
| ----- | ----- | ----- | ----- | --- | --- | ----- |
| 1     | 5     | 1     | 0     | 0   | 5   | $x_3$ |
| 2     | 1     | 0     | 1     | 0   | 4   | $x_4$ |
| -1    | -1    | 0     | 0     | 1   | 0   | Z     |

3. Lihatlah koefisien fungsi MAX(). Lihatlah kolom yang memiliki koefisien **terendah**. Kolom tersebut akan dinamakan kolom pivot. Kemudian, lihatlah koefisien-koefisien di atas. Saya akan memilih -1 paling kiri karena ada 2 koefisien yang $-1$.
4. Kita bagikan nilai $C$ masing-masing barisan dengan koefisien yang terdapat di kolom pivot. Di sini, terdapat $5/1 = 5$ dan $4/2 = 2$.
5. Lihatlah barisan yang memiliki hasil pembagian **terkecil**. Barisan ini akan dinamakan barisan pivot. Di sini terdapat $4/2 = 2$.
6. Lihatlah interseksi kolom pivot dengan barisan pivot. Elemen tersebut akan dinamakan elemen pivot. Di sini terdapat $2$.
7. Kita perlu mengumah elemen pivot kita menjadi 1. Di sini, kita akan bagi **semua variabel** di barisan pivot dengan $2$.

| $x_1$ | $x_2$ | $x_3$ | $x_4$ | Z   | C   |       |
| ----- | ----- | ----- | ----- | --- | --- | ----- |
| 1     | 5     | 1     | 0     | 0   | 5   | $x_3$ |
| **1** | 0.5   | 0     | 0.5   | 0   | 2   | $x_4$ |
| -1    | -1    | 0     | 0     | 1   | 0   | Z     |

8. Lihat barisan di atas elemen pivot. Kita perlu elemen di atas elemen pivot menjadi 0. Di sini, kita perlu mengkalikan keseluruhan barisan pivot dengan $-1$.
9. Lihat seluruh barisan pivot, kemudian tambahkan **keseluruhan barisan** atas dengan barisan pivot yang termodifikasi:

| *$x_1$* | $x_2$ | *$x_3$* | $x_4$  | *Z* | *C* |         |
| ------- | ----- | ------- | ------ | --- | --- | ------- |
| *0*     | *4.5* | *1*     | *-0.5* | *0* | 3   | *$x_3$* |
| ***1*** | *0.5* | *0*     | *0.5*  | *0* | 2   | *$x_4$* |
| *-1*    | *-1*  | *0*     | *0*    | *1* | *0* | *Z*     |

10. Lihat barisan di bawah elemen pivot. kita perlu elemen di bawah elemen pivot menjadi 0. Di sini, kita tidak perlu mengubah barisan pivot.
11. Tambahkan barisan pivot yang sudah termodifikasi dengan barisan di bawah barisan pivot:

| *$x_1$* | $x_2$  | *$x_3$* | $x_4$  | *Z* | *C* |         |
| ------- | ------ | ------- | ------ | --- | --- | ------- |
| *0*     | *4.5*  | *1*     | *-0.5* | *0* | 3   | *$x_3$* |
| ***1*** | *0.5*  | *0*     | *0.5*  | *0* | 2   | *$x_4$* |
| 0       | *-0.5* | *0*     | *0.5*  | *1* | 2   | *Z*     |

12. Sekarang, kita lihat matrix di mana setiap kolom memilki koefisien 1:

| $x_1$ | $x_3$ | $Z$ | $C$ |
| ----- | ----- | --- | --- |
| 0     | 1     | 0   | 3   |
| 1     | 0     | 0   | 2   |
| 0     | 0     | 1   | 2   |

13. Kita dapatkan ekspresi berikut:
	- $x_1 = 3$
	- $x_2 = 0$
	- $x_3 = 2$
	- $x_4 = 0$
	- $Z = 2$

14. Lihat lagi tabel kita:

| *$x_1$* | $x_2$  | *$x_3$* | $x_4$  | *Z* | *C* |         |
| ------- | ------ | ------- | ------ | --- | --- | ------- |
| *0*     | *4.5*  | *1*     | *-0.5* | *0* | 3   | *$x_3$* |
| ***1*** | *0.5*  | *0*     | *0.5*  | *0* | 2   | *$x_4$* |
| 0       | *-0.5* | *0*     | *0.5*  | *1* | 2   | *Z*     |

15. Jika **elemen barisan paling bawah positif semua**, maka ekspresi tersebut adalah jawaban kita.
16. Namun, masih terdapat $-0.5$ di barisan paling bawah. Ulangi lagi dari tahap nomor 3:

| *$x_1$* | $x_2$    | *$x_3$* | $x_4$  | *Z* | *C* |         |
| ------- | -------- | ------- | ------ | --- | --- | ------- |
| *0*     | *4.5*    | *1*     | *-0.5* | *0* | 3   | *$x_3$* |
| 1       | *0.5*    | *0*     | *0.5*  | *0* | 2   | *$x_4$* |
| 0       | **-0.5** | *0*     | *0.5*  | *1* | 2   | *Z*     |

17. Kita lihat masing-masing C di masing-masing barisan jika dibagi dengan koefisien di kolom pivot: $3/4.5 = 0.\bar{6}$ dan $2/0.5 = 4$. Nilai terkecil adalah $3/4.5 = 0.\bar{6}$. Maka, elemen pivot adalah $4.5$.
18. Kita perlu elemen pivot kita sama dengan 1. Bagi seluruh barisan pivot dengan $4.5$:

| *$x_1$* | $x_2$    | *$x_3$*     | $x_4$        | *Z* | *C*         |         |
| ------- | -------- | ----------- | ------------ | --- | ----------- | ------- |
| *0*     | 1        | $\bar{0.2}$ | $-0.\bar{1}$ | *0* | $\bar{0.6}$ | *$x_3$* |
| 1       | *0.5*    | *0*         | *0.5*        | *0* | 2           | *$x_4$* |
| 0       | **-0.5** | *0*         | *0.5*        | *1* | 2           | *Z*     |

19. Lihat elemen di bawah elemen pivot. Kita harus ubah elemen itu menjadi 0. Kalikanlah barisan pivot dengan $-0.5$, kemudian tambahkan barisan pivot ke barisan tersebut:

| *$x_1$* | $x_2$    | *$x_3$*      | $x_4$        | *Z* | *C*         |         |
| ------- | -------- | ------------ | ------------ | --- | ----------- | ------- |
| *0*     | 1        | $\bar{0.2}$  | $-0.\bar{1}$ | *0* | $\bar{0.6}$ | *$x_3$* |
| 1       | 0        | $-0.\bar{1}$ | $0.\bar{5}$  | 0   | 1.667       | *$x_4$* |
| 0       | **-0.5** | *0*          | *0.5*        | *1* | 2           | *Z*     |

20. Kalikan barisan pivot dengan $0.5$ untuk mengubah elemen di bawah elemen pivot menjadi 0, kemudian tambahkan barisan pivot ke barisan tersebut:

| *$x_1$* | $x_2$ | *$x_3$*     | $x_4$         | *Z* | *C*         |         |
| ------- | ----- | ----------- | ------------- | --- | ----------- | ------- |
| *0*     | 1     | $\bar{0.2}$ | $-0.\bar{1}$  | *0* | $\bar{0.6}$ | *$x_3$* |
| 1       | 0     | $0.\bar{1}$ | $-0.0\bar{5}$ | *0* | $0.\bar{3}$ | *$x_4$* |
| 0       | 0     | $0.\bar{1}$ | $0.4445$      | 1   | $0.533$     | *Z*     |

21. Sekarang, kita lihat lagi matrix koefisien 1:

| $x_1$ | $x_2$ | $Z$ | $C$         |
| ----- | ----- | --- | ----------- |
| 0     | 1     | 0   | $0.\bar{6}$ |
| 1     | 0     | 0   | $\bar{0.3}$ |
| 0     | 0     | 1   | $0.533$     |

Dapat kita lihat, maksimal dari $x_1 + x_2 + Z$ dengan kendala yang diberikan adalah ketika:
- $x_1 = 0.\bar{6}$
- $x_2 = 0.\bar{3}$
- $Z = 0.533$

