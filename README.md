# 🌍 WebGIS Teristris & Engineering Calculation Engine

Aplikasi berbasis web (*WebGIS & Engineering Sheet*) yang dirancang khusus untuk mengotomatisasi pengolahan data ukur tanah teristris. Dibangun menggunakan antarmuka modern dengan Tailwind CSS, Leaflet.js untuk pemetaan spasial, dan SheetJS untuk manajemen data Excel.

---

## 🚀 Fitur Utama

1. **Hitungan Kerangka Kontrol Horizontal (KKH - Theodolite)**
   * Perhitungan sudut terukur ($\beta$) dan koreksi penutup sudut otomatis.
   * Perataan poligon tertutup menggunakan **Metode Bowditch** untuk mendistribusikan kesalahan linier ($Fx, Fy$).
   * Perhitungan matriks lengkap: Azimuth ($\alpha$), $D \sin(\alpha)$, $D \cos(\alpha)$, hingga koordinat akhir $X$ (Easting) dan $Y$ (Northing).
   * Visualisasi poligon 2D interaktif langsung di atas peta Leaflet.

2. **Hitungan Kerangka Kontrol Vertikal (KKV - Waterpass)**
   * Pengolahan beda tinggi metode pergi-pulang ($\Delta h$).
   * Perhitungan jarak total, koreksi seksi, dan elevasi akhir titik ($H$).

3. **Perhitungan Detail Situasi (Tacheometry)**
   * Pengolahan data takimetri lengkap (Tinggi alat, BA, BT, BB, sudut Deg, Min, Sec).
   * **Deteksi Anomali Otomatis:** Sistem secara cerdas mendeteksi kesalahan format sudut (salah azimut) dan titik bergeser/mental (*outlier* jarak ekstrem).
   * Pemetaan titik detail langsung terhubung dari stasiun poligon tempat alat berdiri.

4. **Dashboard Audit & Toleransi Alat**
   * Pemeriksaan kesalahan penutup sudut terhadap spesifikasi toleransi alat (berdasarkan resolusi detik alat $m \times \sqrt{n}$).
   * Evaluasi rasio ketelitian linier aktual terhadap target orde proyek (misal $1:5000$).
   * Identifikasi titik kritis poligon yang menyerap koreksi terbesar beserta rekomendasi perbaikan lapangannya.

---

## 🛠️ Teknologi yang Digunakan

* **HTML5 & JavaScript (ES6+)** - Engine perhitungan otomatis di sisi klien (*Client-side calculation*).
* **Tailwind CSS** - Desain antarmuka responsif dan profesional ala *engineering sheet*.
* **Leaflet.js** - Peta interaktif untuk visualisasi spasial titik poligon dan detail situasi.
* **SheetJS (XLSX)** - Fitur unggah data dan unduh template lembar kerja Excel.

---

## ⚙️ Cara Menjalankan

1. Clone repositori ini atau unduh file sumbernya.
2. Pastikan file utama bernama **`index.html`**.
3. Buka file `index.html` menggunakan browser web modern apa saja (Chrome, Edge, Firefox).
4. Aplikasi siap digunakan secara *offline* maupun di-host melalui **GitHub Pages**.

---
© 2026 WebGIS Teristris by 123230055
