# AGENTS.md — Kontrak Kerja Proyek ArenaBook

## Misi
Bangun dan rawat front-end **Sistem Informasi Booking Lapangan Olahraga Berbasis Web dengan Payment Gateway** menggunakan React + Vite + Tailwind CSS. Fokus pada antarmuka dan interaksi front-end dengan data dummy sampai pemilik proyek secara eksplisit menyetujui tahap backend.

## Sumber kebenaran
1. `SOT.md` adalah spesifikasi produk utama.
2. `PROMPT_EXECUTION.md` adalah prompt eksekusi awal.
3. Jika instruksi bertentangan, pertahankan ruang lingkup SOT dan tanyakan sebelum memperluasnya.

## Batasan wajib
- Jangan menambahkan fitur di luar SOT.
- Jangan mengintegrasikan layanan/backend/payment sungguhan pada tahap front-end.
- Jangan menyimpan API key, kredensial, atau data pribadi nyata.
- Jangan mengklaim pembayaran berhasil secara nyata; semua pembayaran pada prototype adalah simulasi.
- Jangan menganggap redirect browser sebagai bukti pembayaran. Untuk integrasi nyata, perlu verifikasi backend dan webhook resmi.
- Gunakan data dummy yang jelas, nama lapangan futsal dan bulu tangkis, serta satu pengelola/lokasi.
- Jangan mengubah konsep menjadi marketplace multi-venue.
- Hindari menambahkan dependency tanpa kebutuhan yang jelas.
- Jaga kode mudah dipahami mahasiswa, komponen cukup kecil, dan penamaan konsisten.

## Standar implementasi
- React function components dan hooks.
- Vite untuk development/build.
- Tailwind CSS untuk styling.
- UI responsif, accessible, label form jelas, tombol memiliki fungsi.
- Data demo dipisahkan dari komponen jika mulai kompleks.
- Hindari `any`-style implicit assumptions; validasi input dasar.
- Format tanggal dan Rupiah menggunakan locale `id-ID`.
- Jangan membuat klaim keamanan atau integrasi yang belum diterapkan.

## Alur kerja agen
1. Baca `SOT.md` dan `README.md`.
2. Periksa struktur proyek dan dependency yang tersedia.
3. Buat rencana singkat sebelum perubahan besar.
4. Implementasikan hanya fitur yang diminta.
5. Jalankan lint/build jika script tersedia.
6. Laporkan file yang diubah, cara menjalankan, hasil pemeriksaan, dan keterbatasan.
7. Jangan menyatakan tes berhasil jika tidak benar-benar dijalankan.

## Definition of Done
- Aplikasi bisa dijalankan dengan instruksi README.
- Modul inti yang ditentukan SOT terlihat dan dapat didemokan.
- Navigasi, filter, modal, pemilihan slot, dan pembuatan booking dummy berfungsi.
- Layout dapat digunakan pada desktop dan mobile.
- Tidak ada integrasi transaksi nyata yang tersirat.
- Ringkasan akhir menjelaskan apa yang selesai dan apa yang masih dummy.
