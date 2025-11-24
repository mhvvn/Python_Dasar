# LATIHAN EDA – DATASET 1 & DATASET 2

## A. Dataset 1: Data Kota dan Jumlah Bandara

### 1. Persiapan Dataset
```python
import pandas as pd

city_names = ['Jakarta', 'Bandung', 'Makassar', 'Surabaya', 'Medan', 'Yogyakarta', 'Malang']
population = [498044, 964254, 491918, 8398748, 653115, 883305, 744955]
num_airports = [2, 2, 8, 3, 1, 3, 2]

df = pd.DataFrame({
    'City Name': city_names,
    'Population': population,
    'Airports': num_airports,
})

df
```

---

## LATIHAN 1 – Statistik Deskriptif (`describe()`, `mean()`, `mode()`)

### Langkah:
- Tampilkan ringkasan statistik
- Hitung rata-rata populasi
- Hitung modus jumlah bandara

### Contoh kode:
```python
# Ringkasan statistik
df.describe()

# Rata-rata populasi
rata_rata_populasi = df['Population'].mean()
print("Rata-rata populasi:", rata_rata_populasi)

# Modus jumlah bandara
modus_airports = df['Airports'].mode()
print("Modus Airports:", modus_airports)
```

### TUGAS:
- Kota mana yang populasinya mendekati rata-rata?  
- Apa arti modus untuk kolom Airports?

---

## LATIHAN 2 – Visualisasi Distribusi (`hist()`)

### Tujuan:
Melihat distribusi jumlah penduduk.

### Contoh kode:
```python
import matplotlib.pyplot as plt

df['Population'].hist()
plt.title("Distribusi Populasi Kota")
plt.xlabel("Jumlah Penduduk")
plt.ylabel("Frekuensi")
plt.show()
```

### TUGAS:
Tuliskan pengamatan dari histogram tersebut.

---

## LATIHAN 3 – Korelasi & Kovarian (`corr()`, `cov()`)

### Tujuan:
Melihat apakah penduduk berhubungan dengan jumlah bandara.

### Contoh kode:
```python
# Korelasi
corr_matrix = df[['Population', 'Airports']].corr()
print("Korelasi:
", corr_matrix)

# Kovarian
cov_matrix = df[['Population', 'Airports']].cov()
print("Kovarian:
", cov_matrix)
```

### TUGAS:
- Apakah korelasinya positif atau negatif?  
- Apakah kota dengan penduduk besar cenderung punya lebih banyak bandara?

---

## LATIHAN 4 – Groupby (`groupby()`, `mean()`, `agg()`)

### Langkah:
- Membuat kolom kategori berdasarkan jumlah bandara

### Contoh kode:
```python
# Menambah kolom kategori
df['Kategori_Bandara'] = df['Airports'].apply(lambda x: 'Banyak' if x >= 3 else 'Sedikit')
df

# Rata-rata populasi per kategori
group_mean = df.groupby('Kategori_Bandara')['Population'].mean()
print(group_mean)

# Agregasi lengkap
group_agg = df.groupby('Kategori_Bandara').agg({
    'Population': ['mean', 'max'],
    'Airports': ['mean', 'count']
})
group_agg
```

### TUGAS:
- Bandingkan populasi kota dengan kategori “Banyak” dan “Sedikit”.  
- Apa kesimpulannya?

---

# B. Dataset 2: Body Measurement

## 1. Persiapan Dataset
```python
import pandas as pd

body_measurement_df = pd.DataFrame.from_records((
  (2, 83.82, 8.4),
  (4, 99.31, 16.97),
  (3, 96.52, 14.41),
  (6, 114.3, 20.14),
  (4, 101.6, 16.91),
  (2, 86.36, 12.64),
  (3, 92.71, 14.23),
  (2, 85.09, 11.11),
  (2, 85.85, 14.18),
  (5, 106.68, 20.01),
  (4, 99.06, 13.17),
  (5, 109.22, 15.36),
  (4, 100.84, 14.78),
  (6, 115.06, 20.06),
  (2, 84.07, 10.02),
  (7, 121.67, 28.4),
  (3, 94.49, 14.05),
  (6, 116.59, 17.55),
  (7, 121.92, 22.96),
), columns=("age", "height_cm", "weight_kg"))

body_measurement_df
```

---

## LATIHAN 5 – Statistik Deskriptif

### Contoh kode:
```python
# Ringkasan statistik
body_measurement_df.describe()

# Rata-rata tinggi & berat
mean_height = body_measurement_df['height_cm'].mean()
mean_weight = body_measurement_df['weight_kg'].mean()
print("Rata-rata tinggi:", mean_height)
print("Rata-rata berat:", mean_weight)

# Modus umur
mode_age = body_measurement_df['age'].mode()
print("Modus umur:", mode_age)
```

### TUGAS:
- Umur berapa yang paling sering muncul?  
- Apakah berat badan rata-rata ringan/sedang/berat?

---

## LATIHAN 6 – Distribusi Tinggi & Berat

### Contoh kode:
```python
import matplotlib.pyplot as plt

# Tinggi
body_measurement_df['height_cm'].hist()
plt.title("Distribusi Tinggi Badan (cm)")
plt.show()

# Berat
body_measurement_df['weight_kg'].hist()
plt.title("Distribusi Berat Badan (kg)")
plt.show()
```

### TUGAS:
Apakah tinggi & berat menyebar rata atau menumpuk?

---

## LATIHAN 7 – Groupby Usia

### Contoh kode:
```python
# Mean
group_mean_age = body_measurement_df.groupby("age").mean()
group_mean_age

# Agg lengkap
group_agg_age = body_measurement_df.groupby("age").agg({
    'height_cm': ['mean', 'min', 'max'],
    'weight_kg': ['mean', 'min', 'max']
})
group_agg_age
```

### TUGAS:
- Usia berapa rata-rata berat paling tinggi?  
- Apakah tinggi meningkat sesuai usia?

---

## LATIHAN 8 – Korelasi & Kovarian

### Contoh kode:
```python
# Korelasi
corr_hw = body_measurement_df[['height_cm', 'weight_kg']].corr()
print(corr_hw)

# Kovarian
cov_hw = body_measurement_df[['height_cm', 'weight_kg']].cov()
print(cov_hw)
```

### TUGAS:
- Apakah korelasinya kuat/lemah?  
- Apakah hubungannya positif?

