# Prediksi Penyakit Diabetes Menggunakan Machine Learning

Proyek ini bertujuan untuk membangun dan mengevaluasi model *machine learning* yang dapat memprediksi kemungkinan seseorang menderita penyakit diabetes berdasarkan berbagai atribut kesehatan. Dua model klasifikasi dibandingkan dalam proyek ini: **Random Forest Classifier** dan **K-Nearest Neighbors (KNN)**.

---

## Daftar Isi

1.  [Latar Belakang](#latar-belakang)
2.  [Tujuan Proyek](#tujuan-proyek)
3.  [Dataset](#dataset)
4.  [Metodologi](#metodologi)
5.  [Hasil Evaluasi Model](#hasil-evaluasi-model)
6.  [Tech Stack](#tech-stack)
7.  [Cara Menjalankan Proyek](#cara-menjalankan-proyek)

---

## Latar Belakang

Diabetes adalah penyakit kronis yang mempengaruhi jutaan orang di seluruh dunia. Deteksi dini merupakan kunci untuk pengelolaan penyakit yang efektif dan pencegahan komplikasi. Dengan memanfaatkan data riwayat kesehatan pasien, *machine learning* dapat membantu mengidentifikasi individu yang berisiko tinggi terkena diabetes, sehingga memungkinkan intervensi medis lebih awal.

## Tujuan Proyek

-   Melakukan pra-pemrosesan pada data kesehatan untuk persiapan pemodelan.
-   Membangun dan melatih dua model klasifikasi yang berbeda: Random Forest dan KNN.
-   Mengevaluasi dan membandingkan performa kedua model menggunakan metrik standar (Akurasi, Presisi, Recall, F1-Score).
-   Menentukan model mana yang memberikan prediksi paling andal untuk kasus ini.

---

## Dataset

Dataset yang digunakan adalah **"Pima Indians Diabetes Database"**, sebuah kumpulan data klasik untuk tugas prediksi diabetes. Dataset ini berisi beberapa variabel prediktor medis dan satu variabel target (outcome).

-   **Fitur**: `Pregnancies`, `Glucose`, `BloodPressure`, `SkinThickness`, `Insulin`, `BMI`, `DiabetesPedigreeFunction`, `Age`.
-   **Target**: `Outcome` (0: Tidak Diabetes, 1: Diabetes).

---

## Metodologi

1.  **Eksplorasi Data (EDA)**: Menganalisis distribusi dan korelasi data untuk mendapatkan wawasan awal.
2.  **Pra-pemrosesan Data**:
    -   Menangani nilai yang hilang (jika ada).
    -   Melakukan standarisasi fitur menggunakan **StandardScaler** agar skala data seragam.
3.  **Pembagian Data**: Membagi dataset menjadi 80% data latih dan 20% data uji.
4.  **Pemodelan**:
    -   Melatih model **Random Forest Classifier**.
    -   Melatih model **K-Nearest Neighbors (KNN)**.
5.  **Evaluasi**: Membandingkan performa kedua model pada data uji.

---

## Hasil Evaluasi Model

Berdasarkan hasil evaluasi, **Random Forest Classifier** menunjukkan performa yang lebih unggul dibandingkan K-Nearest Neighbors di semua metrik evaluasi.

| Model | Akurasi | Presisi | Recall | F1-Score |
| :--- | :---: | :---: | :---: | :---: |
| **Random Forest** | **77.27%** | **71.43%** | **55.56%** | **62.50%** |
| **K-Nearest Neighbors** | 75.97% | 67.31% | 55.56% | 60.87% |

Meskipun akurasi keduanya cukup baik, Random Forest memberikan keseimbangan yang lebih baik antara presisi dan recall, yang ditunjukkan oleh F1-Score yang lebih tinggi.

---

## Tech Stack

-   **Bahasa Pemrograman**: Python
-   **Library Utama**:
    -   Pandas & NumPy (Manipulasi Data)
    -   Scikit-learn (Pemodelan & Evaluasi)
    -   Matplotlib & Seaborn (Visualisasi)

---

## Cara Menjalankan Proyek

1.  **Clone Repositori Ini**
    ```bash
    git clone https://github.com/haaahabib/diabetes_prediction.git
    ```
2.  **Masuk ke Direktori Proyek**
    ```bash
    cd diabetes_prediction
    ```
3.  **Install Library yang Dibutuhkan**
    ```bash
    pip install pandas numpy scikit-learn matplotlib seaborn jupyter
    ```
4.  **Jalankan Jupyter Notebook**
    Buka dan jalankan file `main.ipynb` untuk melihat keseluruhan alur kerja proyek.
    ```bash
    jupyter notebook main.ipynb
    ```
