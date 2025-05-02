# 📄 Dokumen Perencanaan Proyek  
## Pekan 9 Perencanaan Proyek & Desain Awal

### Tugas Kelompok :
1. Pembentukan Kelompok dan pembagian peran.
2. Analisis Kebutuhan jaringan PT. Nusantara Network.
3. Brainstorming desain jaringan awal.

---

### 👥 Daftar Anggota dan Peran

| Nama Anggota     | NIM        | Peran                                        |
|------------------|------------|--------------------------------------------- |
| Az-Zahra Atikah Nurhaliza | 10231022 | Network Architect |
|Chintya | 10221078 | Network Engineer |
| Djaky Abbyyu Fauzan | 10231032 | Network Services Specialist |
| Djaky Abbyyu Fauzan | 10231032 | Network Security & Documentation Specialist |

---

### 📌 Analisis Kebutuhan Jaringan
Untuk mendukung operasional PT. Nusantara Network yang terdiri dari dua lokasi (Kantor Pusat dan Kantor Cabang) serta 6 departemen, maka jaringan komputer harus mampu melayani:

- **Kantor Pusat (Gedung A)**:
  - Departemen IT: 40 komputer
  - Departemen Keuangan: 25 komputer
  - Departemen SDM: 20 komputer
  - Server Farm: 10 server

- **Kantor Cabang (Gedung B)**:
  - Departemen Marketing: 30 komputer
  - Departemen Operasional: 35 komputer

- Setiap departemen berada dalam VLAN yang terpisah untuk keamanan dan manajemen traffic.
- Koneksi antar gedung menggunakan teknologi WAN dengan bandwidth terbatas.
- Implementasi NAT untuk akses internet melalui ISP.
- Layanan DHCP untuk alokasi IP otomatis di setiap departemen.
- Layanan DNS untuk resolusi nama internal dan eksternal.
- Access Control List (ACL) untuk membatasi akses antar departemen.
- Routing dinamis menggunakan OSPF.
- Monitoring dan manajemen jaringan terpusat.

---

#### Perangkat yang dibutuhkan 

| Perangkat         | Jumlah         | Keterangan                                     |
|-------------------|----------------|------------------------------------------------|
| Router            | 2              | 1 di kantor pusat dan 1 di kantor cabang       |
| Switch            | 6–10           | 1–2 per departemen tergantung jumlah komputer  |
| Komputer Client   | 150            | Total seluruh komputer dari 6 departemen       |
| Server            | 10             | Untuk layanan internal dan eksternal           |
| Printer Jaringan  | 2–4            | 1 per gedung atau per 2 departemen             |
| Kabel LAN         | ±160           | Disesuaikan dengan jumlah perangkat dan ruangan|

---

### 📆 Timeline Rencana kerja 7 Pekan

| Pekan | Kegiatan                                             |
|-------|-----------------------------------------------------|
| 9 | Diskusi Kelompok, Pembagian Jobdesk & Perencanaan Proyek & Desain Awal |
| 10| Desain Topologi & Skema Pengalamatan |
| 11| Implementasi Topologi Dasar & VLAN |
| 12| Implementasi Routing & WAN |
| 13| Implementasi Layanan Jaringan |
| 14| Implementasi Keamanan & Pengujian |
| 15| Finalisasi Dokumentasi & Presentasi |

---

### Sketsa Awal Desain Jaringan
Berikut adalah Sketsa awal topologi jaringan yang digunakan.

<img src="Topologi Pekan 9.png" alt="" width="300"/>



Penjelasan Topologi Jaringan PT. Nusantara Network
Desain topologi jaringan PT. Nusantara Network dibagi menjadi dua bagian utama, yaitu Gedung A dan Gedung B. Masing-masing gedung memiliki beberapa departemen yang terhubung menggunakan switch Layer 2 (L2) dan switch Layer 3 (L3) untuk pengelolaan lalu lintas data secara efisien.

Di Gedung A, terdapat empat departemen: IT, Keuangan, SDM, dan Server Farm.

Departemen IT memiliki 40 PC yang terhubung melalui Switch L2 – IT.

Departemen Keuangan memiliki 25 PC dan satu Printer 1, semuanya terhubung melalui Switch L2 – Keuangan.

Departemen SDM memiliki 20 PC yang terhubung melalui Switch L2 – SDM.

Server Farm terdiri dari 10 server yang dikelola melalui Switch L2 – Server Farm.
Semua switch L2 pada gedung ini terhubung ke Switch L3 - Core, yang kemudian terhubung ke Router Gedung A sebagai pintu gerbang keluar jaringan gedung.

Sementara itu, di Gedung B terdapat dua departemen: Marketing dan Operasional.

Departemen Marketing memiliki 30 PC yang terkoneksi dengan Switch L2 – Marketing.

Departemen Operasional memiliki 35 PC dan Printer 2, semua terhubung melalui Switch L2 – Operasional.
Keduanya terhubung ke Switch L3 yang selanjutnya tersambung ke Router Gedung B.

Router Gedung A dan Router Gedung B memungkinkan kedua gedung saling terhubung dan bertukar data. Dengan struktur ini, jaringan antar departemen maupun antar gedung bisa berjalan dengan baik, aman, dan terorganisir.
