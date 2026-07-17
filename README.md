# E-Learning Platform Analytics: End-to-End BI Project

Project ini berfokus pada proses **ETL (Extract, Transform, Load)**, **Data Modeling (Star Schema)**, dan pembuatan **Interactive Dashboard Business Intelligence** untuk menganalisis aktivitas pengguna pada platform e-learning.

## Project Overview & Objective
Tujuan utama dari project ini adalah mengintegrasikan data aktivitas belajar mahasiswa yang berasal dari berbagai sumber (*multi-source*), membersihkan anomali data (data kotor), menyusun arsitektur data warehouse sederhana menggunakan model *Star Schema*, hingga menyajikan *insight* bisnis yang interaktif bagi manajemen e-learning.

## Tech Stack & Tools
* **Data Cleaning & ETL:** Python (Pandas) via Google Colab
* **Data Modeling:** Star Schema (Tabel Fakta & Dimensi)
* **Business Intelligence / Visualisasi:** Tableau Desktop & Tableau Public

Data Cleaning & ETL Challenges
Dataset awal memiliki banyak masalah umum di dunia nyata. Berikut adalah tantangan data yang berhasil diselesaikan menggunakan Python (Pandas):

Multi-Source Integration: Menggabungkan 5 file berbeda (3 format .xlsx dan 2 format .csv) menjadi satu pipeline data yang terintegrasi.

Handling Typo & Inkonsistensi Kategori: Mengoreksi kesalahan penulisan (typo) pada nama instruktur, program studi, dan merapikan kategori yang tidak konsisten.

Handling Duplicate & Missing Value: Mengidentifikasi data transaksi ganda, serta menangani nilai kosong (null values) agar tidak merusak kalkulasi akurasi performa belajar.

Standardisasi Format Tanggal: Menyeragamkan berbagai format tanggal penulisan yang berbeda dari tiap sumber menjadi format standar ISO YYYY-MM-DD.

Script pembersihan lengkap dapat dilihat di folder: etl_scripts/elearning_etl_process.ipynb

Data Modeling (Star Schema)
Data yang telah dibersihkan kemudian ditransformasikan ke dalam desain Star Schema untuk mengoptimalkan kinerja query pada dashboard BI:

Fact Table: fact_aktivitas_belajar (menyimpan metrik kuantitatif seperti durasi belajar, nilai, jumlah klik, dan foreign keys).

Dimension Tables:

dim_mahasiswa (informasi demografi mahasiswa)

dim_instruktur (informasi instruktur pengampu)

dim_course (detail materi dan modul e-learning)

Interactive Tableau Dashboard
Berikut adalah link visualisasi interaktif yang sudah dirancang:
https://public.tableau.com/app/profile/rahmank/vizzes
