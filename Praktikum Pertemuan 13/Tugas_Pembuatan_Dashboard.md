# Penting!

Praktikum ini merupakan lanjutan dari materi Latihan Membuat Visualisasi Data. Oleh karena itu, sebelum melanjutkan materi ini, pastikan Anda telah menyelesaikan latihan tersebut.


## Tujuan
Pertama, kita akan melanjutkan proyek analisis data Dicoding Collection dengan menjalankan proses membuat dashboard sederhana. Proses ini memiliki tujuan antara lain:

membuat sebuah report analisis data yang interaktif dalam sebuah dashboard; dan
mempermudah audiens atau user dalam melihat hasil analisis data.


## Alur Praktikum
Berikut tahapan dalam latihan ini.

## Persiapan.
Menyiapkan DataFrame yang akan digunakan.
Membuat komponen filter pada dashboard.
Melengkapi dashboard dengan berbagai visualisasi data.


## Persiapan
Sebelum mulai mengerjakan latihan ini, terdapat beberapa hal yang harus disiapkan terlebih dahulu.

1. Pertama, siapkanlah Google Colab atau Jupyter Notebook yang sebelumnya digunakan pada materi Latihan Membuat Visualisasi Data.
2. Pastikan Anda menjalankan kembali seluruh kode yang ada pada notebook tersebut.
3. Pada bagian akhir tambahkan kode berikut untuk menyimpan berkas data yang telah dibersihkan.
```all_df.to_csv("all_data.csv", index=False)```

4. Unduh berkas data tersebut dengan mengklik tombol Download pada bagian file.
![](https://assets.cdn.dicoding.com/original/academy/dos:b6710246b93a5ae15c64fef083e24ee020230310141757.jpeg)

1. Instal berbagai library yang digunakan dengan beberapa perintah berikut pada terminal anaconda atau vscode.
   
   ``pip install streamlit babel`` dan ```pip install plotly```

2. Buka code editor VSCODE Anda dan buatlah sebuah proyek baru dengan nama dashboard.
   
3. Pindahkan berkas data (file csv)  yang sebelumnya sudah diunduh ke dalam folder proyek dashboard. 


# Menyiapkan DataFrame

Setelah tahap persiapan selesai, kini kita dapat mulai membuat dashboard dengan streamlit. Pada tahap awal tentunya kita perlu membuat sebuah berkas python dengan nama dashboard.py. Bukalah berkas tersebut dan tambahkan perintah berikut untuk mengimpor seluruh library yang dibutuhkan pada proyek ini.

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import streamlit as st
from babel.numbers import format_currency
sns.set(style='dark')

```

Tahap berikutnya adalah menyiapkan DataFrame yang akan digunakan untuk membuat visualisasi data. Untuk melakukan hal ini, kita perlu membuat beberapa helper function seperti berikut. Sebagai catatan, kode di bawah ini merupakan contoh kode yang telah kita gunakan pada materi latihan sebelumnya.

- **create_daily_orders_df()** digunakan untuk menyiapkan ``daily_orders_df``
```python
def create_daily_orders_df(df):
    daily_orders_df = df.resample(rule='D', on='order_date').agg({
        "order_id": "nunique",
        "total_price": "sum"
    })
    daily_orders_df = daily_orders_df.reset_index()
    daily_orders_df.rename(columns={
        "order_id": "order_count",
        "total_price": "revenue"
    }, inplace=True)
    
    return daily_orders_df

```


- **create_sum_order_items_df()** bertanggung jawab untuk menyiapkan ``sum_orders_items_df``
```python
def create_daily_orders_df(df):
    daily_orders_df = df.resample(rule='D', on='order_date').agg({
        "order_id": "nunique",
        "total_price": "sum"
    })
    daily_orders_df = daily_orders_df.reset_index()
    daily_orders_df.rename(columns={
        "order_id": "order_count",
        "total_price": "revenue"
    }, inplace=True)
    
    return daily_orders_df
```
- **create_sum_order_items_df()** bertanggung jawab untuk menyiapkan ```sum_orders_items_df.```

```python
def create_sum_order_items_df(df):
    sum_order_items_df = df.groupby("product_name").quantity_x.sum().sort_values(ascending=False).reset_index()
    return sum_order_items_df
```
- **create_bygender_df()** digunakan untuk menyiapkan ```bygender_df```

- **create_byage_df()** merupakan helper function yang digunakan untuk menyiapkan ``byage_df``.

```python
def create_byage_df(df):
    byage_df = df.groupby(by="age_group").customer_id.nunique().reset_index()
    byage_df.rename(columns={
        "customer_id": "customer_count"
    }, inplace=True)
    byage_df['age_group'] = pd.Categorical(byage_df['age_group'], ["Youth", "Adults", "Seniors"])
    
    return byage_df
```
- **create_bystate_df()** digunakan untuk menyiapkan ``bystate_df``


```python
def create_bystate_df(df):
    bystate_df = df.groupby(by="state").customer_id.nunique().reset_index()
    bystate_df.rename(columns={
        "customer_id": "customer_count"
    }, inplace=True)
    
    return bystate_df
```

- **create_rfm_df()** bertanggung jawab untuk menghasilkan ``rfm_df``

```python
def create_rfm_df(df):
    rfm_df = df.groupby(by="customer_id", as_index=False).agg({
        "order_date": "max", #mengambil tanggal order terakhir
        "order_id": "nunique",
        "total_price": "sum"
    })
    rfm_df.columns = ["customer_id", "max_order_timestamp", "frequency", "monetary"]
    
    rfm_df["max_order_timestamp"] = rfm_df["max_order_timestamp"].dt.date
    recent_date = df["order_date"].dt.date.max()
    rfm_df["recency"] = rfm_df["max_order_timestamp"].apply(lambda x: (recent_date - x).days)
    rfm_df.drop("max_order_timestamp", axis=1, inplace=True)
    
    return rfm_df
```
setelah menyiapkan beberapa helper function tersebut, tahap berikutnya ialah load berkas **all_data.csv** sebagai sebuah DataFrame menggunakan kode berikut.

```python
all_df = pd.read_csv("all_data.csv")
```
Seperti yang telah kita lihat pada materi Latihan Exploratory Data Analysis, all_df memiliki dua kolom yang bertipe **datetime**, yaitu **order_date** dan **delivery_date**.

Kolom order_date inilah yang akan menjadi kunci dalam pembuatan filter nantinya. Nah, untuk mendukung hal ini, kita perlu mengurutkan DataFrame berdasarkan order_date serta memastikan kedua kolom tersebut bertipe datetime.  

Berikut kode yang dapat kita gunakan untuk melakukan hal tersebut.


```python
datetime_columns = ["order_date", "delivery_date"]
all_df.sort_values(by="order_date", inplace=True)
all_df.reset_index(inplace=True)
 
for column in datetime_columns:
    all_df[column] = pd.to_datetime(all_df[column])
```


## Membuat Komponen Filter

Setelah berhasil menyiapkan DataFrame yang akan digunakan, tahap berikutnya ialah menambahkan filter pada dashboard yang akan dibuat. Pada latihan ini, kita akan menggunakan widget date input sebagai filternya dan akan ditempatkan pada bagian sidebar. Selain itu, untuk alasan estetika, kita juga perlu menambahkan logo perusahaan ke dalam sidebar tersebut. 

Berikut merupakan contoh kode yang dapat Anda gunakan untuk membuat filter dengan widget date input serta menambahkan logo perusahaan pada sidebar.


```python
min_date = all_df["order_date"].min()
max_date = all_df["order_date"].max()
 
with st.sidebar:
    # Menambahkan logo perusahaan
    st.image("https://raw.githubusercontent.com/mhvvn/dashboard_alldata/refs/heads/main/img/tshirt.png")
    
    # Mengambil start_date & end_date dari date_input
    start_date, end_date = st.date_input(
        label='Rentang Waktu',min_value=min_date,
        max_value=max_date,
        value=[min_date, max_date]
    )
```
Kode di atas akan menghasilkan start_date dan end_date yang selanjutnya akan digunakan untuk memfilter DataFrame. Berikut merupakan tampilan sidebar yang akan dihasilkan dari kode tersebut.

![](/Praktikum%20Pertemuan%2013/img/image1.png)


``start_date`` dan ``end_date`` di atas akan digunakan untuk memfilter ``all_df``.  Data yang telah difilter ini selanjutnya akan disimpan dalam ``main_df``

Proses ini dijalankan menggunakan kode berikut.

```python
main_df = all_df[(all_df["order_date"] >= str(start_date)) & 
                (all_df["order_date"] <= str(end_date))]
```

DataFrame yang telah difilter (main_df) inilah yang digunakan untuk menghasilkan berbagai DataFrame yang dibutuhkan untuk membuat visualisasi data. Proses ini tentunya dilakukan dengan memanggil helper function yang telah kita buat sebelumnya.

```python
daily_orders_df = create_daily_orders_df(main_df)
sum_order_items_df = create_sum_order_items_df(main_df)
bygender_df = create_bygender_df(main_df)
byage_df = create_byage_df(main_df)
bystate_df = create_bystate_df(main_df)
rfm_df = create_rfm_df(main_df)
```

## Melengkapi Dashboard dengan Berbagai Visualisasi Data

setelah membuat filter dan menyiapkan seluruh DataFrame yang dibutuhkan, kini saatnya kita melengkapi dashboard tersebut dengan berbagai visualisasi data. Pada bagian awal, kita perlu menambahkan header pada dashboard tersebut. Berikut merupakan kode untuk melakukannya.

```python
st.header('My Collection Dashboard :sparkles:')
```
Kode tersebut akan menghasilkan tampilan header seperti di bawah ini.

![alt text](image.png)

Tahap berikutnya adalah menambahkan informasi terkait daily orders pada dashboard yang akan kita buat. Pada proyek ini, kita akan menampilkan tiga informasi terkait daily orders, yaitu jumlah order harian serta total order dan revenue dalam range waktu tertentu. 

Pada contoh proyek ini, kita menampilkan informasi total order dan revenue dalam bentuk metric() yang ditampilkan menggunakan layout columns(). Di lain sisi, informasi tentang jumlah order harian ditampilkan dalam bentuk visualisasi data seperti kode berikut.

```python
st.subheader('Daily Orders')
 
col1, col2 = st.columns(2)
 
with col1:
    total_orders = daily_orders_df.order_count.sum()
    st.metric("Total orders", value=total_orders)
 
with col2:
    total_revenue = format_currency(daily_orders_df.revenue.sum(), "AUD", locale='es_CO') 
    st.metric("Total Revenue", value=total_revenue)
 
fig, ax = plt.subplots(figsize=(16, 8))
ax.plot(
    daily_orders_df["order_date"],
    daily_orders_df["order_count"],
    marker='o', 
    linewidth=2,
    color="#90CAF9"
)
ax.tick_params(axis='y', labelsize=20)
ax.tick_params(axis='x', labelsize=15)
 
st.pyplot(fig)
```
kode tersebut akan menghasilkan tampilan dashboard seperti berikut.

![](https://assets.cdn.dicoding.com/original/academy/dos:f36f44cadc6f411a2b7b146ba714d20120230310141758.jpeg)


Selain informasi terkait daily orders, kita juga perlu menyertakan informasi tentang performa penjualan dari setiap produk. Pada proyek ini, kita akan menampilkan 5 produk paling laris dan paling sedikit terjual melalui sebuah visualisasi data.

ling laris dan paling sedikit terjual melalui sebuah visualisasi data. 


```python

st.subheader("Best & Worst Performing Product")
 
fig, ax = plt.subplots(nrows=1, ncols=2, figsize=(35, 15))
 
colors = ["#90CAF9", "#D3D3D3", "#D3D3D3", "#D3D3D3", "#D3D3D3"]
 
sns.barplot(x="quantity_x", y="product_name", data=sum_order_items_df.head(5), palette=colors, ax=ax[0])
ax[0].set_ylabel(None)
ax[0].set_xlabel("Number of Sales", fontsize=30)
ax[0].set_title("Best Performing Product", loc="center", fontsize=50)
ax[0].tick_params(axis='y', labelsize=35)
ax[0].tick_params(axis='x', labelsize=30)
 
sns.barplot(x="quantity_x", y="product_name", data=sum_order_items_df.sort_values(by="quantity_x", ascending=True).head(5), palette=colors, ax=ax[1])
ax[1].set_ylabel(None)
ax[1].set_xlabel("Number of Sales", fontsize=30)
ax[1].invert_xaxis()
ax[1].yaxis.set_label_position("right")
ax[1].yaxis.tick_right()
ax[1].set_title("Worst Performing Product", loc="center", fontsize=50)
ax[1].tick_params(axis='y', labelsize=35)
ax[1].tick_params(axis='x', labelsize=30)
 
st.pyplot(fig)
```

Hasil yang akan Anda dapatkan dari kode di atas adalah seperti berikut.

![](https://assets.cdn.dicoding.com/original/academy/dos:04b3272ec2e21a170eb62b4715ca745820230310141757.jpeg)

Informasi berikutnya yang ingin kita tampilkan pada dashboard tersebut ialah terkait demografi pelanggan yang kita miliki. Pada materi Latihan Membuat Visualisasi Data, kita telah membuat tiga buah visualisasi data untuk menjelaskan hal tersebut.


kita akan memasukkan ketiganya ke dalam dashboard dengan kode seperti berikut.

```python
st.subheader("Customer Demographics")
 
col1, col2 = st.columns(2)
 
with col1:
    fig, ax = plt.subplots(figsize=(20, 10))
 
    sns.barplot(
        y="customer_count", 
        x="gender",
        data=bygender_df.sort_values(by="customer_count", ascending=False),
        palette=colors,
        ax=ax
    )
    ax.set_title("Number of Customer by Gender", loc="center", fontsize=50)
    ax.set_ylabel(None)
    ax.set_xlabel(None)
    ax.tick_params(axis='x', labelsize=35)
    ax.tick_params(axis='y', labelsize=30)
    st.pyplot(fig)
 
with col2:
    fig, ax = plt.subplots(figsize=(20, 10))
    
    colors = ["#D3D3D3", "#90CAF9", "#D3D3D3", "#D3D3D3", "#D3D3D3"]
 
    sns.barplot(
        y="customer_count", 
        x="age_group",
        data=byage_df.sort_values(by="age_group", ascending=False),
        palette=colors,
        ax=ax
    )
    ax.set_title("Number of Customer by Age", loc="center", fontsize=50)
    ax.set_ylabel(None)
    ax.set_xlabel(None)
    ax.tick_params(axis='x', labelsize=35)
    ax.tick_params(axis='y', labelsize=30)
    st.pyplot(fig)
 
fig, ax = plt.subplots(figsize=(20, 10))
colors = ["#90CAF9", "#D3D3D3", "#D3D3D3", "#D3D3D3", "#D3D3D3", "#D3D3D3", "#D3D3D3", "#D3D3D3"]
sns.barplot(
    x="customer_count", 
    y="state",
    data=bystate_df.sort_values(by="customer_count", ascending=False),
    palette=colors,
    ax=ax
)
ax.set_title("Number of Customer by States", loc="center", fontsize=30)
ax.set_ylabel(None)
ax.set_xlabel(None)
ax.tick_params(axis='y', labelsize=20)
ax.tick_params(a
```

Kode di atas akan menghasilkan tampilan dashboard seperti di bawah ini.

![](https://assets.cdn.dicoding.com/original/academy/dos:513ca0bc978b1a6ac61b5bd59469dedc20230310141757.jpeg)

Informasi terakhir yang harus kita tampilkan ialah terkait parameter RFM (Recency, Frequency, & Monetary). Nah, pada proyek ini, kita akan menampilkan nilai average atau rata-rata dari ketiga parameter tersebut menggunakan widget metric(). Selain itu kita juga akan menampilkan hasil visualisasi data dari latihan sebelumnya. Berikut kode untuk melakukan hal tersebut.


```python
st.subheader("Best Customer Based on RFM Parameters")
 
col1, col2, col3 = st.columns(3)
 
with col1:
    avg_recency = round(rfm_df.recency.mean(), 1)
    st.metric("Average Recency (days)", value=avg_recency)
 
with col2:
    avg_frequency = round(rfm_df.frequency.mean(), 2)
    st.metric("Average Frequency", value=avg_frequency)
 
with col3:
    avg_frequency = format_currency(rfm_df.monetary.mean(), "AUD", locale='es_CO') 
    st.metric("Average Monetary", value=avg_frequency)
 
fig, ax = plt.subplots(nrows=1, ncols=3, figsize=(35, 15))
colors = ["#90CAF9", "#90CAF9", "#90CAF9", "#90CAF9", "#90CAF9"]
 
sns.barplot(y="recency", x="customer_id", data=rfm_df.sort_values(by="recency", ascending=True).head(5), palette=colors, ax=ax[0])
ax[0].set_ylabel(None)
ax[0].set_xlabel("customer_id", fontsize=30)
ax[0].set_title("By Recency (days)", loc="center", fontsize=50)
ax[0].tick_params(axis='y', labelsize=30)
ax[0].tick_params(axis='x', labelsize=35)
 
sns.barplot(y="frequency", x="customer_id", data=rfm_df.sort_values(by="frequency", ascending=False).head(5), palette=colors, ax=ax[1])
ax[1].set_ylabel(None)
ax[1].set_xlabel("customer_id", fontsize=30)
ax[1].set_title("By Frequency", loc="center", fontsize=50)
ax[1].tick_params(axis='y', labelsize=30)
ax[1].tick_params(axis='x', labelsize=35)
 
sns.barplot(y="monetary", x="customer_id", data=rfm_df.sort_values(by="monetary", ascending=False).head(5), palette=colors, ax=ax[2])
ax[2].set_ylabel(None)
ax[2].set_xlabel("customer_id", fontsize=30)
ax[2].set_title("By Monetary", loc="center", fontsize=50)
ax[2].tick_params(axis='y', labelsize=30)
ax[2].tick_params(axis='x', labelsize=35)
 
st.pyplot(fig)
 
st.caption('Copyright (c) My COllection 2025')

Hasil yang akan kita peroleh akan terlihat seperti di bawah ini.

![](https://assets.cdn.dicoding.com/original/academy/dos:e31bb7f30287f7eb2d0b7491456c757120230310141757.jpeg)

itulah berbagai visualisasi data yang harus kita tampilkan dalam dashboard. Jika seluruh proses di atas berjalan lancar, Anda akan memperoleh tampilan dashboard seperti berikut.

```
Selamat! Anda telah berhasil membuat dashboard dengan streamlit.


Semoga seluruh materi pada kelas ini dapat menjadi bekal bagi Anda untuk memulai karier sebagai seorang praktisi data.


## Tugas
- Silahkan Modifikasi codingan tersebut, agar dapat berjalan di platform **share.streamlit.io** dengan mengganti library **matplotlib** dengan **plotly** sebagai alternatif https://plotly.com/python/ 

- sehingga hasilnya seperti dashboard pada link berikut ini 
  https://dashboardalldata.streamlit.app/