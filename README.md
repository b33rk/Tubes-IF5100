**Tugas Besar - Pemrograman untuk Data Analitik (Kelompok 10)**

Repository ini berisi kode dan laporan untuk analisis dataset *Hotel Booking Demand*. Proyek ini bertujuan untuk melakukan *Exploratory Data Analysis* (EDA), *Preprocessing* data, dan membangun model *Machine learning* untuk memprediksi apakah suatu pemesanan hotel akan dibatalkan (`is_canceled`) atau tidak.

## Anggota Kelompok 10
* **Abdullah Mubarak** (13522101)
* **Viody Alfaridzi** (23525039)
* **Iskandar Muda Rizky Parlambang** (23525058)

## Struktur File
* `PDA_Tubes.ipynb`: Jupyter Notebook utama yang berisi seluruh *pipeline* pengerjaan mulai dari pemuatan data, EDA, *cleaning*, hingga pemodelan.
* `Laporan_TUBES_PDA_Kel_10.pdf`: Laporan teknis lengkap mengenai metodologi, analisis mendalam, dan hasil evaluasi model.
* `hotel_bookings.csv`: File dataset.

## Tentang Dataset
Dataset yang digunakan adalah **Hotel Booking Demand** yang diperoleh dari Kaggle.
* **Sumber:** [Kaggle - Hotel Booking Demand](https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand/data)
* **Jumlah Data:** 119,390 baris dan 32 kolom.
* **Target Variabel:** `is_canceled` (0 = Tidak Batal, 1 = Batal).

## Alur Kerja (Workflow)

### 1. Data Understanding & EDA
Melakukan eksplorasi data untuk memahami karakteristik fitur:
* Pengecekan tipe data dan *missing values*.
* Analisis distribusi numerik dan kategorikal.
* Visualisasi korelasi antar fitur dan terhadap target.
* Analisis *skewness* pada data numerik.

### 2. Data Preparation & Cleaning
Langkah-langkah pembersihan data yang dilakukan dalam `PDA_Tubes.ipynb`:
* **Filtering:** Menghapus data anomali di mana jumlah orang dewasa (`adults`) adalah 0.
* **Koreksi Data:** Menggabungkan kategori *meal* "Undefined" ke dalam "SC" (*Self Catering*).
* **Handling Missing Values:** Strategi imputasi untuk kolom seperti `children`, `country`, `agent`, dan `company`.
* **Splitting:** Pembagian data latih (80%) dan uji (20%) berdasarkan urutan waktu reservasi (*time-series split logic*).

### 3. Preprocessing
Menggunakan `sklearn.pipeline` untuk otomatisasi:
* **Numerik:** *Imputation* dan *Scaling*.
* **Kategorikal:** *One-Hot Encoding* atau *Label Encoding*.

### 4. Modeling
Beberapa algoritma *machine learning* yang diimplementasikan dan dibandingkan:
* Logistic Regression
* Random Forest Classifier
* XGBoost

## Cara Menjalankan
1.  Pastikan Anda telah menginstal Python dan Jupyter Notebook/Lab.
2.  Install *library* yang dibutuhkan.
3.  Letakkan file dataset `hotel_bookings.csv` di folder yang sama dengan notebook.
4.  Buka file `PDA_Tubes.ipynb` dan jalankan sel secara berurutan.
