**Nama:** Ananda Dwi Rizkyta  
**NIM:** 20210801197  
**Universitas:** Universitas Esa Unggul  
**Mata Kuliah:** UTS Jaringan Komputer Lanjut

# Konfigurasi Topologi Jaringan Menggunakan RIP

## Penjelasan Topologi

### Komponen Utama

- **3 Router:**
  - `R1 KHI`
  - `R2 KJ`
  - `R3 CR`
- **3 PC** yang terhubung pada setiap router dengan subnet berbeda:
  - PC dengan subnet `192.168.10.1/24` terhubung ke `R1 KHI`
  - PC dengan subnet `192.168.20.1/24` terhubung ke `R2 KJ`
  - PC dengan subnet `192.168.30.1/24` terhubung ke `R3 CR`

### Subnet dan Interface

- **Router R1 KHI**
  - **Ethernet 2:** Terhubung ke PC dengan subnet `192.168.10.1/24`
  - **Ethernet 3:** Terhubung ke jaringan `15.15.15.1`, menghubungkan ke `R3 CR`
  - **Ethernet 4:** Terhubung ke jaringan `14.14.14.1`, menghubungkan ke `R2 KJ`
- **Router R2 KJ**
  - **Ethernet 2:** Terhubung ke PC dengan subnet `192.168.20.1/24`
  - **Ethernet 3:** Terhubung ke jaringan `13.13.13.1`, menghubungkan ke `R3 CR`
  - **Ethernet 4:** Terhubung ke jaringan `14.14.14.2`, menghubungkan ke `R1 KHI`
- **Router R3 CR**
  - **Ethernet 2:** Terhubung ke PC dengan subnet `192.168.30.1/24`
  - **Ethernet 3:** Terhubung ke jaringan `13.13.13.2`, menghubungkan ke `R2 KJ`
  - **Ethernet 4:** Terhubung ke jaringan `15.15.15.2`, menghubungkan ke `R1 KHI`

### Jaringan Antar-Router

- **Jaringan `15.15.15.0/24`:** Menghubungkan `R1 KHI` dan `R3 CR`
- **Jaringan `14.14.14.0/24`:** Menghubungkan `R1 KHI` dan `R2 KJ`
- **Jaringan `13.13.13.0/24`:** Menghubungkan `R2 KJ` dan `R3 CR`
