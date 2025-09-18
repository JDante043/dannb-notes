Network device adalah perangkat yang menghubungkan user dengan internet, beserta dengan perangkat pembantu.

# Network Device
Merupakan perangkat yang perannya khusus untuk meng-handle *traffic* network.

Contoh:
- NIC/LAN Adapter
- Hub / Switch
- Router
- Access Point
- Firewall
# End-User Device
User dan aplikasi user berinteraksi dengan device ini.

Contoh:
- Komputer / PC / Laptop
- HP

# Topologi
Merupakan struktur sebuah network
## Fisikal
Gambaran / struktur transmisi data dalam sebuah network

Contoh:
- P2P (Point to point) Mesh
Setiap node terhubung langsung dengan node lain, memiliki status yang sama, dan dapat menginisiasikan komunikasi. Simpel, namun rumit jika koneksi banyak.

- Bus
Suatu kabel menghubungkan semua node. Setiap node memiliki status yang sama. Tidak bergantung pada suatu server (jika satu rusak, network aman), namun bergantung pada kabel bus.

- Extended Star
Setiap node terhubung ke suatu hub. Setiap paket data akan melalui hub. Gampang dan simpel untuk di implementasikan; namun jika hub rusak, maka network down.

- Ring
Setiap node terhubung menjadi sebuah lingkaran. Semua device adalah penerima, namun hanya device tujuan paket yang memproses data tersebut; device lain menolak paket tersebut. Kerusakan satu device akan menyebabkan network down.

## Logika
Gambaran / struktur relasi antar node dalam sebuah network

Contoh:
- Broadcast
Bisa di topologi mesh, bus, dan hub.
First come first serve; Bisa bertabrakan jika 2 device broadcast sekaligus.
Bisa menggunakan akses kontrol agar hanya 1 device yang bisa broadcast

- Token passing
Misal di topologi ring; akan ada token yang mengelilingi setiap node.
Jika sebuah node ingin mengirim pesan, dia harus menunggu token sampai ke dia terlebih dahulu.