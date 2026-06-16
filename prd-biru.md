# Product Requirement Document (PRD) — Technical & Content Specification

## Project: Revamp Static Website Company Profile — Biru Security Services

---

## 1. Metadata Proyek

* **Nama Proyek:** Revamp Website Biru Security Services
* **Tipe Produk:** Corporate Profile Website (Static Site)
* **Prinsip Fungsional Utama:** Aksesibel (WCAG 2.1 AA), Cepat (High Performance), dan Multibahasa (ID/EN).

---

## 2. Tech Stack & Arsitektur Situs Statis

Untuk menjamin kecepatan pemuatan maksimal, keamanan tinggi, dan kemudahan pelokalan bahasa:

* **Static Site Generator (SSG):** **Astro**. Memanfaatkan routing berbasis sub-direktori semantik untuk pengelolaan multibahasa bawaan (i18n):
  * Bahasa Indonesia (Default): `domain.com/`
  * Bahasa Inggris: `domain.com/en/`
* **Styling Framework:** **Tailwind CSS** (Pendekatan *Mobile-First Design* dari 320px hingga 1920px).
* **Ikonografi:** **Phosphor Icons** atau **Lucide Icons** berbentuk SVG murni dengan bobot (*weight*) visual yang seragam di seluruh section.
* **Hosting & CI/CD Platform:** Cloudflare Pages, Vercel, atau Netlify.

---

## 3. Panduan Aksesibilitas (WCAG 2.1 Level AA)

* **Kontras Warna Terstandar (Success Criterion 1.4.3):** Rasio kontras warna teks utama terhadap latar belakang wajib memenuhi standar minimal **4.5:1**. 
* **Navigasi Keyboard (Success Criterion 2.1.1):** Seluruh elemen interaktif harus memiliki penanda fokus visual (`:focus-visible`) berupa garis luar kontras yang jelas saat dijelajahi menggunakan tombol `Tab`.
* **Target Sentuh (Success Criterion 2.5.5):** Seluruh area klik pada tombol interaktif, tautan, dan *language switcher* memiliki ukuran minimal **44 x 44 piksel**.
* **HTML Semantik:** Wajib menggunakan struktur tag HTML5 standar (`<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`) dengan urutan tingkat heading (`<h1>` -> `<h2>` -> `<h3>`) yang logis.

---

## 4. Spesifikasi Saluran Komunikasi & Tautan Resmi

Seluruh elemen kontak di dalam website wajib dikunci hanya menggunakan data tautan resmi berikut:

1. **WhatsApp Link (Tunggal):** Gunakan tautan resmi ini untuk semua tombol aksi utama atau CTA bertuliskan "Hubungi via WhatsApp":
   `https://api.whatsapp.com/send/?phone=6281230743984&text&type=phone_number&app_absent=0`
2. **Panggilan Telepon Langsung (Direct Phone Call):** Nomor-nomor berikut murni diatur menggunakan tautan protokol `tel:` untuk panggilan seluler/telepon kantor langsung (jangan hubungkan ke WhatsApp):
   * Kantor Pusat: `+62 21-21693719`
   * Seluler: `+62 811-9517-111`
3. **Media Sosial Resmi (Footer):**
   * Instagram: `https://www.instagram.com/birufms.id/`
   * YouTube: `https://www.youtube.com/channel/UCqTAFPYVGauwxSNqjxEFNoQ`
4. **Tautan Bisnis Eksternal:** Sediakan tautan keluar yang aman ke domain `birufms.com` sebagai rujukan unit bisnis Facility Management lainnya.

---

## 5. Struktur Komponen Halaman & Distribusi Konten

### 5.1 Header / Navigation Bar
* **Kiri:** Logo PT. Bangun Insan Reksa Utama (BIRU) berupa komponen inline SVG bersih/teks ter-styling rapi.
* **Tengah:** Link Navigasi (Tentang Kami, Layanan, Mengapa Kami, Produk, Galeri, Kontak).
* **Kanan:**
  * Tombol CTA WhatsApp tunggal dengan ukuran target sentuh minimal 44px.
  * *Language Switcher:* Teks minimalis **"ID"** dan **"EN"** (Tanpa ikon bendera negara).

### 5.2 Hero Section
* **Visual:** Gambar representatif beresolusi tinggi dari URL eksternal Unsplash bertema *security guard / office safety* (CLS < 0.05).
* **Teks Utama (H1):** *"Solusi Layanan Pengamanan dan Manajemen Fasilitas Terpadu"*
* **Paragraf Deskripsi:** *"BIRU Security Services merupakan bagian terintegrasi dari PT. Bangun Insan Reksa Utama (BIRU). Kami menyediakan layanan prima di bidang Facility Management Services yang mencakup Security, Cleaning Service, Parking Service, Engineering Service, IT Support, hingga Building Management."*
* **Tombol Aksi:** Tombol primer "Hubungi via WhatsApp" dan tombol sekunder "Pelajari Layanan".

### 5.3 Section: Tentang Kami
* **Layout:** Grid 2 kolom.
* **Konten Teks:** *"Kami menyediakan Jasa Keamanan profesional, andal, dan tepercaya untuk menjaga perkantoran, pabrik, pasar, hotel, apartemen, rumah sakit, pusat perbelanjaan, kawasan industri, hingga kompleks perumahan. Operasional kami didukung penuh oleh infrastruktur Teknologi Informasi terintegrasi, aplikasi pemantauan khusus tugas di lapangan, serta pengawasan konstan 24/7 dari Command Center Service BIRU."*
* **Visual:** Placeholder gambar tim keamanan dengan border-radius halus.

### 5.4 Section: Layanan Utama (Grid 3 Kolom)
Ditampilkan dalam bentuk kartu-kartu (*cards*) minimalis. Teks judul dan deskripsi wajib menggunakan warna gelap demi kontras WCAG yang optimal.

1. **Security Bank:** Pengamanan khusus area perbankan untuk keselamatan nasabah dan kelancaran transaksi keuangan.
2. **Security Pabrik:** Pengamanan aset fisik berskala besar dan proteksi perimeter operasional wilayah pabrik.
3. **Security Pasar:** Penjagaan ketertiban pasar guna menjamin keamanan aktivitas jual-beli masyarakat dari potensi gangguan luar.
4. **Security Hotel & Apartemen:** Proteksi menyeluruh dan layanan ramah untuk memastikan kenyamanan tamu dan penghuni selama menginap.
5. **Security Tempat Tinggal:** Pengamanan lingkungan perumahan secara responsif dan terjadwal, baik siang maupun malam hari.
6. **Security Mall & Store:** Manajemen ketertiban area retail publik yang mencakup aspek pengamanan fisik, personel, informasi, dan teknis.
7. **Security Objek Vital:** Penjagaan ketat kawasan strategis, industri krusial, dan fasilitas milik negara dengan tingkat kerawanan tinggi.
8. **Security Gedung:** Tata kelola keamanan gedung perkantoran, pemeriksaan identitas pengunjung secara berkala, dan penanganan darurat.
9. **Layanan Fasilitas Lainnya:** Penyedia Jasa Keamanan terdepan dan outsourcing profesional untuk berbagai kebutuhan pendukung bisnis Anda.

### 5.5 Section: Mengapa Memilih Kami?
* **Kredensial Utama:** Penegasan rekam jejak berkiprah sejak tahun 2004 (lebih dari 18 tahun pengalaman) serta legalitas lengkap yang terdaftar resmi di sistem OSS dan Mabes Polri.
* **6 Pilar Keunggulan (Grid minimalis dengan SVG Icon seragam):**
  1. *Berbasis Teknologi:* Aplikasi absensi internal, laporan patroli digital *real-time*, dan integrasi Command Center 24/7.
  2. *Keamanan Tinggi:* Penyediaan paket solusi dan konsultasi risiko keamanan komprehensif tanpa biaya tambahan dalam kontrak.
  3. *Penjaga Terlatih:* Sertifikasi wajib berjenjang (Gada Pratama, Gada Madya, Gada Utama) serta rutinitas Latihan Bina Fisik Mental.
  4. *Peralatan Terbaru:* Dukungan integrasi sistem CCTV pintar, alarm peringatan dini, face recognition, dan aplikasi *e-Visitor*.
  5. *SDM Berkualitas:* Seleksi ketat melalui proses Medical Check Up berkala dan evaluasi komprehensif via *Performance Management System*.
  6. *Sertifikasi Kompetensi Internasional:* Kepemilikan standar mutu resmi **ISO 9001:2015, ISO 14001:2015, ISO 45001:2018, dan SMK3**.
* **Mitra Strategis (Klien Kami):** Grid logo mitra (Kedubes Malaysia, Sinar Mas, Hana Bank, Adhi Karya, WIKA, Pasar Jaya) disajikan dalam bentuk elemen teks atau SVG monokromatik abu-abu netral yang seragam.

### 5.6 Section: Produk & Sistem Keamanan
Menampilkan daftar solusi perangkat keras dan lunak dalam bentuk list kartu berikon bersih:
* CCTV System, Barrier Gate, Sistem Pemantauan Alarm, Sistem Manajemen Pengunjung (e-Visitor), Sistem Patroli Satpam (Scan QR Code), dan Sistem Keamanan Perimeter.

### 5.7 Section: Galeri Operasional
* Grid responsif yang menampilkan placeholder gambar aktivitas pelatihan dan pengawasan lapangan berformat ringan (`.webp` lewat tautan eksternal).

### 5.8 Footer
Dibagi menjadi 4 kolom bersih:
* **Kolom 1:** Nama perusahaan, deskripsi singkat, dan teks hak cipta statis resmi.
* **Kolom 2 (Hubungi Kami):** Alamat fisik kantor pusat, email aktif (`info@birufms.com`), tautan WhatsApp resmi tunggal, serta nomor telepon kantor/seluler dengan protokol `tel:`.
* **Kolom 3 (Unit Bisnis FM Lainnya):** Daftar teks layanan pendukung (Kebersihan, Parkir, MEP, IT Support, Manajemen Gedung) yang dibungkus tautan keluar aman menuju domain `birufms.com`.
* **Kolom 4 (Media Sosial):** Ikon SVG minimalis yang mengarah langsung ke akun Instagram (`birufms.id`) dan YouTube resmi perusahaan.

---

## 6. Lokalisasi Konten (i18n Translation Mapping)

Seluruh isi konten teks, judul, deskripsi 9 layanan, serta penjabaran 6 poin keunggulan di atas wajib direplikasi secara identik ke dalam versi folder rute `/en/` dengan terjemahan Bahasa Inggris (English) yang natural dan profesional, serta memastikan pengaturan tag `<html lang="en">` berjalan dengan tepat.