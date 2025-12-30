# Praktikum Pembuatan Dashboard Customers

1. Download file dataset ``customers.csv`` pada link berikut ini.
    https://drive.google.com/file/d/1on5TCiYvn-bR5eEv-oOmZUrcdNSk1vlN/view 
2. Buatlah folder baru untuk praktikum kali ini, dengan nama Dashboard_Customers
3. Copy / pindahkan file csv yg di download ke dalam file tersebut
4. Bukalah code editor VSCode untuk melakukan praktikum 
5. Buat file python  dengan nama ``streamlit_app.py``

Langkah-langkah hampir sama dengan pertemyan sebelumnya

copy potongan kode berikut ini kedalam file project anda lalu running dan lihat perubahan pada web browser

perintah untuk menjalankan pada terminal ``streamlit run namafile.py``


```python
import streamlit as st
import pandas as pd
import plotly.express as px
```

```python
st.title("Customer Analytics Dashboard")
```
Jalankan dan lihat perubahanya
``streamlit run namafile``

```python
df = pd.read_csv("customers.csv")

```
Jalankan dan lihat perubahanya

```python
st.sidebar.header("Filter Data")
departments = st.sidebar.multiselect(
    "Pilih Departments",
    df["Department"].dropna().unique()
)
```
Jalankan dan lihat perubahanya
```python
genders = st.sidebar.multiselect(
    "Pilih Gender",
    df["Gender"].dropna().unique()
)
```

Jalankan dan lihat perubahanya
```python
st.sidebar.header("Filter Rentang Umur")
min_usia, max_usia = int(df["Age"].min()), int(df["Age"].max())
usia_range = st.sidebar.slider(
    "Usia",
    min_value=min_usia,
    max_value=max_usia,
    value=(min_usia, max_usia)
)
```

Jalankan dan lihat perubahanya
```python
df_filtered = df[
    (df["Department"].isin(departments)) &
    (df["Gender"].isin(genders)) &
    (df["Age"].between(usia_range[0], usia_range[1]))
]
```

Jalankan dan lihat perubahanya
```python
st.subheader("Data Tabel")
```
```python
st.dataframe(df_filtered)
```
Jalankan dan lihat perubahanya
```python
st.subheader("Visualisasi Statistik")
```
```python
col1, col2 = st.columns(2)
```
```python
with col1:
    st.subheader("Distribusi Gender")
    pie_gender = px.pie(
        df_filtered,
        names="Gender",
        color="Gender",
        color_discrete_sequence=px.colors.qualitative.Set2
    )
    st.plotly_chart(pie_gender)
```

Jalankan dan lihat perubahanya
```python
with col2:
    st.subheader("Gaji Rata-rata per Department")

    salary_dept = (
        df_filtered
        .groupby("Department")["AnnualSalary"]
        .mean()
        .reset_index()
    )

    bar_salary = px.bar(
        salary_dept,
        x="Department",
        y="AnnualSalary",
        color="Department",
        color_discrete_sequence=px.colors.qualitative.Pastel
    )
    st.plotly_chart(bar_salary)
```

Jalankan dan lihat perubahanya
```python

st.subheader("Rata-rata Gaji Berdasarkan Usia")
```

Jalankan dan lihat perubahanya
```python
salary_age = (
    df_filtered
    .groupby("Age")["AnnualSalary"]
    .mean()
    .reset_index()
    .sort_values("Age")
)

line_age = px.line(
    salary_age,
    x="Age",
    y="AnnualSalary",
    markers=True
)

st.plotly_chart(line_age)
```
```python

st.subheader("Tambahakn Chart Lainnya Versi Anda Sendiri!")
st.write("Untuk menambahkan chart lihat dan pahami struktur tabel data set file customers.csv")
```

Jalankan dan lihat perubahanya


Sebelum di upload ke share.streamlit.io silahkan tambahkan file berikut ini ```requirements.txt```

```python
streamlit
pandas
plotly

```


# Modifikasi dan tambahkan chart lainya dengan mengacu pada tabel pada file customers.csv

![](/Praktikum%20Pertemuan%2013/img/image.png)