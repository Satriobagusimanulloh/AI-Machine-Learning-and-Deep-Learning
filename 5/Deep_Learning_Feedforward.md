# **Deep Learning Feedforward**

## **Perceptron Feedforward**
Perceptron feedforward adalah model dasar dari jaringan saraf atau blok struktural dari deep learning.

### **Cara Kerjanya**
Perceptron menjumlahkan semua input dikali dengan bobot mereka masing-masing, kemudian menambahkan bias. Setelah itu, fungsi aktivasi non-linear diterapkan pada jumlah dengan bias untuk menghasilkan prediksi.

### **Ilustrasi**
![Perceptron](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*6HtyqOTYyYUzUeERVXL8Ag.png)

### **Formula**
![Formula Perceptron](https://miro.medium.com/v2/resize:fit:1088/format:webp/0*KDSWamHw3Eb9Rcys)

## **Fungsi Non-Linearitas**
Fungsi non-linearitas memasukkan non-linearitas ke dalam output model. Fungsi non-linearitas umum meliputi:
- Fungsi sigmoid (biasanya digunakan untuk klasifikasi biner)
- Fungsi ReLU (rentang output antara 0, ∞)
- Fungsi tanh (rentang output antara -1, 1)
- dan lain-lain

## **Perceptron Multi-Output**
![Perceptron Multi-Output](https://makshay.com/static/43efa5a81e1d4372ab48ebacd4414b88/89552/multi_output_perceptron.png)

Penjelasan:
- x = input
- z = operasi linear
- y = output
- Semua input terhubung ke semua output, disebut lapisan padat/sepenuhnya terhubung.

## **Jaringan Saraf Dalam**
Jaringan saraf dalam adalah jenis jaringan dengan banyak lapisan tersembunyi antara lapisan input dan output. Ini memungkinkan pembelajaran fitur yang lebih kompleks.

## **Fungsi Kerugian**
Hasil yang dihasilkan oleh model jaringan saraf tidak selalu benar. Oleh karena itu, diperlukan metrik untuk mengukur seberapa baik model memprediksi nilai target yang benar, dikenal sebagai fungsi kerugian.

### **Jenis-Jenis Fungsi Kerugian**
- Mean Squared Error (MSE): Biasanya digunakan untuk model regresi.
- Mean Absolute Error (MAE): Biasanya digunakan untuk model regresi.
- Cross-Entropy Loss: Biasanya digunakan untuk model klasifikasi.
- Binary Cross-Entropy Loss: Biasanya digunakan untuk model klasifikasi biner.
- K-means Loss: Biasanya digunakan untuk model pengelompokan.
- dan lain-lain

## **Gradient Descent**
Setelah menentukan nilai kerugian dalam model, kita perlu meningkatkannya menggunakan fungsi optimisasi, salah satunya adalah gradient descent.

### **Formula Gradient Descent**
**W_baru = W_lama - lr * dJ/dW**

Penjelasan:
- W_baru = bobot baru
- W_lama = bobot lama
- lr = tingkat pembelajaran
- dJ/dW = turunan fungsi kerugian terhadap bobot

### **Contoh**
Misalnya, untuk nilai (W = 3)
J(W) = W^2
dJ/dW = 2W (turunan dari J(W))
lr = tingkat pembelajaran
- W_baru = W_lama - lr * dJ/dW
- W_baru = 3 - lr * 2W
- W_baru = 3 - lr * (2x3)
- W_baru = 3 - 6lr

## **Kesimpulan Gradient Descent**
- Jika nilai dJ/dW positif, itu menunjukkan bahwa nilai W terlalu besar (slope positif).
- Jika nilai dJ/dW negatif, itu menunjukkan bahwa nilai W terlalu kecil (slope negatif).
- Keduanya bergerak menuju nilai minimum (fungsi kerugian).
- Tingkat pembelajaran kecil membutuhkan waktu lama dan umumnya tidak mencapai nilai minimum fungsi kerugian.
- Tingkat pembelajaran besar membutuhkan waktu singkat dan bisa melampaui nilai minimum fungsi kerugian.

## **Implementasi di PyTorch - Model Feedforward**
Notebook Google Colab yang disediakan (`5_1_Deep_Learning_Feedforward_PyTorch.ipynb` dan `5_2_Deep_Learning_Feedforward_PyTorch.ipynb`) menunjukkan implementasi jaringan saraf feedforward menggunakan PyTorch. Notebook ini mencakup pembuatan model feedforward untuk berbagai tugas.

### **Komponen-Komponen Utama:**
- Definisi model PyTorch untuk jaringan saraf feedforward.
- Loop pelatihan menggunakan optimisasi gradient descent.
- Evaluasi pada dataset uji.
- Visualisasi metrik pelatihan dan validasi.

Implementasi ini menawarkan contoh praktis membangun dan melatih jaringan saraf feedforward menggunakan kerangka kerja PyTorch.

## **Implementasi di TensorFlow - Model Feedforward**
Notebook Google Colab yang disediakan (`5_1_Deep_Learning_Feedforward_TensorFlow.ipynb`, `5_2_Deep_Learning_Feedforward_TensorFlow.ipb`, dan `5_3_Deep_Learning_Feedforward_TensorFlow.ipb`) memperlihatkan implementasi jaringan saraf feedforward menggunakan TensorFlow. Notebook ini mencakup pembuatan model feedforward untuk aplikasi yang berbeda.

### **Komponen-Komponen Utama:**
- Pembuatan model TensorFlow dengan lapisan Dense.
- Kompilasi model dan pelatihan menggunakan optimisasi gradient descent.
- Visualisasi akurasi/kerugian pelatihan dan validasi menggunakan Matplotlib.

Implementasi ini berfungsi sebagai panduan praktis dalam membangun dan melatih jaringan saraf feedforward menggunakan kerangka kerja TensorFlow.

Jika Anda memiliki pertanyaan lebih lanjut atau memerlukan bantuan tambahan, jangan ragu untuk bertanya!