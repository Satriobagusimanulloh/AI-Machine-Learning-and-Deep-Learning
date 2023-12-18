# **Clustering Algorithm**
Clustering adalah teknik dalam machine learning untuk **mengelompokkan data atau objek berdasarkan kemiripan**. Tujuannya **meningkatkan kemiripan** sesama kelompok dan **meningkatkan perbedaan** antar kelompok. 

## **1. Konsep  Dasar**
#### A. K-Means
K-Means adalah algoritma clustering dengan cara **mengelompokan data ke dalam `k` kelompok/cluster** berdasarkan **kesamaan atribut**. Dalam memilih jumlah cluster `k` ada beberapa metode:
- **Metode Elbow**
    + Melakukan K-Means dengan sejumlah nilai `k` tertentu
    + Menghitung inersia (sum squared distances) setiap cluster
    + Memilih nilai `k` ketika penurunan inersia menurun secara tajam (membentuk siku pada grafik)
- **Metode Silhouette**
    + Menghitung koefisien siluet untuk berbagai nilai `k`
    + Memilih nilai `k` dengan koefisien siluet paling tinggi

#### B. Hierarchical Clustering
Hierarchical clustering adalah metode clustering yang **membangun hirarki dari cluster**. Metode ini menghasilkan **dendrogram**, yang merupakan **representasi visual** (pohon yang menunjukan pengelompokan hirarki dari cluster) dari **hirarki cluster**. Terdapat dua pendekatan utama dalam hierarchical clustering:
- **Agglomerative Hierarchical Clustering**
    + Dimulai dengan setiap data sebagai cluster terpisah
    + Satu per satu, dua cluster terdekat digabungkan menjadi satu cluster baru
    + Proses ini diulang sampai semua data berada dalam satu cluster
- **Divisive Hierarchical Clustering**
    + Dimulai dengan satu cluster berisi semua data
    + Cluster tersebut kemudian dibagi menjadi dua cluster terpisah
    + Proses ini diulang secara rekursif hingga setiap data memiliki clusternya sendiri
#### C. DBSCAN (Density-Based Spatial Clustering of Applications with Noise)
DBSCAN (Density-Based Spatial Clustering of Applications with Noise) adalah algoritma clustering yang **mengelompokan data berdasarkan kepadatan, mengidentifikasi area yang padat dan area yang lebih jarang**. DBSCAN **tidak memerlukan jumlah cluster** sebelumnya dan **dapat mengenali noise**. 

## **2. Cara Kerja**
#### A. K-Means
- **Inisialisasi pusat cluster** dengan memilih acak `k` sebagai pusat awal cluster
- **Pengelompokan data** dengan menentukan setiap data ke cluster dengan pusat terdekat 
- **Pembaruan pusat cluster** dengan menghitung ulang pusat cluster sebagai rata-rata dari data dalam setiap cluster
- **Iterasi** dengan mengulangi langkah 2 dan 3 hingga konvergensi
- **Konvergensi** ketika tidak ada perubahan signifikan dalam pengelompokan

#### B. Hierarchical Clustering
- **Inisialisasi** setiap data dianggap sebagai cluster awal
- **Perhitungan matriks jarak** antar cluster atau antar data (biasanya menggunakan Euclidean distance atau linkage methods seperti Ward, Complete, atau Average linkage)
- **Pengelompokkan atau penggabungan (Agglomerative) atau pemisahan (Divisive)**
- **Dendogram** merepresentasikan hasil pengelompokkan
- **Ulangi Langkah 2 hingga 4** hingga semua data berada dalam satu cluster (Agglomerative) atau setiap data memiliki clusternya sendiri (Divisive)

#### C. DBSCAN (Density-Based Spatial Clustering of Applications with Noise)
- **Inisialisasi** dengan memilih titik awal secara acak
- **Mencari tetangga** dengan menemukan semua titik dalam radius ε dari titik awal, jika titik tersebut memiliki setidaknya MinPts tetangga, itu adalah core point
- **Ekspansi cluster** dengan menambahkan semua tetangga core point ke dalam cluster, mengulangi proses untuk setiap titik dalam cluster.
- **Mengganti pusat** dengan memilih titik core baru yang belum termasuk dalam cluster dan ulangi proses
- **Label noise** dengan menentukan titik-titik yang tidak termasuk dalam cluster sebagai noise

## **3. Kelebihan Algoritma**
#### A. K-Means
- **Sederhana dan efisien** komputasi, membuatnya mudah diimplementasikan dan cocok untuk dataset besar
- **Kesederhanaan interpretasi** secara mudah, terutama jika data memiliki bentuk yang jelas dan terpisah
- **Skalabilitas yang baik** dan dapat menangani dataset yang besar dengan baik
- **Cocok untuk cluster berbentuk spherical** dan ukuran yang seragam
- **Kekurangan sensitivitas terhadap outlier** dibandingkan dengan metode clustering lainnya

#### B. Hierarchical Clustering
- **Interpretabilitas tinggi** mudah dipahami dan diinterpretasikan
- **Tidak bergantung pada jumlah cluster awal** 
- **Mudah diterapkan** tidak memerlukan asumsi tertentu tentang ukuran dan bentuk cluster

#### C. DBSCAN (Density-Based Spatial Clustering of Applications with Noise)
- **Mampu mengatasi bentuk cluster yang kompleks** 
- **Mampu mengenali data noise/outlier** dapat diidentifikasi dan diabaikan
- **Tidak bergantung pada cluster awal** 
- **Tidak sensitif dengan bentuk dan ukuran cluster** atau tidak terpengaruh

## **4. Kekurangan Algoritma**
#### A. K-Means
- **Memerlukan jumlah cluster awal `k`** yang mungkin sulit jika tidak ada informasi apriori tentang jumlah cluster yang sesuai
- **Sensitif terhadap posisi awal pusat cluster** inisialisasi yang buruk dapat menghasilkan hasil yang kurang optimal
- **Tidak cocok untuk cluster dengan bentuk dan ukuran yang variatif** 
- **Kurang cocok untuk data non-spherical** seperti cluster elips atau berbentuk lainnya
- **Tidak dapat menghandle noise dengan baik** 
- *Sensitif terhadap skala** antar fitur, sehingga normalisasi atau standarisasi sering kali diperlukan sebelum penerapan
- **Tidak menghasilkan hierarki cluster**

#### B. Hierarchical Clustering
- **Komputasi mahal** khususnya pada dataset yang besar
- **Tidak efisien untuk data besar** memerlukan banyak memori untuk menyimpan matriks jarak
- **Sensitif terhadap data noise dan outlier**
- **Kesulitan dalam menentukan jumlah cluster yang optimal** pemilihan jumlah cluster dapat menjadi subjektif dan memerlukan interpretasi lebih lanjut
- **Tidak cocok untuk data yang berdimensi tinggi atau data dengan fitur yang tidak relevan**

#### C. DBSCAN (Density-Based Spatial Clustering of Applications with Noise)
- **Sensitif terhadap parameter ε dan MinPts** yang tepat
- **Tidak cocok untuk data dengan kepadatan yang variatif** membuat algoritma ini tidak efektif
- **Kurang efisien pada data berdimensi tinggi** dapat menurunkan kinerja algoritma DBSCAN karena konsep kepadatan menjadi lebih kompleks
- **Tidak cocok untuk cluster dengan kepadatan yang berbeda** dapat menyulitkan untuk mengelompokkan

## **5. Penggunaan Data**
#### A. K-Means
- **Pengelompokkan pelanggan** berdasarkan perilaku pembelian atau preferensi produk
- **Segmentasi pasar** untuk menentukan kelompok target berdasarkan karakteristik tertentu seperti usia, pendapatan, atau perilaku konsumen

#### B. K-Means
- Mengelompokkan gen atau sampel dalam **analisis bioinformatika**, membantu memahami hubungan genetik atau ekspresi gen
- Mengelompokkan wilayah geografis berdasarkan karakteristik sosial ekonomi untuk **analisis kebijakan dan perkembangan wilayah**
- Mengelompokkan orang berdasarkan tes kepribadian untuk **analisis psikologis**

#### C. K-Means
- **Mendeteksi anomali** dalam data, seperti aktivitas yang tidak biasa atau perilaku yang mencurigakan
- **Pemantauan jaringan** untuk mengelompokkan aliran data pada jaringan komputer untuk mendeteksi serangan atau anomali
- **Pemrosesan citra** untuk mengelompokkan piksel dalam citra berdasarkan kepadatan warna, membantu dalam segmentasi citra

## **6. Input Data**
K-Means, Hierarchical Clustering, dan DBSCAN secara umum dirancang untuk menangani **data numerik**. Oleh karena itu, mereka paling cocok untuk data yang terdiri dari **fitur numerik atau kontinu**. Namun, terdapat **cara-cara untuk mengatasi data campuran** (numerik dan kategorikal) dengan **mengonversi atau mentransformasikan data tersebut**.
#### A. K-Means
- **One-Hot Encoding** mengonversi variabel kategorikal ke dalam bentuk vektor biner
- **K-Modes** modifikasi dari K-Means yang dirancang khusus untuk menangani data kategorikal

#### B. Hierarchical Clustering
- **Similarity Measures** menggunakan metrik kesamaan yang sesuai untuk mengukur kesamaan antar data numerik dan kategorikal
- **Gower's Distance** mengukur kesamaan antar data campuran dengan menggabungkan metrik Euclidean untuk variabel numerik dan coefisien Jaccard untuk variabel kategorikal

#### C. DBSCAN (Density-Based Spatial Clustering of Applications with Noise)
- **One-Hot Encoding** mengonversi variabel kategorikal ke dalam bentuk vektor biner
- **Similarity Measures** menggunakan metrik kesamaan yang sesuai untuk mengukur kesamaan antar data numerik dan kategorikal