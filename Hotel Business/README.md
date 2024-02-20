# 🏨Investigate Hotel Business using Data Visualization

Tool : Jupyter Notebook\
Programming Language : Python\
Libraries : Pandas\
Visualization : Matplotlib, Seaborn\
Dataset : [Superstore Dataset](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)

## 🔖 Table of Content
- [Introduction](#introduction)
- [Data Preprocessing](#data-preprocessing)
- [Data Visualization](#data-visualization)
- [Conclusion](#conclusion)

## Introduction

### Background
Analisis kinerja bisnis menjadi kunci utama bagi kesuksesan perusahaan dalam operasionalnya. Dengan melakukan analisis, perusahaan dapat mengenali masalah, kelemahan, dan keunggulan yang dimilikinya. Dalam industri perhotelan, pemahaman terhadap perilaku pelanggan menjadi hal yang krusial. Dengan memahami perilaku pelanggan, perusahaan dapat mengidentifikasi faktor-faktor yang memengaruhi keputusan pelanggan dalam memesan kamar hotel. Selain itu, perusahaan juga dapat mengenali produk atau layanan yang tidak diminati di pasar, sehingga dapat disesuaikan dengan strategi bisnis yang sesuai. Langkah ini bertujuan untuk meningkatkan pengalaman pelanggan dan mencapai tujuan bisnis jangka panjang.

### Business Question
- Bagaimana demografi dari pelanggan?
- Apakah durasi menginap mempengaruhi tingkat pembatalan pemesanan hotel?
- Apakah masa tunggu antara pemesanan dan hari kedatangan mempengaruhi tingkat pembatalan pemesanan hotel?
### Objective
Membuat visualisasi data sebagai insight bagi bisnis perhotelan

## Data Preprocessing
### Data Overview
- Data terdiri dari **36275 baris** dan **19 kolom**
- Tipe data : **float, int, object**

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
|Anomali Data|**Durasi menginap = 0**| Drop data|
|Ubah format|**Bulan bertipe integer**|Ubah menjadi Datetime|

Hasil dari data asessment
- Data sebelum : 36275 baris
- Data setelah : 26197 baris
  
## Data Visualization
### Customer Demography

<p align="center"><img src="https://github.com/dikfaj/Python/assets/39393133/1bfb22ad-b886-4d5c-ac9d-7d37fe0f464e"></p>

97.44% pelanggan hotel adalah pelanggan baru sedangkan 2.56% adalah pelanggan lama atau yang pernah melakukan pemesanan. Manajamen hotel dapat mempertimbangkan untuk mengirimkan notifikasi email kepada pelanggan lama dengan tujuan untuk mendorong mereka kembali memesan hotel. Selain itu, pihak manajaemen juga harus memberikan pelayanan terbaik kepada pelanggan baru agar mereka kembali memesan hotel di masa depan.

<p align="center"><img src="https://github.com/dikfaj/Python/assets/39393133/910e36bd-0923-41ce-ab00-d6942f0545f9"></p>
  
32.83% pelanggan melakukan pembatalan pemesanan.


<p align="center"><img src="(https://github.com/dikfaj/Python/assets/39393133/6fd283d6-72e8-423e-9add-4069228c1fb1"></p>

Pada bulan Januari, tercatat **jumlah pemesanan yang rendah** dengan **tingkat pembatalan yang minimal**. Seiring berjalannya waktu, **jumlah pemesanan mengalami peningkatan**, namun **tingkat pembatalan juga meningkat** sejalan dengan itu. 
Terdapat peristiwa signifikan pada bulan Juli, di mana terjadi **penurunan drastis dalam jumlah pemesanan**, disertai dengan mencapainya **tingkat pembatalan tertinggi sebesar 45%**. 
Yang menarik adalah ketika pemesanan **mencapai puncak** akan diikuti dengan **penurunan**, misalnya pada bulan April-Mei, Juni-Juli dan Oktober-November.


<p align="center"><img src="https://github.com/dikfaj/Python/assets/39393133/88174b02-f43e-4276-9b97-e6a5b2560620"></p>

Online merupakan market segment type yang paling banyak melakukan pemesanan sedangkan aviation merupakan market segment type dengan pemesanan paling sedikit. Manajemen hotel dapat melakukan kerja sama dengan perusahaan aviasi lainnya untuk melakukan pemesanan di hotel agar jumlah pemesanan pada market segment type ini meningkat.

### Stay Duration Analysis
Analisis ini bertujuan untuk mengetahui hubungan antara durasi menginap dengan pembatalan pemesanan hotel.

<p align="center"><img src="https://github.com/dikfaj/Python/assets/39393133/e8e46be1-cd0b-4542-a0b9-c2bceb56c89b"></p>

**Semakin lama durasi menginap**, maka **tingkat pembatalan semakin tinggi**.
Manajemen hotel dapat mempertimbangkan strategi khusus untuk mengurangi tingkat pembatalan pada durasi menginap yang lebih lama. Misalnya, promosi khusus untuk pemesanan jangka panjang atau komunikasi lebih aktif dengan pelanggan untuk memastikan kejelasan rencana mereka. 
Selain itu, durasi menginap kurang dari 1 minggu memiliki tingkat pembatalan yang rendah, manajemen juga dapat menerapkan strategi khusus misalnya dengan membatasi durasi menginap.

### Lead Time Analysis
Analisis ini bertujuan untuk mengetahui hubungan antara masa tunggu dengan pembatalan hotel.

<p align="center"><img src="https://github.com/dikfaj/Python/assets/39393133/7d90a911-355a-4c89-8209-20aa241bf2b6"></p>

Tingkat pembatalan pemesanan cenderung meningkat seiring dengan peningkatan masa tunggu. Dengan kata lain, **semakin lama masa tunggunya**, **semakin tinggi kemungkinan mereka membatalkan pemesanan**.
Manajemen hotel dapat mempertimbangkan strategi khusus untuk mengurangi tingkat pembatalan terutama pada masa tunggi 6 bulan sampai lebih dari 1 tahun, seperti menawarkan kebijakan pembatalan yang flexibel atau promosi khusus untuk mendorong tetapnya reservasi.

## Summary and Recomendations
1. 97,44% merupakan pelanggan baru dan 2.56% merupakan pelanggan lama. Dengan pembatalan hotel 32,83% dan pelanggan paling banyak berada pada segmen online sedangkan paling sedikit pada segmen aviasi. Beberapa 
- 97,44% merupakan pelanggan baru : Manajaemen hotel harus memberikan pelayanan terbaik kepada pelanggan baru agar mereka kembali memesan hotel di masa depan.
- 2.56% merupakan pelanggan lama : Manajamen hotel dapat mempertimbangkan untuk mengirimkan notifikasi email kepada pelanggan lama dengan tujuan untuk mendorong mereka kembali memesan hotel atau memberikan promosi khusus seperti voucher diskon.
-  dengan tingkat pembatalan sebesar 32.83%. Dengan total pemesanan tertinggi pada bulan Juni dan Oktober. Market segment yang paling banyak melakukan pemesanan adalah online dan offline.

### 2. Apakah durasi menginap mempengaruhi tingkat pembatalan hotel?
Semakin lama durasi menginap, maka tingkat pembatalan semakin tinggi. Durasi menginap dibawah 1 minggu memiliki tingkat pembatalan yang rendah  yaitu 32%.

### 3. Apakah masa tunggu mempengaruhi tingkat pembatalan hotel?

Tingkat pembatalan hotel cenderung meningkat seiring dengan peningatan masa tunggu. Dengan kata lain semakin lama masa tunggunya, maka semakin besar kemungkinan pelanggan untuk membatalkan pesanannya.




