# Definisi
Telekomunikasi adalah pertukaran informasi jarak jauh.

Informasi akan diubah menjadi sinyal listrik, yang kemudian akan disalurkan melalui suatu media. Penerima kemudian menginterpretasikan sinyal listrik tersebut

# Komponen
- **Terminal Equipment (TE)**: Merupakan interface / "pengirim / penerima informasi". Contohnya Telefon & Komputer
- **Switching Equipment (SE)**: Merupakan alat yang menghubungkan TE. Contohnya network switch
- **Transmission Line**: Cara informasi tersebut disalurkan / medianya. Contohnya kabel ethernet, wifi, dan sinyal radio

## Contoh Komponen Dalam Situasi Nyata
Contoh ketiga komponen beraksi adalah ketika mengirim SMS:
`HP 1 <-> BTS <-> BSC <-> MSC <-> SMSC <-> MSC <-> BSC <-> BTS <-> HP 2`

- HP merupakan TE. Mereka mengubah pesan dari manusia menjadi sinyal listrik dan sebaliknya.
- BTS, BSC, MSC, dan SMSC adalah SE. Mereka menyalurkan pesan dari HP 1 ke HP 2 dan sebaliknya.
- Transmission Line adalah sinyal radio dan kabel yang digunakan HP dan tower-tower tersebut.

# Tipe Telekomunikasi
## Berdasarkan Tipe Informasi
- Data
- Suara
- Artikel & Gambar

## Berdasarkan Metode Pengiriman
- Point-to-Point
- Point-to-Multipoint
- Multipoint-to-Multipoint
- Kombinasi Mesh & Star

# Tipe Sirkuit
## Dedicated
- Jalur terdedikasi / permanen. Misalnya modem rumah (milik ISP) ke server ISP.
- Tidak tergantung pada keaktifan channel.
- Kurang efisien
- Lebih mahal

## Switched
- Dibuat ketika terdapat data yang ingin dikirim
- Channel di-diskonek ketika tidak ada data yang dikirim
- Lebih efisien; bisa melayani lebih banyak terminal dengan hardware yang sama.

# Masalah Pada Sistem Telekomunikasi
- Efisiensi / Harga
- Multiplexing
- Waktu respons & stabilitas

# Faktor Dalam Pembuatan Sistem Telekomunikasi
- Signalling -> Cara signalling. Wireless? Atau Wired?
- Transmisi -> 
- Numbering Check -> Melihat jumlah pelanggan
- Metode Routing -> Cara routing 2 atau lebih terminal
- Tariff -> Harga sistem telekomunikasi

# Penggunaan Sistem Telekomunikasi Dalam Kehidupan Sehari-hari dan Dunia Bisnis
## Objektif / Tujuan
- Transmisi data yang efisien
- Penggunaan komputer secara remote
- Setralisasi & Desentralisasi data
- Memudahkan manajemen data
- Mengurangi waktu pemrosesan data
- Meningkatkan keandalan sistem
- Meningkatkan penyebaran informasi

## Gunanya Sirkuit
- Meningkatkan kepuasan customer
- Menjadi lebih kompetitif dan responsif dari perusahaan lain
- Meningkatkan tingkat dan kualitas penyaluran data inter-perusahaan

## Hal-hal Yang Tercapai Dengan Sistem Komunikasi Data
- Kualitas servis bagi customer meningkat
- Kualitas data meningkat, karena data yang tidak tercatat terkurang
- Delay pembuatan laporan detail terkurang
- Delay pengambilan keputusan terkurang

## Hal-hal yang Dipertimbangkan Ketika Membuat Sistem Komunikasi Data di Dunia Bisnis
- Tipe & seberapa pentingnya transaksi / data <-> lokasi & nomor situs yang akan dihubungkan
- Harga servis <-> Pertumbuhan yang diharapkan
- Volume data <-> Distribusi data
- Bahasa pemrograman <-> Keandalan & akurasi