# **Deep Learning Backward**

## **Backpropagation dalam Deep Learning**
Backpropagation adalah metode yang digunakan dalam pembelajaran mesin untuk melatih jaringan saraf tiruan. Metode ini memungkinkan jaringan saraf untuk memperbarui bobotnya guna menghasilkan prediksi yang lebih akurat untuk data pelatihan.

### **Langkah-Langkah Backpropagation:**
1. Inisialisasi bobot dan bias secara acak pada awal pelatihan.
2. Penerusan: Data input dilewatkan melalui jaringan untuk menghasilkan prediksi. Setiap neuron melakukan komputasi berdasarkan bobot dan fungsi aktivasi.
3. Hitung perbedaan antara output yang diprediksi dan nilai sebenarnya; perbedaan ini adalah kesalahan.
4. Penerusan mundur: Propagasi kesalahan ke belakang melalui jaringan. Perbarui bobot dan bias berdasarkan kesalahan menggunakan gradien descresi.
5. Sesuaikan bobot dan bias untuk meminimalkan kesalahan. Tingkat pembelajaran (learning rate) memengaruhi besaran penyesuaian ini.
6. Ulangi langkah-langkah 2 hingga 5 untuk seluruh dataset pelatihan (epoch). Pelatihan berhenti ketika kesalahan sudah cukup kecil atau setelah jumlah epoch tertentu.

### **Fungsi Aktivasi:**
Fungsi aktivasi menentukan apakah suatu neuron harus menghasilkan output. Fungsi aktivasi umum meliputi sigmoid, tanh, dan ReLU.

### **Gradient Descent dalam Backpropagation:**
Gradient descent digunakan untuk menemukan nilai minimum dari fungsi kesalahan. Dalam backpropagation, ini digunakan untuk menyesuaikan bobot dan bias guna meminimalkan kesalahan.

#### **Formulas:**
- **Perhitungan Gradien untuk Bobot (W):**
  dL/dWij = δj . ai
  Dimana:
  - L = fungsi kerugian
  - Wij = bobot dari neuron i ke j
  - δj = gradien kesalahan pada neuron j
  - ai = Output dari neuron i

- **Perhitungan Gradien untuk Bias (b):**
  dL/dbj = δj
  Dimana:
  - δj = gradien kesalahan pada neuron j
  - bj = bias pada neuron j

- **Perhitungan Gradien untuk Kesalahan Neuron Tersembunyi (δj):**
  δj = f′(zj)∑k (Wjk.δk)
  Dimana:
  - δj = Gradien kesalahan pada neuron j
  - f′(zj) = Turunan dari fungsi aktivasi pada neuron j
  - zj = Input total (weighted sum) pada neuron j
  - Wjk = Bobot dari neuron j ke neuron k
  - δk = Gradien kesalahan pada neuron k yang terhubung ke neuron j

## **Implementasi di PyTorch - Model LSTM**
Notebook Google Colab yang disediakan (`6_1_Deep_Learning_Backward_PyTorch.ipynb`) menunjukkan implementasi backpropagation menggunakan PyTorch. Notebook ini mencakup pembuatan model LSTM untuk analisis sentimen pada dataset IMDB.

Komponen-Komponen Utama:
- Definisi model PyTorch untuk jaringan LSTM.
- Loop pelatihan menggunakan optimisasi gradien descresi.
- Evaluasi pada dataset uji.
- Fungsi prediksi untuk analisis sentimen pada kalimat baru.

## **Implementasi di TensorFlow - Model CNN-LSTM**
Notebook Google Colab yang menyertainya (`6_1_Deep_Learning_Backward_TensorFlow.ipynb`) memamerkan implementasi backpropagation menggunakan TensorFlow. Notebook ini melibatkan pembuatan model dengan kombinasi lapisan Convolutional Neural Network (CNN) dan Long Short-Term Memory (LSTM) untuk analisis sentimen pada dataset IMDB.

Komponen-Komponen Utama:
- Pembuatan model TensorFlow dengan lapisan Embedding, Conv1D, MaxPooling1D, LSTM, dan Dense.
- Kompilasi model dan pelatihan menggunakan optimisasi gradien descresi.
- Visualisasi akurasi/kerugian pelatihan dan validasi menggunakan Matplotlib.

Implementasi ini memberikan wawasan praktis tentang penerapan backpropagation dalam deep learning menggunakan dua kerangka kerja yang umum digunakan, yaitu PyTorch dan TensorFlow. Jika Anda memiliki pertanyaan lebih lanjut atau memerlukan bantuan tambahan, jangan ragu untuk bertanya!