# Mini Assignment

Berdasarkan contoh yang telah dilakukan, kerjakan tugas berikut:
- Ubah pembagian dataset menjadi 70% training dan 30% testing.
- Ganti algoritma Logistic Regression dengan Random Forest Classifier.
- Bandingkan hasil akurasi Logistic Regression dan Random Forest.
- Tampilkan Confusion Matrix dari kedua algoritma.
- Analisis algoritma mana yang memberikan hasil klasifikasi lebih baik.
- Jelaskan mengapa evaluasi model tidak cukup hanya menggunakan accuracy dalam konteks klasifikasi kanker.

## Expected Output
Mahasiswa harus mengumpulkan:
- Source code Python atau tautan Google Colab.
- Hasil pengujian kedua algoritma.
- Perbandingan accuracy, precision, recall, dan F1-score.
- Confusion Matrix.
- Kesimpulan hasil eksperimen.

## Pengumpulan Mini Assignment melalui GitHub Pull Request (PR)
Pengumpulan Mini Assignment dilakukan menggunakan mekanisme **GitHub Pull Request (PR)** melalui repository praktikum berikut:

**Repository:** [uckypradestha/aibiology](https://github.com/uckypradestha/aibiology)

Setiap mahasiswa wajib melakukan *fork* repository, mengerjakan assignment pada repository masing-masing, kemudian mengajukan Pull Request ke repository utama untuk proses pemeriksaan dan penilaian.

### A. Ketentuan Pengumpulan

**1. Fork Repository**

- Buka repository utama: https://github.com/uckypradestha/aibiology.
- Klik tombol **Fork** untuk menyalin repository ke akun GitHub masing-masing.
- Pastikan repository hasil fork tersedia pada akun GitHub pribadi.

**2. Buat Branch Assignment**

Buat branch baru khusus untuk mengerjakan Mini Assignment dengan format:

`mini-assignment/nama-nim`

Contoh:

`mini-assignment/ucky-123456`

**3. Kerjakan Assignment**

- Kerjakan seluruh instruksi yang terdapat pada Mini Assignment.
- Gunakan Python atau Google Colab untuk implementasi dan pengujian.
- Gunakan pembagian dataset yang sama untuk kedua algoritma, yaitu 70% training dan 30% testing.
- Implementasikan Logistic Regression dan Random Forest Classifier.
- Sertakan hasil evaluasi, Confusion Matrix, serta analisis perbandingan kedua algoritma.

**4. Struktur File Pengumpulan**

Simpan hasil pekerjaan pada folder berikut:

    aibiology/
    └── assignments/
        └── mini-assignment/
            └── nama-nim/
                ├── README.md
                ├── mini_assignment.ipynb
                └── results/
                    ├── confusion_matrix.png
                    └── evaluation_results.png

Keterangan:

| File/Folder | Keterangan |
|---|---|
| `README.md` | Identitas mahasiswa, deskripsi eksperimen, hasil evaluasi, dan kesimpulan. |
| `mini_assignment.ipynb` | Source code Python beserta hasil eksekusi. |
| `results/` | Visualisasi Confusion Matrix dan hasil evaluasi kedua algoritma. |

**5. Commit dan Push**

Setelah seluruh pekerjaan selesai, lakukan commit dan push ke branch assignment masing-masing.

```bash
git add .
git commit -m "Add mini assignment - Nama NIM"
git push origin mini-assignment/nama-nim

### Ketentuan Tambahan
1. Setiap mahasiswa wajib mengumpulkan tugas melalui akun GitHub masing-masing.
2. Satu mahasiswa hanya diperbolehkan mengajukan satu Pull Request untuk Mini Assignment ini.
3. Pengumpulan wajib menyertakan source code dan hasil eksekusi, bukan hanya kode program tanpa hasil.
4. Notebook harus memiliki output hasil eksperimen yang dapat diperiksa.
5. Hasil evaluasi harus berasal dari eksperimen yang benar-benar dilakukan, bukan angka yang dibuat atau disalin dari mahasiswa lain.
6. Mahasiswa wajib memberikan analisis terhadap hasil klasifikasi, khususnya perbedaan precision dan recall dalam konteks deteksi kanker.
7. Pull Request yang tidak mengikuti struktur pengumpulan dapat diminta untuk diperbaiki.
8. Perbaikan dapat dilakukan dengan melakukan commit dan push kembali ke branch yang sama. Perubahan tersebut akan otomatis masuk ke Pull Request yang sudah diajukan.
