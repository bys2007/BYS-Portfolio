# Portofolio BYS

Repositori ini menyimpan kode sumber portofolio pribadi **Brillian Yusuf Sejati (BYS)** yang dipublikasikan pada GitHub Pages. Situs ini dirancang khusus untuk memamerkan keahlian sebagai programmer (web developer & IoT) serta editor & desainer visual melalui antarmuka modern yang interaktif, elegan, dan sepenuhnya responsif.

## Demo Langsung
- Produksi: [https://bys2007.github.io/BYS-Portfolio/](https://bys2007.github.io/BYS-Portfolio/)

## Tampilan Sekilas
![Tangkapan layar portofolio BYS](assets/Screenshot%20(1580).webp)

## Sorotan Fitur & Struktur Halaman
Situs ini dibangun dengan pendekatan satu halaman (*single-page layout*) yang mengalir mulus dengan beberapa fitur utama berikut:
- **Desain Mode Gelap (Dark Mode) Eksklusif**: Visual futuristik dengan pola grid latar belakang (*bg-grid*), panel transparan bergaya *glassmorphism*, dan tipografi premium menggunakan font *Space Grotesk*.
- **Latar Belakang Hero Dinamis**: Gambar latar belakang bagian beranda (*Hero section*) berganti secara acak dengan transisi *crossfade* lembut, ditarik langsung secara dinamis dari berkas manifest.
- **Navigasi Cerdas (Sticky & Scrollspy)**: Header navigasi yang melayang dengan detektor posisi halaman aktif (*Scrollspy* menggunakan `IntersectionObserver`), tautan cepat, dan menu responsif untuk perangkat seluler.
- **Dua Sisi Projek (I Have Two Sides)**: Fitur pemilah interaktif untuk menyaring karya antara sisi **Programmer** (proyek web, sistem Laravel, integrasi Arduino) dan sisi **Editor & Desainer** (sunting video musik MV, sinematografi sekolah, dll.). Pilihan sisi terakhir disimpan secara otomatis di `localStorage` peramban.
- **Lini Masa Perjalanan (Journey)**: Lini masa pendidikan dan perkembangan minat BYS dari masa kecil hingga lulus sebagai salah satu siswa terbaik RPL di SMK.
- **Galeri Foto Dinamis & Deep Zoom**: Memuat dokumentasi kegiatan secara asinkron memanfaatkan kombinasi **PhotoSwipe** dan **PhotoSwipe Deep Zoom** untuk pengalaman pembesaran (*lightbox zoom*) resolusi tinggi tanpa pecah.
- **Transkrip Rapor & Hasil Belajar**: Tabel transkrip nilai terperinci dari Semester I hingga Ujian Kelulusan (ASAJ) beserta nilai PKL (di PT Telkom Indonesia Regional 4 Semarang) dan peringkat kelas.
- **Modal Media Universal**: Penampil gambar dan video proyek sekali klik (*pop-up lightbox modal*) yang mendukung navigasi keyboard (panah kanan/kiri untuk galeri mini dan tombol Escape).
- **Integrasi Donasi & Kontak**: Tautan dukungan Saweria, tombol unduh CV langsung, dan tautan sosial media resmi.

## Teknologi yang Digunakan
- **HTML5**: Elemen semantik penuh untuk struktur dokumen yang bersih dan ramah SEO.
- **Tailwind CSS (CDN)**: Kerangka kerja CSS untuk desain responsif cepat dengan konfigurasi kustom (warna brand `sky` extend) langsung di kepala dokumen.
- **JavaScript ES6 (Modern Type Module)**: Logika interaksi asli tanpa dependensi jQuery, mencakup pemuatan manifest asinkron, *Intersection Observer*, navigasi modal, dan pengelolaan *local storage*.
- **PhotoSwipe & PhotoSwipe Deep Zoom**: Pustaka visual untuk menyajikan galeri foto interaktif berkualitas tinggi.
- **Google Fonts (Space Grotesk)**: Tipografi utama berkarakter modern dan bersih.

## Struktur Proyek
```
.
├─ index.html                        # Halaman utama sekaligus entry point aplikasi
├─ README.md                         # Dokumentasi proyek (berkas ini)
└─ assets/
   ├─ CV-BYS.pdf                     # Berkas Curriculum Vitae (CV) BYS
   ├─ Logo bys.webp                  # Logo/Favicon situs
   ├─ Screenshot (1580).webp         # Tangkapan layar proyek untuk README
   ├─ icon/                          # Ikon teknologi & software penunjang
   │  ├─ programmer/                 # Ikon HTML, CSS, JS, PHP, Laravel, React, Arduino, dll.
   │  └─ desainer_editor/            # Ikon Alight Motion, Premiere, AE, Blender, Figma, dll.
   ├─ pencapaian/                    # Gambar bukti sertifikat & piagam penghargaan
   ├─ projek_programmer/             # Cuplikan gambar/video untuk showcase proyek programmer
   ├─ random_foto/                   # Kumpulan foto dokumentasi untuk galeri dinamis
   ├─ random_foto_manifest.json      # Berkas manifest JSON yang mendaftarkan path foto galeri
   └─ vendor/                        # Pustaka pihak ketiga (PhotoSwipe & Deep Zoom)
```

## Cara Menjalankan Secara Lokal
1. Kloning (*clone*) atau unduh repositori ini ke komputer Anda.
2. Buka folder proyek tersebut.
3. Jalankan server statis sederhana untuk menghindari kendala pemuatan *ES Module* dan berkas manifest JSON. Anda bisa menggunakan:
   - **Node.js (serve)**:
     ```bash
     npx serve .
     ```
   - **Python**:
     ```bash
     python -m http.server 8000
     ```
   - **VS Code Extension**: Gunakan fitur **Live Server**.
4. Buka alamat lokal yang diberikan (misalnya `http://localhost:3000` atau `http://127.0.0.1:8000`) di peramban Anda.

## Pengembangan & Kustomisasi
- **Hero & Latar Acak**: Sunting bagian `<section id="home">`. Jika ingin mengubah foto yang tampil acak di latar hero, pastikan foto diletakkan di `assets/random_foto/` dan terdaftar di dalam `assets/random_foto_manifest.json`.
- **Tentang & Keahlian**: Perbarui teks profil serta tag keahlian (`chip`) pada `<section id="about">`.
- **Projek**: Tambah atau ubah kartu pada kontainer `#projectGrid`. Gunakan atribut `data-side="dev"` untuk projek pemrograman dan `data-side="edit"` untuk projek penyuntingan/desain.
- **Pencapaian**: Tambahkan sertifikat baru dalam format kartu gambar/video di `<section id="achievement">`.
- **Rapor**: Perbarui tabel nilai rapor di `<section id="rapor">`.
- **Galeri**: Tambahkan berkas foto baru ke direktori `assets/random_foto/` dan masukkan nama path barunya ke dalam array di `assets/random_foto_manifest.json` agar terbaca secara otomatis oleh skrip galeri.

## Deployment
Situs ini dirancang sepenuhnya statis dan sangat optimal dideploy pada:
1. **GitHub Pages** (Otomatis aktif melalui cabang `main`).
2. **Vercel / Netlify / Cloudflare Pages** dengan memilih opsi "Static HTML/No Build".

## Kontak
Hubungi BYS untuk kolaborasi, freelance, atau peluang kerja:
- **Email**: [un10102007@gmail.com](mailto:un10102007@gmail.com)
- **GitHub**: [github.com/bys2007](https://github.com/bys2007)
- **Instagram**: [@bys.2007](https://instagram.com/bys.2007/)
- **Domisili**: Weleri, Kendal, Jawa Tengah

Terima kasih telah mengunjungi portofolio BYS!
