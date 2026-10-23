# RekaDanaNeon

Infrastruktur dan konfigurasi layanan cloud Neon untuk RekaDana.

## Layanan yang Dikonfigurasi di `neon.ts`

- **PostgreSQL (Lakebase Postgres):** Database serverless utama
- **Neon Auth:** Managed Better Auth untuk session & autentikasi pengguna
- **Neon Object Storage:** S3-compatible private bucket (`assets`) untuk bukti transaksi
- **Neon AI Gateway:** Gateway inference model LLM
- **Neon Functions:** Serverless long-running functions (termasuk `hello.ts`)
- **Neon Realtime:** Live query subscriptions

## Cara Menggunakan

### 1. Login ke Neon
```bash
neon login
```

### 2. Preview Perubahan
```bash
neon config plan
```

### 3. Deploy dan Tarik Environment Variables ke Web App
```bash
neon deploy --env ../RekaDana/.env.local
```
Perintah ini akan mem-provision semua layanan dan otomatis mengisi file `.env.local` pada project Next.js `RekaDana`.
