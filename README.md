# 💈 Tritama Barber - Sistem Manajemen Barbershop

Sistem manajemen barbershop modern berbasis web dengan fitur lengkap untuk manajemen antrian, booking, transaksi, penggajian, dan laporan.

![Tritama Barber](https://img.shields.io/badge/Tritama-Barber-8b1f3a?style=for-the-badge&logo=scissors)
![Laravel](https://img.shields.io/badge/Laravel-11-FF2D20?style=for-the-badge&logo=laravel)
![React](https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react)
![Tailwind](https://img.shields.io/badge/Tailwind-3-38B2AC?style=for-the-badge&logo=tailwind-css)

## ✨ Fitur Utama

### 🎯 Manajemen Antrian
- Sistem antrian real-time dengan nomor urut
- Notifikasi panggilan antrian
- Status: Menunggu → Sedang Dikerjakan → Selesai

### 📅 Booking Online
- Booking janji temu dengan barber pilihan
- Reminder otomatis sebelum jadwal
- Manajemen slot waktu

### 💰 Transaksi & POS
- Point of Sale (POS) terintegrasi
- Multi metode pembayaran (Cash, Debit, QRIS, Transfer)
- Diskon dan promo

### 👨‍💼 Manajemen Barber
- Profil barber dengan spesialisasi
- Sistem komisi otomatis (10%)
- Jadwal kerja

### 💵 Penggajian
- Slip gaji otomatis dengan PDF
- Perhitungan gaji pokok + komisi
- Email notifikasi ke barber

### 📊 Laporan
- Laporan harian, mingguan, bulanan
- Analisis pendapatan dan pengeluaran
- Performa barber

## 🎨 Tema Warna

Tema warna mengikuti logo Tritama Barber:

| Warna | Hex | Penggunaan |
|-------|-----|------------|
| Merah | `#8b1f3a` | Primary, header, button utama |
| Emas | `#c9942e` | Secondary, accent, highlights |
| Cream | `#fdf9ed` | Background, cards |

## 🚀 Teknologi

### Backend
- **Laravel 11** - PHP Framework
- **Laravel Sanctum** - API Authentication
- **MySQL** - Database
- **DomPDF** - PDF Generation
- **Laravel Mail** - Email Notifications

### Frontend
- **React 18** - UI Library
- **Vite** - Build Tool
- **Tailwind CSS** - Styling
- **Axios** - HTTP Client
- **Zustand** - State Management
- **Lucide React** - Icons

## 📁 Struktur Folder

```
barbershop-pos/
├── backend/              # Laravel API
│   ├── app/
│   ├── config/
│   ├── database/
│   ├── resources/views/  # Email templates
│   └── routes/
├── frontend/             # React App
│   ├── src/
│   │   ├── components/   # UI Components
│   │   ├── pages/        # Page Components
│   │   ├── layouts/      # Layout Components
│   │   └── stores/       # State Management
│   └── public/
└── README.md
```

## 🛠️ Instalasi

### Prasyarat
- PHP 8.2+
- Node.js 18+
- MySQL 8.0+
- Composer
- NPM/Yarn

### 1. Clone Repository

```bash
git clone https://github.com/username/tritama-barber.git
cd tritama-barber
```

### 2. Setup Backend

```bash
cd backend

# Install dependencies
composer install

# Copy environment file
cp .env.example .env

# Generate application key
php artisan key:generate

# Setup database (sesuaikan .env terlebih dahulu)
php artisan migrate --seed

# Install storage link
php artisan storage:link
```

### 3. Setup Frontend

```bash
cd ../frontend

# Install dependencies
npm install

# Copy environment file
cp .env.example .env.local

# Jalankan development server
npm run dev
```

### 4. Konfigurasi Environment

#### Backend (.env)
```env
APP_NAME="Tritama Barber"
APP_URL=http://localhost:8000
FRONTEND_URL=http://localhost:3000

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=tritama_barber
DB_USERNAME=root
DB_PASSWORD=

MAIL_MAILER=smtp
MAIL_HOST=smtp.gmail.com
MAIL_PORT=587
MAIL_USERNAME=your-email@gmail.com
MAIL_PASSWORD=your-app-password
MAIL_FROM_ADDRESS=noreply@tritamabarber.com
```

#### Frontend (.env.local)
```env
VITE_API_URL=http://localhost:8000/api
```

## 🎯 Default Login

| Role | Email | Password |
|------|-------|----------|
| Admin | admin@tritama.com | password |
| Kasir | kasir@tritama.com | password |
| Barber | barber@tritama.com | password |

## 📧 Fitur Email

Email otomatis dikirim untuk:
- ✅ Verifikasi akun
- ✅ Reset password
- ✅ Slip gaji dibuat
- ✅ Slip gaji dibayar
- ✅ Welcome email

## 📱 Screenshot

![Dashboard](screenshots/dashboard.png)
*Dashboard Admin*

![Antrian](screenshots/queue.png)
*Manajemen Antrian*

![Slip Gaji](screenshots/salary.png)
*Slip Gaji PDF*

## 📝 License

MIT License - Tritama Barber System

---

💈 **Tritama Barber** - Professional Barbershop Management System
