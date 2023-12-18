# **Linear Regression dan Logistic Regression**

### **1. Definisi**
##### 1.1 Linear Regression
Linear regression adalah salah algoritma regresi yang digunakan untuk **memodelkan hubungan linier antara variabel dependent (target) dan variabel independent (fitur)**. Outputnya berupa **nilai kontinu**.
##### 1.2 Logistic Regression 
Logistic regression adalah algoritma klasifikasi untuk mengetahui **kemungkinan output (kelas tertentu) dari suatu inputan data**. Outputnya berupa **probabilitas yang diubah menjadi nilai biner dengan menggunakan ambang batas tertentu**.

### **2. Fungsi Persamaan**
##### 2.1 Linear Regression
y = wX + b
dimana:
`y` adalah variabel dependen (target).
`X` adalah variabel independen (fitur).
`w` adalah weight (slope)
`b` adalah bias (intercept)
Untuk kasus dengan lebih dari satu variabel independen, persamaannya menjadi lebih kompleks:
y = w1X1 + w2X2 + w3X3 + ...... + wnXn + b
##### 2.2 Logistic Regression
P(y=1) = 1/1 + e^-(mx + b)
dimana:
`P(y=1)` adalah probabilitas bahwa instance termasuk ke dalam kelas positif
`x` adalah variabel independen (fitur)
`w` adalah weight (slope)
`b` adalah bias (intercept)
`e` adalah basis logaritma natural

### **3. Penggunaan Data**
##### 3.1 Linear Regression
Dapat digunakan dengan **variabel dependen kontinu**.
##### 3.2 Logistic Regression
Biasanya digunakan untuk **variabel dependen biner (dua kelas)**, tetapi dapat diperluas untuk masalah klasifikasi multikelas.

### **4. Input Data**
##### 4.1 Linear Regression
Dapat digunakan dengan **data numerik**.
##### 4.2 Logistic Regression
Dapat digunakan dengan **data numerik atau kategorikal**, tetapi variabel independen biasanya **diubah menjadi nilai numerik**.

### **5. Kasus Penggunaan**
##### 5.1 Linear Regression
Cocok untuk memprediksi **nilai-nilai kontinu** seperti harga, suhu, atau pendapatan.
##### 5.2 Logistic Regression
Cocok untuk masalah **klasifikasi biner** seperti prediksi apakah email adalah spam atau bukan.

### **6. Pendekatan Optimisasi**
##### 6.1 Linear Regression
Minimalkan jumlah kuadrat dari **selisih antara nilai prediksi dan nilai sebenarnya** (least squares).
##### 6.2 Logistic Regression
**Maksimalkan likelihood function dari data pelatihan** untuk menentukan parameter model.

### **7. Istilah**
 - Slope (m) adalah angka yang menggambarkan seberapa curam atau landai garis.
 - Intercept (b) adalah titik di mana garis potong sumbu y
 - Variabel Dependensi (Y) adalah variabel yang ingin diprediksi atau dijelaskan oleh model. Juga dikenal sebagai variabel respons atau target.
 - Variabel Independen (X) adalah variabel yang digunakan untuk memprediksi atau menjelaskan variabel dependen. Juga dikenal sebagai variabel fitur atau prediktor.
 - Residuals adalah selisih antara nilai sebenarnya dari variabel dependen dan nilai yang diprediksi oleh model.
 - Threshold adalah nilai ambang batas yang digunakan untuk mengklasifikasikan probabilitas menjadi kelas tertentu.