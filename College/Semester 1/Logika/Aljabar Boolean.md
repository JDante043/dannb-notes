# Definisi
Aljabar boolean adalah cabang dari aljabar di mana hasil fungsi dan variabel hanya bernilai antara 0 atau 1, dan operator yang digunakan adalah [[Operator Logika]] (NOT, AND, XOR, dll.). 

Berbeda juga dengan aljabar aritmatika, nilai-nilai variabel yang akan dimasukkan sudah diketahui. Suatu fungsi dapat dilihat hasil akhirnya, dengan memasukkan 0 atau 1 secara berurutan di sebuah **Truth Table**. Urutan ini disebut **Gray code**. Total kemungkinan dapat dihitung dengan rumus $2^{\text{ banyak variabel}}$. Berikut adalah contoh dari gray code dari fungsi $f(x,y,z)$:

| x   | y   | z   | f(x) |
| --- | --- | --- | ---- |
| 0   | 0   | 0   |      |
| 0   | 0   | 1   |      |
| 0   | 1   | 0   |      |
| 0   | 1   | 1   |      |
| 1   | 0   | 0   |      |
| 1   | 0   | 1   |      |
| 1   | 1   | 0   |      |
| 1   | 1   | 1   |      |
$f(x)$ di tabel tersebut menandakan nilai hasil akhir fungsi.

# Fungsi Boolean
Fungsi boolean adalah fungsi di mana semua variabel yang dikandung di dalamnya hanya bernilai antara 1 atau 0, dan jawaban akhir yang dihasilkan fungsi tersebut juga antara 1 atau 0.

Fungsi ini memiliki 2 bentuk, sederhana dan kanonikal / standard. Bentuk standard adalah ketika semua bagian ("*term*") memiliki variabel yang lengkap. Bentuk sederhana adalah bentuk di mana variabel di setiap bagian dikurangi sehingga bentuk lebih sederhana, tetapi masih memiliki hasil akhir yang sama di *truth table*

Berikut adalah contoh bentuk standard dan sederhana:

- $f(w,x,y,z) = wxy^\prime z^\prime+wx^\prime yz+wx^\prime yz^\prime+wx^\prime y^\prime z^\prime+w^\prime xy^\prime z^\prime+w^\prime x^\prime yz^\prime+w^\prime x^\prime y^\prime z^\prime$
- $f(w,x,y,z) = wx^\prime y+w^\prime x^\prime yz^\prime+y^\prime z^\prime$

# SOP & POS
SOP (Sum-of-Product) dan POS (Product-of-Sum) adalah bentuk fungsi boolean.

## SOP
Fungsi boolean SOP berbentuk perkalian yang ditambahkan, seperti $f(w,x,y,z) = wxy^\prime z^\prime+wx^\prime yz+wx^\prime yz^\prime+wx^\prime y^\prime z^\prime+w^\prime xy^\prime z^\prime+w^\prime x^\prime yz^\prime+w^\prime x^\prime y^\prime z^\prime$. Setiap suku dari bentuk fungsi ini menandakan hasil 1 / TRUE dan setiap komplemen ($\prime$) menandakan 0, sementara non-komplemen (huruf biasa) menandakan 1

## POS
Fungsi boolean POS berbentuk pertambahan yang dikalikan, seperti $f(w,x,y,z)= (y\prime + z)(w\prime + x\prime + y + z)(x + y)$. Setiap suku dari fungsi ini menandakan hasil 0 / FALSE dan setiap komplemen menandakan 1, sementara non-komplemen menandakan 0.

# Karnaugh Map
Karnaugh map adalah cara untuk menyederhanakan suatu fungsi boolean. K-map memiliki total petak sebanyak $2^{\text{ Banyak variabel }}$. Contoh berikut adalah contoh dengan fungsi 4 variabel:

$$
f(w,x,y,z) = wxy^\prime z^\prime+wx^\prime yz+wx^\prime yz^\prime+wx^\prime y^\prime z^\prime+w^\prime xy^\prime z^\prime+w^\prime x^\prime yz^\prime+w^\prime x^\prime y^\prime z^\prime
$$

Peta Karnaugh fungsi tersebut adalah peta 4x4 yang disusun seperti di bawah, setiap suku fungsi menandakan 1 di tabel :
```
	WX →
YZ ↓
  | 00 | 01 | 11 | 10 |
00|  1 |  1 |  1 |  1 |
01|    |    |    |    |
11|    |    |    |  1 |
10|  1 |    |    |  1 |

```

Untuk menyederhanakan:
- 1 yang berderetan dikumpulkan kedalam satu grup, grup ini boleh vertikal atau horizontal.
- setiap grup mempunyai nilai 2 dipangkat ($2^0; 2^1; 2^2, ...$)
- Di contoh di atas, terdapat 3 grup, atas, kiri, dan kanan
- Di setiap grup, lihat variabel yang tidak berubah:
	- Di grup atas, hanya variabel Y dan Z saja yang tidak berubah, yaitu ketika mereka nilainya 0, maka suku pertama fungsi adalah Y'Z'
	- Di grup kanan, W, X, dan Y tidak berubah, maka suku kedua adalah WX'Y
	- Di grup kiri, semua variabel tidak berubah, maka suku ketiga adalah W'X'YZ'
- Setelah semua suku sudah disederhanakan, maka bisa dibuat fungsi sederhana bentuk SOP: $f(x) = Y\prime Z\prime + WX\prime Y + W\prime X\prime YZ\prime$

