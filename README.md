# Analisis Sentimen E-Commerce Indonesia

Proyek ini melakukan analisis sentimen terhadap review pengguna dari berbagai platform e-commerce di Indonesia (Shopee, Tokopedia, Bukalapak, dan Lazada) menggunakan berbagai algoritma Machine Learning.

## 📋 Ringkasan

Penelitian ini bertujuan untuk menganalisis sentimen (positif/negatif) dari review pengguna e-commerce Indonesia periode 2020-2022. Sistem ini membandingkan performa 5 algoritma klasifikasi untuk menentukan model terbaik dalam mengklasifikasikan sentimen review berbahasa Indonesia.

**Platform yang Dianalisis:**
- Shopee (400 reviews)
- Bukalapak (348 reviews)
- Tokopedia (295 reviews)
- Lazada (289 reviews)

**Total Dataset:** 1,332 reviews

## 📊 Dataset

### Distribusi Data
- **Shopee:** 400 reviews (201 Negatif, 199 Positif)
- **Bukalapak:** 348 reviews (183 Negatif, 165 Positif)
- **Tokopedia:** 295 reviews (207 Negatif, 88 Positif)
- **Lazada:** 289 reviews (184 Negatif, 105 Positif)

### File Dataset
- `dataset_ready_modif.csv` - Dataset utama dengan review yang sudah dilabeli
- `normalisasi. csv` - File normalisasi kata untuk preprocessing
- `stopwords.csv` - Daftar stopwords bahasa Indonesia

### Struktur Dataset
Dataset memiliki kolom:
- `Review` - Teks review pengguna
- `SENTIMEN` - Label sentimen (POSITIF/NEGATIF)
- `SOURCE` - Platform e-commerce
- `DATE_REVIEW` - Tanggal review
- `MONTH` - Bulan review
- `YEAR` - Tahun review
- `TRIMESTER` - Trimester review
- `CONCAT` - Gabungan tahun-trimester

## 🔄 Pipeline Analisis

### 1. **Data Loading & Exploration**
   - Import dataset dari CSV
   - Eksplorasi distribusi data per platform
   - Visualisasi sentimen per e-commerce

### 2. **Text Preprocessing**
   - **Case Folding:** Konversi teks ke huruf kecil
   - **Cleaning:** Menghapus URL, mention, hashtag, angka, dan tanda baca
   - **Tokenization:** Memecah teks menjadi token kata
   - **Normalization:** Normalisasi kata tidak baku menggunakan kamus normalisasi
   - **Stopword Removal:** Menghapus kata-kata umum yang tidak relevan
   - **Stemming:** Mengubah kata ke bentuk dasar menggunakan Sastrawi

### 3. **Feature Extraction**
   - **TF-IDF Vectorization:** Konversi teks menjadi fitur numerik

### 4. **Data Splitting**
   - Split data menjadi Training Set dan Testing Set

### 5. **Model Training & Evaluation**
   Melatih 5 algoritma klasifikasi:
   - **K-Nearest Neighbors (KNN)**
   - **Multinomial Naive Bayes**
   - **Stochastic Gradient Descent (SGD)**
   - **Decision Tree**
   - **Support Vector Machine (SVM)**

### 6. **Performance Evaluation**
   Evaluasi menggunakan metrik:
   - Accuracy
   - Precision
   - Recall
   - F1-Score
   - Confusion Matrix

## 📈 Hasil Model (Data Uji)

Berdasarkan notebook analisis, berikut adalah hasil evaluasi model pada data uji:

| Model         | Akurasi | Presisi | Recall | F1-Score |
| ------------- | ------- | ------- | ------ | -------- |
| KNN           | 0,815   | 0,740   | 0,878  | 0,803    |
| MNB           | 0,885   | 0,920   | 0,802  | 0,857    |
| SGD           | 0,870   | 0,853   | 0,843  | 0,848    |
| Decision Tree | 0,772   | 0,740   | 0,727  | 0,733    |
| SVM           | 0,860   | 0,920   | 0,738  | 0,819    |


## Kesimpulan

Proyek ini memberikan insight tentang:
1. Distribusi sentimen pengguna di berbagai platform e-commerce Indonesia
2. Trend sentimen dari periode 2020-2022
3. Perbandingan performa berbagai algoritma machine learning untuk analisis sentimen bahasa Indonesia
4. Model terbaik untuk klasifikasi sentimen review e-commerce


## 👤 Author

**BroBay24**
**ryanputranda**

---
