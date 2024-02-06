
# 🏬 RFM Analysis Using Superstore Dataset

Tool : Jupyter Notebook\
Programming Language : Python\
Libraries : Pandas\
Visualization : Matplotlib, Seaborn\
Dataset : [Superstore Dataset](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)

## 🔖 Table of Content
- [Overview](#overview)
- [Data Preprocessing](##data-preprocessing)
- [Exploratory Data Analysis](##exploratory-data-analysis)
- [RFM Analysis](##rfm-analysis)
- [Recomendation](##recomendation)

## Overview
Dengan meningkatnya permintaa dan persaingan ketat di pasar, Superstore Giant ingin mengetahui produk, wilayah, kategori, dan segmen pelanggan mana yang sebaiknya menjadi target atau dihindari.

Apa yang akan dilakukan:
* Exploratory Data Analysis
* RFM Segmentation

## 📂 Data Preprocessing

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

## 📑 Exploratory Data Analysis
### Transaction Data
#### Statistical Summary

- **Transaksi paling besar** terjadi di tahun **2014**
- **Transaksi bulanan terbesar** terjadi pada bulan **November**
- **Transaksi kuartal terbesar** terjadi pada **kuarter ke empat**
- **Transaksi harian terbesar** dalam sebulan biasanya terjadi pada **tanggal 21**
- **Transaksi harian terbesar** dalam seminggu biasanya terjadi pada **hari jumat**

#### Number of Transaction per Month
![transactionpermonth](https://github.com/dikfaj/Python/assets/39393133/8e5b5a3e-5f40-460f-8e9f-9226d537337a)

Transaksi cenderung mengalami kenaikan yang **stabil dari bulan februari sampai agustus** dan mengalami **kenaikan yang signifikan di bulan september**. Lalu transaksi mengalami **penurunan yang drastis di bulan oktober**. Namun setelah itu transaksi mengalami **kenaikan yang signifikan di bulan november**. Perlu dilakukan analisis lebih lanjut mengenai hal ini.

#### Number of Daily Transaction per Month
![transactionperday](https://github.com/dikfaj/Python/assets/39393133/a4164723-d459-4b08-8008-624774ca73ad)
Tren transaksi harian fluktuatif namun mengalami kenaikan pada akhir tahun. Transaksi **terbesar terjadi pada tanggal 3 September dan 11 November**.

#### Daily Transaction Trend
![dailytransaction](https://github.com/dikfaj/Python/assets/39393133/d5d034e8-904f-4611-a5a4-d92e21eba7ca)

- Transaksi menurun signifikan di hari libur
- **Jumat** adalah hari paling banyak **transaksi**

### Product Data
#### Statistical Summary
![Transaksi](https://github.com/dikfaj/Python/assets/39393133/51d12956-061d-4a13-ad90-a683d13d4c39)
- Category paling banyak dibeli adalah **office supplies** denngan 60% dari total transaksi
- **15.29%** dari customer membeli di sub category **binders**
- **2.27%** dari customer membeli **staples**

#### Sales and Profit by Category
![salesandprofit](https://github.com/dikfaj/Python/assets/39393133/fb9b076d-043d-4784-9cbc-9e97d4644975)
- **Technology** menghasilkan **sales dan profit** paling tinggi
- Meskipun **sales** furniture dan office supplies tidak jauh berbeda, tetapi **ada perbedaan signifikan pada profit**

### Customer Data
![customerdata](https://github.com/dikfaj/Python/assets/39393133/de5887cc-f492-4139-b6b3-20ed2bcab314)
- **William Brown** merupakan customer yang paling sering bertransaksi
- **51.94%** pelanggan berada pada segment **consumer**
- **20.02%** pelanggan tinggal di **California**
- **32.04%** pelanggan berasal dari **West Region**

## 🗃️ RFM Analysis
Analisis Recency, Frequency, Monetary (RFM) merupakan proses analisis perilaku pelanggan. Dalam menentukan segmentasi pelanggan, digunakan model RFM berdasarkan tiga variabel yaitu recency terakhir melakukan transaksi, frequency dari transaksi, dan monetary dari jumlah transaksi setiap pelanggan.
Sistem scoring dijelaskan sebagai berikut:

- **Recency Score** : Mendapatkan **nilai 5** apabila terdapat **transaksi terakhir yang baru-baru ini**. Mendapatkan **nilai 1** apabila transaksi tersebut terjadi **lebih lama**.

- **Frequency Score** : Mendapatkan **nilai 5** jika pelanggan **sering berbelanja**. Mendapatkan **nilai 1** jika pelanggan **berbelanja jarang**.

- **Monetary Score** : Mendapatkan **nilai 5** apabila pelanggan **menghabiskan jumlah uang yang paling banyak**. Mendapatkan **nilai 1** jika pelanggan **menghabiskan jumlah uang yang paling sedikit**.

Berikut adalah sampel dari RFM Score dan segmentasinya.
![RFMtable](https://github.com/dikfaj/Python/assets/39393133/762a157f-7002-42b5-b741-e0b71a76ff72)

Berikut adalah interpretasi dari 10 segment

|Segment|Interpretasi|
|--------|-----------|
|Champions|Transaksi baru-baru ini, sering bertransaksi, menghabiskan banyak uang|
|Loyal Customers|Membeli secara rutin|
|Potential Loyalist|Pembeli baru dengan frekuensi transaksi rata-rata|
|New Customer|Pembeli terbaru, namun tidak sering bertransaksi|
|Promising|Pembeli baru-baru ini, namun belum menghabiskan banyak uang|
|Need Attention|Bertransaksi rata-rata, mungkin belum membeli akhir-akhir ini|
|About to Sleep|Tidak sering bertransaksi, mungkin akan hilang bila tidak diaktifkan kembali|
|At risk|Tidak sering bertransaksi, namun frekuensi pembelian diatas rata-rata|
|Cant't lose them|Dulu sering bertransaksi namun sudah lama tidak kembali|
|Hibernating|Pembelian terakhir sudah lama terjadi dan jumlah pesanan rendah|

![squarify](https://github.com/dikfaj/Python/assets/39393133/475ed3c3-ce54-4a19-9932-7c8b81381c8a)

![monetar](https://github.com/dikfaj/Python/assets/39393133/9f78aa24-99e5-4a16-841e-7c9c377da0f9)
- **Pelanggan paling banyak** berada pada segmen **Hibernating (21.56%), Loyal Customer (18.79%), dan Potential Loyalist (14.12%)**
- **Hibernating** menjadi segment **terbesar** dengan 171 customer (21.56%) dengan rata-rata terakhir pembelian yaitu 376 hari atau lebih dari 1 tahun lalu.
- **Sales tertinggi** berada pada segmen **Can't loose them (15,28%)** dan **Champion (14.11%)**


## 💡 Recomendation
Keseluruhan :
- Mengingat transaksi yang **paling sedikit** terjadi pada hari **Sabtu dan Minggu**, dapat dibuatkan program khusus seperti **Weekend Sale**.
- Dengan **sebagian besar pelanggan** berada di **California**, mungkin layak untuk meluncurkan promosi khusus di wilayah tersebut.


Berdasarkan jumlah pelanggan, segment paling besar yaitu Hibernating, Loyal Customer, dan Potential Analyts. Berikut beberapa hal yang bisa dilakukan:
- **Hibernating** : Program khusus seperti diskon dapat diciptakan sehingga mendorong mereka untuk melakukan transaksi kembali walaupun belum begitu sering sehingga bisa naik ke segment New Customer bahkan Potential Loyalist.
- **Loyal Customer** : Tawarkan produk-produk baru berdasarkan pembelian sebelumnya.
- **Potential Loyalist** : Buatkan mereka program seperti bundling program sehingga mereka dapat sering bertransaksi.

Berdasarkan sales dari pelanggan, segment paling besar yaitu **Can't Loose Them** dan **Champion**. Berikut beberapa hal yang bisa dilakukan
- Tawarkan penawaran waktu terbatas dan rekomendasikan berdasarkan pembelian sebelumnya.
- Jual produk bernilai lebih tinggi dan ajak mereka untuk meberikan ulasan positif.

