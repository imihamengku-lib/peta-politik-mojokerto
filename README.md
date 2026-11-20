# Peta Politik Kabupaten Mojokerto (Tanpa DPT)

Aplikasi web interaktif *single-file* (`index.html`) untuk pemetaan politik wilayah administratif **Kabupaten Mojokerto** (**18 Kecamatan** dan **304 Desa/Kelurahan** — 299 Desa & 5 Kelurahan) tanpa menggunakan DPT, lengkap dengan peta vektor geografis asli, verifikasi hak suara, multi-calon dinamis, kuota 1–3 suara per wilayah, dan kalkulator rekapitulasi otomatis.

## Fitur Utama

1. **Peta Vektor Geografis Asli & Drill-Down**
   - Tampilan awal menampilkan keseluruhan Kabupaten Mojokerto terbagi ke dalam 18 Kecamatan.
   - **Hover** pada kecamatan menampilkan ringkasan jumlah desa/kelurahan lolos, kuota suara, dan sebaran dukungan per calon.
   - **Klik** pada kecamatan melakukan *zoom* halus ke pembagian wilayah desa/kelurahan di dalamnya (dengan kawasan hutan dirender terpisah sebagai konteks geografis non-desa).
2. **Tahap 1 — Verifikasi Database (Lolos vs Tidak Lolos / Gugur)**
   - Tandai kecamatan maupun desa/kelurahan yang tidak lolos verifikasi database menggunakan kuas **`⊘ Gugur`**.
   - Wilayah gugur otomatis diarsir abu-abu dan dikeluarkan dari seluruh hitungan kalkulator suara, lengkap dengan toggle **Fokus Daerah Lolos Saja**.
3. **Tahap 2 — Multi-Calon Dinamis & Kuota 1–3 Suara per Wilayah**
   - Default tersedia 4 calon (`A`, `B`, `C`, `D`) + status **`★` Potensial / Belum Berpihak**, dan dapat ditambah/edit nama, kode pin, serta warnanya melalui menu **Atur Calon**.
   - Setiap kecamatan maupun desa/kelurahan lolos dapat diatur memiliki **1, 2, atau 3 suara** yang bisa diarahkan utuh ke 1 calon atau dipecah ke beberapa calon berbeda.
4. **Kalkulator Rekapitulasi Otomatis & Ekspor Data**
   - Menghitung otomatis **Grand Total Suara Sah** (Suara Kecamatan + Suara Desa), **Target Mayoritas (`>50%`)**, leaderboard peringkat calon, dan tabel matriks 18 Kecamatan × semua calon.
   - Data tersimpan otomatis di `localStorage` browser serta mendukung **Backup/Impor JSON**, **Unduh CSV Rekap Kecamatan**, dan **Unduh CSV Detail 304 Desa**.

## Cara Menggunakan

- **Langsung di Browser**: Unduh atau buka file `index.html` langsung di Chrome, Edge, atau Safari (tidak perlu instalasi maupun backend).
- **GitHub Pages**: Aktifkan *Settings → Pages → Deploy from branch `main` (`/root`)* untuk mengakses aplikasi secara online.

## Sumber Batas Wilayah

Data batas administratif Kecamatan dan Desa/Kelurahan Kabupaten Mojokerto (`id3516`) berasal dari dataset HDX-BPS (`JfrAziz/indonesia-district`) yang telah disederhanakan dan diproyeksikan ke SVG ringan (`data/mojokerto_geo.json`).
