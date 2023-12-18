# **Random Forest & Ensemble Learning**

## **Konsep Dasar**
#### 1. Pohon Keputusan
Pohon keputusan adalah **struktur pohon** yang digunakan machine learning **untuk mengambil keputusan berdasarkan serangkaian pertanyaan yang mengarah ke jawaban atau prediksi**. **Setiap simpul** di pohon keputusan mewakili **keputusan berdasarkan fitur tertentu**, **daun pohon berisi hasil atau prediksi**.
#### 2. Ensemble Learning
Ensemble learning adalah pendekatan dimana **beberapa model digabungkan** untuk mendapatkan **stabilitas prediksi dan meningkatkan akurasi**. Dua jenis teknik ensemble yang digunakan dalam pembelajaran mesin:
#### a. Bagging (Bootstrap Aggregating)
Bagging melibatkan **pembuatan beberapa subset acak** dari data pelatihan dengan menggunakan **teknik pengambilan sampel dengan penggantian** (bootstrap). Setiap subset digunakan untuk **melatih model secara independen** dari yang lain dan kemudian **menggabungkannya**.
##### - Random Forest
Random forest adalah **algoritma ensemble learning** yang terdiri dari **banyak pohon keputusan**. Setiap pohon keputusan dibangun secara acak dengan **mengambil sampel acak dari data training** dan **mengambil subset acak dari fitur** untuk membangun pohon. Prediksi akhir dari Random Forest diambil dengan **mengambil rata-rata (regresi)** atau **mayoritas (klasifikasi)** prediksi dari setiap pohon.
#### b. Boosting
Boosting melibatkan **pembuatan model secara berurutan** dengan **memberikan bobot pada setiap instance data**, di mana **setiap iterasi difokuskan untuk memperbaiki kesalahan prediksi model sebelumnya** dengan memberikan perhatian lebih pada data yang salah diprediksi sebelumnya.
##### - Gradient Boosting
**Menggabungkan prediksi dari model lemah secara berurutan**. Pada setiap iterasi, model mencoba **memperbaiki kesalahan yang dilakukan oleh model sebelumnya**. XGBoost dan LightGBM adalah dua implementasi populer dari algoritma gradient boosting.

## **Cara Kerja**
##### 1. Random Forest
Random Forest adalah suatu teknik ensemble learning yang menggabungkan beberapa pohon keputusan untuk meningkatkan performa prediksi. Berikut adalah langkah-langkahnya:
- Pilih Dataset
Ambil dataset yang berisi informasi terkait cuaca dan label apakah hujan atau tidak. Contoh dataset:
| Suhu | Kelembaban | Angin | Label  |
|------|------------|-------|--------|
| 25   | 80         | Kuat  | Hujan  |
| 30   | 65         | Lemah | Tidak  |
| 22   | 75         | Kuat  | Hujan  |
| 28   | 70         | Sedang| Hujan  |
- Bagi Dataset
Pisahkan dataset menjadi dua bagian: satu untuk melatih model (training set) dan satu untuk menguji model (testing set).
- Bagging (Bootstrap Aggregating)
a. Ambil secara acak subset dari training set.
b. Bangun pohon keputusan pada subset tersebut.
c. Pilih secara acak atribut untuk melakukan split pada setiap node pohon.
d. Ulangi langkah a-c hingga pohon mencapai kedalaman maksimum atau sampai kondisi berhenti tertentu terpenuhi.
Contoh pohon keputusan:
Random Forest
|
|-- Pohon Keputusan 1
|   |-- Node 1: Kelembaban > 75?
|   |   |-- Ya: Hujan
|   |   |-- Tidak: Tidak Hujan
|
|-- Pohon Keputusan 2
|   |-- Node 1: Suhu > 28?
|   |   |-- Ya: Hujan
|   |   |-- Tidak: Tidak Hujan
- Buat Banyak Pohon Keputusan
Ulangi langkah 3 sebanyak yang diinginkan untuk membuat banyak pohon keputusan.
- Voting
Lakukan voting untuk setiap input dari pohon-pohon yang telah dibuat. Hasil akhirnya akan diambil berdasarkan mayoritas voting.
- Evaluasi
Gunakan testing set untuk mengevaluasi performa model Random Forest yang telah dibuat.

##### 2. Gradient Boosting
- Membuat model lemah(awal) untuk membuat prediksi pada data pelatihan.
- Merhitungan gradien dari fungsi kerugian (loss function) terhadap prediksi model awal dihitung.
- Membuat model berikutnya untuk memperbaiki kesalahan dengan memperhitungkan gradien dari residual sebelumnya.
- Prediksi dari model baru dikalikan dengan suatu bobot (learning rate) dan ditambahkan ke prediksi sebelumnya
- Langkah 3 hingga 5 diulang sejumlah iterasi yang ditentukan atau sampai mencapai kriteria berhenti tertentu.
- Prediksi akhir dihasilkan dengan menjumlahkan prediksi dari semua model yang telah dibuat.

## **Teknik Ensemble Learning Meningkatkan Kinerja Model**
- Dengan membuat beberapa model independen pada subset acak data (Bagging)
    + variasi dan risiko overfitting dapat dikurangi
    + menghasilkan model yang lebih stabil dan general pada data baru. 
- Boosting fokus pada pembuatan model secara berurutan untuk memperbaiki kesalahan prediksi sebelumnya
    + Meningkatkan akurasi secara signifikan
    + Memiliki mekanisme bawaan untuk menangani overfitting.
- Meningkatkan robustness dengan kombinasi model-model yang dapat menangani outliers atau noise dalam data.

## **Penggunaan Data Ensemble Learning**
- Jumlah data besar
- Memiliki banyak atribut

## **Input Data Ensemble Learning**
- Data terstruktur seperti tabel
- Data numerikal atau kategorikal, dapat menanganinya tanpa memerlukan transformasi khusus.

## **Kasus Penggunaan Ensemble Learning**
- Klasifikasi seperti klasifikasi spam atau non-spam, identifikasi penyakit berdasarkan gejala, dll.
- Regressi seperti memprediksi harga rumah berdasarkan fitur-fitur tertentu.
- Feature importance memberikan perkiraan kepentingan fitur, membantu dalam pemahaman mengapa suatu keputusan dibuat.

## **Istilah Penting**
- Feature impotance memberikan nilai kepentingan pada setiap fitur, membantu kita memahami kontribusi masing-masing fitur terhadap prediksi. (Random Forest)
- Pemilihan acak fitur pada setiap pohon membantu mencegah model menjadi terlalu spesifik pada satu fitur atau variabel tertentu. (Random Forest)