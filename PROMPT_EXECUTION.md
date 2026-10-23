# Prompt Execution — Tahap Awal ArenaBook

Salin prompt ini ke coding agent setelah folder proyek dibuka:

---

Anda adalah senior front-end engineer dan UI/UX engineer. Bangun prototype front-end berdasarkan `SOT.md` dan patuhi kontrak `AGENTS.md`.

**Tujuan:** implementasikan UI modern SaaS bernama ArenaBook untuk Sistem Informasi Booking Lapangan Olahraga Berbasis Web dengan Payment Gateway.

**Teknologi wajib:** React + Vite + Tailwind CSS. Gunakan JavaScript (bukan TypeScript) kecuali struktur proyek yang sudah ada jelas menggunakan TypeScript.

**Ruang lingkup:** dashboard pelanggan/admin, kartu lapangan futsal dan bulu tangkis, pencarian/filter tanggal, slot jadwal, modal booking, perhitungan tarif × durasi, riwayat booking, status pembayaran, dashboard admin, laporan transaksi ringkas. Gunakan data dummy.

**Arahan visual:** sporty-futuristic tetapi tetap profesional; midnight navy, electric blue, cyan, lime sebagai aksen terbatas, latar terang/gelap yang terkontrol, kartu dengan border halus, tipografi terbaca, ruang kosong cukup, responsif. Jangan memakai gradient mencolok atau animasi berlebihan.

**Aturan penting:**
- Jangan membangun backend, database, autentikasi nyata, atau integrasi payment gateway sungguhan.
- Tampilkan label bahwa pembayaran hanya simulasi.
- Jangan menambahkan marketplace, multi-venue, atau fitur di luar SOT.
- Slot yang sudah terpakai harus ditandai dan tidak dapat dipilih.
- Booking demo harus memperbarui state lokal dan muncul di riwayat.
- Gunakan format Rupiah `id-ID`.
- Buat komponen yang jelas dan hindari dependency yang tidak perlu.

**Eksekusi:**
1. Baca SOT dan AGENTS.
2. Periksa proyek yang ada sebelum mengubah konfigurasi.
3. Implementasikan UI dan interaksi.
4. Jalankan `npm run build` bila tersedia.
5. Laporkan hasil build yang benar-benar dijalankan, daftar file utama, cara menjalankan, dan batasan demo.

Jangan berhenti setelah membuat mockup statis; pastikan interaksi utama bekerja. Jangan mengklaim layanan eksternal telah terhubung.
