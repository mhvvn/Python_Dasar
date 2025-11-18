
# PRAKTIKUM: DATA WRANGLING 

**Mata Kuliah:** Pemrograman Dasar dengan Python dan Analisis Data  
**Tujuan:** Mahasiswa memahami proses menyiapkan dan membersihkan data agar siap digunakan untuk analisis.

---

# Tujuan Pembelajaran
Setelah mengikuti praktikum ini, mahasiswa mampu:

- Menjelaskan konsep dasar **Data Wrangling**.  
- Melakukan proses **Assessing** (menilai kualitas data).  
- Melakukan **Cleaning** (pembersihan data sederhana).  
- Mengimplementasikan proses Data Wrangling menggunakan Python di Google Colab.  

---

# 1. Pengenalan Data Wrangling

### **Apa itu Data Wrangling?**
Data Wrangling adalah proses menyiapkan data mentah agar siap dianalisis dengan cara **gathering**, **assessing**, dan **cleaning** data.

Tujuan utamanya adalah mengubah data mentah menjadi **data yang rapi (tidy data)** sehingga mudah diproses pada tahap analisis atau visualisasi.

### **Tahapan Umum:**

| Tahap          | Kegiatan Utama                         | Tujuan                                      |
|----------------|-----------------------------------------|---------------------------------------------|
| Gathering Data | Mengambil data dari berbagai sumber     | Mendapatkan dataset yang diperlukan         |
| Assessing Data | Menilai kualitas & struktur data        | Menemukan masalah data                      |
| Cleaning Data  | Memperbaiki kesalahan data              | Menghasilkan data siap pakai untuk analisis |

---

# 2. Gathering Data (Membuat Data Manual)

Pada tahap ini, kita membuat data dummy agar mudah dipahami.

```python
import pandas as pd

# Membuat data dummy mahasiswa
data = {
    'Nama': ['Aldi', 'Budi', 'Citra', 'Dewi', 'Eka', 'Fajar'],
    'Umur': [20, 21, 22, None, 23, 21],
    'Nilai_Tugas': [85, 90, None, 78, 88, 90],
    'Nilai_UAS': [80, 92, 85, 70, None, 95],
    'Jurusan': ['Energi', 'Energi', 'Teknik', 'Teknik', 'Energi', None]
}

df = pd.DataFrame(data)
df
```

---

# 3. Assessing Data (Menilai Kualitas Data)

### a. Melihat Ringkasan Data
```python
df.info()
```

### b. Melihat Statistik Deskriptif
```python
df.describe()
```

### c. Mendeteksi Nilai Hilang
```python
df.isnull().sum()
```

### d. Menemukan Data Ganda
```python
df.duplicated().sum()
```

---

# 4. Cleaning Data (Membersihkan Data)

## a. Mengisi Nilai Kosong (Missing Values)
```python
# Mengisi nilai kosong di kolom numerik dengan nilai rata-rata
df['Umur'] = df['Umur'].fillna(df['Umur'].mean())
df['Nilai_Tugas'] = df['Nilai_Tugas'].fillna(df['Nilai_Tugas'].mean())
df['Nilai_UAS'] = df['Nilai_UAS'].fillna(df['Nilai_UAS'].mean())

# Mengisi nilai kosong di kolom kategorik dengan 'Tidak Diketahui'
df['Jurusan'] = df['Jurusan'].fillna('Tidak Diketahui')

df
```

---

## b. Menghapus Baris Duplikat
```python
# Tambahkan satu data duplikat untuk simulasi
df.loc[len(df)] = ['Aldi', 20, 85, 80, 'Energi']

# Cek jumlah duplikat
print("Jumlah duplikat sebelum dihapus:", df.duplicated().sum())

# Hapus duplikat
df = df.drop_duplicates()

print("Jumlah duplikat setelah dihapus:", df.duplicated().sum())
```

---

## c. Menstandarkan Format Data
```python
# Ubah semua nama jurusan menjadi huruf kapital
df['Jurusan'] = df['Jurusan'].str.upper()

df
```

---

#  5. Latihan Praktikum: Data Wrangling

### **Tugas Mahasiswa**
1. Download file *mahasiswa.csv* yang ada pada repositpry github, cara download seperti gambar berikut ini : ![example](/Praktikum%20Pertemuan%2008/image/downloadz-csv_file.png)
   
2. Lalu buat file google collab baru dengan nama latihan 08
   
3. Setelah itu, klik pada icon file -> klik icon upload file dan upload file mahasiswa.csv,  sperti gambar di bawah ini
   ![example](/Praktikum%20Pertemuan%2008/image/images01.png)
4. Selanjutnya buka file **Latihan_08.ipynb** lalu ikuti step by step nya
5. Buatlah laporan sesuai dengan yang di kerjakan pada pertemuan 08 ini.
6. file **Latihan_08.ipynb**  bisa di lihat di link berikut : https://colab.research.google.com/drive/1VQePS4i1a32iLtlxPxEvz1iyAWQ7aybc?usp=sharing 
   ```

---

# Ringkasan Tahapan Data Wrangling

| Tahap     | Tujuan                                 | Contoh Kode                     |
|-----------|-----------------------------------------|---------------------------------|
| Gathering | Mengambil atau membuat data             | `pd.DataFrame(data)`            |
| Assessing | Menilai kualitas data                  | `.info()`, `.isnull()`, `.duplicated()` |
| Cleaning  | Membersihkan & menstandarkan data      | `.fillna()`, `.drop_duplicates()`, `.str.upper()` |


# Kesimpulan

- **Data Wrangling adalah fondasi utama** sebelum analisis data dilakukan.  
- Proses ini memastikan data **bersih, lengkap, dan konsisten**.  
- Menguasai proses *gathering*, *assessing*, dan *cleaning* akan mempermudah tahapan analisis berikutnya.  

---

