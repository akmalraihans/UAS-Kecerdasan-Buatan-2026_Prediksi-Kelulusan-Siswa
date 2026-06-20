# 🎓 Prediksi Kelulusan Siswa dengan Machine Learning

Proyek Machine Learning untuk memprediksi apakah seorang siswa akan **lulus** atau **tidak lulus** berdasarkan faktor demografis, sosial, dan kebiasaan belajar.

---

## 📌 Deskripsi Proyek

Proyek ini merupakan tugas UAS mata kuliah **Kecerdasan Buatan** yang mengimplementasikan algoritma Machine Learning untuk klasifikasi kelulusan siswa.

**Target Prediksi:** Siswa dinyatakan **Lulus** jika nilai akhir (G3) ≥ 10, dan **Tidak Lulus** jika G3 < 10.

---

## 📂 Struktur Repository

```
├── student_ml.ipynb          # Source code utama (Jupyter Notebook)
├── README.md                 # Dokumentasi proyek
├── student_dataset.csv       # Dataset (dibuat otomatis saat notebook dijalankan)
└── results/
    ├── confusion_matrix.png
    ├── roc_curve.png
    ├── feature_importance.png
    ├── perbandingan_model.png
    ├── eda_distribusi.png
    └── heatmap_korelasi.png
```

---

## 📊 Dataset

- **Jenis:** Dataset sintetis (dibuat secara programatik)
- **Jumlah Data:** 500 siswa ✅ (memenuhi syarat minimum 300)
- **Fitur:** 20 fitur (demografis, sosial, kebiasaan belajar)
- **Target:** Lulus (1) / Tidak Lulus (0)

### Fitur Utama

| Fitur | Deskripsi |
|-------|-----------|
| `age` | Usia siswa (15–21) |
| `Medu` / `Fedu` | Pendidikan orang tua (0–4) |
| `studytime` | Waktu belajar per minggu (1–4) |
| `failures` | Jumlah kegagalan sebelumnya (0–3) |
| `absences` | Jumlah absensi (0–29) |
| `famrel` | Kualitas hubungan keluarga (1–5) |
| `health` | Status kesehatan (1–5) |
| `internet` | Akses internet (yes/no) |

---

## ⚙️ Metodologi

```
Dataset → EDA → Preprocessing → Training → Testing → Evaluasi → Demo
```

1. **Preprocessing:** Label Encoding, StandardScaler, Split 80% train / 20% test (stratified)
2. **Training:** 3 model dibandingkan
   - ✅ **Random Forest** (model terbaik)
   - Decision Tree
   - Logistic Regression
3. **Evaluasi:** Accuracy, Confusion Matrix, Classification Report, ROC-AUC, 5-fold Cross Validation

---

## 📈 Hasil Evaluasi

| Model | Test Accuracy | CV Accuracy |
|-------|:-------------:|:-----------:|
| **Random Forest** | **~0.78** | **~0.76** |
| Logistic Regression | ~0.74 | ~0.73 |
| Decision Tree | ~0.73 | ~0.71 |

> *Nilai aktual muncul saat notebook dijalankan.*

---

## 🚀 Cara Menjalankan

### Google Colab (Direkomendasikan)

1. Buka [Google Colab](https://colab.research.google.com)
2. Upload file `student_ml.ipynb`
3. Klik **Runtime → Run All**
4. Selesai — dataset dan semua grafik dibuat otomatis

### Lokal

```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
jupyter notebook student_ml.ipynb
```

---

## 🛠️ Tech Stack

- **Python** 3.8+
- **Scikit-learn** — Machine Learning
- **Pandas & NumPy** — Data manipulation
- **Matplotlib & Seaborn** — Visualisasi
- **Google Colab / Jupyter** — Environment

---

## 🎥 Video Demo

📺 [Link Video Demo](#) *(3–5 menit)*

---

*Tugas UAS Kecerdasan Buatan – Teknik Elektro, Universitas Brawijaya 2025/2026*  
*Dosen: Dr. Raden Arief Setyawan, ST., MT*
