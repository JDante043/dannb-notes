- Tugas switch adalah membagi suatu network menjadi beberapa Collision Domain
	- Arti Collision Domain ialah segmen network di mana device-device dalam network itu dapat bertabrakan. Bayangkan switch dalam laboratorium komputer sebuah kampus. Setiap ruangan dapat 1 switch. Maka, ruangan A dengan ruangan B adalah 2 collision domain yang berbeda karena komputer A1 dengan B1 paketnya tidak mungkin bertabrakan, namun A1 dengan A2 dapat bertabrakan
	- Switch berperan untuk mengurangi kemungkinan collision dalam domain yang dia atur, yang artinya network lebih efisien.
	- Switch dapat mengatur beberapa koneksi sekaligus dan mengisolasi satu koneksi dengan koneksi lain.
	- Switch merupakan "konektor", sehingga dia tidak bisa memberikan limit bandwidth kepada suatu device

| Layer 2 Switching                                       | Layer 3 Switching       |
| ------------------------------------------------------- | ----------------------- |
| Menggunakan MAC Address                                 | Menggunakan IP Address  |
| Membagi suatu network menjadi beberapa collision domain |                         |
| Menggunakan satu broadcast domain                       |                         |
| Switch & Bridge                                         | Router & Layer 3 switch |

# Lan Segmentation
- Proses pembagian suatu LAN menjadi beberapa segmen
- Setiap segmen merupakan satu collision domain
- Mengurangi kemungkinan collision karena network dibagi menjadi lebih kecil
- Karena collision terkurangi, maka bandwidth, efisiensi, dan performa network meningkat

<figure>
	<img src="College/Semester 3/Komunikasi Data/Pertemuan 11/Resource/LAN Segmentation small.png">
	<figcaption style="text-align: center;">Pembagian LAN oleh 1 switch</figcaption>
</figure>
<figure>
	<img src="College/Semester 3/Komunikasi Data/Pertemuan 11/Resource/LAN Segmentation medium.png">
	<figcaption style="text-align: center;">Pembagian LAN oleh beberapa switch</figcaption>
</figure>
# Kombinasi
## Switch & Hub
> Hub adalah suatu hardware yang mem-broadcast semua data yang diterima kepada setiap port
- Hub lebih murah
- Meningkatkan efisiensi & performa
- Masih berada dalam satu collision domain

## Switch & Router
- Memungkinkan integrasi beberapa network
- Dapat membatasi broadcast traffic
- Membagi network menjadi beberapa broadcast domain

# Content Address Memory (CAM)
- Sebuah memory dalam switch
- Menyimpan MAC address device yang terkoneksi
- Switch menggunakan CAM untuk menentukan port mana untuk mengirim sebuah paket

