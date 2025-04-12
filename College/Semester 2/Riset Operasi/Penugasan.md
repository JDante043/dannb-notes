# Seimbang
1. Lihat setiap kolom tabel. Kurangi nilai di kolom tersebut dengan nilai terendah di kolom masing-masing
2. Lihat setiap barisan tabel. Kurangi nilai di barisan tersebut dengan nilai terendah di barisan masing-masing
3. Coret semua sel 0 dengan garis vertikal / horizontal seminimal mungkin
4. Jika $\text{Jumlah coretan } = \text{ Jumlah kolom/baris}$, lompat ke langkah $10$
5. Jika $\text{Jumlah coretan } < \text{Jumlah kolom/baris}$, tabel belum bisa digunakan untuk mencari jawaban
6. Lihatlah sel-sel yang tidak tercoret. Carilah nilai yang terkecil
7. Kurangi semua sel tidak tercoret dengan nilai tersebut
8. Tambahkan sel tercoret berinterseksi dengan nilai tersebut
9. Hapus coretan, kemudian balik ke langkah $3$.
10. Jika $\text{Jumlah coretan } = \text{ Jumlah kolom/baris}$, tabel sudah siap digunakan untuk mencari jawaban
11. Carilah sel 0 yang sendiri di suatu barisan / kolom
12. Hapuslah / Coretlah barisan **dan** kolom sel tersebut
13. Lakukanlah sampai semua tabel tertutup
14. Lihatlah lokasi sel 0 yang terpilih
15. Pindahkan lokasi tersebut ke matriks penugasan awal
16. Sel-sel di lokasi tersebutlah pilihan optimal

# Tidak Seimbang
Jika tabel tidak seimbang, tambahkan barisan / kolom dummy dengan isi 0 agar menjadi seimbang, setelah itu langkahnya sama dengan [[Penugasan#Seimbang|cara seimbang]]