# Analisis Ekspresi Gen untuk Klasifikasi Kanker dan Pengelompokan Sampel Berbasis Machine Learning

**Deskripsi.** Proyek ini memanfaatkan data aktivitas (ekspresi) ribuan gen dari basis data terbuka NCBI GEO (GSE9476) untuk membedakan sampel leukemia mieloid akut (AML) dari sel sumsum tulang/darah normal menggunakan pembelajaran mesin. Sel kanker memiliki pola aktivitas gen yang berbeda dari sel normal, tetapi jumlah fitur (±22 ribu probe) jauh lebih banyak daripada jumlah sampel pasien (64 sampel). Karena itu analisis ini menerapkan pemodelan terarah (supervised) dengan seleksi fitur untuk menyaring gen penanda biologis (biomarker) utama, sekaligus metode pengelompokan tanpa arahan (unsupervised: PCA, K-Means, Hierarchical Clustering) untuk melihat apakah sampel kanker dan normal terpisah secara alami, lalu membandingkannya dengan literatur medis.

Dataset: NCBI GEO **GSE9476**, microarray Affymetrix HG-U133A (GPL96), 64 sampel (opsi #5 pada tugas: *Gene expression*).

## Struktur
```
data/        cel_header_names.csv  (+ file unduhan otomatis: series matrix, GPL96.annot.gz)
notebooks/   GSE9476_ML_Biologi.ipynb   <- jalankan ini (Restart & Run All)
r/           rma_from_cel.R            <- opsi B: RMA dari CEL mentah
figures/ results/                      <- dibuat otomatis oleh notebook
requirements.txt
```
CEL mentah (`GSE9476_RAW.tar`, 225 MB) jangan di-commit ke GitHub; taruh di `.gitignore`.

## Cara menjalankan
1. `pip install -r requirements.txt`
2. `jupyter notebook notebooks/GSE9476_ML_Biologi.ipynb` lalu *Restart & Run All* (perlu internet pada run pertama).
3. Periksa tabel silang label di Tahap 2.2. Label dibuat dengan regex dan harus dikonfirmasi.

## Kerangka laporan (3-5 halaman, isi angka dari output notebook Anda)
1. **Latar belakang**: AML, mengapa ekspresi gen berguna, rumusan pertanyaan (Tahap 1).
2. **Data & EDA**: 64 sampel, ±22 ribu probe, proporsi kelas, 4 gambar EDA.
3. **Metode**: Pipeline (imputasi, filter variansi, scaling, SelectKBest), 4 model, 5-fold CV, GridSearchCV, nested CV, uji permutasi; PCA, K-Means (silhouette), Ward.
4. **Hasil**: tabel CV (rata-rata ± std), evaluasi test, PCA/klaster vs label.
5. **Interpretasi**: gen teratas (DE, koefisien, loading PC1) dan kesesuaian dengan literatur.
6. **Diskusi & keterbatasan**: lihat Tahap 7.
7. **Kesimpulan**.
