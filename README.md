# Prediksi Harga Rumah

Project ini bertujuan untuk melakukan prediksi harga rumah menggunakan data dari platform `pashouse`. Proses yang dilakukan meliputi: 
1. **Data Scraping**  
   Mengumpulkan data dari platform jual-beli rumah `pashouse` melalui proses web scraping dengan beautifulsoup.

2. **Data Cleaning & Preparation**  
   Melakukan pembersihan data mentah untuk menghilangkan missing values, duplikasi, dan inkonsistensi sehingga menghasilkan dataset yang siap digunakan.

3. **Exploratory Data Analysis (EDA)**  
   Menganalisis karakteristik data secara visual dan statistik untuk memahami distribusi, hubungan antar fitur, serta mendeteksi anomali atau pola penting.

4. **Data Splitting**  
   Membagi dataset menjadi data pelatihan (training set) dan data pengujian (test set) untuk evaluasi model yang adil dan tidak bias.

5. **Outlier Handling**  
   Menerapkan teknik winsorization pada kolom numerik untuk mengurangi dampak outlier, dengan fitting pada data training dan transformasi dilakukan pada data training dan testing.

6. **Feature Engineering & Scaling**  
   Melakukan encoding fitur kategori menggunakan One-Hot Encoding dan standarisasi fitur numerik menggunakan StandardScaler untuk memastikan skala fitur yang konsisten.

7. **Modeling & Comparison**  
   Membangun dan membandingkan berbagai model regresi, termasuk Linear Regression, Regularisasi (Lasso, Ridge, ElasticNet), Support Vector Regression (SVR), dan Random Forest Regressor.

8. **Hyperparameter Tuning**  
   Melakukan optimasi parameter model menggunakan GridSearchCV untuk mendapatkan kombinasi parameter terbaik yang meningkatkan performa model.

9. **Assumptions check**   
   Mengidentifikasi pelanggaran asumsi yang dapat menyebabkan bias, ketidakstabilan koefisien, dan prediksi yang kurang akurat, sehingga memungkinkan perbaikan model agar performa dan interpretasinya lebih baik.


Dari enam model yang diuji, terdapat dua model yang perlu diperhatikan: **1. Random Forest**, yang memiliki error sangat rendah dan nilai R² tinggi pada data train (), namun menunjukkan selisih signifikan pada data test, mengindikasikan overfitting; dan **2. Ridge Regression**, yang menunjukkan performa lebih stabil dengan gap train-test lebih kecil. Hal ini mencerminkan efek positif regularisasi L2 dalam mengontrol kompleksitas model. Oleh karena itu, Ridge Regression memberikan performa lebih baik secara keseluruhan pada dataset yang relatif kecil, karena model yang lebih sederhana ini lebih cepat dilatih, mampu mengurangi dampak noise, dan memiliki kemampuan generalisasi yang lebih baik dibanding model yang lebih kompleks.
