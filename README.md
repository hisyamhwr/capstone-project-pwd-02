# AWS - SaaS Sales

Berikut untuk melihat PPT -> [Klik Disini untuk melihat PPT](https://drive.google.com/file/d/1FNO5nWuo1-l1Tauh2fEMWfGEkAS_bHId/view?usp=sharing) 

Berikut untuk melihat file Tableau -> [Klik Disini untuk melihat Tableau Public](https://public.tableau.com/views/capstone2_17591512335460/DashboardSaas_sales?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)


Purwadhika Data Science Capstone Project Module 2

Proyek ini menganalisis dataset **SaaS Sales** untuk menjawab pertanyaan bisnis terkait **pertumbuhan pendapatan, profitabilitas, segmentasi pelanggan, dampak diskon,** dan **perbedaan kontribusi pelanggan baru vs lama**.  
Seluruh proses meliputi **Data Understanding → Data Cleaning → EDA → Uji Statistik → Insight & Rekomendasi** dan divisualisasikan menggunakan **Python** serta **Tableau**.

## Objective & Business Questions

1. Siapa kontributor **revenue** dan **profit** terbesar (Plan, Region, Industry)?  
2. Apakah **Plan/Region/Industry** memengaruhi perbedaan revenue? (ANOVA)  
3. Bagaimana **distribusi profit** serta pengaruh **diskon** terhadap profit?  
4. **Pelanggan baru vs lama**: apakah ada perbedaan kontribusi revenue yang signifikan? (t-test / Mann–Whitney)  
5. Bagaimana porsi **Non‑Profit** terhadap total penjualan dan profit?  
6. Arah **strategi pricing, diskon, dan retensi** apa yang sebaiknya diambil?

## Data Cleaning

- Perbaikan tipe data (tanggal, numerik).  
- Penanganan nilai hilang, duplikat, dan format tidak konsisten.  
- **Rule-based cleaning** (contoh): buang `Quantity <= 0`; validasi **profit negatif** (memisahkan valid vs invalid sesuai konteks bisnis).  
- Normalisasi nilai diskon dan pembatasan anomali ekstrem (jika terdeteksi).

## Exploratory Data Analysis (EDA)

- **Deskriptif**: statistik pusat & sebaran untuk `Sales`, `Profit`, `Discount`.  
- **Tren**: revenue & profit bulanan; pola musiman.  
- **Segmentasi**: per `Plan`, `Region`, `Industry`.  
- **Distribusi**: histogram/boxplot; identifikasi outlier.
- **Proporsi Non‑Profit** menurut `Plan`, `Region`, `Industry`.

## Visualisasi Utama

- Tren bulanan `Sales` & `Profit`.  
- Perbandingan `Plan` (Basic, Premium, Enterprise).  
- Perbandingan `Region` & `Industry`.  
- **Profit vs Discount** (scatter/boxplot) untuk melihat dampak diskon.  
- **Proporsi Non‑Profit** per `Plan`, `Region`, `Industry`.  
- Performa **New vs Returning Customers**.

### Berdasarkan hasil uji analisa dibeberapa sisi seperti Tren Pelanggan dan hasil revenue hingga retensi pelanggan baru dan lama kita bisa simpulkan bahwa: 

- Pada segment Strategic & Enterprise, Region North America, serta industri Technology adalah penyumbang revenue tertinggi. Segmen Basic Plan dan Non-Profit memiliki kontribusi revenue paling kecil.
- Ditemukan transaksi dengan profit negatif, terutama akibat diskon yang terlalu tinggi, Produk dengan margin tinggi lebih banyak berasal dari plan Premium & Enterprise.
- Jumlah pelanggan baru di bulan-bulan awal, namun setelah pertengahan 2020 jumlah New Customer terus menurun hingga hampir nol.
- Produk tanpa diskon cenderung menghasilkan profit lebih stabil.
- Plan dan Region terbukti signifikan memengaruhi revenue
- Profit tidak merata antar segmen; sebagian besar profit terkonsentrasi pada segment Premium/Enterprise.
- Region lain (misalnya Asia atau EMEA) berkontribusi lebih kecil, sehingga masih ada ruang untuk ekspansi.

### Rekomendasi atau usulan untuk bisnis

1. Fokus Retention & Upselling

- Memprioritaskan pelanggan Strategic & Enterprise melalui program loyalty, customer success, atau fitur eksklusif.
- Melakukan upselling pada pelanggan Basic agar naik ke plan lebih tinggi atau di barengi harga promo atau package agar pengguna lebih tertarik untuk berpindah dari Basic ke Strategic.

2. Evaluasi Pricing & Diskon
- Memberikan batasan pada diskon untuk menghindari profit negatif, Berikan package lain atau tawaran lain selain discount untuk menghindari kerugian atau profit negatif dari dampak discount yang sangat besar.
- Menerapkan A/B testing pada package pricing untuk menentukan harga optimal di tiap region.

3. Perkuat Onboarding Pelanggan Baru
- Menyediakan training, onboarding support, atau free trial untuk mendorong konversi pelanggan baru agar pelanggan dapat lebih mempercayai product dan meningkatkan upselling.

4. Segmen baru pada product non-profit
- Buat Strategi paket khusus dengan fitur terbatas namun harga terjangkau.
- Strategi ini bisa meningkatkan brand image sekaligus penetrasi pasar baru.
- Gunakan Pemisahan dengan menggunakan add-on agar beberapa fitur menjadi eksklusif dan mendapat daya jual yang baru.

5. Strategi Regional & Industri
- Fokus ekspansi di North America & Technology Industry karena profit tinggi.
- Optimalkan budget marketing sesuai kontribusi masing-masing region.
- Ekspansi Bisnis ke market yang lebih luas di arah asia dan sekitarnya dengan membuat campaign untuk small business di wilayah asia.
- Kembangkan metrik Customer Lifetime Value (CLV) agar strategi lebih berorientasi jangka panjang.


