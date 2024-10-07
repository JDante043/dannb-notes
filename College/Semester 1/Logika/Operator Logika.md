Operator di logika merupakan sebuah fungsi boolean. Di dunia nyata, operator merupakan sebuah *device*.

# Operator
Di dalam logika terdapat beberapa operator:

[List simbol logika di LaTeX](https://en.wikipedia.org/wiki/List_of_logic_symbols)
- AND / Konjungsi ($\wedge$)
- OR / Disjungsi ($\vee$)
- NOT / Negasi ($!, \neg$)
- IMPLY / Implikasi($\rightarrow, \implies, \supset$)
- EQUIV / Biimplikasi ($\leftrightarrow,\iff$)
- NAND / Tidak Dan ($|$)
- NOR / Tidak Atau ($\mp$)
- XOR / Disjungsi Eksklusif ($\oplus$)

## AND / Konjungsi
Disimbolkan dengan $\wedge$, AND memberikan hasil TRUE jika semua argumen adalah TRUE:

| A   | B   | A $\wedge$ B |
| --- | --- | ------------ |
| T   | T   | T            |
| T   | F   | F            |
| F   | T   | F            |
| F   | F   | F            |

## OR / Disjungsi
Disimbolkan dengan $\vee$, OR memberikan hasil TRUE jika salah satu argumen adalah TRUE:

| A   | B   | A $\vee$ B |
| --- | --- | ---------- |
| T   | T   | T          |
| T   | F   | T          |
| F   | T   | T          |
| F   | F   | F          |
## NOT / Negasi
Disimbolkan dengan $!$, Negasi merupakan operator yang membalikkan hasil:

| A   | $!$A |
| --- | ---- |
| T   | F    |
| F   | T    |

## IMPLY / Implikasi
Disimbolkan dengan $\rightarrow$, Implikasi menghasilkan TRUE **kecuali** A adalah TRUE
dan B adalah FALSE:

| A   | B   | A $\rightarrow$ B |
| --- | --- | ----------------- |
| T   | T   | T                 |
| T   | F   | F                 |
| F   | T   | T                 |
| F   | F   | T                 |

## EQUIV / Bi-Implikasi
Disimbolkan dengan $\leftrightarrow$, Bi-implikasi menghasilkan TRUE jika kedua A dan B nilainya sama:

| A   | B   | A $\leftrightarrow$ B |
| --- | --- | --------------------- |
| T   | T   | T                     |
| T   | F   | F                     |
| F   | T   | F                     |
| F   | F   | T                     |

## NAND / Tidak Dan
Disimbolkan dengan $|$, NAND menghasilkan TRUE **kecuali** kedua A dan B nilainya **TRUE**:

| A   | B   | A \| B |
| --- | --- | ------ |
| T   | T   | F      |
| T   | F   | T      |
| F   | T   | T      |
| F   | F   | T      |

## NOR / Tidak Atau
Disimbolkan dengan $\mp$ (Minus di atas plus), NOR menghasilkan TRUE **jika** kedua A dan B nilainya **FALSE**:

| A   | B   | A $\mp$ B |
| --- | --- | --------- |
| T   | T   | F         |
| T   | F   | F         |
| F   | T   | F         |
| F   | F   | T         |

## XOR
Disimbolkan dengan $\oplus$, XOR adalah operator digital yang menghasilkan TRUE **jika jumlah TRUE ganjil**:

| A   | B   | A $\oplus$ B |
| --- | --- | ------------ |
| T   | T   | F            |
| T   | F   | T            |
| F   | T   | T            |
| F   | F   | F            |

# Tips
## AND & OR
Lebih baik menggunakan 0 dan 1 daripada T dan F, kemudian misalkan AND adalah perkalian, dan OR adalah pertambahan. Hasil 0 adalah False, yang lainnya TRUE