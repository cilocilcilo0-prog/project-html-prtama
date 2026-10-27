# SUARA SYIAR — Platform Sewa Penceramah, Pengajian & Hadroh

Platform web kelas enterprise untuk penyewaan penceramah, da'i, pembawa acara (MC), qari/qariah, dan grup hadroh.

## 🚀 Fitur Unggulan Sesuai Wireframe
1. **Peralihan Peran Ganda (Dual-Role Switcher)**: Beralih instan antara Mode Penyewa dan Mode Talent tanpa login ulang.
2. **Wizard Verifikasi Talent 4 Langkah**: Upload foto profil, foto KTP panduan OCR/anti-pantulan dengan enkripsi AES-256 S3, portofolio & tarif, serta rekening bank.
3. **Pencegahan Double-Booking (ACID Serializable Transaction)**: Memastikan tidak ada tanggal acara yang tumpang tindih.
4. **Keranjang Multi-Talent & Simulasi Virtual Account**: Mendukung 7 bank utama Indonesia (BNI, BRI, BCA, Mandiri, BSI, CIMB Niaga, SeaBank).
5. **Kalender Acara & Bukti Kehadiran**: Talent dapat menandai blokir tanggal mandiri dan mengunggah foto kehadiran selfie di lokasi panggung acara.
6. **Room Chat Real-time & Rundown Attachment**: Koordinasi acara dengan sematan langsung template rundown acara.

## 📁 Struktur Direktori
- `prisma/schema.prisma`: Skema lengkap PostgreSQL dengan RLS policies.
- `src/lib/security/`: Dual-Token JWT, Argon2id, Redis sliding-window brute-force limiter.
- `src/services/`: Service layer untuk booking transaction dan role rotation.
- `src/components/`: Komponen UI mobile-first dengan bingkai desktop simulator.

## 💻 Cara Menjalankan
```bash
npm install
npx prisma generate
npm run dev
```
Akses aplikasi melalui browser di `http://localhost:3000`.
