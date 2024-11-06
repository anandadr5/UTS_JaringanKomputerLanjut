### Nama : Ananda Dwi Rizkyta

### NIM : 20210801197

### Mata Kuliah : Jaringan Komputer Lanjut

### Kode Mata Kuliah : CIE722

# ESSAY

## 1. Jelaskan menurut anda apa itu Routing Static?

Menurut saya, Routing statik adalah metode routing di mana jalur jaringan diatur secara manual oleh administrator dan tidak berubah otomatis. Rute ini tetap stabil kecuali diubah secara manual, sehingga cocok untuk jaringan kecil atau topologi yang jarang berubah. Routing statik membutuhkan sedikit sumber daya tetapi kurang fleksibel dibandingkan routing dinamis, yang dapat menyesuaikan jalur sesuai kondisi jaringan.

## 2. Jelaskan menurut anda apa itu Routing Dynamic?

Menurut saya, Routing dinamis adalah metode di mana perangkat jaringan, seperti router, otomatis menentukan dan memperbarui jalur terbaik berdasarkan kondisi jaringan yang berubah. Menggunakan protokol seperti OSPF atau RIP, routing dinamis memungkinkan perangkat bertukar informasi dan menyesuaikan jalur tanpa intervensi manual. Meskipun memerlukan lebih banyak sumber daya, routing dinamis ideal untuk jaringan besar dan kompleks karena memberikan fleksibilitas dan efisiensi dalam pengelolaan lalu lintas.

## 3. Jelaskan menurut anda apa itu Firewall?

Menurut saya, Firewall adalah sistem keamanan jaringan yang mengontrol lalu lintas masuk dan keluar berdasarkan aturan tertentu, melindungi jaringan internal dari ancaman eksternal. Beroperasi sebagai perangkat keras, perangkat lunak, atau kombinasi keduanya, firewall menganalisis paket data untuk memutuskan apakah diizinkan masuk atau keluar. Firewall mencegah akses tidak sah, serangan malware, dan pencurian data, menjadikannya komponen penting dalam keamanan jaringan.

## 4. Jelaskan menurut anda apa itu NAT?

Menurut saya, Network Address Translation (NAT) adalah teknik untuk mengubah alamat IP pada paket data yang melewati router, menyembunyikan alamat IP internal dari jaringan eksternal. NAT memungkinkan banyak perangkat di jaringan lokal menggunakan satu alamat IP publik untuk mengakses internet, menghemat alamat IP publik dan meningkatkan keamanan jaringan dengan menyembunyikan topologi internal.

# CASED

# TOPOLOGI

![Topologi Jaringan Komputer_20210801197_Ananda Dwi Rizkyta](https://github.com/user-attachments/assets/7c9c410e-bd6c-4a35-a96c-839b9a4c43ab)

1. Router di Setiap Kampus: Setiap kampus memiliki satu router yang terhubung ke internet melalui koneksi Ethernet (Eth1) dan ke jaringan lokal melalui Ethernet (Eth2).

- R1 CR: Router di Kampus CR dengan IP jaringan lokal 192.168.1.0/24.
- R2 KJ: Router di Kampus KJ dengan IP jaringan lokal 192.168.20.0/24.
- R3 KHI: Router di Kampus KHI dengan IP jaringan lokal 192.168.30.0/24.

2. Koneksi Internet: Setiap router memiliki akses ke internet melalui alamat IP publik dari masing-masing kampus:

- Kampus CR: 198.51.100.10/24
- Kampus KJ: 198.51.100.11/24
- Kampus KHI: 198.51.100.12/24

3. IPIP Tunnel: Untuk menghubungkan ketiga kampus, digunakan IPIP Tunnel dengan rentang IP 10.0.1.0/24. Berikut konfigurasinya:

- R1 CR - R2 KJ: IPIP Tunnel menggunakan 10.0.1.1/24 di R1 CR dan 10.0.1.2/24 di R2 KJ.
- R2 KJ - R3 KHI: IPIP Tunnel menggunakan 10.0.2.1/24 di R2 KJ dan 10.0.2.3/24 di R3 KHI.

4. Switch dan PC: Setiap kampus memiliki satu switch yang menghubungkan beberapa PC di jaringan lokal:

- Kampus CR: Switch dengan alamat jaringan 192.168.1.0/24.
- Kampus KJ: Switch dengan alamat jaringan 192.168.20.0/24.
- Kampus KHI: Switch dengan alamat jaringan 192.168.30.0/24.

5. R2 KJ sebagai Hub Sentral: Router di Kampus KJ (R2 KJ) berfungsi sebagai hub sentral untuk menghubungkan ketiga kampus. Semua lalu lintas data dari dan ke Kampus CR dan KHI melewati R2 KJ sebagai penghubung utama.
