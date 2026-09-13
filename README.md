# Mushroom Classification — Take-Home Challenge

## 📌 Overview
Proyek ini menjawab pertanyaan: **"Can Machine Learning Identify Whether a Mushroom is Edible or Poisonous?"**

Menggunakan dataset karakteristik fisik jamur, notebook ini membangun dan membandingkan beberapa model Machine Learning (Logistic Regression, Decision Tree, Random Forest) dan satu model Deep Learning (Neural Network) untuk mengklasifikasikan jamur sebagai **Edible (dapat dimakan)** atau **Poisonous (beracun)**, dilengkapi dengan EDA, preprocessing, hyperparameter tuning, model interpretation, dan eksplorasi regresi eksperimental.

## 📂 Dataset
- **File:** `mushrooms.csv` (8.124 baris, 23 kolom, seluruhnya kategorikal)
- **Target:** `class` → `e` = Edible, `p` = Poisonous
- **Sumber Dataset:** [UCI Mushroom Classification — Kaggle](https://www.kaggle.com/datasets/uciml/mushroom-classification/data)

> Dataset digunakan sesuai ketentuan penyelenggara. Seluruh hak cipta dataset tetap menjadi milik pemilik/sumber aslinya (UCI Machine Learning Repository, dipublikasikan ulang melalui Kaggle).

## 🧪 Metodologi
1. **Problem Definition** — mendefinisikan masalah sebagai binary classification.
2. **Data Understanding** — struktur, tipe data, unique value, target distribution.
3. **EDA** — distribusi target & fitur, hubungan fitur vs target (`odor`, `bruises`, `gill-size`, `habitat`, dll).
4. **Data Preprocessing** — penanganan nilai `?` pada `stalk-root`, pengecekan duplikat, penghapusan fitur konstan (`veil-type`), Label Encoding.
5. **Modeling** — Logistic Regression (baseline), Decision Tree, Random Forest, Neural Network (Keras/TensorFlow).
6. **Evaluation & Comparison** — Accuracy, Precision, Recall, F1 Score, Confusion Matrix untuk seluruh model.
7. **Hyperparameter Tuning** — `GridSearchCV` pada Random Forest.
8. **Model Interpretation** — Feature Importance & Permutation Importance.
9. **Regression Exploration** — target numerik eksperimental `rarity_score` (bukan sekadar e/p → 0/1) untuk mendemonstrasikan regresi yang metodologis benar, sekaligus menjelaskan mengapa dataset ini pada dasarnya adalah Classification Problem.

## 📊 Hasil Utama (Test Set)

| Model | Accuracy | Precision | Recall | F1 Score |
|---|---|---|---|---|
| Logistic Regression | ~95.4% | ~96.0% | ~94.5% | ~95.2% |
| Decision Tree | 100% | 100% | 100% | 100% |
| Random Forest | 100% | 100% | 100% | 100% |
| Neural Network | 100% | 100% | 100% | 100% |

Dataset Mushroom (UCI) dikenal separable secara sempurna menggunakan kombinasi fitur kategorikalnya — khususnya `odor`, `gill-color`, `gill-size`, `spore-print-color`, dan `ring-type` — sehingga model tree-based dan neural network dapat mencapai performa sempurna tanpa indikasi overfitting.

## 🏁 Kesimpulan
**Ya**, Machine Learning dapat mengidentifikasi status keamanan konsumsi jamur dengan akurasi sangat tinggi berdasarkan ciri fisiknya. Namun, mengingat konsekuensi fatal dari kesalahan klasifikasi di dunia nyata, model ini sebaiknya diposisikan sebagai **alat bantu skrining**, bukan pengganti verifikasi ahli mikologi. Penjelasan lengkap, termasuk seluruh insight EDA, analisis interpretasi model, dan pembahasan mendalam ada di dalam notebook.

## 📁 Struktur Repository
```
Mushroom-Classification/
│
├── data/
│   └── mushrooms.csv
│
├── notebook/
│   └── Nama_NIM_TakeHomeML.ipynb
│
└── README.md
```

## 🤖 Penggunaan AI
Sesuai ketentuan tugas, AI (Claude) digunakan sebagai asisten belajar untuk membantu menyusun kode, analisis, dan narasi di dalam notebook. Seluruh keputusan metodologis (preprocessing, pemilihan model, interpretasi hasil) tetap perlu dipahami dan dapat dipertanggungjawabkan oleh peserta.

---
*Catatan: Ganti "Nama_NIM_TakeHomeML.ipynb" dan bagian "Nama / NIM / Jurusan" pada notebook dengan data diri Anda sebelum submission.*
