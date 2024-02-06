
# RFM Analysis

Tool : Jupyter Notebook\
Programming Language : Python\
Libraries : Pandas\
Visualization : Matplotlib, Seaborn\
Dataset : 

## Overview
Dengan meningkatnya permintaa dan persaingan ketat di pasar, Superstore Giant ingin mengetahui produk, wilayah, kategori, dan segmen pelanggan mana yang sebaiknya menjadi target atau dihindari.

Apa yang akan dilakukan:
* Exploratory Data Analysis
* RFM Segmentation

## B. Data Preprocessing

### Data Overview
Dataset terdiri dari 9994 records dan 21 fitur

### Data Assessment
Asesment data dilakukan untuk memastikan bahwa data yang digunakan untuk analisis selanjutnya sudah siap dan sesuai dengan kebutuhan analisis. Hal yang dilakukan:

- Mengecek duplikasi data
- Mengecek nilai null atau missing value pada data
- Merubah tipe data dan konsistensi nilai
- Memeriksa outlier atau data yang tidak biasa

Hasil dari Data Assessment yaitu

| Data Assessment | Finding | Handling |
|---------|---------|---------|
|Duplikasi Data| **Tidak ada duplikasi data**|-|
|Missing Value|**Tidak ada missing value**|-|
|Tipe data tidak sesuai|Fitur **Order Date** dan **Ship Date** tidak sesuai|Merubah tipe data menjadi **Datetime**|
|Data yang tidak diperlukan|Fitur **Row ID** sama dengan index|Drop fitur||

## C. Data Analysis
### Exploratory Data Analysis
#### Transaction Data
##### Statistical Summary
[Gamber]

- **Transaksi paling besar** terjadi di tahun **2014**
- **Transaksi bulanan terbesar** terjadi pada bulan **November**
- **Transaksi kuartal terbesar** terjadi pada **kuarter ke empat**
- **Transaksi harian terbesar** dalam sebulan biasanya terjadi pada **tanggal 21**
- **Transaksi harian terbesar** dalam seminggu biasanya terjadi pada **hari jumat**

##### Number of Transaction per Month
[Gambar]

Transaksi cenderung mengalami kenaikan yang **stabil dari bulan februari sampai agustus** dan mengalami **kenaikan yang signifikan di bulan september**. Lalu transaksi mengalami **penurunan yang drastis di bulan oktober**. Namun setelah itu transaksi mengalami **kenaikan yang signifikan di bulan november**. Perlu dilakukan analisis lebih lanjut mengenai hal ini.

##### Daily Transaction Trend
[Gamber]

- Transaksi menurun signifikan di hari libur
- **Jumat** adalah hari paling banyak **transaksi**

#### Product Data
##### Statistical Summary
[Gamber]
- Category paling banyak dibeli adalah **office supplies** denngan 60% dari total transaksi
- **15.29%** dari customer membeli di sub category **binders**
- **2.27%** dari customer membeli **staples**

##### Sales and Profit by Category
[Gamber]
- **Technology** menghasilkan **sales dan profit** paling tinggi
- Meskipun **sales** furniture dan office supplies tidak jauh berbeda, tetapi **ada perbedaan signifikan pada profit**

#### Customer Data

- **William Brown** merupakan customer yang paling sering bertransaksi
- **51.94%** pelanggan berada pada segment **consumer**
- **20.02%** pelanggan tinggal di **California**
- **32.04%** pelanggan berasal dari **West Region**

## RFM Analysis
Analisis Recency, Frequency, Monetary (RFM) merupakan proses analisis perilaku pelanggan. Dalam menentukan segmentasi pelanggan, digunakan model RFM berdasarkan tiga variabel yaitu recency terakhir melakukan transaksi, frequency dari transaksi, dan monetary dari jumlah transaksi setiap pelanggan.
Sistem scoring dijelaskan sebagai berikut:

- **Recency Score** : Mendapatkan **nilai 5** apabila terdapat **transaksi terakhir yang baru-baru ini**. Mendapatkan **nilai 1** apabila transaksi tersebut terjadi **lebih lama**.

- **Frequency Score** : Mendapatkan **nilai 5** jika pelanggan **sering berbelanja**. Mendapatkan **nilai 1** jika pelanggan **berbelanja jarang**.

- **Monetary Score** : Mendapatkan **nilai 5** apabila pelanggan **menghabiskan jumlah uang yang paling banyak**. Mendapatkan **nilai 1** jika pelanggan **menghabiskan jumlah uang yang paling sedikit**.

Berikut adalah sampel dari RFM Score dan segmentasinya.
[gambar]



- **Pelanggan paling banyak** berada pada segmen **Hibernating (21.56%), Loyal Customer (18.79%), dan Potential Loyalist (14.12%)**
- **Hibernating** menjadi segment **terbesar** dengan 171 customer (21.56%) dengan rata-rata terakhir pembelian yaitu 376 hari atau lebih dari 1 tahun lalu.
- **Sales tertinggi** berada pada segmen **Can't loose them (15,28%)** dan **Champion (14.11%)**


## Recomendation
Keseluruhan :
- Mengingat transaksi yang paling sedikit terjadi pada hari Sabtu dan Minggu, dapat dibuatkan program khusus seperti "Weekend Sale."
- Dengan sebagian besar pelanggan berada di California, mungkin layak untuk meluncurkan promosi khusus di wilayah tersebut.


Berdasarkan jumlah pelanggan, segment paling besar yaitu Hibernating, Loyal Customer, dan Potential Analyts. Berikut beberapa hal yang bisa dilakukan:
- **Hibernating** : Program khusus seperti diskon dapat diciptakan sehingga mendorong mereka untuk melakukan transaksi kembali walaupun belum begitu sering sehingga bisa naik ke segment New Customer bahkan Potential Loyalist.
- **Loyal Customer** : Tawarkan produk-produk baru berdasarkan pembelian sebelumnya.
- **Potential Loyalist** : Buatkan mereka program seperti bundling program sehingga mereka dapat sering bertransaksi.

Berdasarkan sales dari pelanggan, segment paling besar yaitu **Can't Loose Them** dan **Champion**. Berikut beberapa hal yang bisa dilakukan
- Tawarkan penawaran waktu terbatas dan rekomendasikan berdasarkan pembelian sebelumnya.
- Jual produk bernilai lebih tinggi dan ajak mereka untuk meberikan ulasan positif.

