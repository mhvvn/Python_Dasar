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
- **create_sum_order_items_df()** bertanggung jawab untuk menyiapkan sum_orders_items_df.

```python
def create_sum_order_items_df(df):
    sum_order_items_df = df.groupby("product_name").quantity_x.sum().sort_values(ascending=False).reset_index()
    return sum_order_items_df
```
- create_bygender_df() digunakan untuk menyiapkan bygender_df
```python
```
```python
```
```python
```
```python
```
```python
```
```python
```
```python
```