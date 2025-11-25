# Deployment Guide - Frontend

## Deploy ke Vercel

### 1. Persiapan

Pastikan Anda sudah:
- Memiliki akun Vercel (https://vercel.com)
- Backend sudah di-deploy dan memiliki URL production

### 2. Setup Environment Variables di Vercel

Setelah membuat project di Vercel, tambahkan environment variable:

**Key**: `VITE_API_URL`
**Value**: `https://your-backend-url.vercel.app/api`

Ganti `your-backend-url.vercel.app` dengan URL backend Anda yang sebenarnya.

### 3. Deploy Manual via CLI

```bash
# Install Vercel CLI (jika belum)
npm install -g vercel

# Deploy
cd frontend
vercel --prod
```

### 4. Deploy via GitHub

1. Push code ke GitHub
2. Import repository di Vercel Dashboard
3. Pilih folder `frontend` sebagai root directory
4. Tambahkan environment variable `VITE_API_URL`
5. Deploy!

### 5. Verifikasi

Setelah deploy berhasil, cek:
- Halaman utama bisa diakses
- API calls ke backend berhasil
- Images dari backend bisa dimuat

## Troubleshooting

### Error: "Failed to fetch"
- Pastikan `VITE_API_URL` sudah diset dengan benar di Vercel
- Pastikan backend sudah di-deploy dan bisa diakses

### Error: "404 Not Found" saat refresh
- `vercel.json` sudah menghandle SPA routing
- Jika masih error, cek konfigurasi di Vercel dashboard

### Images tidak muncul
- Pastikan backend URL sudah benar
- Cek CORS setting di backend
