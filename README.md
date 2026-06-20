# Analisis Perilaku Pengguna Sepeda Divvy: Member vs Casual (2013-2026)

![Data Analysis](https://img.shields.io/badge/Data_Analysis-Python-blue?style=for-the-badge&logo=python)
![Data Size](https://img.shields.io/badge/Dataset_Size-2.01_GB-green?style=for-the-badge)
![Total Rows](https://img.shields.io/badge/Total_Rows-54.9_M-orange?style=for-the-badge)

Proyek ini merupakan analisis data berskala besar untuk mengeksplorasi perbedaan perilaku antara pengguna **Member** (berlangganan) dan **Casual** (menit) pada sistem peminjaman sepeda Divvy Bikes di Chicago. Analisis ini menggunakan kerangka kerja **Google Data Analytics Methodology** (*Ask, Prepare, Process, Analyze, Share, Act*).

---

## 📌 Daftar Isi
1. Latar Belakang & Business Task
2. Dataset & Batasan Data
3. Struktur isi
4. Temuan Utama (Key Findings)
5. Kesimpulan & Rekomendasi Strategis
6. Eksplorasi Lanjutan: Retensi Member & Gender
7. Teknologi yang Digunakan
8. Artifact & Dokumen Pendukung

---

## 🎯 Latar Belakang & Business Task

### Latar Belakang
Divvy adalah sistem pembagian sepeda (*bike-share*) di Chicago yang beroperasi sejak 2013 dengan sistem stasiun fleksibel. Direktur Pemasaran meyakini bahwa kunci sukses masa depan perusahaan bergantung pada pemaksimalan jumlah keanggotaan tahunan (*annual memberships*). Sebagai tim analis pemasaran, tugas kami adalah memahami bagaimana pengguna kasual mengeksplorasi layanan secara berbeda dari pengguna anggota terdaftar agar dapat merumuskan strategi konversi yang tepat.

### Business Task
> **Objective:** Mengidentifikasi perbedaan perilaku antara pengguna Casual dan Member berdasarkan pola waktu (tren bulanan, mingguan, harian, per jam), lokasi geografis, rute, serta durasi berkendara guna merumuskan strategi pemasaran yang efektif untuk memaksimalkan langganan dan konversi keanggotaan tahunan.

---

## 📊 Dataset & Batasan Data

Analisis ini menggunakan gabungan data historis perjalanan dari **Juni 2013 hingga Mei 2026**.
*   **Nama & Format File:** `divvy_total_2013_2026.parquet`
*   **Ukuran File:** 2,01 GB *(Dikompresi secara efisien dari bentuk awal CSV berukuran total 8,80 GB berisi 104 file)*.
*   **Jumlah Baris:** 54.936.117 baris data.
*   **Jumlah Kolom:** 17 kolom awal sebelum proses *feature engineering*.
*   **Proporsi Pengguna (Berdasarkan total perjalanan):** 
    *   **Member:** 66,7% (36.633.856 perjalanan) — Dominan karena frekuensi penggunaan berulang yang tinggi.
    *   **Casual:** 33,3% (18.253.682 perjalanan).

*Catatan: Link data: https://divvy-tripdata.s3.amazonaws.com/index.html

---

## 📂 Struktur Repositori

Berdasarkan struktur proyek pada `gambar.png`, repositori ini diatur sebagai berikut:

```text
analisis-pengguna-divvy-bikes/
├── notebooks/
│   └── process.ipynb   # Kode Python untuk data cleaning
│   └── analisis.ipynb   # Kode Python untuk analisis
├── reports/
│   ├── presentasi_analisis.pdf       # File PDF presentasi/slide deck utama
│   └── penjelasan_detail_proses.pdf  # Dokumentasi detail proses pembersihan & metodologi
└── README.md                         # Dokumentasi utama proyek
