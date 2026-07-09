# Supermarket Customer Segmentation Using K-Means Clustering

## Deskripsi Proyek
Proyek ini mengimplementasikan algoritma K-Means Clustering untuk melakukan segmentasi pada pelanggan berstatus "Member" berdasarkan data transaksi historis sebuah supermarket. Analisis ini bertujuan untuk mengekstraksi wawasan terkait pola perilaku pembelian guna mendukung perumusan strategi pemasaran yang lebih efektif, personal, dan tepat sasaran.

## Tautan Presentasi Bisnis
* **Dokumentasi Lengkap (Notion)**:(https://app.notion.com/p/PORTOFOLIO-DATA-ANALYST-ZAKII-RAMADHAN-3770d45be53980c4b15cf0451a6cafd5?source=copy_link)
## Metodologi dan Pendekatan Analisis
Proyek ini mengadopsi kerangka kerja standar industri CRISP-DM (Cross Industry Standard Process for Data Mining):
1. **Data Understanding**: Menganalisis 1.000 baris data transaksi supermarket (Januari-Maret 2019) dan memfilter dataset hanya untuk pelanggan berstatus "Member" (565 observasi).
2. **Data Preparation & Feature Selection**: Mengisolasi variabel fungsional yang merepresentasikan perilaku belanja, yaitu `Unit Price`, `Quantity`, `Sales`, dan `Rating`.
3. **Data Standardization**: Menerapkan transformasi nilai menggunakan `StandardScaler` untuk menyamakan skala fitur numerik agar kalkulasi jarak algoritma tidak bias.
4. **Modeling & Evaluation**: Evaluasi hyperparameter untuk mencari jumlah klaster optimal menggunakan metode *Elbow Method* dan metrik *Silhouette Score*.

## Hasil Klasterisasi Utama
Evaluasi matematis membuktikan bahwa titik optimal pembagian klaster berada pada $k=4$. Algoritma berhasil mengelompokkan pelanggan ke dalam empat persona:
 **Cluster 0 (Pelanggan Hemat Pasif)**: Kelompok dengan tingkat pembelian, nilai transaksi, dan rating yang paling rendah.
  **Cluster 1 (Pelanggan Prioritas)**: Kontributor utama pendapatan perusahaan yang mencatatkan nilai transaksi dan kuantitas pembelian tertinggi.
**Cluster 2 (Pelanggan Premium Potensial)**: Pelanggan yang membeli produk dengan harga (Unit Price) tinggi, namun frekuensi atau kuantitas barangnya masih tergolong rendah.
**Cluster 3 (Pelanggan Hemat Aktif)**: Pelanggan yang gemar membeli produk berharga terjangkau secara masif dan memiliki tingkat kepuasan (Rating) paling tinggi.

## Cara Menjalankan Proyek
1. Kloning repositori ini ke komputer lokal Anda.
2. Pastikan pustaka pendukung seperti `pandas`, `scikit-learn`, dan `matplotlib`/`seaborn` telah terinstal di lingkungan kerja Python Anda.
3. Jalankan *Jupyter Notebook* `[Nama_File_Anda].ipynb` untuk mereproduksi pipeline preprocessing dan modeling secara end-to-end.
