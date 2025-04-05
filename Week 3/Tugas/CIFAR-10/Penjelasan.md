# Penjelasan Metrik Evaluasi pada Proyek CNN dan MLP

## 1. Akurasi (Accuracy)

**Rumus:**
```
Accuracy = Jumlah Prediksi Benar / Total Prediksi
```

**Penjelasan:**
Mengukur seberapa sering model memprediksi dengan benar dari seluruh data.

## 2. Presisi (Precision)

**Rumus:**
```
Precision = TP / (TP + FP)
```

**Penjelasan:**
Presisi menunjukkan proporsi prediksi positif yang benar. Cocok untuk menghindari terlalu banyak false positive.

## 3. Recall

**Rumus:**
```
Recall = TP / (TP + FN)
```

**Penjelasan:**
Recall menunjukkan proporsi data positif yang berhasil dikenali oleh model. Penting untuk menghindari false negative.

## 4. F1-Score

**Rumus:**
```
F1 = 2 * (Precision * Recall) / (Precision + Recall)
```

**Penjelasan:**
F1-Score adalah rata-rata harmonik dari presisi dan recall. Digunakan saat kita butuh keseimbangan antara keduanya.

## 5. AUC (Area Under Curve)

**Penjelasan:**
AUC mengukur area di bawah kurva ROC. Semakin besar nilai AUC, semakin baik performa model. Untuk multi-kelas, biasanya dihitung dengan pendekatan One-vs-Rest.

## 6. ROC (Receiver Operating Characteristic)

**Rumus dasar:**
```
TPR = TP / (TP + FN)
FPR = FP / (FP + TN)
```

**Penjelasan:**
ROC menggambarkan hubungan antara True Positive Rate dan False Positive Rate. Tidak digambarkan dalam proyek ini, tapi AUC-nya tetap dihitung.
