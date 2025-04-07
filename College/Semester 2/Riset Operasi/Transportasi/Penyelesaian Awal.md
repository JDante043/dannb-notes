Terdapat 3 cara untuk mendapatkan penyelesaian awal soal Transportasi:

# Metode Barat-Laut / North-West Corner Rule
1. Lihat sel paling atas kiri, isi dengan $MAX(\text{Source, Demand})$
2. Jika demand terpenuhi, pindah ke demand selanjutnya (kekanan)
3. Jika source habis, pindah ke source selanjutnya (kebawah)

# Metode Harga Terendah / Lowest Cost Method
1. Cek harga setiap sel
2. Pilih harga terendah
3. Isi harga terendah dengan $MAX(\text{Source, Demand})$
4. Ulangi sehingga semua demand terpenuhi

# Metode Vogel / Vogel's Approximation Method (VAM)
1. Cek selisih harga sel terendah dengan harga sel terendah kedua untuk setiap kolom & barisan
2. Pilih kolom/barisan yang mengandung nilai selisih tertinggi
3. Isi sel harga terendah di kolom/barisan tersebut dengan $MAX(\text{Source, Demand})$
4. Coret kolom/barisan tersebut karena antara demand / source pasti habis
5. Hitung ulang / balik ke step 1 hingga semua demand terisi