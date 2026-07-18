# 🏨 Hotel Booking Cancellation Analysis

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Wrangling-lightblue?logo=pandas)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

## 📌 Deskripsi Project

Project ini menganalisis pola pembatalan booking pada industri perhotelan menggunakan dataset **Hotel Booking Demand** dari Kaggle yang berisi 119.390 data transaksi nyata dari dua hotel di Portugal (2015–2017). Setelah proses data cleaning, tersisa **87.396 baris data bersih** yang digunakan untuk analisis.

Tingkat pembatalan booking yang terus meningkat dari tahun ke tahun menjadi tantangan serius bagi manajemen hotel karena berdampak langsung pada hilangnya potensi pendapatan. Project ini bertujuan mengidentifikasi pola pembatalan dan memberikan rekomendasi bisnis yang actionable.

---

## 🎯 Business Questions

1. Bagaimana tren cancellation rate dari waktu ke waktu — apakah ada musim atau bulan tertentu dengan lonjakan pembatalan yang signifikan?
2. Channel pemesanan mana yang menghasilkan tingkat pembatalan tertinggi, dan bagaimana hubungannya dengan Average Daily Rate (ADR)?
3. Bagaimana perbandingan profil tamu yang cancel vs tidak cancel — dilihat dari lead time, tipe tamu, dan lama menginap?

---

## 🔍 Key Findings

| # | Temuan | Rekomendasi |
|---|---|---|
| B1 | Cancellation rate meningkat tiap tahun (2015: ~20% → 2017: ~31%). Puncaknya di **Juli–Agustus** yang justru merupakan high season | Terapkan **early bird non-refundable rate** khusus Juli–Agustus — tamu yang booking jauh hari dapat harga lebih murah tapi tidak bisa di-cancel |
| B2 | **Online TA** memiliki cancellation rate tertinggi (35%) sekaligus volume booking terbesar (51.618) dan ADR tertinggi (~118) | Negosiasi ulang kontrak dengan platform Online TA untuk terapkan **kebijakan deposit minimum 20–30%** saat booking |
| B3 | Tamu yang cancel rata-rata memesan **105 hari** lebih awal dan berencana menginap lebih lama — potensi revenue yang hilang lebih besar | Terapkan **cancellation fee berjenjang** berdasarkan lead time + **reschedule gratis 1x** untuk tamu Transient |

---

## 🛠️ Tools & Library

- **Python** — Bahasa pemrograman utama
- **Pandas** — Data wrangling & cleaning
- **Matplotlib** — Visualisasi data
- **Google Colab** — Environment pengerjaan notebook
- **Dataset:** [Hotel Booking Demand — Kaggle](https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand)

---

## 🧹 Proses Data Cleaning

| Masalah | Penanganan |
|---|---|
| 31.994 baris duplikat | Di-drop → data tersisa 87.396 baris |
| Missing values di `agent` & `company` | Diisi `0` (tanpa agen/perusahaan) |
| Missing values di `country` | Diisi `'Unknown'` |
| Nilai `children = 10` & NaN | Diisi `0` |
| Nilai `adr` negatif & ekstrem (>3000) | Diganti dengan nilai median (98.10) |

---

## 📁 Struktur Repository

```
hotel-booking-analysis/
│
├── hotel_booking_analysis.ipynb   
│
├── data/
│   ├── hotel_bookings_clean.csv  
│   └── README.md                 
│
├── img/
│   ├── b1_cancellation_trend.png     
│   ├── b2_channel_analysis.png    
│   └── b3_customer_profile.png   
│
└── README.md
```

---

## 👤 Author

**Muhammad Zacky Alan Fernando**
Mahasiswa Sistem Informasi | Aspiring Data Analyst

[![GitHub](https://img.shields.io/badge/GitHub-MuhammadZackyAlanFernando-black?logo=github)](https://github.com/MuhammadZackyAlanFernando)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-muhammad--zacky--alan--fernando-blue?logo=linkedin)](https://www.linkedin.com/in/muhammad-zacky-alan-fernando)


