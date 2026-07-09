# Supermarket Customer Segmentation Using K-Means Clustering

## Deskripsi Proyek
[cite_start]Proyek ini mengimplementasikan algoritma K-Means Clustering untuk melakukan segmentasi pada pelanggan berstatus "Member" berdasarkan data transaksi historis sebuah supermarket[cite: 5, 6]. [cite_start]Analisis ini bertujuan untuk mengekstraksi wawasan terkait pola perilaku pembelian guna mendukung perumusan strategi pemasaran yang lebih efektif, personal, dan tepat sasaran[cite: 9, 24].

## Tautan Presentasi Bisnis
* **Dokumentasi Lengkap (Notion)**:[ [Masukkan Tautan Notion Anda]](https://app.notion.com/p/PORTOFOLIO-DATA-ANALYST-ZAKII-RAMADHAN-3770d45be53980c4b15cf0451a6cafd5?source=copy_link)

## Metodologi dan Pendekatan Analisis
[cite_start]Proyek ini mengadopsi kerangka kerja standar industri CRISP-DM (Cross Industry Standard Process for Data Mining)[cite: 25]:
1. [cite_start]**Data Understanding**: Menganalisis 1.000 baris data transaksi supermarket (Januari-Maret 2019) dan memfilter dataset hanya untuk pelanggan berstatus "Member" (565 observasi)[cite: 183, 193, 196, 234].
2. [cite_start]**Data Preparation & Feature Selection**: Mengisolasi variabel fungsional yang merepresentasikan perilaku belanja, yaitu `Unit Price`, `Quantity`, `Sales`, dan `Rating`[cite: 23, 163].
3. [cite_start]**Data Standardization**: Menerapkan transformasi nilai menggunakan `StandardScaler` untuk menyamakan skala fitur numerik agar kalkulasi jarak algoritma tidak bias[cite: 34, 47].
4. [cite_start]**Modeling & Evaluation**: Evaluasi hyperparameter untuk mencari jumlah klaster optimal menggunakan metode *Elbow Method* dan metrik *Silhouette Score*.

## Hasil Klasterisasi Utama
[cite_start]Evaluasi matematis membuktikan bahwa titik optimal pembagian klaster berada pada $k=4$[cite: 52]. Algoritma berhasil mengelompokkan pelanggan ke dalam empat persona:
* [cite_start]**Cluster 0 (Pelanggan Hemat Pasif)**: Kelompok dengan tingkat pembelian, nilai transaksi, dan rating yang paling rendah.
* [cite_start]**Cluster 1 (Pelanggan Prioritas)**: Kontributor utama pendapatan perusahaan yang mencatatkan nilai transaksi dan kuantitas pembelian tertinggi[cite: 65, 66].
* [cite_start]**Cluster 2 (Pelanggan Premium Potensial)**: Pelanggan yang membeli produk dengan harga (Unit Price) tinggi, namun frekuensi atau kuantitas barangnya masih tergolong rendah[cite: 68].
* [cite_start]**Cluster 3 (Pelanggan Hemat Aktif)**: Pelanggan yang gemar membeli produk berharga terjangkau secara masif dan memiliki tingkat kepuasan (Rating) paling tinggi[cite: 70, 71].

## Cara Menjalankan Proyek
1. Kloning repositori ini ke komputer lokal Anda.
2. Pastikan pustaka pendukung seperti `pandas`, `scikit-learn`, dan `matplotlib`/`seaborn` telah terinstal di lingkungan kerja Python Anda.
3. Jalankan *Jupyter Notebook* `[Nama_File_Anda].ipynb` untuk mereproduksi pipeline preprocessing dan modeling secara end-to-end.
