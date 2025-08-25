# Portofolio Website - Vue 3 & Tailwind CSS
![Preview Website](/public/app.png)

## Daftar Isi

- [Deskripsi](#deskripsi)
- [Fitur](#fitur)
- [Teknologi](#teknologi)
- [Instalasi](#instalasi)
- [Struktur Proyek](#struktur-proyek)
- [Penggunaan](#penggunaan)
- [Konfigurasi Tambahan](#konfigurasi-tambahan)
- [Kontribusi](#kontribusi)
- [Lisensi](#lisensi)

---

## Deskripsi

Website Portofolio ini dibangun menggunakan **Vue 3** dan **Tailwind CSS**. Website ini bertujuan untuk menampilkan profil, pengalaman, proyek, dan kontak secara profesional dan responsif.

## Fitur

- Tampilan responsif (mobile & desktop)
- Halaman profil pribadi
- Daftar pengalaman kerja & pendidikan
- Galeri proyek dengan deskripsi
- Formulir kontak
- Navigasi dinamis
- Animasi transisi halus
- Dark mode (opsional)

## Teknologi

- [Vue 3](https://vuejs.org/)
- [Tailwind CSS](https://tailwindcss.com/)
- [Vite](https://vitejs.dev/) (opsional, untuk build & dev server)
- [Vue Router](https://router.vuejs.org/) (jika multi halaman)
- [EmailJS](https://www.emailjs.com/) (opsional, untuk kontak)

## Instalasi

1. **Clone repository:**
    ```bash
    git clone https://github.com/4lifbima/portofolio-vue3.git
    cd portofolio-vue3
    ```

2. **Install dependencies:**
    ```bash
    npm install
    # atau
    yarn install
    ```

3. **Jalankan server pengembangan:**
    ```bash
    npm run dev
    # atau
    yarn dev
    ```

4. **Build untuk produksi:**
    ```bash
    npm run build
    # atau
    yarn build
    ```

## Struktur Proyek

```
portofolio-vue/
├── public/
├── src/
│   ├── assets/
│   ├── components/
│   │   ├── About.vue
│   │   ├── Footer.vue
│   │   ├── Hero.vue
│   │   ├── Navbar.vue
│   │   ├── Portfolio.vue
│   │   ├── Services.vue
│   │   └── Testimonials.vue
│   ├── views/
|   |   └── Home.vue
│   ├── router/
│   │   └── index.js
│   ├── App.vue
│   └── main.js
├── tailwind.config.js
├── package.json
└── README.md
```

## Penggunaan

- Edit data profil di `src/views/Home.vue` atau file terkait.
- Tambahkan proyek di `src/data/projects.js` (atau sesuai struktur Anda).
- Sesuaikan komponen di folder `components` sesuai kebutuhan.
- Atur routing di `router/index.js` untuk navigasi.
- Ubah style di `tailwind.config.js` atau file CSS.

## Konfigurasi Tambahan

- **Tailwind CSS:**  
  Sudah terintegrasi, konfigurasi di `tailwind.config.js`.
- **Vue Router:**  
  Untuk navigasi antar halaman.
- **Dark Mode:**  
  Aktifkan dengan menambah konfigurasi di Tailwind dan komponen.

## Kontribusi

1. Fork repo ini
2. Buat branch fitur: `git checkout -b fitur-baru`
3. Commit perubahan: `git commit -m 'Tambah fitur baru'`
4. Push ke branch: `git push origin fitur-baru`
5. Buat Pull Request

## Lisensi

Proyek ini menggunakan lisensi [MIT](LICENSE).

---

**Dibuat dengan ❤️ [4lifbima](https://alifbima.vercel.app/) menggunakan Vue 3 & Tailwind CSS**