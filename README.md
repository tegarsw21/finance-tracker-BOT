
---

# 📊 Finance Tracker BOT

Bot WhatsApp berbasis Node.js untuk membantu Anda mencatat, mengelola, dan memantau aktivitas keuangan harian secara otomatis—langsung dari obrolan WhatsApp Anda.

![Nero happy to see you](src/assets/nero.gif)

---

## 🛠️ Persyaratan Sistem

- Node.js ≥ 18.x
- npm atau yarn
- Database (PostgreSQL direkomendasikan)
- Akun WhatsApp aktif di ponsel Anda

---

## 📥 Instalasi

Ikuti langkah-langkah berikut untuk menjalankan bot secara lokal:

### 1. Clone Repositori

```bash
git clone https://github.com/Hnzsama/finance-tracker-BOT.git
cd finance-tracker-BOT
```

### 2. Instal Dependensi

```bash
npm install
```

### 3. Konfigurasi Environment

Buat file `.env` dari template yang tersedia:

```bash
cp .env.example .env
```

Kemudian, edit file `.env` sesuai dengan konfigurasi database Anda. Contoh:

```env
DATABASE_URL="postgresql://user:password@localhost:5432/finance_tracker"
```

### 4. Inisialisasi Database

Jalankan migrasi Prisma untuk membuat skema database:

```bash
npx prisma migrate dev --name init
```

> Pastikan layanan database (misalnya PostgreSQL) sedang berjalan.

### 5. Jalankan Aplikasi

```bash
npm start
```

Saat pertama kali dijalankan, terminal akan menampilkan **QR code**.  
**Scan QR code tersebut menggunakan WhatsApp di ponsel Anda** untuk mengaktifkan koneksi.

Setelah terhubung, bot siap menerima perintah.

---

## 🧪 Contoh Penggunaan

Kirim pesan ke bot melalui WhatsApp:

```
berapa total pengeluaran minggu ini?
```

Bot akan memproses permintaan dan memberikan ringkasan berdasarkan data yang telah direkam.

---

## 📁 Struktur Proyek

- `src/` – Kode sumber aplikasi
- `auth/` – Session otentikasi WhatsApp (dihasilkan otomatis)
- `prisma/` – Skema dan migrasi database
- `.env` – Konfigurasi lingkungan (tidak di-commit)
- `package.json` – Dependensi dan skrip

---

## 📜 Lisensi

Proyek ini dilisensikan di bawah **GNU General Public License v2.0**.  
Untuk informasi selengkapnya, lihat file [LICENSE](LICENSE).

---

## 🙏 Kontribusi

Kontribusi dalam bentuk laporan bug, saran fitur, atau pull request sangat dihargai. Silakan buka issue di repositori ini terlebih dahulu sebelum mengirimkan kontribusi.

---

> Dikembangkan dengan ❤️ oleh [Hnzsama](https://github.com/Hnzsama)  
> Proyek ini bersifat open-source dan gratis untuk digunakan, dimodifikasi, serta didistribusikan sesuai ketentuan lisensi.

--- 

Jika Anda menggunakan proyek ini, pertimbangkan untuk memberikan ⭐ di GitHub! Terima kasih.