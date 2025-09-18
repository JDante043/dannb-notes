# OSI
Open Systems Interconnection adalah sebuah standar / framework dari ISO (International Organization for standardization). Framework ini membagi komunikasi network menjadi 7 layer / lapis dengan tujuan sebagai standar cara sistem antar network berkomunikasi.

Setiap layer adalah kategori yang memuat standar-standar:

| Nama         | Standar              | Deskripsi                                                                                    |
| ------------ | -------------------- | -------------------------------------------------------------------------------------------- |
| Physical     | cat 5e, RS232        | Standar dari data-link                                                                       |
| Data-link    | Ethernet, PPP        | Cara pengiriman dan penerimaan data                                                          |
| Network      | IP, ICMP, IGMP       | Menangani address penerima dan pengirim                                                      |
| Transport    | TCP, UDP             | Cara paket dari session dikirim. Memuat alamat / address pengirim dan penerima               |
| Session      | HTTP, FTP, IMAP, SSH | Menghubungkan sistem dengan network lain. Membuat dan mengirim packet ke sistem lain.        |
| Presentation | NCP, NDR             | Menghubungkan session dengan aplikasi. Melakukan enkripsi & dekripsi, kompresi & dekompresi. |
| Application  | SDP, NetBIOS         | Protokol untuk aplikasi user                                                                 |

## Kenapa menjadi layer?
- Memvisualisasikan layer network agar lebih mudah dipelajari
- Mempermudah manajemen dan *troubleshooting*
- Menggambarkan *data flow* secara jelas
- Mencegah perubahan pada satu layer memengaruhi layer lain
- Mempermudah hardware dan software berbeda berkomunikasi satu sama lain
