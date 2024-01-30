
# Customer Behavior Analysis

Tool : Jupyter Notebook\
Programming Language : Python\
Libraries : Pandas\
Visualization : Matplotlib, Seaborn\
Dataset : 

## A. Problem Statement

### Introduction
Analisis perilaku pengguna merupakan kunci penting bagi perusahaan untuk mencapai keberhasilan dalam bisnisnya. 
Perusahaan dapat melakukan ananlisis untuk memeriksa bagaimana pelanggan berinteraksi dengan produk, layanan, atau platform untuk memahami tindakan, preferensi, dan proses pengambilan keputusan.\

### Business Questions
*   Bagaimana karakteristik dari pengguna?
*   Apakah karakteristik pengguna dapat mempengaruhi tingkat pembelian?

### Objective
Membuat visualisasi berbasis data sebagai insight

## B. Data Preprocessing

### Data Overview
Dataset terdiri dari 500 records dan 9 fitur

### Data Assessment
Asesment data dilakukan untuk memastikan bahwa data yang digunakan untuk analisis selanjutnya sudah siap dan sesuai dengan kebutuhan analisis. Hal yang dilakukan:

- Mengecek duplikasi data
- Mengecek nilai null atau missing value pada data
- Melakukan tipe data dan konsistensi nilai
- Memeriksa outlier atau data yang tidak biasa

Hasil dari Data Assessment yaitu **tidak terdapat duplikasi data** dan **tidak ada missing value**.

## C. Data Analysis
### 1. Bagaimana distribusi dari pengguna?
![customer dist](https://github.com/dikfaj/Python/assets/39393133/304d778c-7fa3-402b-aabf-5ec5808ec16f)

- Usia pelanggan berkisar antara **18 sampai 35 tahun** 
- **Pelanggan laki-laki** lebih banyak daripada perempuan
- **Mobile** adalah device yang **paling banyak** digunakan untuk melakukan pembelian
- **Kolkata dan Delhi** merupakan 2 kota yang paling banyak melakukan pembelian

![byGender](https://github.com/dikfaj/Python/assets/39393133/fd97d09b-c6d5-45f1-aef8-30c26a1ab53d)

- **Rata-rata usia pelanggan adalah 26 tahun** baik laki-laki maupun perempuan. Coba untuk memfokuskan produk yang menyasar usia kelompok ini.
- **Perempuan lebih banyak menambahkan item ke dalam keranjang (5.27)** namun rata-rata item yang dijual lebih sedikit dibandingkan laki-laki. Pertimbangkan untuk memberikan promo yang menargetkan perempuan sehingga angka penjualan bisa naik.
- **Waktu yang dihabiskan perempuan lebih tinggi (31.55)** dibandingkan laki-laki (30.00) pertimbangkan untuk optimalkan sistem rekomendasi produk sehingga dapat meningkatkan pembelian dan mengurangi waktu yang dihabiskan untuk melakukan browsing.
- **Total halaman yang dilihat oleh laki-laki lebih rendah (26.82) dibanding perempuan (27.58)** pertimbangkan untuk mengoptimalkan tata letak situs atau rekomendasi produk yang dapat menarik perhatian mereka.

![perbandingan](https://github.com/dikfaj/Python/assets/39393133/125f8247-3ce6-4300-a4f5-b39738079cc1)
- Waktu yang dihabiskan untuk menjelajahi produk, berkisar antara 10 hingga 20 menit, menunjukkan bahwa pengguna cenderung menambahkan sedikit item ke keranjang belanja, namun menghasilkan tingkat pembelian yang tinggi.
- Waktu yang dihabiskan untuk menjelajahi produk, berkisar antara 10 hingga 50 menit, cenderung mengakibatkan penurunan tingkat pembelian, meskipun item yang ditambahkan ke keranjang mengalami fluktuasi.
