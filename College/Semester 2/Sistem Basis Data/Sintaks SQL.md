# Note
- Jika terdapat kode `<xxx>`, artinya ganti dengan instruksi di dalam kurung sudut tanpa kurung sudut tersebut. Misal kita ingin membuat tabel negara, maka substitusikan `<Negara>` menjadi `Indonesia`.
- Sintaks untuk OracleSQL

# Pembuatan Tabel 
## Basic
```
CREATE TABLE <namaTabel> (
	<namaKolom1> <tipeData>,
	<namaKolom2> <tipeData>,
	...
);
```

## Dengan Constraint Cara 1
```
CREATE TABLE <namaTabel> (
	<namaKolom1> <tipeData>,
	<namaKolom2> <tipeData>,
	...
	CONSTRAINT <namaVariabelConstraint> <TIPE_CONSTRAINT> (<namaKolom>)
);
```

## Dengan Constraint Cara 2
```
CREATE TABLE <namaTabel> (
	<namaKolom1> <tipeData> <constraint>
	...
);
```

# DROP TABEL
```
DROP TABLE <namaTabel>;
```

# Modifikasi Tabel
## Rename Kolom/Tabel
```
ALTER TABLE <namaTabel> RENAME COLUMN <namaKolom> TO <namaBaru>; -- Kolom
ALTER TABLE <namaTabel> RENAME TO <namaBaru> -- Tabel
```

## DROP kolom
```
ALTER TABLE <namaTabel> DROP COLUMN <namaKolom>;
```

## ADD Kolom
```
ALTER TABLE <namaTabel> ADD <namaKolom> <tipeData>;
```

## Alter Kolom
```
ALTER TABLE <namaTabel> MODIFY <namaKolom> <tipeDataBaru>;
```

# Penambahan Data
```
INSERT INTO <namaTabel> (<kolom1, kolom2, ...>) VALUES (<dataKolom1, dataKolom2, ...>); -- Satu data / Barisan
```

# Pengambilan Data
## Semua data / kolom dalam tabel
```
SELECT * FROM <namaTabel>;
```

## Modifikasi header data yang disajikan
```
SELECT <kolom1> AS "<namaHeader1>", <kolom2> AS "<namaHeader2>", ... FROM <namaTabel>;
```

## Modifikasi data yang disajikan
```
SELECT <kolom1> <operasi> AS "<namaHeader1>", <kolom2> <operasi> AS "<namaHeader2>", ... FROM <namaTabel>;

-- Contoh
SELECT nama_murid || ' ' || nim_murid AS "NAMA & NIM", jurusan_murid AS "Jurusan" FROM database_mahasiswa;

SELECT nama_karyawan || ' | ' || gaji_karyawan AS "Karyawan & Gaji Sekarang", gaji_karyawan*2 AS "Gaji setelah kenaikan" FROM database_pekerja;
```

## Menyaring data yang disajikan
```
SELECT <kolom1>, <kolom2>, ... FROM <namaTabel> WHERE <filter>;

-- Contoh
-- Tampilkan mahasiswa dengan NIM 2025
SELECT nama_mahasiswa AS "Mahasiswa 2025", nim_mahasiswa AS "NIM", jurusan_mahasiswa AS "Jurusan"
FROM database_semua_mahasiswa_ukrida
WHERE nim_mahasiswa LIKE '%2025%';

-- Tampilkan mahasiswa yang nilai UASnya lulus dan nilainya 80-100
SELECT nama_mahasiswa AS "Mahasiswa", nilai_uas AS "Nilai UAS", verdict_uas AS "Verdict"
FROM database_uas_mahasiswa_2025
WHERE verdict_uas IN ('LULUS') AND nilai_uas BETWEEN 80 AND 100;
```

## Mengurut data yang disajikan
```
SELECT <kolom1>, <kolom2>, ... FROM <namaTabel> ORDER BY <kolom> <order>;

-- Contoh
SELECT nama_mahasiswa_2024, nim_mahasiswa_2024
FROM database_mahasiswa_ukrida
ORDER BY nim_mahasiswa_2024 DESC;

-- Tampilkan mahasiswa hanya dari angkatan 2025, urut secara Ascending
SELECT nama_mahasiswa AS 'Nama', nim_mahasiswa AS 'NIM'
FROM database_mahasiswa_ukrida
WHERE nim_mahasiswa LIKE '%2024%'
ORDER BY 'NIM';
```

## Proses khusus
### List Proses Khusus
- `LOWER(parameter)` = mengubah parameter menjadi lowercase semua
- `UPPER(parameter)` = mengubah parameter menjadi uppercase semua
- `INITCAP(parameter)` = mengubah parameter agar setiap karakter pertama kata menjadi kapital, lainnya lowercase
- `SUBSTR(word, begin, end)` = "memotong" `word` dari `begin` (mulai dari 1) hingga `end` (opsional). Misal "HelloWorld" -> Hello adalah `SUBSTR("HelloWorld", 1, 5).
- `LENGTH(word)` = menghitung panjang `word`
- `INSTR(word, letter)` = mencari index `letter` di `word`. Misal `INSTR('HelloWorld', 'W')` akan menghasilkan `6`.
- `LPAD(word, length, string)` dan `RPAD(word, length, string)` akan meng-pad kan word agar sepanjang `length` menggunakan `string`. Misal `HelloWorld` adalah 10 karakter panjang, maka `LPAD('HelloWorld', 15, '*') = *****HelloWorld`
- `TRIM(Leading/Trailing/BOTH str FROM word)` = mempangkas `str` dari `word`, mulai dari `Leading/Trailing/Both`
- `REPLACE(word, find, replace)` = mengganti `find` dengan `replace` di `word`

```
-- Contoh

-- Cari mahasiswa yang nama depannya "juanito"
SELECT nama_depan_mahasiswa, nama_belakang_mahasiswa FROM database_mahasiswa_ukrida
WHERE lower(nama_depan_mahasiswa) = 'juanito';

-- Tampilkan panjang nama mahasiswa
SELECT nama_mahasiswa AS "Nama", LENGTH(nama_mahasiswa) AS "Panjang" FROM database_mahasiswa_ukrida;

-- Lihat apabila mahasiswa memiliki huruf 'd' di namanya
SELECT nama_mahasiswa AS "Nama", INSTR(LOWER(nama_mahasiswa), 'd') AS "Indeks d" FROM database_mahasiswa

-- Penerapan sensor
SELECT REPLACE(message_text, bad_words, '***') FROM user_messages, bad_words;
```
