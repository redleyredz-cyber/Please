# e-BizTrack | Sistem Laporan Usahawan

Aplikasi pengurusan laporan bulanan usahawan untuk kakitangan PPPK.

## 🚀 Panduan Deployment (Cloudflare Pages)

### Langkah 1: Build Aplikasi
Pastikan anda mempunyai Node.js dipasang. Jalankan arahan berikut di terminal:
```bash
npm install
npm run build
```
Fail website yang telah siap akan berada dalam folder `/dist`.

### Langkah 2: Deploy ke Cloudflare
1. Buka [Cloudflare Dashboard](https://dash.cloudflare.com/).
2. Navigasi ke **Workers & Pages** > **Pages** > **Create application**.
3. **Manual Upload**: Pilih folder `dist` dan muat naik.
4. **Git Integration**: Sambungkan ke GitHub/GitLab, pilih preset **Vite**, dan tetapkan output directory ke `dist`.

### Langkah 3: Konfigurasi Backend
Aplikasi ini memerlukan Google Apps Script sebagai API. 
1. Pastikan `SCRIPT_URL` dalam `services/api.ts` adalah betul.
2. Pastikan Deployment di Google Apps Script disetkan kepada **"Anyone"**.

## 🛠 Ciri-ciri Utama
- **Mod Offline**: Boleh diakses tanpa internet menggunakan Service Worker (PWA).
- **Export Excel**: Laporan boleh dimuat turun dalam format .xlsx.
- **Analisa Visual**: Carta prestasi menggunakan Recharts.
- **Security**: Log masuk berasaskan peranan (User/Admin).

## 📱 PWA (Progressive Web App)
Aplikasi ini boleh di-install ke telefon pintar (Android/iOS) melalui butang "Add to Home Screen" di pelayar Chrome atau Safari.