Setelah menggunakan salah satu [[Penyelesaian Awal|metode penyelesaian awal]], kita bisa cek optimalisasi dengan metode-metode berikut:

# Degenerasi
Solusi degenerasi adalah solusi di mana $\text{Jumlah sel terisi} < \text{Jumlah header kolom } + \text{ Jumlah header baris }-1$.
Kita tidak bisa mengoptimalkan solusi degenerasi, maka harus kita tambahkan $\epsilon$ ke beberapa sel.
1. Carilah **sel tidak terisi termurah** dan tambahkan $\epsilon$.
2. Jika setelah menambahkan $\epsilon$, kita **tidak** bisa membuat loop, maka penempatan tersebut **benar**.
3. Jika masih degenerasi, ulangi penambahan $\epsilon$.
4. Jika sudah tidak, maka lanjut dengan proses optimalisasi
# Stepping Stone Method
1. Pilih salah satu sel tidak terisi
2. Buatlah loop untuk mengecek optimalitas sel tersebut:
	1. Tambahkan $+$ ke sel tersebut
	2. Lihat sel terisi di antara baris / kolom sel kosong tersebut
	3. Tambahkan $-$ ke sel tersebut
	4. Lihat sel tidak terisi di antara baris / kolom sel terisi tersebut
	5. Tambahkan $+$ ke sel tersebut
	6. Ulangi logika ini sampai balik lagi ke sel tidak terisi awal
	7. Garis harus Horizontal / vertikal dan harus dimulai dengan sel kosong & diakhiri dengan sel yang sama, dan jalan yang dilalui harus merupakan sel terisi
3. Lihat loop yang telah dibuat
4. Tambahkan dan kurangkan **harga** sel-sel yang dilalui oleh loop
5. Jika harga total positif, sel kosong tersebut sudah optimal
6. Jika harga total negatif, lihat sel pengurangan yang **nilainya terkecil**. Nilai tersebut adalah "nilai modifikasi". Tambahkan / kurangkan nilai modifikasi ke sel-sel yang dilalui loop tadi.
7. Jika semua sel tidak terisi positif, maka solusi sudah optimal