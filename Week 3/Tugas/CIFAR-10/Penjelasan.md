# Penjelasan Metrik Evaluasi pada Proyek CNN dan MLP (CIFAR-10 & SVHN)

Dokumen ini berisi penjelasan setiap metrik evaluasi yang digunakan dalam proyek klasifikasi gambar menggunakan CNN dan MLP, baik dengan framework PyTorch maupun TensorFlow, pada dataset CIFAR-10 dan SVHN.

---

## ✪ 1. Akurasi (Accuracy)

### Rumus:
\[
\text{Accuracy} = \frac{\text{Jumlah Prediksi Benar}}{\text{Total Prediksi}}
\]

### Penjelasan:
Akurasi mengukur seberapa sering model membuat prediksi yang benar secara keseluruhan. Contoh: jika model memprediksi 80 dari 100 gambar dengan benar, maka akurasinya adalah 80%.

---

## ✪ 2. Presisi (Precision)

### Rumus:
\[
\text{Precision} = \frac{TP}{TP + FP}
\]

### Penjelasan:
Presisi menunjukkan seberapa banyak prediksi positif yang benar-benar positif. Berguna dalam konteks di mana kesalahan positif (false positive) harus diminimalkan. Untuk multi-kelas, digunakan rata-rata **macro**.

- **TP (True Positive):** Prediksi benar sebagai positif  
- **FP (False Positive):** Prediksi salah sebagai positif

---

## ✪ 3. Recall

### Rumus:
\[
\text{Recall} = \frac{TP}{TP + FN}
\]

### Penjelasan:
Recall menunjukkan seberapa banyak data positif yang berhasil dikenali oleh model. Berguna untuk menghindari kesalahan negatif (false negative). Untuk multi-kelas, digunakan rata-rata **macro**.

- **FN (False Negative):** Label positif yang tidak terdeteksi

---

## ✪ 4. F1-Score

### Rumus:
\[
\text{F1} = 2 \times \frac{\text{Precision} \times \text{Recall}}{\text{Precision} + \text{Recall}}
\]

### Penjelasan:
F1-Score adalah rata-rata harmonik dari Precision dan Recall. Digunakan ketika kita ingin keseimbangan antara keduanya, terutama saat data tidak seimbang.

---

## ✪ 5. AUC (Area Under Curve)

### Rumus (konseptual):
\[
\text{AUC} = \int_0^1 \text{TPR}(FPR) \, dFPR
\]

### Penjelasan:
AUC mengukur area di bawah kurva ROC. Dalam multi-class, AUC dihitung dengan pendekatan **One-vs-Rest (OvR)** dan mengambil rata-rata dari semua kelas.

---

## ✪ 6. ROC (Receiver Operating Characteristic)

### Definisi TPR dan FPR:
\[
\text{TPR (Recall)} = \frac{TP}{TP + FN}
\]
\[
\text{FPR} = \frac{FP}{FP + TN}
\]

### Penjelasan:
Kurva ROC menggambarkan hubungan antara True Positive Rate (Recall) dan False Positive Rate. Walaupun kurva ROC tidak ditampilkan di proyek ini, nilai AUC-nya tetap dihitung untuk menilai kinerja model secara menyeluruh.

---

> Catatan: Semua metrik di atas dihitung dengan pendekatan macro-average untuk multi-class classification (10 kelas) seperti pada CIFAR-10 dan SVHN.

---

**Lisensi**: Bebas digunakan untuk keperluan belajar dan dokumentasi projek ML/Data Science.

