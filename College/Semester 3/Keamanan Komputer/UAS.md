# Ethereum Smartcontract
- Smartcontract di blockchain Ethereum menggunakan standar ERC20 (Ethereum Request for Comments 20)
- Smartcontract mirip dengan sebuah program, memastikan interaksi yang menggunakan token konsisten di mana saja.
- Setiap smartcontract memiliki 6 properti wajib:
	- `name`, nama token, seperti "token Universitas Kristen Krida Wacana"
	- `symbol`, alias token, seperti "tUKRIDA"
	- `decimals`, jumlah desimal, contohnya Ether / ETH menggunakan 18
	- `totalSupply`, jumlah keseluruhan supply
	- `balances`, map / peta yang menyimpan balance setiap alamat
	- `allowances`, map / peta delegasi token (`transferFrom`)
- Setiap smartcontract memiliki 2 event yang wajib dicatat oleh blockchain untuk melacak perubahan status:
	- Transfer, setiap kali token dikirim akan tercatat penerima, pengirim, dan jumlah
	- Approval, setiap kali pemilik menyetujui alamat lain untuk menggunakan token miliknya akan tercatat penerima, pengirim, dan jumlah
- Untuk melakukan operasi basic pada blockchain, maka diperlukan 6 fungsi berikut:
	- `totalSupply() -> uint256`, mengembalikan total supply
	- `balanceOf(address account) -> uint256`, mengembalikan dana suatu alamat
	- `transfer(address to, uint256 value) -> bool`, mengirim sejumlah `value` kepada alamat `to`.
	- `approve(address spender, uint256 value) -> void`, membolehkan `spender` untuk menggunakan sejumlah dana `value`.
	- `allowance(address owner, address spender) -> uint256`, melihat jumlah token `owner` yang boleh dipakai oleh `spender`
	- `transferFrom(address from, address to, uint256 value) -> bool`, mengirim sejumlah token `value` dari `from` ke `to` jika jumlahnya dibawah/sama dengan jumlah allowance

# Malware
Malware adalah sebuah program yang diinstal kepada suatu sistem secara rahasia tanpa diketahui oleh pemilik sistem yang tujuannya adalah merusak, mencuri, atau membatasi akses data pada sistem.

Virus adalah sebuah software yang akan mengeksekusi dan meretas sistem jika file terinfeksi dieksekusi. Malware setiap OS dan kelemahan berbeda dan biasanya mengikuti stage **Dormant** -> idle; **Propagation** -> Membuat copy ke program lain; **Triggering** -> Diaktivasikan oleh suatu hal seperti sistem mengeksekusi program yang terinfeksi; **Execution** -> Kode malware virus tereksekusi
## Terminologi
- Virus: Sebuah malware yang dapat menyebar ke komputer lain
- Worm: Seperti virus, namun dapat menyebar secara sendiri tanpa perlu komputer target untuk mengeksekusi program terinfeksi
- Logic Bomb: Suatu kondisi pada suatu program yang akan menginfeksi komputer jika terpenuhi
- Trojan Horse: Malware yang menyerupai program aman namun memiliki fungsionalitas ekstra
- Backdoor: Jalur untuk memberikan orang luar aksse tanpa otorisasi
- Mobile code: Mengirim *copy* kepada platform yang sama untuk dieksekusi
- Auto-rooter kit: program yang membuat malware
- Spammer & Flooder: program yang mengirim banyak paket "sampah"
- keylogger: program yang mengawasi tekanan keyboard dan mouse
- rootkit: malware yang memberikan akses root kepada peretas
- Zombie: Device terinfeksi yang menyerang device sehat lain
- Payload: kode yang dieksekusi malware
- Crimeware: Malware yang mengotomatisasi cybercrime
- Advanced Persistent Threats (APT): sebuah serangan kompleks yang dilakukan sepanjang suatu waktu.
<!-- Too much bullshit, may God bless you-->
# Denial of Service (DoS)
Sebuah serangan yang menggunakan network, sistem, atau aplikasi untuk menghabiskan / menguras kemampuan sistem untuk memberikan servis. Biasanya yang ditargetkan seperti CPU, memory, internet bandwidth, diskspace, atau aplkasi (sehingga aplikasi tidak dapat menyediakan servis).

## Flooding attack
Menargetkan kapasitas bandwidth sistem. Dipisahkan menjadi 3 kategori, berdasarkan protokol:

**ICMP / Ping Flood**
Menggunakan ping yang jumlahnya banyak untuk memakan bandwidth sistem dan kemungkinan CPU sistem. Gampang terdeteksi kecuali menggunakan alamat IP sekali pakai.

**UDP Flood**
Penyerang menargetkan suatu port dalam sistem dan mengirim paket UDP

**TCP SYN Flood**
Penyerang akan mengirim paket SYN yang banyak, sehingga komputer target kewalahan untuk melacak koneksi yang terjalan

## DDoS
Peretas menggunakan worm untuk menginfeksi banyak komputer sebelum melakukan serangan menggunakan device-device terinfeksi yang membentuk botnet

## Serangan HTTP
### HTTP Flood
Server diserang dengan cara dikirimi banyak request HTTP.

### Slowloris
Request HTTP yang tidak dapat diselesaikan

## Serangan Refleksi
Penyerang menggunakan alamat sistem A untuk menyerang sistem B. Sistem B akan menjawab langsung ke sistem A, bukan ke penyerang

## Amplifikasi DNS
Penyerang menggunakan alamat korban untuk mengirim request DNS sehingga ketika korban mengirim query DNS, komputer korban kewalahan.

## Mitigasi dan response
- Alamat yang diketahui palsu diblock oleh router
- 