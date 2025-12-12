# Latihan Membuat Visualisasi Data

Setelah memahami teori tentang data visualization serta explanatory analysis, kini saatnya kita menerapkannya dalam sebuah proyek analisis data sederhana. Pada materi ini, kita akan melanjutkan proyek analisis data Pada Pertemuan Sebelumnya. 

**Penting!**

Latihan ini merupakan lanjutan dari materi Latihan Exploratory Data Analysis. Oleh karena itu, sebelum melanjutkan materi ini, pastikan Anda telah menyelesaikan latihan tersebut.

Tujuan
Pertama, kita akan melanjutkan proyek analisis data Dicoding Collection dengan menjalankan proses membuat visualisasi data dan explanatory analysis. Proses ini memiliki tujuan antara lain:

menjawab seluruh pertanyaan analisis atau bisnis yang sebelumnya telah dibuat; dan
membuat visualisasi data untuk mempermudah penyampaian hasil analisis data.


## Tujuan
Pertama, kita akan melanjutkan proyek analisis data Dicoding Collection dengan menjalankan proses membuat visualisasi data dan explanatory analysis. Proses ini memiliki tujuan antara lain:

- menjawab seluruh pertanyaan analisis atau bisnis yang sebelumnya telah dibuat; dan
- membuat visualisasi data untuk mempermudah penyampaian hasil analisis data.
  
## Alur Latihan
Berikut tahapan dalam latihan ini.

- Persiapan.
- Membuat visualisasi data yang menjawab pertanyaan bisnis.

# Persiapan
Sebelum mulai mengerjakan latihan ini, terdapat beberapa hal yang harus disiapkan terlebih dahulu.

- Pertama, siapkanlah Google Colab atau Jupyter Notebook yang sebelumnya digunakan pada materi Latihan Exploratory Data Analysis.
- Pastikan Anda menjalankan kembali seluruh kode yang ada pada notebook tersebut.
Last but not least, siapkan juga camilan beserta segelas teh atau kopi sebagai sumber energi Anda dalam mengarungi latihan ini.


## Membuat Visualisasi Data yang Menjawab Pertanyaan Bisnis

Setelah tahap persiapan selesai, kita akan masuk ke tahap pembuatan visualisasi data serta melakukan explanatory analysis. Seperti yang telah dibahas sebelumnya, pada tahap ini kita akan fokus menjawab berbagai pertanyaan bisnis yang sebelumnya telah kita buat.

Pada materi Latihan Exploratory Data Analysis, kita telah mendefinisikan beberapa pertanyaan bisnis seperti berikut.

1. Bagaimana performa penjualan dan revenue perusahaan dalam beberapa bulan terakhir?
2. Produk apa yang paling banyak dan paling sedikit terjual?
3. Bagaimana demografi pelanggan yang kita miliki?
4. Kapan terakhir pelanggan melakukan transaksi?
5. Seberapa sering seorang pelanggan melakukan pembelian dalam beberapa bulan terakhir?
6. Berapa banyak uang yang dihabiskan pelanggan dalam beberapa bulan terakhir?

Nah, sekarang tugas kita adalah membuat visualisasi data dan explanatory analysis guna menjawab berbagai pertanyaan tersebut. Tentunya Anda sudah siap, bukan? Yuk, kita mulai dengan menjawab pertanyaan pertama.


### Bagaimana Performa Penjualan dan Revenue Perusahaan dalam Beberapa Bulan Terakhir?

Untuk menjawab pertanyaan pertama, kita perlu membuat sebuah DataFrame baru untuk menampung informasi terkait jumlah order dan total revenue yang diperoleh pada tiap bulannya. Oleh karena itu, kita perlu mengubah frekuensi dari data yang awalnya harian menjadi bulanan.

Seperti biasa, library tercinta kita yaitu pandas telah menyediakan sebuah method bernama resample(). Method ini memungkinkan kita untuk mengubah frekuensi atau melakukan resampling terhadap DataFrame yang memiliki komponen time series. Untuk menggunakan method ini, kita harus mendefinisikan parameter rule (mengatur target konversi) dan on (nama kolom bertipe datetime yang akan diubah frekuensinya). Selengkapnya, Anda dapat membaca dokumentasi berikut: [pandas.DataFrame.resample](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.resample.html).

Berikut contoh kode untuk mengubah frekuensi data untuk memperoleh informasi terkait jumlah order dan total revenue yang diperoleh setiap bulannya. 

```python
monthly_orders_df = all_df.resample(rule='M', on='order_date').agg({
    "order_id": "nunique",
    "total_price": "sum"
})
monthly_orders_df.index = monthly_orders_df.index.strftime('%Y-%m')
monthly_orders_df = monthly_orders_df.reset_index()
monthly_orders_df.rename(columns={
    "order_id": "order_count",
    "total_price": "revenue"
}, inplace=True)
monthly_orders_df.head()
```

Pada kode di atas, kita ingin melakukan resample data order_date menjadi bulanan serta melakukan agregasi terhadap data tersebut untuk memperoleh informasi terkait jumlah order dan total revenue yang diperoleh tiap bulan. Gambar di bawah ini merupakan tampilan dari data tersebut.

![](https://assets.cdn.dicoding.com/original/academy/dos:acbf1fa3e1cc59b92c29979c46fcdbe920230309161832.jpeg)


sekarang kita telah memiliki sebuah DataFrame yang memuat informasi yang dibutuhkan untuk menjawab pertanyaan pertama ini. Namun, untuk mempermudah orang lain dalam memahami informasi dari DataFrame tersebut, kita perlu membuat visualisasi datanya. Apakah Anda bisa menebak bentuk visualisasi data apa yang akan kita gunakan?, betul sekali kita akan menggunakan bentuk line chart untuk memvisualkan informasi terkait jumlah order dan total revenue yang diperoleh tiap bulan. 

Di bawah ini contoh kode yang dapat Anda gunakan untuk membuat line chart terkait jumlah order per bulan.

```python
monthly_orders_df = all_df.resample(rule='M', on='order_date').agg({
    "order_id": "nunique",
    "total_price": "sum"
})
monthly_orders_df.index = monthly_orders_df.index.strftime('%B') #mengubah format order date menjadi nama bulan
 
monthly_orders_df = monthly_orders_df.reset_index()
monthly_orders_df.rename(columns={
    "order_id": "order_count",
    "total_price": "revenue"
}, inplace=True)
 
plt.figure(figsize=(10, 5)) 
plt.plot(monthly_orders_df["order_date"], monthly_orders_df["order_count"], marker='o', linewidth=2, color="#72BCD4") 
plt.title("Number of Orders per Month (2021)", loc="center", fontsize=20) 
plt.xticks(fontsize=10) 
plt.yticks(fontsize=10) 
plt.show()
```

Kode di atas akan menghasilkan visualisasi data berikut.

![](https://assets.cdn.dicoding.com/original/academy/dos:ec59b9d826e605be52d9c776a0778d3820230309162253.png)

Berdasarkan visualisasi di atas, kita dapat melihat bahwa jumlah order terbanyak terjadi pada bulan Maret. Selain itu, kita juga dapat melihat adanya penurunan jumlah order yang cukup signifikan pada bulan Februari, April, Mei, dan Oktober. 

Tentunya penurunan tersebut akan berdampak pada total revenue yang diperoleh perusahaan. Untuk memvalidasi hal ini, buatlah line chart menggunakan contoh kode berikut.

```python
plt.figure(figsize=(10, 5))
plt.plot(
    monthly_orders_df["order_date"],
    monthly_orders_df["revenue"],
    marker='o', 
    linewidth=2,
    color="#72BCD4"
)
plt.title("Total Revenue per Month 2021 (AUD)", loc="center", fontsize=20)
plt.xticks(fontsize=10)
plt.yticks(fontsize=10)
plt.show()
```

Kode tersebut akan menghasilkan visualisasi data seperti di bawah ini.

![](https://assets.cdn.dicoding.com/original/academy/dos:d1a5944d509abe01a4c5b6f403e1f38720230309162350.png)


Penurunan jumlah orderan yang sangat signifikan terjadi pada bulan Februari, April, Mei, dan Oktober berdampak terhadap penurunan revenue perusahaan. Normalnya, kita harus mencari tahu penyebab terjadinya penurunan tersebut dengan mempertimbangkan banyak hal, seperti keberadaan kompetitor, campaign, dll. Namun, untuk studi kasus ini, kita tidak memiliki cukup informasi terkait hal tersebut.

### Produk Apa yang Paling Banyak dan Paling Sedikit Terjual?

Pada pertanyaan bisnis selanjutnya, kita ingin mengidentifikasi produk dengan penjualan terbanyak dan paling sedikit. Untuk melakukan ini, tentunya kita harus membuat sebuah DataFrame baru guna menampung informasi terkait jumlah penjualan tiap produk. Berikut merupakan contoh kode untuk melakukannya.

```python
sum_order_items_df = all_df.groupby("product_name").quantity_x.sum().sort_values(ascending=False).reset_index()
sum_order_items_df.head(15)
```

Kode di atas akan menghasilkan DataFrame seperti di bawah ini.

![](https://assets.cdn.dicoding.com/original/academy/dos:fb42f27e9ed319c399544ee77ca5c7ed20230309161832.jpeg)

Untuk mempermudah kita dalam menyampaikan informasi tersebut, kita harus membuat visualisasi data dalam bentuk bar chart. Selain itu, untuk mempermudah orang lain dalam mengidentifikasi produk dengan performa terbaik dan terburuk, kita perlu membuat dua buah visualisasi data dalam satu gambar visual. Untuk melakukan ini, gunakanlah function subplot(). Berikut contoh kode untuk membuatnya.

```python
fig, ax = plt.subplots(nrows=1, ncols=2, figsize=(24, 6))

```

Kode tersebut akan menghasilkan kanvas kosong dengan object berupa fig dan ax seperti di bawah ini.

![](https://assets.cdn.dicoding.com/original/academy/dos:6bf191b9d2280ac92bae2cfba802add520230309162725.png)

Selanjutnya, tentunya kita harus mengisi kanvas kosong tersebut dengan bar chart. Berikut contoh kode untuk melakukannya

```python
fig, ax = plt.subplots(nrows=1, ncols=2, figsize=(24, 6))
 
colors = ["#72BCD4", "#D3D3D3", "#D3D3D3", "#D3D3D3", "#D3D3D3"]
 
sns.barplot(x="quantity_x", y="product_name", data=sum_order_items_df.head(5), palette=colors, ax=ax[0])
ax[0].set_ylabel(None)
ax[0].set_xlabel(None)
ax[0].set_title("Best Performing Product", loc="center", fontsize=15)
ax[0].tick_params(axis ='y', labelsize=12)
 
sns.barplot(x="quantity_x", y="product_name", data=sum_order_items_df.sort_values(by="quantity_x", ascending=True).head(5), palette=colors, ax=ax[1])
ax[1].set_ylabel(None)
ax[1].set_xlabel(None)
ax[1].invert_xaxis()
ax[1].yaxis.set_label_position("right")
ax[1].yaxis.tick_right()
ax[1].set_title("Worst Performing Product", loc="center", fontsize=15)
ax[1].tick_params(axis='y', labelsize=12)
 
plt.suptitle("Best and Worst Performing Product by Number of Sales", fontsize=20)
plt.show()
```
Pada kode di atas, kita mengisi kanvas sebelumnya dengan bar chart yang dibuat menggunakan library seaborn. ax[0] merupakan object untuk kanvas pertama (bagian kiri) dan ax[1] merupakan object untuk kanvas kedua (bagian kanan). Berikut hasil visualisasi data yang akan Anda peroleh.

![](https://assets.cdn.dicoding.com/original/academy/dos:5c60b89721a56d630914e89bbac95f2420230309162927.png)

Berdasarkan gambar di atas, Anda dapat melihat bahwa produk Denim merupakan produk yang paling laris. Kontras dengan hal tersebut, produk Mandarin Collar merupakan produk yang paling sedikit terjual.  


### Bagaimana Demografi Pelanggan yang Kita Miliki?

Pertanyaan selanjutnya yang ingin kita jawab ialah terkait demografi pelanggan yang kita miliki. Untuk menjawab hal ini, tentunya kita bisa membuat DataFrame baru untuk menampung informasi terkait jumlah pelanggan untuk demografi tertentu seperti gender, state, dll.

- **Berdasarkan gender**
  
  Untuk mengidentifikasi jumlah pelanggan berdasarkan gender, Anda bisa menggunakan kode berikut.

```python
bygender_df = all_df.groupby(by="gender").customer_id.nunique().reset_index()
bygender_df.rename(columns={"customer_id":"customer_count"}, inplace=True)

plt.figure(figsize=(10,5))
sns.barplot(
 y="customer_count",
 x="gender",
 data=bygender_df.sort_values(by="customer_count", ascending=False),
 palette=colors
)
plt.title("Number of Customer by Gender", loc="center", fontsize=15)
plt.ylabel(None)
plt.xlabel(None)
plt.tick_params(axis='x', labelsize=12)
plt.show()

```

Kode di atas akan menghasilkan visualisasi data berikut.

![](https://assets.cdn.dicoding.com/original/academy/dos:998bd3da143d0b6efb636b184e8d195820230309163324.png)

Berdasarkan gambar di atas, diketahui bahwa kebanyakan pelanggan tidak bersedia untuk memberitahukan informasi terkait gender-nya.


- **Berdasarkan age**
  
  Untuk melihat demografi pelanggan berdasarkan usia, kita bisa mengelompokkannya sesuai kelompok usia. Selanjutnya, kita bisa memvisualisasikan hasil pengelompokkan tersebut. Anda dapat menggunakan kode di bawah ini untuk melakukannya.

```python
byage_df = all_df.groupby(by="age_group").customer_id.nunique().reset_index()
byage_df.rename(columns={
    "customer_id": "customer_count"
}, inplace=True)
byage_df
byage_df['age_group'] = pd.Categorical(byage_df['age_group'], ["Youth", "Adults", "Seniors"])
plt.figure(figsize=(10, 5))
colors_ = ["#D3D3D3", "#72BCD4", "#D3D3D3", "#D3D3D3", "#D3D3D3"]
 
sns.barplot(
    y="customer_count", 
    x="age_group",
    data=byage_df.sort_values(by="age_group", ascending=False),
    palette=colors_
)
plt.title("Number of Customer by Age", loc="center", fontsize=15)
plt.ylabel(None)
plt.xlabel(None)
plt.tick_params(axis='x', labelsize=12)
plt.show()
```

Gambar di bawah ini merupakan hasil visualisasi data yang akan Anda peroleh.

![](https://assets.cdn.dicoding.com/original/academy/dos:6e1182dd93b8cd2b9772205f41968c1020230309163958.png)

Seperti yang bisa Anda lihat, pelanggan yang kita miliki didominasi oleh kelompok usia dewasa.

- **Berdasarkan states**

  Selain berdasarkan gender dan age, kita juga bisa melihat demografi pelanggan berdasarkan states atau negara bagiannya. Berikut contoh kode untuk melakukannya.

```python
bystate_df = all_df.groupby(by="state").customer_id.nunique().reset_index()
bystate_df.rename(columns={
    "customer_id": "customer_count"
}, inplace=True)
bystate_df
plt.figure(figsize=(10, 5))
colors_ = ["#72BCD4", "#D3D3D3", "#D3D3D3", "#D3D3D3", "#D3D3D3", "#D3D3D3", "#D3D3D3", "#D3D3D3"]
sns.barplot(
    x="customer_count", 
    y="state",
    data=bystate_df.sort_values(by="customer_count", ascending=False),
    palette=colors_
)
plt.title("Number of Customer by States", loc="center", fontsize=15)
plt.ylabel(None)
plt.xlabel(None)
plt.tick_params(axis='y', labelsize=12)
plt.show()
```

Kode di atas akan menghasilkan visualisasi data seperti berikut.

![](https://assets.cdn.dicoding.com/original/academy/dos:a08c248bbe0aa93b6638fd40734a9b0120230309164119.png)

Berdasarkan visualisasi data tersebut, dapat diketahui bahwa pelanggan yang kita miliki paling banyak berasal dari negara bagian South Australia.


Sebenarnya, Anda masih dapat mengidentifikasi demografi pelanggan berdasarkan kategori tertentu. Namun, untuk studi kasus ini, kita hanya akan melihat demografi pelanggan berdasarkan tiga kategori tersebut.


### RFM Analysis
Untuk menjawab tiga pertanyaan analisis terakhir, kita bisa menggunakan teknik analisis lanjutan yang bernama RFM analysis. Sederhananya, RFM analysis merupakan salah satu metode yang umum digunakan untuk melakukan segmentasi pelanggan (mengelompokkan pelanggan ke dalam beberapa kategori) berdasarkan tiga parameter, yaitu recency, frequency, dan monetary.

- Recency: parameter yang digunakan untuk melihat kapan terakhir seorang pelanggan melakukan transaksi.
- Frequency: parameter ini digunakan untuk mengidentifikasi seberapa sering seorang pelanggan melakukan transaksi.
- Monetary: parameter terakhir ini digunakan untuk mengidentifikasi seberapa besar revenue yang berasal dari pelanggan tersebut.

Nah, berdasarkan tiga parameter tersebut, kita bisa mengidentifikasi pelanggan mana yang memiliki high value (sering melakukan transaksi dan menghasilkan revenue yang besar) dan low value. 

Untuk melakukan RFM analysis, kita perlu membuat sebuah DataFrame untuk menampung informasi terkait tiga parameter tersebut. Berikut contoh kode yang dapat Anda gunakan untuk memperoleh informasi terkait recency, frequency, dan monetary.

```python
rfm_df = all_df.groupby(by="customer_id", as_index=False).agg({
    "order_date": "max", # mengambil tanggal order terakhir
    "order_id": "nunique", # menghitung jumlah order
    "total_price": "sum" # menghitung jumlah revenue yang dihasilkan
})
rfm_df.columns = ["customer_id", "max_order_timestamp", "frequency", "monetary"]
 
# menghitung kapan terakhir pelanggan melakukan transaksi (hari)
rfm_df["max_order_timestamp"] = rfm_df["max_order_timestamp"].dt.date
recent_date = orders_df["order_date"].dt.date.max()
rfm_df["recency"] = rfm_df["max_order_timestamp"].apply(lambda x: (recent_date - x).days)
 
rfm_df.drop("max_order_timestamp", axis=1, inplace=True)
rfm_df.head()
```

Kode di atas akan menghasilkan DataFrame berikut.

![](https://assets.cdn.dicoding.com/original/academy/dos:19e4d290b63e407096687fcecce6e3f820230309161832.jpeg)

Nah, pada tahap ini Anda dapat mengidentifikasi best customer berdasarkan parameter frequency, monetary, dan recancy menggunakan kode berikut.


```python
fig, ax = plt.subplots(nrows=1, ncols=3, figsize=(30, 6))
 
colors = ["#72BCD4", "#72BCD4", "#72BCD4", "#72BCD4", "#72BCD4"]
 
sns.barplot(y="recency", x="customer_id", data=rfm_df.sort_values(by="recency", ascending=True).head(5), palette=colors, ax=ax[0])
ax[0].set_ylabel(None)
ax[0].set_xlabel(None)
ax[0].set_title("By Recency (days)", loc="center", fontsize=18)
ax[0].tick_params(axis ='x', labelsize=15)
 
sns.barplot(y="frequency", x="customer_id", data=rfm_df.sort_values(by="frequency", ascending=False).head(5), palette=colors, ax=ax[1])
ax[1].set_ylabel(None)
ax[1].set_xlabel(None)
ax[1].set_title("By Frequency", loc="center", fontsize=18)
ax[1].tick_params(axis='x', labelsize=15)
 
sns.barplot(y="monetary", x="customer_id", data=rfm_df.sort_values(by="monetary", ascending=False).head(5), palette=colors, ax=ax[2])
ax[2].set_ylabel(None)
ax[2].set_xlabel(None)
ax[2].set_title("By Monetary", loc="center", fontsize=18)
ax[2].tick_params(axis='x', labelsize=15)
 
plt.suptitle("Best Customer Based on RFM Parameters (customer_id)", fontsize=20)
plt.show()
```

Hasilnya akan terlihat seperti gambar di bawah ini.

![](https://assets.cdn.dicoding.com/original/academy/dos:ea85c2505e93101fd798de0c5b6b58cf20230309164756.png)

Dari visualisasi data di atas, kita dapat melihat beberapa pelanggan terbaik berdasarkan ketiga parameter tersebut. Informasi ini tentunya dapat membantu kita dalam menjawab tiga pertanyaan analisis terakhir.

Selamat, sekarang Anda telah berhasil menjawab seluruh pertanyaan analisis yang telah dibuat sebelumnya. Selain itu, Anda juga telah berhasil membuat visualisasi data yang cukup efektif untuk menyampaikan informasi guna menjawab pertanyaan analisis tersebut. 


### buatlah laporan seperti biasanya dan Jawab pertanyaan berikut

1. Pada pilihan berikut, manakah ungkapan yang paling tepat untuk mendeskripsikan tahap data visualization?
- A. Cara kita dalam menyajikan data dalam bentuk visual.
- B. Proses untuk membersihkan data.
- C. Proses penyampaian pesan.
- D. Proses untuk menganalisis data.
1

2. Box plot merupakan salah satu bentuk visualisasi data yang digunakan untuk ....
- A. merepresentasikan nilai IQR beserta ambang batas bawah dan atas dari sebuah data data kuantitatif.
- B. mengidentifikasi distribusi pada data kategoris.
- C. menggambarkan tren nilai dari suatu variabel terhadap variabel lain
- D. melihat hubungan antara dua atau lebih variabel data kuantitatif.

3. Pada pilihan berikut, manakah yang bukan merupakan masalah atau kesalahan umum dalam visualisasi data yang buruk?
- A. Distracts
- B. Hides
- C. Misleading
- D. Colorful

4. Scatter plot merupakan salah satu bentuk visualisasi data yang digunakan untuk ....
- A. melihat hubungan antara dua atau lebih variabel data kuantitatif.
- B. merepresentasikan nilai IQR beserta ambang batas bawah dan atas dari sebuah data data kuantitatif.
- C. menggambarkan tren nilai dari suatu variabel terhadap variabel lain.
- D. mengidentifikasi distribusi pada data kategoris.