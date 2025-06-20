Graf adalah sebuah koleksi simpul / *vertices* / *nodes* yang memiliki sebuah nilai dan dihubungkan oleh sisi / *edges* / *lines*.

Notasi sebuah graf adalah $G=(V,E)$. Di mana $V$ adalah himpunan simpul seperti $\{v1,v2,...,vn\}$ dan $E$ adalah himpunan sisi seperti $\{e1,e2,...,en\}$.

# Contoh Graf
Lihatlah graf berikut:
![[Graph example.png]]  ^405952
## Notasi
Notasi graf tersebut adalah $V = \{A,B,C,D\}$ dan $E=\{e1,e2,e3,e4,e5,e6,e7\} = \{AC,AC,AB,AB,AD,DC,DB\}$ .

## Relasi
Pada himpunan $E$, terdapat 2 **sisi ganda**, yaitu sisi yang menghubungkan 2 simpul yang sama ($AC\text{ dan }AB$).

Di gambar tersebut juga tidak ada **gelang**, yaitu sisi yang mulai dan akhirnya adalah suatu simpul.

# Tipe Graf
## Berdasarkan isi
Tipe graf tersebut adalah **graf tidak kosong**. Graf kosong adalah graf yang **tidak mempunyai sisi**

Contoh graf kosong:
![[Graf kosong.png]] 

## Berdasarkan kondisi sisi
Lihat [[Graf#^405952| Gambar graf pertama kita]]. Perhatikan bahwa sisinya tidak mempunyai arah. Graf merupakan graf **tidak berarah**. Jika terdapat arah, maka graf tersebut merupakan graf **berarah**.

### Tabel Tipe Graf

| Jenis             | Berarah? | Boleh Ganda? | Boleh Loop? |
| ----------------- | -------- | ------------ | ----------- |
| Sederhana         | X        | X            | X           |
| Ganda             | X        | O            | X           |
| Semu              | X        | O            | O           |
| Berarah Sederhana | O        | X            | O           |
| Ganda Berarah     | O        | O            | O           |

### Graf Tidak Berarah
Berikut adalah beberapa jenis graf tidak berarah:
#### Graf Sederhana / *Simple Graph*
![[Graf sederhana.png]]
- Tidak berarah
- Setiap simpul hanya ada 1 sisi
- Tidak Bergelang

#### Graf Ganda / *Multigraph*
![[Graf Ganda.png]]
- Tidak berarah
- Tidak mengandung Gelang

#### Graf Semu / *Pseudo Graph*
![[Graf Semu.png]]
- Tidak berarah
- Mengandung Loop

### Graf Berarah
#### Graf Berarah Sederhana / *Directed Simple Graph*
![[Graf Berarah Sederhana.png]]
- Setiap simpul hanya memiliki 1 sisi
- Boleh mengandung loop

#### Graf Ganda Berarah / *Directed Multigraph*
![[Graf Ganda Berarah.png]]

# Terminologi Graf
Berikut adalah terminologi yang digunakan dalam materi *Graph Theory*:
## Bertetangga / *Adjacent*
![[Graf sederhana.png]]
2 Simpul dikatakan bertetangga jika dihubungkan dengan sisi. $SQ$ bertetangga, sementara $PR$ tidak.

## Bersisian / *Incidency*
![[Graph example.png]]
Suatu sisi dikatakan bersisian dengan simpul jika sisi tersebut menghubungkan simpul. $e1$ bersisian dengan $A$ dan $C$, tetapi tidak bersisian dengan $B$.

## Simpul Terpencil / *Isolated Node*
![[Simpul terpencil.png]]
Suatu simpul dikatakan terpencil jika tidak dihubungkan dengan sisi. $T$ dan $U$ adalah simpul terpencil

## Derajat / *Degree*
![[Graph example.png]]
Derajat suatu simpul adalah jumlah sisi yang menghubungkan simpul tersebut. $d(D) = 3$ dan $d(A) = 5$

Total derajat suatu graf dapat dihitung dengan rumus $\Sigma d = e\cdot 2$.
Misal di gambar tersebut ada 7 sisi, maka derajat di graf tersebut ada 14.
Derajat selalu genap karena setiap sisi selalu menghubungkan 2 simpul. Jangan lupa, **loop masih dihitung menghubungkan 2 simpul**
## Notasi arah
![[Graf Berarah Sederhana.png]]
Cara penulisan suatu sisi adalah dengan $d_{\text{in/out}}(V)$. Titik S memiliki derajat $d_{\text{out}}(S) = 1$ dan $d_{\text{in}}(S) = 2$ maka $d(S) = 3$.

## Lintasan / *Path*
![[Graf Berarah Sederhana.png]]
Lintasan adalah jalur dari sebuah simpul awal sampai simpul akhir. **Setiap sisi hanya boleh dilewati sekali** Misal, $SRQP$.

Lintasan yang dimulai dan diakhiri dengan simpul yang sama dinamakan **siklus**.

Panjang suatu lintasan adalah jumlah sisi yang dilewati.

Diameter suatu graf adalah **lintasan terpanjang** pada graf tersebut.

## Graf Lengkap / *Complete Graph*
Graf lengkap adalah sebuah graf sederhana yang setiap simpul dihubungkan ke simpul lainnya. Karena itu, jumlah sisi suatu graf lengkap adalah $\Sigma E = \frac{n(n-1)}{2}$ di mana $n$ adalah jumlah simpul.
![[Graf Lengkap.png]]

## Graf Lingkaran / *Cycle Graph*
Graf lingkaran adalah graf di mana semua simpulnya berderajat 2 dan memiliki siklus.
![[Graf Lingkaran.png]]
## Graf Roda / *Wheels Graph*
Graf roda adalah graf lingkaran namun ditambahkan 1 simpul yang menghubungkan semua simpul lain kepadanya pada setiap $Cn$.
![[Graf Roda.png]]

## Graf Teratur / *Regular Graphs*
Graf teratur adalah graf di mana semua simpul memiliki derajat yang sama. Jumlah sisi pada graf tipe ini adalah $\Sigma E = \frac{nr}{2}$, di mana $n$ adalah jumlah simpul dan $r$ adalah derajat setiap simpul.

![[Graf Teratur.png]]

## Graf Planar / *Planar Graph* dan Graf Bidang / *Plane Graph*
Graf planar adalah graf **yang dapat** digambar sedemikian rupa agar tidak ada sisi yang memotong. Graf bidang adalah graf planar yang digambar dengan cara tersebut.
![[Graf Planar.png]]

Perhatikan graf (a) dan (b) memiliki jumlah sisi, derajat simpul, dan "bentuk" yang sama. Kedua graf tersebut adalah graf planar, namun hanya graf (b) adalah graf bidang.

## Formula Euler
Misalkan graf $G$ adalah graf planar, dengan $e$ jumlah sisi, $v$ jumlah simpul dan $r$ jumlah daerah, maka $$r = e-v+2$$

- Jika $e\ge 3$, maka $$e\le 3v-6$$
- Jika $e\ge 3$ dan **tidak memuat sirkuit**, maka $$e\le 2v-4$$
## Graf Bipartit / *Bipartite Graph*
Graf sederhana dikatakan bipartit jika dapat dipisah menjadi 2 himpunan dan setidaknya 1 simpul menghubungkan kedua himpunan tersebut.
![[Graf Bipartit 1.png]]
![[Graf Bipartit 2.png]]

Perhatikan bahwa setiap simpul menghubungkan $V_1$ dengan $V_2$

## Graf Berlabel / Berbobot / *Weighted Graph*
Graf berlabel adalah graf di mana setiap sisinya memiliki suatu bobot / nilai
![[Graf Berlabel.png]]

## Kehubungan & Sub Graf
Setiap graf dibilang terhubung jika terdapat jalur yang menghubungkan suatu simpul dengan simpul lain.
![[Graf Terhubung.png]]

Perhatikan graf paling kanan. Graf tersebut tidak terhubung karena terdapat sub graf $\{a,c,b,d\}$ dan $\{p,q,r\}$

