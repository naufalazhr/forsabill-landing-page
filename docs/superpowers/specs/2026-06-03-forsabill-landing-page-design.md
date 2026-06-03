# Design Spec: Landing Page FORSABILL

## Overview

Landing page statis untuk Forum Stabilitas Lingkungan (FORSABILL), organisasi kemasyarakatan di Kopo Permai, Bandung. Desain formal, minimalis, berkelas, dan elegan.

## Tech Stack

- **HTML5 + CSS3 + Vanilla JS** (single-page)
- Deploy: Cloudflare Pages
- No build step, no framework

## Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| primary-red | #c41e3a | Aksen, heading underline, CTA |
| primary-yellow | #ffd700 | Highlight kecil dari logo |
| dark | #1a1a1a | Background hero/footer, text utama |
| white | #ffffff | Background sections terang |
| light-gray | #f9f9f9 | Background sections alternatif |
| medium-gray | #6b7280 | Body text |

## Typography

- **Heading**: Playfair Display (serif) — formal, elegan
- **Body**: Inter (sans-serif) — bersih, modern, mudah dibaca
- Fallback: system fonts

## Sections

### 1. Hero
- Background: solid dark (#1a1a1a) atau gradient very subtle
- Logo FORSABILL center, ukuran besar
- Tagline: "Forum Stabilitas Lingkungan" — Playfair Display, putih, 32-48px
- Sub-tagline: "Komplek Kopo Permai" — Inter, abu-abu terang
- CTA: button "Kenali Kami" — outline style, border merah, teks merah, hover fill merah
- Smooth scroll ke section berikutnya
- Height: 100vh, content center-aligned

### 2. Visi & Misi
- Background: putih
- Heading: "Visi & Misi" — Playfair Display, dengan garis aksen merah 40px di bawah
- Visi: display sebagai quote block, font italic, border-left merah
- Misi: ordered list, numbering style bersih
- Max-width: 800px, center-aligned container

### 3. Arti Lambang
- Background: #f9f9f9
- Layout: 2 kolom (logo kiri, penjelasan kanan) di desktop, stack di mobile
- Logo ditampilkan dalam ukuran sedang
- Penjelasan per elemen:
  - Tulisan FORSABILL (hitam + outline kuning) = akronim
  - 7 Bintang = 7 RW di Kopo Permai
  - Rantai = eratnya persatuan
  - Lingkaran Oval = fleksibilitas semangat Sapta Tunggal
  - Tulisan FORUM STABILITAS LINGKUNGAN = nama resmi

### 4. Struktur Organisasi
- Background: putih
- Heading: "Struktur Organisasi"
- Hierarki visual dengan card/box:
  - Level 1: Ketua FORSABILL — H. Tb. Raditya Indrajaya, SE
  - Level 2: Pengurus Inti (4 orang)
  - Level 3: Dewan Pengawas (9 orang)
  - Level 4: Pengurus Bidang (43 orang)
- Layout: centered, card-style dengan border tipis
- Tidak perlu foto, cukup jabatan + jumlah

### 5. Legalitas
- Background: #f9f9f9
- Heading: "Legalitas"
- Card style formal:
  - Akta Perubahan No: 01, 1 September 2022
  - Notaris: Alfian Faudi Mukdas, S.H., M.Kn.
  - SK Kemenkumham No: AHU-0001719.AH.01.08 Tahun 2022
- Tampilan: badge/card dengan border merah atau background sangat terang

### 6. Kontak / Sekretariat
- Background: dark (#1a1a1a)
- Heading: putih
- Informasi:
  - Alamat: Komplek Kopo Permai II 13 B No.17 RT/RW 001/008, Desa Sukamenak, Kec. Margahayu, Kab. Bandung
  - Telepon: 0817-9933-444
- Layout: 2 kolom (info kiri, map kanan) atau stack
- Google Maps embed opsional

### 7. Footer
- Background: dark (sama dengan kontak)
- Copyright: © 2026 FORSABILL
- Mungkin quote penutup dari profil: "Tetaplah berbuat dan menjadi baik bermanfaat"

## Global Design Rules

- **Spacing**: section padding 80-120px top/bottom
- **Max-width container**: 1200px
- **Responsive breakpoints**: mobile (<768px), tablet (768-1024px), desktop (>1024px)
- **Animations**: subtle fade-in on scroll using Intersection Observer
- **Smooth scroll**: CSS scroll-behavior: smooth
- **No external dependencies**: pure HTML/CSS/JS, Google Fonts via CDN

## File Structure

```
/
├── index.html
├── style.css
├── script.js
└── assets/
    └── forsyth-logo.jpeg (rename from forsbill-logo.jpeg)
```

## Content Source

All text content extracted from `Salinan dari Profile FORSABILL.pdf`:
- Visi & Misi: page 8
- Arti Lambang: page 2
- Struktur Organisasi: pages 5-6
- Legalitas: page 3
- Kontak: page 11
- Logo: `forsabill-logo.jpeg`
