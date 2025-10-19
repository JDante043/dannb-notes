# Telekomunikasi
- Adalah pertukaran informasi dan pergantian bentuk dari informasi tersebut menjadi listrik
- Hal ini dilakukan agar mempercepat konversi menjadi listrik, memperluas area komunikasi, dan mempermudah pergantian bentuk informasi ke bentuk lain
- Dibuat dari 3 komponen:
	- **Terminal Equipment**; Sebuah interface / konverter. HP, komputer, laptop, dll.
	- **Switching Equipment**; Alat yang mengatur jalur sinyal
	- **Transmission Line**; Media perjalanan informasi. Radio, coaxial, fibre optic, dll.

## Contoh Komponen Dalam Situasi Nyata
Contoh ketiga komponen beraksi adalah ketika mengirim SMS:
`HP 1 <-> BTS <-> BSC <-> MSC <-> SMSC <-> MSC <-> BSC <-> BTS <-> HP 2`

- HP merupakan Terminal. Mereka mengubah pesan dari manusia menjadi sinyal listrik dan sebaliknya.
- BTS, BSC, MSC, dan SMSC adalah Switch. Mereka menyalurkan pesan dari HP 1 ke HP 2 dan sebaliknya.
- Transmission Line adalah sinyal radio dan kabel yang digunakan HP dan tower-tower tersebut.

## Tipe Telekomunikasi
## Berdasarkan Tipe Informasi
- Data
- Suara
- Artikel & Gambar

## Berdasarkan Metode Pengiriman
- Point-to-Point
- Point-to-Multipoint
- Multipoint-to-Multipoint
- Kombinasi Mesh & Star

## Tipe Sirkuit
## Dedicated
- Jalur terdedikasi / permanen. Misalnya modem rumah (milik ISP) ke server ISP.
- Tidak tergantung pada keaktifan channel.
- Kurang efisien
- Lebih mahal

## Switched
- Dibuat ketika terdapat data yang ingin dikirim
- Channel di-diskonek ketika tidak ada data yang dikirim
- Lebih efisien; bisa melayani lebih banyak terminal dengan hardware yang sama.

## Masalah Pada Sistem Telekomunikasi
- Efisiensi / Harga
- Multiplexing
- Waktu respons & stabilitas

## Faktor Dalam Pembuatan Sistem Telekomunikasi
- Signalling -> Cara signalling. Wireless? Atau Wired?
- Transmisi -> 
- Numbering Check -> Melihat jumlah pelanggan
- Metode Routing -> Cara routing 2 atau lebih terminal
- Tariff -> Harga sistem telekomunikasi

## Penggunaan Sistem Telekomunikasi Dalam Kehidupan Sehari-hari dan Dunia Bisnis
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

# OSI Model
Open Systems Interconnection Model adalah sebuah konsep / model reference / standard / framework dari ISO (International Organization for Standardization) untuk menjelaskan / memodelkan komunikasi dalam network komputer.

Model ini sangat penting untuk beberapa hal:
- Standardisasi antar vendor
- Efisiensi & Efektivitas
- Menjaga harga antar vendor untuk suatu alat
- Meningkatkan kesaingan antar vendor



| Layer # |  Layer Name  |                              Description                               |               Example                |
| :-----: | :----------: | :--------------------------------------------------------------------: | :----------------------------------: |
|    1    |   Physical   |                      Medium penghantar komunikasi                      |            Cat 5e, RS232             |
|    2    |  Data-Link   |         Pengiriman data antar node / device dalam network, MAC         |       Ethernet, Wi-Fi (802.11)       |
|    3    |   Network    |                      Routing / packet forwarding                       |            IPv4/6, Router            |
|    4    |  Transport   |                  Protocol suatu komunikasi dilakukan                   |            TCP/IP, UDP/IP            |
|    5    |   Session    |                  Membuka sesi antara 2 node / device                   | Secure Copy(SCP)/SSH, "HTML session" |
|    6    | Presentation | Mengubah data dari layer 7 <-> layer 6 (Data translation & encryption) | CODEC (Multimedia), ASCII -> UNICODE |
|    7    | Application  |                   Data yang digunakan oleh aplikasi                    |        SSH, DNS, HTTP/S, FTP         |
## Kenapa menjadi layer?
- Memudahkan penjelasan dan pengajaran
- Menyederhanakan manajemen network
- Membuat jelas dan memudahkan rute data / *data flow*
- Menghindari perubahan satu layer memengaruhi layer lain
- Mempermudah *troubleshooting*
- Memperbolehkan dan mempermudah hardware dan software berkomunikasi

# Istilah networking
- Peer-to-peer (P2P) Communication: Komunikasi antara 2 device pada layer yang sama
- Protocol: Set peraturan cara device dalam network berkomunikasi
- Enkapsulasi: Proses flow data sebelum dikirim
- Protocol Data Unit (PDU): Informasi yang ditukar pada komunikasi antar-layer

# TCP/IP Model
Berbeda dengan OSI, lebih spesifik ke transmisi data. Dibuat untuk membuat transmisi tanpa-eror, kompatibilitas antar-network, transmisi yang stabil dan *reliable*, dan menaikkan efisiensi

|        Layer         |                                           Deskripsi                                           |      Contoh       |
| :------------------: | :-------------------------------------------------------------------------------------------: | :---------------: |
|     Application      |                       Protokol *high-level*; enkoding dan dekoding data                       | FTP, SMTP, Telnet |
|      Transport       | Konektivitas logikal, operasi end-to-end, segmentasi, *error correction*, dan *flow  control* |     TCP, UDP      |
|       Network        |                           Packet Switching, Best path determination                           |        IP         |
| Data-Link & Physical |                          Enkapsulasi paket -> frame & koneksi fisik                           |        PPP        |
## Transport
- Data segmentasi
- Control flow = sliding window
- reliability = sequence & acknowledgement number
- TCP; UDP; SPX; X.3
- koneksi virtual setelah 3-way handshake

**TCP**:
- Membuka koneksi virtual
- TCP pengirim dan penerima harus aktif
- mengirim data berbasis nomor port

**IP**:
- Rute sender <-> penerima menggunakan best path
- IP semua device dalam rute harus aktif
- Mengirim data berbasis IP

## TCP vs UDP
| TCP                                         | UDP                                                |
| ------------------------------------------- | -------------------------------------------------- |
| Connection-based                            | Connectionless                                     |
| End-to-end                                  |                                                    |
| Full Duplex                                 |                                                    |
| Reliable (Sequence & Acknowledement number) | Unreliable delivery, but enough for stable network |
| Flow control (Window size & sliding)        | No flow control                                    |
| HTTP, FTP, SMTP, Telnet                     | DNS, TFTP, SNMP, RIP                               |
## 3-way handshake
- SEND|RECV SYN
- RECV|SEND SYN
- SEND|RECV ACK

 # Alat Network (Network Devices)
Dipisah menjadi 2:

## Network Devices
- Merupakan alat yang tugasnya mengatur routing paket 
- Router, Access point, Firewall, Hub/Switch, LAN Adapter

## End-User Devices
- Device yang user gunakan / "Terminal Equipment"
- HP, Laptop, PC

# Topologi
Dibedakan menjadi 2:

## Physical
- Koneksi fisik
### Point-to-point (Mesh)
- Setiap node statusnya sama
- Setiap node bebas menginisiasikan komunikasi
- Setiap node memiliki koneksi fisikal
- **Simpel**
- **Koneksi yang memungkinkan terbatas**

### Bus
- Tidak ada node primer/sekunder / status sama
- **Kerusakan satu node tidak memengaruhi network**
- **Software kompleks karena banyak koneksi dari banyak node**

### Star
- Semua node terhubung ke node sentral
- Setiap node statusnya sama
- Setiap koneksi harus melalui node / hub sentral
- **Mudah dimengerti & diimplementasi**
- **Kerusakan hub sentral berarti network *down***

### Ring
- Setiap device terhubung, membentuk sebuah ring
- Setiap node statusnya sama
- Setiap pesan / transmisi diterima setiap komputer, namun hanya destinasi saja yang memproses
- **Kerusakan satu node berarti network *down***
## Logical
- Relasi antara 2 node
### Token passing
- Sebuah token bersirkulasi dalam network. Komputer yang memiliki token dapat mengirim pesan.

### Broadcast
- Setiap device bebas mengirim pesan ke device lain
- Untuk menghindari tabrakan, digunakan *access control*; berbasis *First Come-First Served*

# Network Media
- Layer 1 OSI.
- Dibedakan menjadi 2 tipe, berdasarkan fisik:
	- Guided (Wired): Coaxial, Twisted Pair, Fibre Optic
	- Un-guided (Wireless): Microwave, Sattelite, Infrared, Bluetooth, Radio
- Mengalami gangguan:
	- Attenuation (Melemahnya sinyal)
	- Distortion (Bergantinya sinyal)
	- Noise

## Twisted Pair
- Kabel tembaga diuntai spiral
- Konektor RJ45
- Gampang terganggu oleh noise
- Digunakan dalam LAN
- Terdapat beberapa kategori:
	- 1: Telefon
	- 2. <= 4Mbps
	- 3: <= 10Mbps
	- 4: <= 16Mbps
	- 5: <= 100Mbps
	- 5e:  100Mbps - 1Gbps
	- 6:  1Gbps - 10Gbps
	- 6A: <= 10Gbps
	- 7: >= 10Gbps
- Memiliki variasi shielded & unshielded; konektor RJ45 juga
- **Murah, sederhana, kecepatan tinggi, ada varian shielded**
- **Jarak terbatas dibandingkan fibre dan coax, bandwidth kecil**

## Coaxial
- Tembaga tebal
- Konektor BNC
- Lebih gambang terganggu oleh noise & interference dibandingkan Fibre
- LAN, WAN, MAN
- Bisa analog & digital
- **Lebih tahan interference daripada TP; kecepatan lebih tinggi daripada TP**
- **Butuh alat spesial; berat & besar; diperlukan atenuasi spesial untuk menginsulasi kabel**

## Fibre Optic
- Campuran kaca & plastik dalam cladding & outer layer / sheath
- Kecepatan tinggi
- Analog & digital
- Single & multi mode
- Sumber cahaya bisa *Light Emitting Diode* (LED) dan *Injected Laser Diode* (ILD)
- **Tidak terpengaruh elektromagnetik luar; kecepatan tinggi; semua signal bisa; keamanan data lebih tinggi**
- **Mahal; butuh alat dan keahlian khusus; tidak semua alat bisa**

# Data-Link
- Bekerja dalam layer 2 (Data-link)
	- Paket -> frame
	- Memutuskan mulai & akhir data
	- Memutuskan kapan data dikirim
	- Deteksi eror
	- ***Physical*** addressing

## Layer 2 (Data-Link) & 3 (Network)
Layer 3 ingin mengirim paket. Layer 2 akan mengubah paket tersebut menjadi beberapa frame; Header, Payload, dan Trailer.

Terdapat beberapa istilah dalam translasi layer 3 <-> layer 2:
- **Framing method**; metode menandai awal & akhir sebuah frame
- **Byte count**; header memiliki ukuran setiap frame (dalam byte)
- **Byte stuffing**; menggunakan flag (byte spesial) spesial "ESC" sebagai tanda delimiter awal/akhir frame. Biasa digunakan dalam protokol PPP
- **Bit stuffing**; sama seperti byte, namun dengan pola bit

## Error detection
- Menggunakan *reduntant bit* untuk mengecek keadaan eror
- Eror dapat berupa *single bit* atau *burst error*. Kedua disebabkan oleh noise, interference, atau kerusakan alat
- Pengirim mengecek eror sebelum paket sampai di layer 1, sedangkan penerima mengecek setelah paket datang di layer 1
- Cocok untuk media yang tingkat eror rendah, seperti kabel / wired
- Contoh implementasi:
	- **Parity**; menggunakan parity bit pada akhir frame. Even XOR, odd ~XOR. Deteksi single bit
	- **Checksum**; menggunakan one's complement. Tidak bise mendeteksi insersi / penghapusan bit 0
	- **Cyclic redundancy check**;  

# LAN
- Area kecil
- Koneksi fisik antar-device
- bandwidth tinggi
- dioperasi oleh administrator lokal
- koneksi full time bagi servis lokal (komputer, *Network Interface Card*, device network, *network media*)
- Faktor yang memengaruhi performa LAN:
	- Jarak antar-device
	- Topologi
	- Media
	- Noise

## Ethernet
- Sederhana dan mudah dipakai & dimaintain
- Handal / Reliable
- Kompatibel dengan teknologi baru
- Murah
- Sejarah:
	- 1976: Robert bertemu dengan Calfe di PARC (Palo Alto Research Centre)
	- 1980: Standardisasi pertama oleh DIX
	- 1980: Kecepatan ethernet pertama; 10Mbps jarak 2km menggunakan kabel coax
	- 1985: Standardisasi oleh IEEE (Ethernet 802.3)

### FCS
- Sender hitung checksum dengan input MAC header & payload
- checksum ditambah ke frame sebelum dikirim
- Penerima melakukan perhitungan yang sama
- Jika sama, lanjut frame
- Jika beda, drop frame

### Mode Operasi
- Half-duplex satu arah
- Full-duplex dua arah

## Token Ring
- Data bergerak 1 arah
- Tidak beresiko tabrakan
- Host bisa menggunakan token jika mendapatkan
- Token akan bersirkulasi keseluruh node dalam network
- Menggunakan alamat MAC
- IEEE 802.5
- Manchester encoding
- max data 4472 Byte
- ~4-16 Mbps early, 100 Mbps now
- 1 byte delimiter, access control, ending delimiter

## Fibre Distributed Data Interface
- Ring topology dengan token passing
- 4B5B encoding
- Data max 4500B
- Perbedaan dengan Ethernet:
	- jumlah bit untuk destinasi alamat MAC
	- jumlah informasi initial di alamat MAC: Routing Information Identifier (RII)
	- Urutan transmisi bit
	- ukuran data di setiap frame

## Wireless LAN (WLAN)
- Area geografik spesifik kecil
- Data ditransmit dalam bentuk gelombang radio
- Media udara
- Kecepatan variabel, tergantung standar device
- Menggunakan Access Point untuk relay data antara Wireless Network Interface Card
- Frekuensi tinggi = lebih cepat = lebih terbatas jangkauan
- Faktor:
	- Kekuatan sinyal
	- Jarak
	- Interference
- Cell: area yang dijangkau 1 AP. Menggunakan channel berbeda dengan cell lain

### 802.11a/b/g
- Mobilitas
- Menjangkau area yang tidak bisa dijangkau LAN
- Efektif untuk mengatur network yang sudah ada
- Bisa berkomunikasi dengan LAN
- Meningkatkan performa device yang sudah ada

### Proses intergasi device baru
- **Authentication**; Device wireless mencari device WLAN dengan Service Set IDentifier (SSID)
- **Association**; Proses device join cell

### Tipe otentikasi
- Unauthenticated & Unassociated
- Authenticated & Unassociated
- Authenticated & Associated

### Metode otentikasi
- **Open System**; otentikasi berbasis SSID
- **Shared Key**; Wireless Equivalency Protocol (WEP)

# Carrier Sense Multiple Access / Collission Avoidance (CSMA/CA)
## Distributed Coordination Function (DCF)
- Physical carrier sense method
- stop-and-wait ARQ
- ACK/NAK
- Time period

## Point Coordination Function (PCF)
- RTS (Request To Transmit)
- CTS (Clear To Transmit)
- AP: Controlled-access technique
- masalah hidden: collision
- time lease
- lebih baik dipakai di LAN sibuk

# Structured Cabling
Perkembangan kabel infrastruktur telekomunikasi 

## Komponen
- Jack & Plug moduler
- Wall outlet
- Patch panel; alat manajemen kabel
- Rak
- Label
- Semi-permanent sheath (radius >= 4 * diameter kabel)
- Panel lantai
- Panel dinding
- Penggunaan kabel terpisah antara antar-muka dengan internal

## Teknik Instalasi
- Kabel:
	- terurut
	- diinspek visual
	- Kabel bertensi (tensioned) ketika suspended
	- bundel diikat ketat
	- memiliki radius bend minimum
	- Pemberhentian api sesuai kode
	- Proteksi sekunder dipasang secara series
	- grounding & bonding sesuai kode
	- elektromagnetik:
		- sesuai kode
		- perpisahan minimum 2 inchi
		- 3.9 derajat cross
	- Administrasi:
		- *colour code*
		- labeling
		- dokumentasi


# Network Access Control
## Akses Centralized
- Master (kontroler akses) & slave
- Mode akses:
	- Sirkuit (network seluler): 
		- Device meminta reservasi ke base station
		- base station mengatur channel
		- 1 channel 1 komunikasi
		- Pembuatan tergantung vendor (CDMA, FDMA, TDMA)
		- **Beberapa komunikasi sekaligus; komunikasi tidak saling bertabrakan**
		- **Hidden Terminal; Exposed Terminal**
	- Polling / Packet (FDDI; Token Ring)
		- Turn-based
		- Device bergantian memakai medium
		- **Tidak ada tabrakan**
		- **Delay**
	- Reservation-Based (Sattelite)
		- 2 Timeslot; Reservasi & Data
		- Slave mengirim reservasi ke timeslot reservasi, master menentukan jadwal data timeslot.
		- FPODA, PDAMA
- **Akses network terkontrol; tabrakan minimal; akses berbasis prioritas**
- **Slave menunggu giliran; Delay ketika menunggu; Single point failure**

## Akses decentralized
- Setiap device memiliki akses
- status sama
- mudah tabrakan


### Metode pengurangan tabrakan
- CSMA/CA
	- Wireless Network
	- Device menunggu IFS, kemudian contention (tick down ketika medium tidak dipakai & random), transmit time untuk mengirim pesan
	- Mencegah tabrakan, bukan recover
	- Interframe Spacing (IFS) Time; Contention Time; Transmit Time
- CSMA/CD
	- Ethernet
	- Deteksi tabrakan ketika sinyal medium meningkat
	- Mendeteksi lebih dari satu tabrakan
	- Mengirim data ketika medium tidak dipakai. Jika tabrakan, sinyal jamming dikirim ke semua device. Device yang menerima akan menunggu BACKOFF interval

# WAN
- Area geografik luas
- Part & full time connectivity
- Akses melalui interface serial & beberapa kecepatan
- service seperti email, internet, file transfer, & e-commerce
- Menggunakan provider untuk konek ke network lain
- Modem; Integrated Service Digital Network (ISDN); Frame relay; Digital Subscriber Line (DSL); Asynchronous Transfer Model (ATM)

## Frame Relay
- Shared Environment
- Frame Relay cloud
- Virtual Circuit
- Commited Information Rate (CIR)
- Packet-switched internet-oriented service
- Menggunakan Data frame Link Access Procedure for Frame Relay (LAPFR)
- OSI Layer 2
- Ukuran frame 1600B-4096B
- 6B overhead di FR Data-link protocol untuk start & end of frame
- Minimal end-to-end delay
- Tidak ada error rrecovery
- bandwidth 56Kbps - 44.736Kbps

### Format Frame

| Flags (8B) | Address (16B) | Data | FCS (8B) | Flags (16B) |
| ---------- | ------------- | ---- | -------- | ----------- |
- FR menerima dari layer 3
- Menambahkan Flas, Address, dan FCS pada layer 2
- menutup frame dengan 01111110
- Mengirim frarme ke layer 1

## Switched Virtual Circuit
- Sirkuit virrtual yang diatur dengan mengirim pesan ke network
- Commited Information Rate (CIR): data rate yang disupport oleh SVC
- Maximum Allowed Rate (MAR): data rate maximum SVC
## Flow Control
- Discard Eligible (DE)
	- Frame memiliki prioritas & dapat di drop ketika network penuh
	- Prioritas dilihat dari alamat
- Excess Congestion Network (ECN):
	- Mekanisme deteksi network penuh (congestion)
	- Forward ECN
		- Jumlah frame yang didrop karena congestion pada network tujuan
	- Backward ECN
		- FECN namun network pengirim

## ATM
- Cell
- Virtual Path Identifier / Virtual Channel Identifier (VPI/VCI)

|         Voice          |              Data              |
| :--------------------: | :----------------------------: |
|       Small size       |           large size           |
|     Prevents echo      |       max throughoutput        |
| minimal delay & jitter | affected by number of stations |

- VPI; VC for transmitting cells across networks
- VCI: VC identifier for transmitting cells
- VPI/VCI assigned by ATM switch to each cell that enters the network; changes everytime the cell passes a switch
