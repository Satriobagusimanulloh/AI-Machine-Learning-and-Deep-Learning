# **Pengenalan tentang Deep Learning**

## **1. Dasar-Dasar Deep Learning**
![AI, ML, DL](https://miro.medium.com/v2/resize:fit:4800/format:webp/0*5NrDYk8PryKASFJD)
(Sumber gambar: [Towards Data Science](https://towardsdatascience.com/understanding-the-difference-between-ai-ml-and-dl-cceb63252a6c))

- **Artificial Intelligence (AI):** Sebuah teknik yang memungkinkan komputer meniru pemikiran dan perilaku manusia.
- **Machine Learning (ML):** Sebuah teknik yang memungkinkan komputer untuk belajar atau mengenali pola dalam set data tanpa diprogram secara eksplisit.
- **Deep Learning (DL):** Sebuah subset dari machine learning yang menggunakan jaringan saraf untuk mengekstrak pola dari data.

## **2. Feedforward Deep Learning**
Jaringan saraf feedforward, model dasar dalam deep learning, dirancang untuk memproses data dalam satu arah—dari input ke output. Jaringan ini terdiri dari lapisan input, satu atau lebih lapisan tersembunyi, dan lapisan output. Setiap lapisan berisi node (neuron) yang melakukan komputasi berdasarkan bobot dan bias yang telah dipelajari.

### **Konsep-Konsep Kunci:**
- **Perceptron Feedforward:** Blok dasar dari jaringan saraf, model perceptron feedforward melibatkan penjumlahan produk input dan bobot, penambahan bias, dan penerapan fungsi aktivasi non-linear untuk menghasilkan prediksi.
- **Fungsi Aktivasi:** Fungsi non-linear seperti sigmoid, ReLU, dan tanh memperkenalkan non-linearitas pada output model, memungkinkannya untuk mempelajari pola yang kompleks.
- **Perceptron Multi-Output:** Konfigurasi di mana semua input terhubung ke semua output, membentuk lapisan yang padat atau sepenuhnya terhubung.

## **3. Deep Learning Backward**
Backpropagation adalah teknik penting dalam pelatihan jaringan saraf. Ini melibatkan pembaruan bobot jaringan berdasarkan gradien fungsi kerugian terhadap bobot. Metode ini memungkinkan jaringan untuk belajar dari kesalahan dan memperbaiki dirinya dari waktu ke waktu.

### **Langkah-Langkah Backpropagation:**
1. Inisialisasi bobot dan bias secara acak.
2. Penerusan: Data input diproses untuk menghasilkan prediksi.
3. Hitung kesalahan antara prediksi dan nilai sebenarnya.
4. Penerusan mundur: Propagasi kesalahan ke belakang melalui jaringan.
5. Pembaruan bobot dan bias menggunakan gradien descresi untuk meminimalkan kesalahan.
6. Ulangi langkah-langkah 2 hingga 5 untuk seluruh dataset pelatihan.

### **Komponen-Komponen:**
- **Fungsi Aktivasi:** Menentukan output neuron; fungsi umum meliputi sigmoid, tanh, dan ReLU.
- **Fungsi Kerugian:** Mengukur perbedaan antara nilai yang diprediksi dan nilai sebenarnya; berbagai jenis meliputi mean squared error, cross-entropy, dan lainnya.
- **Gradient Descent:** Mengoptimalkan model dengan menyesuaikan bobot dan bias berdasarkan gradien kesalahan.

Konsep-konsep pengantar ini membentuk dasar pemahaman yang lebih dalam tentang proses feedforward dan backward dalam deep learning.