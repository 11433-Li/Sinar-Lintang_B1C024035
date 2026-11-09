# 📄 Mini Assignment

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

Seluruh file Mini Assignment wajib ditempatkan pada direktori berikut di repository hasil fork masing-masing:

`assignments/01-mini-project/`

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
```
**6. Buat Pull Request**
- Buka repository hasil fork.
- Pilih menu Contribute → Open pull request atau New Pull Request.
- Pastikan target repository adalah repository utama uckypradestha/aibiology.
- Pilih branch assignment sebagai source branch.
- Isi judul dan deskripsi Pull Request sesuai ketentuan berikut.

**Format judul Pull Request:**

`[Mini Assignment] Nama Lengkap - NIM`

Contoh:

`[Mini Assignment] Ucky Pradestha - H1D022001`

**Format deskripsi Pull Request:**

Gunakan template berikut pada deskripsi PR:

```
## Identitas Mahasiswa
- Nama:
- NIM:
- Kelas:

## Deskripsi Assignment
Implementasi dan perbandingan algoritma Logistic Regression dan Random Forest Classifier untuk klasifikasi kanker.

## Eksperimen
- [x] Pembagian dataset 70% training dan 30% testing
- [x] Implementasi Logistic Regression
- [x] Implementasi Random Forest Classifier
- [x] Perbandingan accuracy, precision, recall, dan F1-score
- [x] Confusion Matrix kedua algoritma
- [x] Analisis hasil eksperimen
- [x] Kesimpulan

## File Pengumpulan
- Source code:
- Hasil eksperimen:
- Dokumentasi:

## Pernyataan
Saya menyatakan bahwa pekerjaan ini merupakan hasil pengerjaan dan pemahaman saya sendiri.
```

**7. Submit Pull Request**
- Periksa kembali seluruh file yang dikumpulkan.
- Pastikan notebook dapat dijalankan tanpa error.
- Klik Create Pull Request.
- Pastikan status Pull Request terbuka (Open) dan bukan Draft.
- Jangan melakukan merge secara mandiri. Proses pemeriksaan dan merge dilakukan oleh dosen/asisten praktikum

## Ketentuan Tambahan
1. Setiap mahasiswa wajib mengumpulkan tugas melalui akun GitHub masing-masing.
2. Satu mahasiswa hanya diperbolehkan mengajukan satu Pull Request untuk Mini Assignment ini.
3. Pengumpulan wajib menyertakan source code dan hasil eksekusi, bukan hanya kode program tanpa hasil.
4. Notebook harus memiliki output hasil eksperimen yang dapat diperiksa.
5. Hasil evaluasi harus berasal dari eksperimen yang benar-benar dilakukan, bukan angka yang dibuat atau disalin dari mahasiswa lain.
6. Mahasiswa wajib memberikan analisis terhadap hasil klasifikasi, khususnya perbedaan precision dan recall dalam konteks deteksi kanker.
7. Pull Request yang tidak mengikuti struktur pengumpulan dapat diminta untuk diperbaiki.
8. Perbaikan dapat dilakukan dengan melakukan commit dan push kembali ke branch yang sama. Perubahan tersebut akan otomatis masuk ke Pull Request yang sudah diajukan.

## Ketentuan Pengumpulan melalui LMS ELDIRU

Selain mengajukan Pull Request (PR) ke repository GitHub utama, setiap mahasiswa **wajib mengumpulkan tugas melalui LMS eLdiru** pada kolom penugasan sebagai bukti pengumpulan resmi mini project.

Ketentuan pengumpulan:

1. Mahasiswa wajib mengunggah file notebook (`.ipynb`) yang telah dikerjakan dan dilengkapi dengan hasil eksekusi ke LMS eLdiru.
2. Mahasiswa wajib menyertakan tautan Pull Request (PR) GitHub yang telah diajukan ke repository utama.
3. Pastikan tautan PR dapat diakses dan mengarah ke Pull Request masing-masing mahasiswa.
4. Pastikan file yang diunggah ke LMS eLdiru merupakan versi terbaru yang sama dengan file pada repository GitHub.
5. Pengumpulan melalui GitHub PR dan LMS eLdiru **keduanya wajib dilakukan**.
6. Tugas dinyatakan lengkap apabila mahasiswa telah mengumpulkan file melalui LMS eLdiru dan berhasil mengajukan Pull Request ke repository utama.
7. Pengumpulan yang hanya dilakukan melalui salah satu platform dianggap belum memenuhi ketentuan pengumpulan.

**File yang dikumpulkan melalui LMS eLdiru:**

- File notebook (`.ipynb`) yang berisi source code dan hasil eksperimen.
- Tautan Pull Request (PR) GitHub masing-masing mahasiswa.

**Catatan:** Pastikan pengumpulan pada LMS eLdiru dilakukan sebelum tenggat waktu yang telah ditentukan.

## Aspek Penilaian
| No. | Komponen Penilaian | Bobot |
|:---:|---|:---:|
| 1 | Kesesuaian hasil pengerjaan dengan luaran yang diminta | 50% |
| 2 | Kelengkapan Dokumentasi dan kerapihan struktur file serta kepatuhan terhadap prosedur pengumpulan melalui GitHub Pull Request dan LMS ELDIRU. | 50% |
| | **Total** | **100%** |
