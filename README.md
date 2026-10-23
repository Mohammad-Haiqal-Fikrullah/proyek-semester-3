# ArenaBook — Sistem Informasi Booking Lapangan Olahraga Berbasis Web

Prototype front-end SaaS modern untuk **Sistem Informasi Booking Lapangan Olahraga Berbasis Web dengan Payment Gateway** sesuai spesifikasi produk `SOT.md` dan panduan kontrak `AGENTS.md`.

---

## 🚀 Teknologi yang Digunakan
- **Framework & Bundler:** React (Function Components & Hooks) + Vite
- **Styling:** Tailwind CSS (Modern sporty-futuristic palette: Midnight Navy, Electric Blue, Cyan, Lime Accent)
- **Icons:** Lucide React
- **Lokalisasi:** Format Rupiah (`id-ID`) dan Tanggal Indonesia

---

## 📦 8 Modul SOT yang Telah Diimplementasikan

1. **Registrasi & Login (UI Demo)**
   - Modal beralih akun demo instan antara Pelanggan (*Haiqal Pratama*, *Nadia Putri*) dan Admin (*Admin Arena Panggulaan*).
   - Form pendaftaran demo pengguna baru dengan validasi lokal.

2. **Informasi Lapangan**
   - Katalog lapangan resmi: **Ben Stadium** (Futsal) dan **Lapangan Bulu Tangkis Panggulaan** (Badminton).
   - Modal detail spesifikasi teknis (material lantai BWF/FIFA grade, pencahayaan LED, dimensi, fasilitas lengkap, dan tata tertib).

3. **Jadwal & Ketersediaan**
   - Matriks slot operasional 08:00 – 22:00 WIB per tanggal.
   - Pembedaan status visual yang jelas: Slot Tersedia (hijau) vs Slot Terisi (abu-abu/disabled).
   - Klik langsung pada slot hijau untuk membuka formulir booking dengan jam terpilih otomatis.

4. **Booking Online**
   - Formulir booking interaktif: tanggal, jam mulai, durasi (1, 2, 3 jam).
   - **Smart Collision Detection**: Pemeriksaan otomatis agar durasi sewa berturut-turut tidak bertabrakan dengan jadwal yang sudah dipesan orang lain.
   - Perhitungan biaya transparan: `Tarif × Durasi = Subtotal`, biaya admin Rp 0, total tagihan.
   - Pemilihan kanal pembayaran (QRIS, BCA VA, Mandiri VA, GoPay).

5. **Pembayaran Payment Gateway (UI Simulasi)**
   - Simulator antarmuka payment gateway (*ArenaPay Sandbox Simulator*).
   - Hitung mundur batas waktu bayar (15 menit).
   - Mode QRIS: Tampilan QR Code SVG tajam & NMID.
   - Mode Virtual Account: Nomor VA dummy dengan tombol salin (copy to clipboard).
   - Tombol simulasi interaktif:
     - ⚡ **"Simulasikan Bayar Berhasil"** (memicu simulasi webhook, mengubah status menjadi `Berhasil` & `Terkonfirmasi`).
     - ❌ **"Simulasikan Bayar Gagal"** (mengubah status menjadi `Gagal` & `Dibatalkan`).
     - 🕒 **"Bayar Nanti"** (status tetap `Menunggu Pembayaran` di riwayat).

6. **Riwayat & Status Booking**
   - Pencarian instan (kode booking, nama, lapangan) dan filter status (*Semua*, *Terkonfirmasi*, *Menunggu Pembayaran*, *Dibatalkan*).
   - Aksi kontekstual: Tombol *"Bayar Sekarang"* untuk pesanan tertunda, tombol *"Lihat E-Tiket"* untuk pesanan lunas, dan tombol pembatalan.
   - Modal E-Tiket / Digital Pass resmi dengan QR Code check-in venue dan tombol cetak/unduh.

7. **Dashboard Admin**
   - KPI operasional real-time: Total Pemesanan, Booking Terkonfirmasi, Menunggu Pembayaran, dan Total Pemasukan.
   - Kontrol lapangan: Ubah status operasional (*Tersedia* vs *Pemeliharaan*) dan ubah tarif sewa.
   - Tabel reservasi pelanggan lengkap dengan fitur *"Konfirmasi Kasir"* (bayar tunai di tempat) dan pembatalan manual.

8. **Laporan Booking & Transaksi**
   - Filter periode audit: Hari ini, 7 hari terakhir, 30 hari terakhir, Bulan ini, Semua periode demo.
   - Visualisasi grafik batang pendapatan riil.
   - Distribusi metode pembayaran (QRIS, VA, E-Wallet) dan okupansi lapangan (Futsal vs Badminton).
   - Rekapitulasi tabel transaksi keuangan dengan total omzet yang hanya menjumlahkan transaksi `Berhasil` sesuai aturan bisnis SOT.

---

## 🛠️ Cara Menjalankan

### 1. Instalasi Dependensi
```bash
npm install
```
*(Catatan Windows: Jika PowerShell memblokir script execution, gunakan `npm.cmd install`)*

### 2. Jalankan Server Development
```bash
npm run dev
```
Buka browser di URL: **http://localhost:5173/**

### 3. Build Produksi
```bash
npm run build
```

---

## ⚠️ Batasan Demo & Catatan Akademik
- Seluruh data booking, pengguna, dan transaksi disimpan pada **state React lokal** (in-memory) dan tidak disimpan ke database permanen.
- Tidak ada integrasi API key atau penagihan uang nyata. Semua pembayaran merupakan simulasi antarmuka.
- Pada sistem produksi tahap berikutnya, konfirmasi pembayaran sesungguhnya wajib menggunakan **verifikasi server-to-server webhook** bertanda tangan kriptografis dari payment gateway resmi (seperti Midtrans atau Xendit).
