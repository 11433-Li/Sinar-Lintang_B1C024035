# Klasifikasi Breast Cancer Menggunakan Machine Learning

Pada contoh ini, kita akan mengembangkan model Machine Learning untuk mengklasifikasikan tumor payudara ke dalam dua kategori, yaitu **jinak (benign)** dan **ganas (malignant)**.

**File contoh:** [AI for Medical Diagnosis – Google Colab](https://colab.research.google.com/drive/1IcW12mwoZ8yZxJ7Wl3p-RAYFrWghbOXE?usp=sharing)

## Hasil Eksperimen dan Analisis Kinerja Model

Pada tahap ini dilakukan evaluasi terhadap model Machine Learning menggunakan algoritma Logistic Regression. Evaluasi dilakukan untuk mengetahui kemampuan model dalam mengklasifikasikan tumor payudara ke dalam kategori Malignant (ganas) dan Benign (jinak).

### 1 Informasi Dataset

Berdasarkan hasil eksplorasi menggunakan Pandas, diperoleh informasi sebagai berikut:

| Parameter | Hasil |
|---|---:|
| Jumlah Sampel | 569 |
| Jumlah Fitur | 30 |
| Jumlah Kelas | 2 |
| Tipe Data | float64 |
| Missing Values | 0 |
| Penggunaan Memori | 133.5 KB |

Dataset memiliki 569 sampel dengan 30 fitur numerik. Seluruh fitur memiliki tipe data `float64` dan tidak ditemukan nilai yang hilang (*missing values*).

### 2 Distribusi Kelas

Hasil pemeriksaan distribusi kelas menunjukkan jumlah sampel sebagai berikut:

| Label | Kategori | Jumlah Sampel |
|---|---|---:|
| 0 | Malignant (Ganas) | 212 |
| 1 | Benign (Jinak) | 357 |
| **Total** | | **569** |

Berdasarkan distribusi tersebut, jumlah sampel tumor jinak lebih banyak dibandingkan tumor ganas. Secara visualisasi distribusi kelas

<img width="618" height="470" alt="image" src="https://github.com/user-attachments/assets/c57ed847-9b7a-442b-b34e-c5f7a7d8ffd0" />

### 3 Pembagian Dataset

Dataset dibagi menjadi data training dan testing dengan proporsi 80:20.

| Parameter | Training | Testing |
|---|---:|---:|
| Jumlah Sampel | 455 | 114 |
| Jumlah Fitur | 30 | 30 |
| Proporsi | 80% | 20% |

Pembagian dilakukan menggunakan `train_test_split()` dengan parameter `stratify=y` untuk mempertahankan proporsi kelas pada data training dan testing.

### 4 Hasil Evaluasi Model

Setelah proses training menggunakan algoritma Logistic Regression, model diuji menggunakan 114 sampel data testing.

Hasil evaluasi menunjukkan:

| Metrik Evaluasi | Nilai |
|---|---:|
| Accuracy | 98.25% |
| ROC-AUC | 0.9954 |

Nilai accuracy sebesar 98.25% menunjukkan bahwa model berhasil mengklasifikasikan sebagian besar data testing dengan benar.

Sementara itu, nilai ROC-AUC sebesar 0.9954 menunjukkan kemampuan diskriminasi model yang sangat baik dalam membedakan kelas malignant dan benign pada data pengujian.

### 5 Classification Report

Hasil evaluasi berdasarkan masing-masing kelas ditampilkan pada tabel berikut:

| Kelas | Precision | Recall | F1-Score | Support |
|---|---:|---:|---:|---:|
| Malignant | 0.98 | 0.98 | 0.98 | 42 |
| Benign | 0.99 | 0.99 | 0.99 | 72 |
| **Macro Average** | **0.98** | **0.98** | **0.98** | **114** |
| **Weighted Average** | **0.99** | **0.98** | **0.99** | **114** |

**Interpretasi:**

- **Precision:** Menunjukkan ketepatan model ketika memprediksi suatu kategori.
- **Recall:** Menunjukkan kemampuan model dalam menemukan seluruh sampel dari kategori tertentu.
- **F1-Score:** Menggambarkan keseimbangan antara precision dan recall.
- **Support:** Menunjukkan jumlah sampel aktual pada masing-masing kategori dalam data testing.

Pada kelas malignant, model memperoleh precision, recall, dan F1-score sebesar 0.98.

Pada kelas benign, model memperoleh precision, recall, dan F1-score sebesar 0.99.

Hasil tersebut menunjukkan bahwa model memiliki performa klasifikasi yang baik pada kedua kategori.

### 7. Confusion Matrix

Confusion Matrix merupakan tabel yang digunakan untuk membandingkan hasil prediksi model dengan kelas sebenarnya.

Confusion Matrix memiliki empat komponen utama:
| Komponen | Keterangan |
|:--|:--|
| True Positive (TP) | Sampel positif yang diprediksi positif |
| True Negative (TN) | Sampel negatif yang diprediksi negatif |
| False Positive (FP) | Sampel negatif yang diprediksi positif |
| False Negative (FN) | Sampel positif yang diprediksi negatif |

Pada dataset ini, kelas positif secara default adalah kelas 1 (Benign), sedangkan kelas negatif adalah kelas 0 (Malignant).

### 6 Analisis Hasil Prediksi

Berdasarkan hasil perbandingan antara label prediksi (`y_pred`) dan label aktual (`y_test`), diperoleh:

- Total data testing: 114 sampel.
- Prediksi benar: 112 sampel.
- Prediksi salah: 2 sampel.

Dengan demikian, akurasi model dapat dihitung sebagai berikut:

\[
Accuracy = \frac{112}{114} \times 100\%
\]

\[
Accuracy = 98.25\%
\]

Hasil ini menunjukkan bahwa terdapat 2 sampel yang mengalami kesalahan klasifikasi yang secara visualisasi dapat dilihat pada Confusion Matrix

<img width="571" height="470" alt="image" src="https://github.com/user-attachments/assets/5286f52b-115c-4622-8020-8c0ea4e0f828" />

### 7 Kesimpulan Eksperimen

Berdasarkan hasil eksperimen, dapat disimpulkan bahwa:

1. Dataset Breast Cancer Wisconsin memiliki 569 sampel dengan 30 fitur numerik.
2. Dataset tidak memiliki missing values sehingga tidak memerlukan penanganan nilai yang hilang.
3. Dataset dibagi menjadi 455 sampel training dan 114 sampel testing.
4. Algoritma Logistic Regression menghasilkan akurasi sebesar 98.25%.
5. Model memperoleh nilai ROC-AUC sebesar 0.9954.
6. Nilai F1-score sebesar 0.98 pada kelas malignant dan 0.99 pada kelas benign menunjukkan bahwa model memiliki performa yang baik pada kedua kelas.

Secara keseluruhan, Logistic Regression mampu mempelajari pola karakteristik sel tumor dan melakukan klasifikasi dengan tingkat akurasi yang tinggi pada dataset pengujian.

**Catatan:** Hasil ini merupakan evaluasi pada satu pembagian dataset dengan `random_state=42`. Performa tersebut belum menjamin kemampuan model pada populasi atau data klinis yang berbeda. Model ini hanya digunakan untuk tujuan pembelajaran dan bukan sebagai sistem diagnosis medis.
