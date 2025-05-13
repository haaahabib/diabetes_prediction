# Laporan Proyek Machine Learning - Muhammad Habibulloh

## Domain Proyek

Diabetes merupakan penyakit metabolik kronis yang ditandai dengan peningkatan kadar glukosa darah atau gula darah, yang lama-kelamaan dapat menyebabkan kerusakan serius pada jantung, pembuluh darah, mata, ginjal, dan saraf. Menurut laporan WHO, sekitar 830 juta orang di seluruh dunia mengidap diabetes [[1]](https://www.who.int/health-topics/diabetes). Untuk mempercepat diagnosis dan mengetahui penyakit diabetes seseorang diperlukan deteksi dini. Deteksi dini penting untuk mencegah komplikasi kerusakan serius pada organ-organ manusia dan meningkatkan kualitas hidup. Proyek ini bertujuan membangun model prediktif untuk mengidentifikasi risiko diabetes berdasarkan parameter klinis pasien.

## Referensi:
1. Dataset: [Pima Indians Diabetes Database](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database/data) (768 sampel).
2. I. Tasin, T. U. Nabil, S. Islam, and R. Khan, "Diabetes prediction using machine learning and explainable AI techniques," Healthcare Technology Letters, vol. 10, no. 1, pp. 1-10, Feb. 2023, doi: 10.1049/htl2.12039. [PubMed](https://pmc.ncbi.nlm.nih.gov/articles/PMC10107388/)
3. World Health Organization, [WHO, 2023](https://www.who.int/health-topics/diabetes)

## Business Understanding

## Business Understanding

### Problem Statements

- Prevalensi diabetes di Indonesia terus meningkat, dari 10.9% menjadi 11.7% pada tahun 2023 (Kemenkes)[https://rspermatajonggol.com/ini-5-sebab-diabetes-tumbuh-subur-di-indonesia/]. 
- Keterlambatan diagnosis diabetes dapat menyebabkan komplikasi serius seperti jantung, pembuluh darah, mata, ginjal, dan saraf.
- Sistem prediksi berbasis machine learning dapat membantu tenaga medis dalam melakukan skrining awal dan mengidentifikasi pasien yang berisiko tinggi, sehingga diagnosis dapat dilakukan lebih cepat.
- Dataset diabetes seringkali memiliki data imbalance, di mana jumlah pasien non-diabetes jauh lebih banyak daripada pasien diabetes. Hal ini dapat menyebabkan model cenderung memprediksi pasien sebagai non-diabetes, sehingga akurasi prediksi untuk pasien diabetes menjadi rendah.

### Goals

- Membangun model klasifikasi machine learning dengan akurasi minimal 75% pada data test.
- Menyediakan sistem yang dapat memberikan probabilitas risiko diabetes dan rekomendasi untuk pemeriksaan lanjutan, sehingga dapat digunakan sebagai alat bantu second opinion bagi tenaga medis.
- Menangani data imbalance menggunakan teknik oversampling SMOTE untuk meningkatkan performa model dalam memprediksi pasien diabetes.

### Solution Statements

Goal 1: Membangun model klasifikasi dengan akurasi minimal 75% pada data test.
- Solusi 1: Membandingkan performa algoritma Logistic Regression, Random Forest, dan Gradient Boosting. Alasannya Logistic Regression adalah algoritma dasar yang mudah diinterpretasi, Random Forest memiliki performa yang baik dan robust, sedangkan Gradient Boosting dapat menghasilkan model yang akurat. Perbandingan ini bertujuan untuk memilih model yang paling optimal untuk dataset diabetes.
- Solusi 2: Meningkatkan performa model terbaik dengan Hyperparameter Tuning. Alasannya, hyperparameter tuning memungkinkan optimasi parameter model untuk mencapai performa terbaik. 

Goal 2: Menyediakan sistem yang dapat memberikan probabilitas risiko diabetes dan rekomendasi untuk pemeriksaan lanjutan, sehingga dapat digunakan sebagai alat bantu second opinion bagi tenaga medis.

Goal 3: Menangani data imbalance untuk meningkatkan performa model dalam memprediksi pasien diabetes. Dengan menerapkan teknik SMOTE (Synthetic Minority Over-sampling Technique) pada data latih. Alasannya adalah SMOTE akan menyeimbangkan jumlah data pasien diabetes dan non-diabetes, sehingga model dapat mempelajari pola dari kedua kelas dengan lebih baik dan meningkatkan performa, khususnya dalam mendeteksi pasien diabetes.
    
## Data Understanding
Paragraf awal bagian ini menjelaskan informasi mengenai data yang Anda gunakan dalam proyek. Sertakan juga sumber atau tautan untuk mengunduh dataset. Contoh: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Restaurant+%26+consumer+data).

Selanjutnya uraikanlah seluruh variabel atau fitur pada data. Sebagai contoh:  

### Variabel-variabel pada Restaurant UCI dataset adalah sebagai berikut:
- accepts : merupakan jenis pembayaran yang diterima pada restoran tertentu.
- cuisine : merupakan jenis masakan yang disajikan pada restoran.
- dst

**Rubrik/Kriteria Tambahan (Opsional)**:
- Melakukan beberapa tahapan yang diperlukan untuk memahami data, contohnya teknik visualisasi data atau exploratory data analysis.

## Data Preparation
Pada bagian ini Anda menerapkan dan menyebutkan teknik data preparation yang dilakukan. Teknik yang digunakan pada notebook dan laporan harus berurutan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan proses data preparation yang dilakukan
- Menjelaskan alasan mengapa diperlukan tahapan data preparation tersebut.

## Modeling
Tahapan ini membahas mengenai model machine learning yang digunakan untuk menyelesaikan permasalahan. Anda perlu menjelaskan tahapan dan parameter yang digunakan pada proses pemodelan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan kelebihan dan kekurangan dari setiap algoritma yang digunakan.
- Jika menggunakan satu algoritma pada solution statement, lakukan proses improvement terhadap model dengan hyperparameter tuning. **Jelaskan proses improvement yang dilakukan**.
- Jika menggunakan dua atau lebih algoritma pada solution statement, maka pilih model terbaik sebagai solusi. **Jelaskan mengapa memilih model tersebut sebagai model terbaik**.

## Evaluation
Pada bagian ini anda perlu menyebutkan metrik evaluasi yang digunakan. Lalu anda perlu menjelaskan hasil proyek berdasarkan metrik evaluasi yang digunakan.

Sebagai contoh, Anda memiih kasus klasifikasi dan menggunakan metrik **akurasi, precision, recall, dan F1 score**. Jelaskan mengenai beberapa hal berikut:
- Penjelasan mengenai metrik yang digunakan
- Menjelaskan hasil proyek berdasarkan metrik evaluasi

Ingatlah, metrik evaluasi yang digunakan harus sesuai dengan konteks data, problem statement, dan solusi yang diinginkan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan formula metrik dan bagaimana metrik tersebut bekerja.

**---Ini adalah bagian akhir laporan---**

_Catatan:_
- _Anda dapat menambahkan gambar, kode, atau tabel ke dalam laporan jika diperlukan. Temukan caranya pada contoh dokumen markdown di situs editor [Dillinger](https://dillinger.io/), [Github Guides: Mastering markdown](https://guides.github.com/features/mastering-markdown/), atau sumber lain di internet. Semangat!_
- Jika terdapat penjelasan yang harus menyertakan code snippet, tuliskan dengan sewajarnya. Tidak perlu menuliskan keseluruhan kode project, cukup bagian yang ingin dijelaskan saja.

