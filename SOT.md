# SOT — ArenaBook
## 1. Ringkasan produk
ArenaBook adalah front-end sistem informasi untuk pemesanan lapangan futsal dan bulu tangkis pada satu pengelola/lokasi. Fokus iterasi pertama adalah UI modern, responsif, dan alur booking menggunakan data dummy. Sistem bukan marketplace multi-venue.

## 2. Tujuan
- Membantu pelanggan melihat informasi lapangan, memilih slot, membuat booking, dan memahami status pembayaran.
- Membantu admin mengelola lapangan, jadwal, booking, serta ringkasan transaksi.
- Menyiapkan batas arsitektur yang jelas untuk integrasi backend dan payment gateway pada tahap berikutnya.

## 3. Pengguna dan hak akses
### Pelanggan
- Melihat informasi lapangan dan harga.
- Memeriksa ketersediaan jadwal.
- Membuat booking simulasi.
- Melihat riwayat dan status booking miliknya.
- Melihat instruksi pembayaran simulasi.

### Admin/Pengelola
- Melihat ringkasan operasional.
- Mengelola data lapangan, tarif, jam operasional, dan jadwal.
- Melihat seluruh booking dan status pembayaran.
- Melihat laporan booking/transaksi berdasarkan periode.

## 4. Modul
1. Registrasi & login (UI demo).
2. Informasi lapangan.
3. Jadwal & ketersediaan.
4. Booking online.
5. Pembayaran payment gateway (UI simulasi, bukan transaksi nyata).
6. Riwayat & status booking.
7. Dashboard admin.
8. Laporan booking & transaksi.

## 5. Aturan bisnis
- Booking harus memiliki lapangan, tanggal, slot, durasi, tarif, dan pelanggan.
- Total biaya = tarif per jam × durasi.
- Slot yang telah dipesan tidak boleh dipilih untuk booking lain.
- Status booking yang digunakan: Menunggu Pembayaran, Terkonfirmasi, Dibatalkan.
- Status pembayaran: Tertunda, Berhasil, Gagal.
- Pada integrasi nyata, status pembayaran hanya boleh berubah setelah verifikasi server-to-server/webhook dari penyedia payment gateway. Redirect kembali ke website tidak cukup.
- Pembatalan/refund mengikuti aturan yang ditetapkan pengelola; tidak disimulasikan sebagai refund sungguhan pada prototype.
- Data yang ditampilkan saat ini adalah data dummy dan tidak disimpan ke database.

## 6. Prioritas ruang lingkup
### Wajib untuk prototype UI
- Navigasi pelanggan/admin.
- Kartu lapangan futsal dan badminton.
- Filter tanggal/jenis lapangan serta slot jadwal.
- Modal/form booking dengan hitung total biaya.
- Riwayat booking dengan status.
- Dashboard admin dan ringkasan transaksi.
- Laporan ringkas dengan filter sederhana.
- Responsive layout untuk desktop dan layar kecil.

### Di luar ruang lingkup iterasi ini
- Backend/API dan database.
- Login/otorisasi nyata.
- Payment gateway sungguhan, webhook, refund.
- WhatsApp/email notification.
- Produksi/deployment dan pengelolaan rahasia/API key.

## 7. Arah UI/UX
- Brand: ArenaBook.
- Visual: modern SaaS, sporty-futuristic, bersih, fokus keterbacaan.
- Warna: midnight navy (#0B1220), electric blue (#3B82F6), cyan (#22D3EE), lime accent (#A3E635), slate neutrals.
- Tipografi: system sans-serif; hierarchy jelas.
- Layout: sidebar desktop, top bar, cards, status pills, tables, modal booking.
- Interaksi: navigasi tab, filter, buka/tutup modal, pemilihan slot, simulasi pembuatan booking.
- Hindari gradient berlebihan, animasi dekoratif, dan komponen yang tidak relevan.

## 8. Kriteria penerimaan
- `npm install` dan `npm run dev` menjalankan aplikasi.
- Tidak membutuhkan API key atau backend.
- UI menunjukkan semua modul utama dengan data dummy.
- User dapat memilih lapangan dan slot, membuka modal, dan menambahkan booking demo.
- Slot yang telah dipakai tidak ditawarkan sebagai slot tersedia.
- Status transaksi secara eksplisit ditandai sebagai simulasi.
- Tampilan responsif dan konsisten dengan brand.
