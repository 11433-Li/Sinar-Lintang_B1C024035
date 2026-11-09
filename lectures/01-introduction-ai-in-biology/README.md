# Lecture Note 01: Introduction to Artificial Intelligence in Biology

<img width="1036" height="346" alt="Infografis Modern Subset AIi" src="https://github.com/user-attachments/assets/af833d66-a98c-47fc-b89c-4e75483db3e9" />

## What is Artificial Intelligence?

Artificial Intelligence (AI) atau kecerdasan buatan merupakan bidang ilmu komputer yang mempelajari bagaimana membangun sistem yang mampu melakukan tugas-tugas yang umumnya membutuhkan kecerdasan manusia.

Kemampuan tersebut meliputi:

- **Learning:** Kemampuan mempelajari pola berdasarkan data.
- **Reasoning:** Kemampuan melakukan penalaran berdasarkan informasi yang tersedia.
- **Prediction:** Kemampuan memperkirakan kondisi atau kejadian berdasarkan pola yang dipelajari.
- **Perception:** Kemampuan mengenali dan memahami informasi dari lingkungan, seperti gambar dan suara.
- **Decision Making:** Kemampuan menghasilkan keputusan berdasarkan informasi dan tujuan tertentu.

Dalam bidang biologi, AI dapat digunakan untuk menganalisis data biologis dalam jumlah besar dan menemukan pola yang sulit diidentifikasi melalui pengamatan manual.

**Contoh penerapan:**

- Mengidentifikasi penyakit pada daun tanaman melalui citra digital.
- Memprediksi struktur tiga dimensi protein.
- Mengklasifikasikan spesies berdasarkan karakteristik morfologi.
- Menganalisis pola ekspresi gen.
- Mengidentifikasi sel kanker melalui citra histologi.

### Evolution of Artificial Intelligence

Perkembangan AI dapat dipahami melalui beberapa tahapan utama:

| Periode | Perkembangan |
|---|---|
| 1950-an–1960-an | Awal penelitian AI dan pengembangan konsep kecerdasan mesin. |
| 1970-an–1980-an | Perkembangan sistem pakar (Expert Systems) dan pendekatan berbasis aturan. |
| 1990-an–2000-an | Perkembangan Machine Learning dan metode statistik untuk analisis data. |
| 2010-an | Perkembangan Deep Learning, didukung peningkatan kemampuan komputasi dan ketersediaan data. |
| 2020-an | Perkembangan Generative AI, foundation models, dan penerapan AI dalam penelitian ilmiah, termasuk biologi. |

Perkembangan tersebut mendorong perubahan pendekatan penelitian biologi, dari analisis yang banyak bergantung pada pengamatan manual menuju pendekatan komputasional berbasis data.

## Mengapa Biologi Membutuhkan AI

1. **Kompleksitas Sistem Biologis**

- **Multiskala:** Sistem biologis memiliki struktur yang kompleks dan tersusun dalam berbagai tingkatan, mulai dari molekul → sel → jaringan → organisme → ekosistem.
- **Variabilitas dan derau (noise) yang tinggi:** Data biologis memiliki tingkat variasi dan derau yang tinggi sehingga sulit dianalisis secara akurat.

2. **Ledakan Data Biologis**

- **Genomik:** Menghasilkan data dalam jumlah sangat besar, dengan miliaran basa DNA yang berhasil diurutkan (*sequenced*).
- **Pencitraan Medis:** Menghasilkan data berukuran terabyte dari MRI, CT Scan, dan mikroskopi.
- **Data Klinis:** Mencakup rekam medis elektronik (*Electronic Health Records* / EHR) dan data dari perangkat pemantau kesehatan (*wearable devices*).

3. **Peran Artificial Intelligence (AI)**

Metode analisis tradisional tidak lagi memadai untuk menangani kompleksitas dan volume data biologis yang terus meningkat. Oleh karena itu, **Artificial Intelligence (AI)** digunakan untuk membantu mengidentifikasi pola tersembunyi (*hidden patterns*) dan memperoleh informasi bermakna dari data biologis dalam jumlah besar.

## Aplikasi Utama AI dalam Biologi

1. **Genomik dan Bioinformatika**
   - Identifikasi variasi genetik (*variant calling*).
   - Anotasi genom (*genome annotation*).
   - Prediksi ekspresi gen (*gene expression prediction*).
   - AI membantu memetakan hubungan antara genotipe (*genotype*) dan fenotipe (*phenotype*).

2. **Pencitraan Medis (*Medical Imaging*)**
   - **Radiologi:**
     - Deteksi kanker melalui citra CT Scan dan MRI.
   - **Patologi:**
     - Klasifikasi otomatis sampel jaringan biologis.

3. **Penemuan Obat (*Drug Discovery*)**
   - Penyaringan molekul secara virtual (*virtual screening*).
   - Prediksi struktur protein, seperti yang dilakukan oleh AlphaFold.
   - Pengembangan pendekatan pengobatan yang dipersonalisasi (*personalized medicine*).

4. **Biologi Sistem (*Systems Biology*)**
   - Pemodelan interaksi dalam jaringan biologis.
   - Prediksi perilaku sistem biologis secara menyeluruh berdasarkan data molekuler.

## Artificial Intelligence, Machine Learning, and Deep Learning

Ketiga istilah ini saling berkaitan, tetapi memiliki cakupan dan karakteristik yang berbeda.

<img width="700" height="400" alt="image" src="https://github.com/user-attachments/assets/85d8c0c8-bf20-4667-922b-d54774468a2e" />

#### A. Artificial Intelligence (AI)

AI merupakan konsep atau bidang yang lebih luas, yaitu pengembangan sistem komputer yang mampu melakukan tugas-tugas yang membutuhkan kecerdasan.

Contoh dalam biologi:
- Sistem pendukung diagnosis penyakit.
- Sistem identifikasi spesies.
- Sistem rekomendasi kandidat senyawa obat.

#### B. Machine Learning (ML)

Machine Learning merupakan bagian dari AI yang memungkinkan komputer mempelajari pola dari data untuk menghasilkan prediksi atau keputusan tanpa harus diprogram secara eksplisit untuk setiap kemungkinan kondisi.

Contoh dalam biologi:
- Klasifikasi penyakit tanaman berdasarkan karakteristik data.
- Prediksi kategori suatu sekuens DNA.
- Pengelompokan spesies berdasarkan karakteristik biologis.

#### C. Deep Learning (DL)

Deep Learning merupakan bagian dari Machine Learning yang menggunakan jaringan saraf tiruan dengan banyak lapisan (Artificial Neural Networks) untuk mempelajari representasi dan pola yang kompleks.

Contoh dalam biologi:
- Identifikasi sel melalui citra mikroskopis.
- Klasifikasi jaringan pada citra histologi.
- Analisis sekuens biologis.
- Prediksi struktur protein.

Secara konseptual, Deep Learning merupakan bagian dari Machine Learning, sedangkan Machine Learning merupakan bagian dari Artificial Intelligence.

## Memahami Dasar Dataset Biologi Sederhana
Berikut contoh dataset sederhana yang berisi karakteristik pengukuran tanaman.

```python
import pandas as pd

data = {
    'temperature': [25, 28, 30, 26, 29],
    'humidity': [80, 75, 65, 85, 70],
    'plant_height': [10, 15, 20, 12, 18],
    'growth_status': [
        'Normal',
        'Normal',
        'Poor',
        'Normal',
        'Poor'
    ]
}

df = pd.DataFrame(data)

print(df)
```

Selengkapnya dapat diakses melalui [Google Colab](https://colab.research.google.com/drive/1oZG72S5U_3OJxw6m5Y7SIHxyEJDzpvR1?usp=sharing)

## Kategori Machine Learning Berdasarkan Pendekatan Pembelajaran

Berdasarkan pendekatan pembelajarannya, *Machine Learning* secara umum dibagi menjadi tiga kategori utama:

### A. Supervised Learning

*Supervised Learning* merupakan metode pembelajaran mesin yang menggunakan data berlabel (*labeled data*).

- Model dilatih menggunakan pasangan data:
  - **Input:** Data masukan yang digunakan untuk proses pembelajaran.
  - **Target Output:** Label atau nilai target yang ingin diprediksi.
- Model mempelajari hubungan antara input dan target output untuk menghasilkan prediksi terhadap data baru.

Dua permasalahan utama dalam *Supervised Learning*:

1. **Classification**
   - Digunakan untuk memprediksi kategori atau kelas suatu data.
   - Contoh penerapan:
     - Mengklasifikasikan daun menjadi sehat atau sakit.
     - Mengidentifikasi jenis spesies tanaman.
     - Mengklasifikasikan citra jaringan menjadi jaringan normal atau abnormal.

2. **Regression**
   - Digunakan untuk memprediksi nilai numerik atau kontinu.
   - Contoh penerapan:
     - Memprediksi tinggi tanaman.
     - Memperkirakan konsentrasi suatu senyawa.
     - Memprediksi tingkat pertumbuhan organisme.

### B. Unsupervised Learning

*Unsupervised Learning* merupakan metode pembelajaran mesin yang menggunakan data tanpa label (*unlabeled data*).

- Tujuan utama:
  - Menemukan pola tersembunyi dalam data.
  - Mengidentifikasi struktur atau hubungan dalam data.
  - Mengelompokkan data berdasarkan kemiripan karakteristik.
- Contoh penerapan:
  - Mengelompokkan spesies berdasarkan karakteristik biologis.
  - Mengidentifikasi kelompok gen berdasarkan pola ekspresi.
  - Mengelompokkan sampel biologis berdasarkan kemiripan karakteristik.
- Salah satu metode yang sering digunakan:
  - **Clustering:** Mengelompokkan data berdasarkan kemiripan karakteristik.
    - Contoh algoritma: K-Means.

### C. Reinforcement Learning

*Reinforcement Learning* merupakan pendekatan pembelajaran mesin yang melibatkan interaksi antara agen (*agent*) dan lingkungan (*environment*).

- Proses pembelajaran:
  - Agen melakukan tindakan (*action*) terhadap lingkungan.
  - Lingkungan memberikan umpan balik (*feedback*).
  - Umpan balik diberikan dalam bentuk:
    - **Reward:** Penghargaan atas tindakan yang tepat.
    - **Penalty:** Hukuman atas tindakan yang kurang tepat.
  - Agen mempelajari strategi untuk memperoleh reward maksimal.
- Contoh penerapan dalam biologi:
  - Optimasi strategi eksperimen biologis.
  - Optimasi proses desain molekul.
  - Pengembangan strategi pengendalian dalam sistem biologis.

## Tahapan Kerja AI dalam Aplikasi Biologi

Secara umum, penerapan *Artificial Intelligence* (AI) dalam bidang biologi melibatkan beberapa tahapan utama sebagai berikut:

### 1. Data Collection (Pengumpulan Data)

Mengumpulkan data biologis sesuai dengan permasalahan yang akan diselesaikan.

- Contoh pengumpulan data:
  - Mengumpulkan citra daun tanaman.
  - Mengambil sampel sekuens DNA.
  - Mengumpulkan data pertumbuhan tanaman.

### 2. Data Preprocessing (Prapemrosesan Data)

Melakukan persiapan dan pengolahan data sebelum digunakan untuk melatih model AI.

- Tahapan prapemrosesan:
  - Membersihkan data yang tidak valid.
  - Menangani data yang hilang (*missing values*).
  - Melakukan normalisasi data (*normalization*).
  - Mengubah ukuran citra (*image resizing*).
  - Melakukan anotasi dan pelabelan data (*data annotation and labeling*).

### 3. Feature Extraction (Ekstraksi Fitur)

Mengidentifikasi atau mengekstraksi karakteristik penting dari data biologis yang digunakan dalam proses pembelajaran model.

- Contoh fitur biologis:
  - Warna, tekstur, dan bentuk daun.
  - Kandungan atau komposisi sekuens biologis.
  - Karakteristik ekspresi gen.
- Pada pendekatan *Deep Learning*:
  - Ekstraksi fitur dapat dipelajari secara otomatis oleh model.
  - Model mampu mempelajari representasi fitur dari data tanpa harus menentukannya secara manual.

### 4. Model Training (Pelatihan Model)

Melatih model AI menggunakan data yang telah dipersiapkan untuk mempelajari pola dan hubungan dalam data biologis.

- Contoh algoritma yang digunakan:
  - **Decision Tree**
  - **Random Forest**
  - **Support Vector Machine (SVM)**
  - **K-Nearest Neighbors (KNN)**
  - **Artificial Neural Network (ANN)**
  - **Convolutional Neural Network (CNN)**

### 5. Model Evaluation (Evaluasi Model)

Mengevaluasi performa model menggunakan data pengujian (*testing data*) yang tidak digunakan selama proses pelatihan.

- Metrik evaluasi yang umum digunakan:
  - **Accuracy:** Mengukur proporsi prediksi yang benar.
  - **Precision:** Mengukur ketepatan prediksi pada kelas positif.
  - **Recall:** Mengukur kemampuan model dalam menemukan seluruh data positif.
  - **F1-Score:** Mengukur keseimbangan antara precision dan recall.
  - **Confusion Matrix:** Menampilkan perbandingan hasil prediksi dengan kelas sebenarnya.
  - **Mean Squared Error (MSE):** Mengukur rata-rata kuadrat kesalahan prediksi.
- Pemilihan metrik evaluasi harus disesuaikan dengan karakteristik permasalahan biologis yang diteliti.

### 6. Prediction and Interpretation (Prediksi dan Interpretasi)

Menggunakan model yang telah dilatih dan dievaluasi untuk menghasilkan prediksi serta menginterpretasikan hasilnya dalam konteks biologis.

- Contoh penerapan:
  - Mengidentifikasi jenis penyakit tanaman.
  - Mengklasifikasikan jenis sel.
  - Memprediksi karakteristik suatu protein.

## Contoh: Klasifikasi Breast Cancer Menggunakan Machine Learning

Pada contoh ini, kita akan mengembangkan model Machine Learning untuk mengklasifikasikan tumor payudara ke dalam dua kategori, yaitu **jinak (benign)** dan **ganas (malignant)**.

Dataset yang digunakan adalah [**Breast Cancer Wisconsin Dataset**](https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic) yang tersedia secara langsung melalui library Scikit-learn.

## Tantangan dan Keterbatasan AI dalam Biologi

Meskipun memiliki potensi besar, penerapan *Artificial Intelligence* (AI) dalam bidang biologi masih menghadapi sejumlah tantangan dan keterbatasan.

1. **Ketersediaan Data (*Data Availability*)**
   - Tidak semua permasalahan biologis memiliki dataset yang cukup besar.
   - Dataset yang tersedia belum tentu representatif terhadap kondisi biologis yang sebenarnya.

2. **Kualitas Data (*Data Quality*)**
   - Kesalahan pengukuran dapat memengaruhi keakuratan data.
   - Kesalahan anotasi dan proses pengumpulan data dapat menurunkan performa model.

3. **Ketidakseimbangan Data (*Data Imbalance*)**
   - Distribusi jumlah sampel antar kelas sering kali tidak seimbang.
   - Kondisi ini dapat menyebabkan model lebih cenderung memprediksi kelas dengan jumlah sampel yang lebih dominan.

4. **Interpretabilitas Model (*Model Interpretability*)**
   - Beberapa model, khususnya *Deep Learning*, sulit dijelaskan proses pengambilan keputusannya.
   - Hal ini menyulitkan peneliti dalam memahami alasan di balik hasil prediksi model.

5. **Sumber Daya Komputasi (*Computational Resources*)**
   - Pelatihan model yang kompleks membutuhkan sumber daya komputasi yang besar.
   - Kebutuhan tersebut dapat mencakup:
     - Kapasitas CPU dan GPU.
     - Memori komputer (RAM).
     - Kapasitas penyimpanan data.

6. **Validasi Biologis (*Biological Validation*)**
   - Hasil prediksi AI tetap memerlukan validasi berdasarkan pengetahuan biologis.
   - Validasi dapat dilakukan melalui:
     - Kajian literatur ilmiah.
     - Pengujian atau eksperimen biologis.
     - Perbandingan dengan hasil penelitian sebelumnya.

7. **Isu Etika dan Privasi (*Ethical and Privacy Issues*)**
   - Penggunaan data biologis dan genomik harus memperhatikan:
     - Privasi individu.
     - Keamanan data.
     - Persetujuan penggunaan data.
     - Etika dalam penelitian biologis.

### Catatan Penting (*Important Note*)

- AI bukan pengganti penelitian dan validasi biologis.
- AI merupakan alat bantu komputasi yang dapat mendukung:
  - Proses analisis data biologis.
  - Prediksi karakteristik dan fenomena biologis.
  - Identifikasi pola tersembunyi dalam data.
  - Pengambilan keputusan dalam penelitian biologi.
- Hasil yang diperoleh dari AI tetap harus diinterpretasikan dan divalidasi berdasarkan prinsip serta pengetahuan biologis.
