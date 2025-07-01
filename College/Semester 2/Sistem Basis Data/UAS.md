# Pembuatan Tabel
```SQL
CREATE TABLE <nama_tabel>(
<nama_variabel_1> <tipe_data>,
<nama_variabel_2> <tipe_data>,
...,
CONSTRAINT <nama_constraint_1> <tipe_constraint_1>,
CONSTRAINT <nama_constraint_2> <tipe_constraint_2>
);
```

# Pengeditan Tabel
```SQL
ALTER TABLE <nama_tabel> ...;

-- Penambahan Kolom
ALTER TABLE <nama_tabel> ADD <nama_kolom_baru> <tipe_data>;

-- Drop Kolom
ALTER TABLE <nama_tabel> DROP COLUMN <nama_kolom>;

-- Rename Kolom
ALTER TABLE <nama_tabel> RENAME COLUMN <nama_kolom_lama> TO <nama_kolom_baru>;

-- Ganti Tipe Data
ALTER TABLE <nama_tabel> MODIFY <nama_kolom> <tipe_data_baru>;

-- Drop Tabel

```
# Pengisian Data
```SQL
INSERT INTO <nama_tabel> (<kolom_1>, <kolom_2>, ...) VALUES (<nilai_kolom_1>, <nilai_kolom_2>, ...);
```
# Pengeditan Data
```SQL
UPDATE <nama_tabel> SET <kolom_1> = <nilai_kolom_1_baru>, 
```

# Pengambilan / Read Data
```SQL
-- View Semua Data Tabel
SELECT * FROM <nama_tabel>;

-- View Beberapa Kolom Tabel
SELECT <nama_kolom_1>, <nama_kolom_2>, ... FROM <nama_tabel>;

-- View Beberapa Kolom Tabel (Kolom di rename)
SELECT <nama_kolom_1> AS "<nama_alternatif_1>", <nama_kolom_2> AS "<nama_alternatif_2>", ... FROM <nama_tabel>;

-- View Semua Data Tabel Dengan Kondisi
SELECT * FROM <nama_tabel> WHERE <kondisi>;

-- View Semua Data Tabel Diurut
SELECT * FROM <nama_tabel> ORDER BY <cara_pengurutan>;
```

# Pencocokan Data / JOIN
```SQL
-- Cross Join
SELECT * FROM <tabel_1> CROSS JOIN <tabel_2>;

-- Inner Join
SELECT * FROM <tabel_1> INNER JOIN <tabel_2> ON <kondisi>;

-- Left/Right Outer Join
SELECT * FROM <tabel_1> LEFT/RIGHT OUTER JOIN <tabel_2> ON <kondisi>;
```
- Cross join "mengkalikan" semua baris / data pada `tabel_1` dengan `tabel_2`; menghasilkan semua kombinasi yang memungkinkan
- Inner join hanya memberikan baris yang terdapat di `tabel_1` dengan `tabel_2` / AND
- Outer join mengambil data pada tabel kiri/kanan (LEFT/RIGHT) dan mencocokan data dengan tabel lainnya

# Functions
- `LOWER(parameter)` = semua bukan kapital
- `UPPER(parameter)` = SEMUA KAPITAL
- `INITCAP(parameter)` = Karakter Pertama Di Setiap Kata Menjadi Upper Case
- `SUBSTR(parameter, start, end)` = parameter dipotong, mulai dari start sampai end.
	- `start` mulai dari 1, bukan 0
	- Misal "Hello World!", "Hello" adalah `SUBSTR('Hello World!', 1, 5)` dan "World!" adalah `SUBSTR('Hello World!', 7, 12)`
- `LENGTH(parameter)` = Menghitung panjang `parameter`
- `INSTR(sentence, letter)` = Mencari index `letter` pertama di `sentence`. Jika tidak ada, maka 0
- `LPAD(sentence, length, string)` dan `RPAD(sentence, length, string)` = Mengisi kiri/kanan sentence dengan `string` hingga keseluruhan sepanjang `length`
	- `LPAD('Hello World!', 15, *) -> '***Hello World!'`
	- `RPAD('Hello World!', 15, *) -> 'Hello World!***'`
- `TRIM(LEADING/TRAILING/BOTH string FROM sentence)` = Meng-trim `string` dari `sentence`
	- `TRIM(LEADING '*' FROM '***Hello World!***') -> 'Hello World!***`
	- `TRIM(TRAILING '*' FROM '***Hello World!***') -> '***Hello World!'`
	- `TRIM(BOTH '*' FROM '***Hello World!***') -> 'Hello World!`
- `REPLACE(sentence, find, replace)` = cari `find` di `sentence`, kemudian ubah menjadi `replace`
	- `REPLACE('Good fucking job', 'fucking, '') -> 'Good job'`