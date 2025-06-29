# Prediksi Suhu Udara Harian Menggunakan Random Forest Regressor

##  Nama Kelompok
- Salma Aulia Nisa – 2306143  
- Vito Gunawan – 2306149

---

##  Penjelasan Langkah Pengerjaan

### 1. Business Understanding
- **Permasalahan:** Prediksi suhu penting dalam sektor pertanian, energi, dan transportasi. Model tradisional membutuhkan komputasi tinggi sehingga diperlukan alternatif berbasis machine learning.  
- **Tujuan:** Mengembangkan model prediksi suhu dengan akurasi tinggi menggunakan Random Forest Regressor.  
- **User:** Petani, BMKG, PLN, operator transportasi, masyarakat umum.  
- **Manfaat AI:** Meningkatkan akurasi prakiraan cuaca, efisiensi energi, serta keselamatan publik.

---

### 2. Data Understanding
- **Sumber data:** Weather History Dataset (Kaggle).  
- **Fitur:** 12 variabel (Formatted Date, Summary, Precip Type, Temperature, Apparent Temperature, Humidity, Wind Speed, Wind Bearing, Visibility, Loud Cover, Pressure, Daily Summary).  
- **Ukuran data:** 96.453 observasi, periode 2006–2016, format .csv.  
- **Target:** Temperature (C) (regresi).

---

### 3. Exploratory Data Analysis (EDA)
- Membuat **histogram suhu** menunjukkan distribusi mendekati normal dengan skew ke kanan.  
- Membuat **heatmap korelasi**, terlihat Temperature dan Apparent Temperature memiliki korelasi sangat tinggi (0.99).  
- Mengecek imbalance, data target kontinu sehingga fokus pada distribusi nilai.

---

### 4. Data Preparation
- **Missing value:** Menghapus baris dengan missing value pada Precip Type.  
- **Encoding:** One-Hot Encoding untuk Summary, Precip Type, dan Daily Summary.  
- **Normalisasi:** StandardScaler pada fitur numerik.  
- **Split data:** Train (80%) dan Test (20%).

---

### 5. Modeling
- **Model:** Random Forest Regressor dan Linear Regression.  
- **Alasan:** Random Forest menangkap hubungan non-linear, Linear Regression sebagai baseline.  
- **Implementasi:** Python scikit-learn.  
- **Hyperparameter tuning:** GridSearchCV dengan hasil terbaik n_estimators=150.

---

### 6. Evaluation
- **Metrik Random Forest:**  
  - RMSE: 0.064  
  - MAE: 0.019  
  - R²: 1.000
- **Metrik Linear Regression:**  
  - RMSE: 0.937  
  - MAE: 0.731  
  - R²: 0.990
- **Interpretasi:** Random Forest memiliki error lebih kecil dan R² mendekati 1, menandakan prediksi hampir sempurna dibanding Linear Regression.

---

### 7. Kesimpulan dan Rekomendasi
Random Forest Regressor terbukti lebih akurat dalam memprediksi suhu harian dibanding Linear Regression karena mampu menangkap pola non-linear. Direkomendasikan penggunaan Random Forest untuk prediksi suhu, serta eksplorasi model ensemble lain seperti Gradient Boosting untuk peningkatan akurasi di masa depan.

---

### 8. Referensi
- Allen, A., et al. (2025). End-to-end data-driven weather prediction. *Nature*. https://doi.org/10.1038/S41586-025-08897-0  
- Bouallègue, Z. Ben, et al. (2024). The rise of data-driven weather forecasting. *Bulletin of the American Meteorological Society*, 105(6), E864–E883. https://doi.org/10.1175/BAMS-D-23-0162.1  
- Cai, S., et al. (2024). Temporal-Spatial Traffic Flow Prediction Model Based on Prompt Learning. *ISPRS International Journal of Geo-Information*, 14(1), 11. https://doi.org/10.3390/IJGI14010011  
- Fauzi, M., et al. (n.d.). Implementasi Machine Learning untuk Memprediksi Cuaca Menggunakan SVM. https://doi.org/10.32409/jikstik.23.1.3449  
- Hanoon, M. S., et al. (2021). Developing machine learning algorithms for meteorological temperature and humidity forecasting. *Scientific Reports*, 11(1), 1–19. https://doi.org/10.1038/S41598-021-96872-W

---
