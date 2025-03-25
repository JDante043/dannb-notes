# Peningkatan Efisiensi
Komputer mengalami peningkatan performa dan penurunan harga yang drastis, namun keberatan & kerumitan operasi juga semakin meningkat. Karena itu, terdapat beberapa metode untuk meningkatkan performa sebuah CPU:
- **Pipelining**
- **Branch Prediction**
- **Superscalar Execution**
- **Data Flow Analysis**
- **Speculative Execution**

Tidak hanya CPU, komponen lain juga mengalami perubahan untuk meningkatkan performa keseluruhan komputer:
- Menambahkan bus DRAM
- Menambahkan kapasitas DRAM
- Menggunakan bus antar CPU-RAM yang lebih efisien
- Menambahkan dan mengefisiensikan cache CPU

# Masalah Dari Peningkatan Kecepatan
- Bagian komputer semakin panas
- Kecepatan memori tidak bisa menandingi kecepatan CPU
- Komponen yang semakin kecil dan tipis meningkatkan *RC delay*, secara sederhana, peningkatan delay karena resistensi dan kapasitansi sebuah sirkuit

# Multicore
Prosesor *multicore* merupakan sebuah prosesor yang memiliki lebih dari 1 core. Hal ini dilakukan dengan cara menggunakan 2 core yang "sederhana" dibandingkan dengan 1 core yang "kompleks" sehingga 2 core tersebut dapat memilki cache yang lebih besar.

Contoh penggunaan dari konsep *multicore* adalah GPU (*Grahics Processing Unit*). Pemrosesan data grafiks bukanlah hal yang kompleks, namun perlu dilakukan secara berulang dan akhirnya memakan banyak waktu. Karena itu, core dalam GPU lebih sederhana, namun lebih cepat.

Untuk melihat peningkatan kecepatan yang diberikan oleh sebuah prosesor *multicore* atau peningkatan lainnya, maka digunakanlah [[Hukum Amdahl]].

# Efisiensi Aplikasi / Software
## Queuing / Little's Law
Dalam sebuah aplikasi, jika terdapat banyak data yang perlu diproses, data tersebut akan ditempatkan di sebuah antrian. Untuk melihat densitas sebuah antrian, dapat menggunakan [[Hukum Little]].

## Benchmark
Benchmark merupakan sebuah operasi / program yang digunakan untuk menguji performa sebuah komputer. Ciri-ciri benchmark yang bagus adalah:
- Tidak spesifik untuk 1 komputer / bisa dipakai di mesin lain
- Menguji suatu sektor pemrograman / sebuah program
- Statistik / performa bisa dilihat dengan jelas dan akurat

Sebuah koleksi benchmark untuk suatu sektor disebut SPEC (*System Performance Evaluation Corporation*)

Contoh dari standard SPEC adalah SPEC CPU2006:
- Standar benchmark untuk prosesor
- Menguji performa prosesor dengan program-program yang menguji hal seperti *encoding/decoding* video, simulasi fisik, simulasi fluida, cuaca, dll.

