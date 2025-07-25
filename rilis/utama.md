<title>Catatan rilis sistem dan situs web | Cara Simera</title>

[Beranda](..) &raquo; [Catatan rilis](.) &raquo; 
# Sistem dan situs web (Terbaru)

> **Daftar isi**
> 
> - [22 Juli 2025](#22-juli-2025)
> - [14 Juli 2025](#14-juli-2025)
> - [8 Juli 2025](#8-juli-2025)
> - [1 Juli 2025](#1-juli-2025)
> - [Yang lebih lama](#yang-lebih-lama)
> - [Informasi lebih lanjut](#informasi-lebih-lanjut)

---

## 22 Juli 2025

|           | Sistem  | Situs web |
| --------- |:-------:|:---------:|
| **Versi** |`0bff0ba`|`deecfa3`  |

### Perubahan

**Peningkatan fitur:**
1. Optimasi kueri dan koneksi DB di siapkan kode pintu versi generate (prosesnya akan semakin cepat)
2. Optimasi kueri dan koneksi DB di siapkan kode pintu versi inject (belum termasuk progress bar di frontend)
3. Opsi 'Timpa' juga tersedia di siapkan kode pintu versi generate (sebelumnya hanya ada di versi inject)
4. Perubahan nama menu: Batas penjualan -> Ketersediaan
5. Perubahan ikon (kamera, kartu, lampiran, dsb) dari simbol/emoji ke SVG, agar tampilannya seragam di semua perangkat
6. [Situs web] Hapus link ke penjualan di header

_Tidak ada halaman baru dan perbaikan bug di rilis ini._

### Tangkapan layar

- _Peningkatan fitur #3 dan #4_
  <br>![gambar](aset/image-25.png)

---

## 14 Juli 2025

|           | Sistem  | Situs web |
| --------- |:-------:|:---------:|
| **Versi** |`bc0a44f`|`d055544`  |

### Perubahan

**Halaman baru:**
1. Halaman beranda
   
   Pengganti halaman pilih acara. Di sini akan terlihat berapa acara yang dimiliki tiap penyelenggara. Ada filter juga, cari acara yang lama lebih gampang.

**Peningkatan fitur:**
1. Revamp menu (lanjutan)
   
   Menu kategori Kelola sekarang muncul di halaman beranda. Akses kelola pengguna lebih gampang, tidak perlu pindah ke kelola acara dulu, langsung bisa diklik dari depan.
2. Metode baru di siapkan kode pintu versi generate
   
   Perubahan metode kirim form data untuk mengatasi "Request Time Out" saat siapkan kode pintu: dari single request single response (saat banyak yang disiapkan, requestnya membesar dan server tak punya cukup waktu nuntuk proses) menjadi multiple request multiple response di mana requestnya dipecah kecil-kecil. Harapannya setiap requestnya tidak perlu waktu lama, dan tidak RTO lagi. Sekarang ada progress barnya juga.
3. Muat ulang peran dan hak akses di kelola akun
   
   Saat ada perubahan role atau penambahan menu baru, sekarang bisa buka halaman kelola akun dari kanan atas. Tidak harus logout dan login lagi.

_Tidak ada perbaikan bug di rilis ini._

### Tangkapan layar

- _Halaman baru #1 dan Peningkatan fitur #1_
  <br>![gambar](aset/image-23.png)
- _Peningkatan fitur #2_
  <br>![gambar](aset/image-24.png)

---

## 8 Juli 2025

|           | Sistem  | Situs web |
| --------- |:-------:|:---------:|
| **Versi** |`6902d42`|`d055544`  |

### Perubahan

**Peningkatan fitur:**
1. Revamp menu (lanjutan)
   
   Header kini sebaris saja, lebih banyak ruang untuk konten utama. Di sini terlihat ID pengguna yang login. Nama dan perannya juga selalu muncul (sebelumnya hanya ada di versi desktop, di versi mobile hanya ada link logout). Ada juga link ke aplikasi domain simera yang lain, tidak perlu lagi bookmark manual.
2. Bisa paksa pakai keluar di daftar lengkap kode pintu
   
   Ini bisa dipakai untuk satu kode yang bisa dipakai berhari-hari, tapi saat akhir hari tidak mau di pakai keluar satu-satu (meskipun saat beli bundling dapatnya hanya satu kode, bukan sesuai jumlah harinya).
   
   Di daftar lengkap kode pintu, pilih kategorinya, pilih tampilkan yang sudah dipakai, nanti muncul tombolnya di bawah.

**Perbaikan bug:**
1. Pakai masuk/pakai keluar/tukar terkadang bakal terus "Gagal diperiksa" setelah integrasi mobile app (misal saat buka tab baru lalu ganti acara, atau sesinya habis). Seharusnya diredirect dan muncul error message, seperti dulu sebelum integrasi mobile app.
2. Terjemahan bahasa Inggris yang hilang untuk judul menu Batas penjualan.
3. Unhandled case di mana pengguna sistem klik "Lihat log" di cetak rincian pesanan, tapi pelanggan belum pernah buka e-vouchernya.

_Tidak ada halaman baru di rilis ini._

### Tangkapan layar

- _Peningkatan fitur #1 - Sebelum_
  <br>![gambar](aset/image-20.png)
- _Peningkatan fitur #1 - Sesudah_
  <br>![gambar](aset/image-21.png)
- _Peningkatan fitur #2_
  <br>![gambar](aset/image-22.png)

---

## 1 Juli 2025

|           | Sistem  | Situs web |
| --------- |:-------:|:---------:|
| **Versi** |`2ec2770`|`d055544`  |

### Perubahan

**Peningkatan fitur:**
1. Revamp menu
   
   Menu kini dibedakan antara sebelum dan setelah pilih acara agar lebih ringan. Masih Work in Progress, sehingga saat mau buka menu kategori "Kelola" harus sebelum pilih acara, klik "Kelola acara" di depan, nanti menunya muncul di kiri. Kalau sudah terlanjur pilih acara, bisa klik logo Simera di kiri atas untuk balik ke depan.
2. Bisa hapus pesanan di hapus data
   
   Catatan: pesanan dan kode pintu disimpan di tabel terpisah. Hapus kode pintu tidak akan langsung menghapus pesanan (karena belum tentu kodenya diterbitkan dari menu pesanan), begitu juga sebaliknya (karena belum tentu pesanannya sudah paid/issued). Jika ada keduanya, silakan dihapus satu per satu.

_Tidak ada halaman baru dan perbaikan bug di rilis ini._

### Tangkapan layar

- _Peningkatan fitur #2_
  <br>![gambar](aset/image-19.png)

---

## Yang lebih lama

- [2025 H1](./utama_2025H1)

---

## Informasi lebih lanjut

Silakan buka diskusi di grup "System Update", atau hubungi William Surya Permana.

---

_Akhir dari dokumen_ &#x7C; [Kembali ke atas](#)