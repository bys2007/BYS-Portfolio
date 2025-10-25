# Portofolio BYS

Repositori ini menyimpan kode sumber portofolio pribadi **Brillian Yusuf Sejati (BYS)** yang dipublikasikan pada GitHub Pages. Situs ini menyorot keahlian sebagai programmer, editor, dan desainer melalui antarmuka modern, interaktif, serta sepenuhnya responsif.

## Demo Langsung
- Produksi: [https://bys2007.github.io/BYS-Portfolio/](https://bys2007.github.io/BYS-Portfolio/)

## Tampilan Sekilas
![Tangkapan layar portofolio BYS](assets/Screenshot%20(1580).png)

## Sorotan Proyek
- Landing page satu halaman dengan tema gelap/terang dan animasi halus.
- Navigasi lengket dengan indikator aktif, scroll halus, serta modal media untuk setiap elemen bergambar.
- Seksi "Projek" dengan pemilah sisi Programmer vs Editor/Desainer yang disimpan pada `localStorage`.
- Galeri foto dinamis yang memanfaatkan PhotoSwipe + Deep Zoom untuk pengalaman zoom tanpa kehilangan detail.
- Kontak lengkap dan CTA unduh CV untuk memudahkan rekrutmen maupun kolaborasi.

## Teknologi yang Digunakan
- **HTML5** elemen semantik untuk struktur konten.
- **Tailwind CSS (CDN)** dengan konfigurasi kustom langsung di `index.html`.
- **JavaScript ES6** untuk logika interaksi (theme toggle, modal gambar, filter projek, galeri dinamis).
- **PhotoSwipe & PhotoSwipe Deep Zoom** (`assets/vendor/photoswipe`) sebagai lightbox.
- **Google Fonts – Space Grotesk** untuk tipografi utama.

## Struktur Proyek
```
.
├─ index.html             # Halaman utama sekaligus entry point
├─ README.md              # Dokumentasi proyek
└─ assets/
   ├─ vendor/             # Dependensi pihak ketiga (PhotoSwipe)
   ├─ projek_programmer/  # Gambar showcase sisi programmer
   ├─ pencapaian/         # Dokumentasi prestasi & sertifikat
   ├─ random_foto/        # Sumber galeri yang dimuat dinamis
   ├─ random_foto_manifest.json
   ├─ Logo bys.webp, CV-BYS.pdf, dll
```

## Cara Menjalankan Secara Lokal
1. Clone atau unduh repositori ini.
2. Buka berkas `index.html` langsung di peramban, atau jalankan server statis sederhana:
   ```bash
   npx serve .
   ```
3. Periksa konsol peramban untuk memastikan tidak ada galat pemuatan aset.

> Catatan: Seluruh gaya berada di kelas Tailwind pada markup. Jika ingin mem-build Tailwind secara mandiri, sesuaikan konfigurasi di `tailwind.config` (inline pada `<script>` di kepala dokumen) dan jalankan pipeline sesuai kebutuhan.

## Pengembangan & Kustomisasi
- **Hero & CTA**: Sunting bagian `<section id="home">` untuk mengubah headline, CTA, atau video latar.
- **About & Skillset**: Konten profil berada pada `<section id="about">`. Perbarui daftar `chip` untuk menambah/meringankan skill.
- **Projek**: Tambah atau ubah kartu pada grid `#projectGrid`. Gunakan atribut `data-side` untuk mengatur kemunculan pada tab Programmer (`dev`) atau Editor (`edit`).
- **Galeri**: Daftar gambar dimuat dari `assets/random_foto_manifest.json`. Pastikan path valid dan berada di dalam folder `assets/random_foto/`.
- **Kontak**: Informasi di `<section id="contact">`. Jaga konsistensi tautan sosial dengan data terbaru.
- **Vendor**: Jangan ubah isi `assets/vendor/photoswipe` kecuali memperbarui versi PhotoSwipe; sertakan lisensi bila diperlukan.

## Deployment
Situs ini dirancang sebagai halaman statis dan optimal untuk:
1. GitHub Pages (sudah aktif pada cabang `main`).
2. Vercel / Netlify / Cloudflare Pages dengan opsi "static site".

Setiap perubahan pada `main` akan otomatis memperbarui GitHub Pages. Untuk jalur lain, pastikan konfigurasi build diarahkan ke akar proyek (`/`).

## Kontak
Silakan hubungi BYS untuk kolaborasi atau peluang baru:
- WhatsApp: [083845879186](https://wa.me/6283845879186)
- Email: [un10102007@gmail.com](mailto:un10102007@gmail.com)
- GitHub: [github.com/bys2007](https://github.com/bys2007)
- Instagram: [@bys.2007](https://instagram.com/bys.2007/)
- TikTok: [@bys.2007](https://www.tiktok.com/@bys.2007)

Terima kasih telah mengunjungi portofolio BYS!
