# **Introduction to AI, Machine Learning, and Deep Learning**

**1. Definisi**
- Machine Learning adalah komputer dilatih/belajar mengenali suatu pola di dataset untuk membuat keputusan/prediksi tanpa diprogram secara eksplisit.
- Deep Learning adalah subset dari ML yang menggunakan neural network (meniru cara kerja saraf manusia) dalam melakukan suatu tugas.
- Artificial Intelligence adalah cabang dari ilmu komputer untuk melakukan/meniru tugas-tugas yang dilakukan manusia.


**2. Pendekatan dan Mekanisme**
- **Machine Learning**
  + Pendekatan: Pembelajaran dari data.
  + Mekanisme: Melatih model machine learning dengan data training untuk membuat prediksi/keputusan dengan data baru (tanpa diprogram secara eksplisit)
- **Deep Learning**
  + Pendekatan: Menggunakan deep neural network.
  + Mekanisme: Menggunakan jaringan saraf tiruan untuk secara otomatis mengekstrak representasi fitur yang kompleks dari data, memungkinkan model untuk menghasilkan output yang akurat.
- **Artificial Intelligence**
  + Pendekatan: Beberapa tipe pendekatan Ruled-Based, Sistem Ekspert, Pembelajaran data (Machine Learning).
  + Mekanisme: Bergantung pada tugasnya, AI dapat menggunakan aturan dan strategi pemrograman eksplisit, atau memanfaatkan pembelajaran dari data untuk meningkatkan performa dan adaptasi.


**3. Kaidah Dasar**
- **Machine Learning**
  + Training: Proses melatih model menggunakan data.
  + Inference: Penggunaan model untuk membuat prediksi pada data baru.
- **Deep Learning**
  + Neural Networks: Model terdiri dari lapisan-lapisan yang dapat belajar representasi yang kompleks.
- **Artificial Intelligence**
  + Kecerdasan Umum (AGI): Tujuan jangka panjang AI untuk mencapai kecerdasan sebanding dengan manusia.


**4. Jenis Utama Machine Learning Deep Learning Artificial Intelligence**
- Jenis Utama Machine Learning
  + Supervised Learning
    * Machine learning model dibuat menggunakan data yang memiliki label. (X -> y)
    * Mempelajari hubungan antara input (1 atau lebih fitur) dan output untuk membuat prediksi yang tepat pada data baru.
    * Contoh:
      - Klasifikasi: Memprediksi kelas dari suatu inputan.
      - Regresi: Memprediksi nilai numerik dari suati inputan.
  + Unsupervised Learning
    * Machine learning model harus memahami struktur/pola dalam data tanpa label.
    * Mengidentifikasi struktur, pola, atau hubungan dalam data.
    * Contoh:
      - Clustering: Mengelompokkan data ke dalam kelompok berdasarkan kemiripan.
      - Association: Menemukan hubungan atau asosiasi antara variabel.
  + Reinforcement Learning
    * Jenis machine learning dimana agen belajar untuk membuat keputusan dengan berinteraksi dengan lingkungan. Agennya memperoleh umpan balik berupa reward atau penalty berdasarkan tindakan yang diambilnya.
    * Model berinteraksi dengan lingkungan dan memutuskan tindakan untuk mencapai tujuan.
    * Contoh:
      - Game Playing: Mengajarkan komputer untuk bermain permainan dan memaksimalkan skor.
      - Robotika: Mengajar robot untuk melakukan tugas-tugas kompleks melalui trial and error.
- Jenis Utama Deep Learning
  + Convolutional Neural Network (CNN)
    * Jenis jaringan saraf yang dirancang khusus untuk memproses data grid seperti foto dan video
    * Contoh: Pengenalan gambar seperti klasifikasi gambar, object detection, segmentasi gambar
  + Recurrent Neural Network (RNN)
    * Jenis jaringan saraf yang dirancang untuk menangani data urutan, dimana informasi dari waktu sebelumnya menjadi acuan dalam memproses data pada waktu berikutnya.  
    * Contoh: NLP seperti Text translation, generasi teks
  + Long Short-Term Memory (LSTM)
    * Jenis dari RNN yang dirancang untuk mengatasi masalah vanishing gradient, yang sering muncul saat melatih RNN pada data urutan panjang.
    * Contoh: NLP seperti pemahaman dan generasi teks
  + Transformers
    * Arsitektur jaringan saraf yang memanfaatkan mekanisme perhatian (attention mechanism) untuk menangani data urutan tanpa memerlukan struktur urutan tertentu.
    * Contoh: NLP seperti text translation, model bahasa
- Jenis Utama Artificial Intelligence
  + Artificial Narrow Intelligence (Weak AI)
    * Dirancang dan dioptimalkan untuk tugas-tugas spesifik/terbatas.
    * Contoh: sistem rekomendasi, asisten virtual, chatbot.
  + Artificial General Intelligence (Strong AI)
    * Jenis AI yang memiliki kemampuan untuk memahami, belajar, dan menyelesaikan tugas-tugas diberbagai domain sebagaimana dilakukan manusia.
    * Contoh: Belum ada implementasi AGI yang sepenuhnya tercapai.


**5. Perbedaan**
- Artificial Intelligence vs. Machine Learning:
  + AI mencakup ML tetapi juga mencakup aspek lain seperti logika, perencanaan, dan pemahaman bahasa alami.
- Machine Learning vs. Deep Learning:
  + ML mencakup berbagai teknik pembelajaran, sementara Deep Learning fokus pada jaringan saraf mendalam.
 
**6. Istilah Penting**
- `Dataset`: Kumpulan data yang digunakan untuk melatih dan menguji model.
- `Underfitting`: Model tidak dapat menangkap kompleksitas data pelatihan dengan baik.
- `Overfitting`: Model tidak baik dalam membuat prediksi/keputusan pada data baru.
- `Algortima`: Serangkaian aturan dan prosedur matematika yang digunakan oleh mesin untuk memecahkan suatu masalah atau membuat prediksi.
- `Natural Language Processing (NLP)`: Kemampuan mesin untuk memahami, menganalisis, dan menghasilkan bahasa manusia dengan cara yang bermakna.
- `Sistem Ekspert`: Program komputer yang dirancang untuk meniru pengetahuan dan keterampilan seorang pakar manusia dalam suatu bidang tertentu.
- `Sistem Ekspert`: Metode yang digunakan untuk mengoptimalkan bobot dan bias dalam jaringan saraf dengan menghitung gradien dari fungsi kesalahan terhadap parameter-parameter tersebut.