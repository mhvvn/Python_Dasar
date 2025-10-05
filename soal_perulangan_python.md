# Soal Latihan Praktikum Perulangan (for dan while) Bahasa Pemrograman Python

## Petunjuk Pengerjaan
Lengkapi bagian kode yang ditandai dengan garis bawah (`______`) pada setiap soal agar program dapat berjalan sesuai dengan deskripsi cerita/kasus yang diberikan. Jawaban harus menggunakan konsep perulangan yang relevan (`for` atau `while`).

---

### **Soal 1: Mencetak Bilangan Ganjil dalam Jangkauan**
**Deskripsi Kasus:**  
Diberikan tugas untuk membuat program yang mencetak semua bilangan ganjil secara berurutan, dimulai dari angka 1 hingga 9. Gunakan perulangan `for` untuk iterasi ini.

```python
print("--- Soal 1 ---")
# Mencetak bilangan ganjil 1 hingga 9
for angka in range(1, 10, 2):
    print(angka)
```

---

### **Soal 2: Pemberhentian Proses oleh Sentinel**
**Deskripsi Kasus:**  
Sebuah sistem memerlukan input angka dari pengguna. Program harus terus meminta input secara berulang (perulangan) dan baru akan berhenti ketika pengguna memasukkan angka `99`. Gunakan perulangan `while` untuk menangani kondisi ini.

```python
print("--- Soal 2 ---")
kode_berhenti = 99
input_pengguna = 0  # Inisialisasi awal

while input_pengguna != kode_berhenti:
    try:
        input_pengguna = int(input("Masukkan angka (99 untuk berhenti): "))
    except ValueError:
        print("Input tidak valid. Harap masukkan angka.")

print("Perulangan telah dihentikan oleh sentinel (99).")
```

---

### **Soal 3: Menghitung Total Belanja dari Daftar**
**Deskripsi Kasus:**  
Anda memiliki sebuah daftar (list) yang berisi harga-harga barang. Buatlah perulangan `for` untuk menjumlahkan seluruh harga barang dalam daftar tersebut untuk mendapatkan total biaya belanja.

```python
print("--- Soal 3 ---")
harga_barang = [15000, 25000, 10000, 5000]
total_belanja = 0

for harga in harga_barang:
    total_belanja += harga

print("Total biaya belanja adalah:", total_belanja)
```

---

### **Soal 4: Batasan Percobaan (Limitasi Iterasi)**
**Deskripsi Kasus:**  
Seorang pengguna diberi tiga kali kesempatan (maksimal) untuk memasukkan password. Buatlah perulangan `while` yang menghitung dan membatasi jumlah percobaan tersebut.

```python
print("--- Soal 4 ---")
percobaan_maksimal = 3
percobaan_saat_ini = 1

while percobaan_saat_ini <= percobaan_maksimal:
    print(f"Percobaan ke-{percobaan_saat_ini}...")
    # Asumsi ada logika input password di sini
    percobaan_saat_ini += 1
    
if percobaan_saat_ini == percobaan_maksimal + 1:  # Karena perulangan berhenti saat menjadi 4
    print("Kesempatan habis.")
else:
    print("Akses diterima.")
```

---

### **Soal 5: Mencetak Karakter dari Teks**
**Deskripsi Kasus:**  
Buat program yang menggunakan perulangan `for` untuk mengiterasi melalui setiap karakter dalam sebuah string, kemudian mencetak setiap karakter tersebut diikuti dengan tanda hubung (`-`).

```python
print("--- Soal 5 ---")
nama_proyek = "PRAKTIKUM"
hasil_output = ""

for karakter in nama_proyek:
    hasil_output += karakter + "-"

print(hasil_output)  # Output: P-R-A-K-T-I-K-U-M-
```

---

## **Soal Latihan Tingkat Lanjut (Menengah Rendah)**

### **Soal 6: Iterasi Mundur**
**Deskripsi Kasus:**  
Anda diminta untuk membuat countdown (hitung mundur) dari angka 5 sampai 1. Program harus mencetak angka 5, 4, 3, 2, 1 secara berurutan. Gunakan perulangan `for` dengan fungsi `range()`.

```python
print("--- Soal 6 ---")
# Countdown dari 5 ke 1
for i in range(5, 0, ______):
    print(i)
```

---

### **Soal 7: Mengakses Elemen dan Indeks Secara Bersamaan**
**Deskripsi Kasus:**  
Diberikan daftar nama-nama bulan. Anda perlu mencetak setiap bulan beserta nomor urut (indeks) bulan tersebut, dimulai dari nomor 1. Gunakan perulangan `for` dan fungsi `enumerate()`.

```python
print("--- Soal 7 ---")
bulan = ["Januari", "Februari", "Maret", "April"]

for ______:
    # i adalah indeks, nama adalah elemen
    print(f"Bulan ke-{i + 1}: {nama}")
```

---

### **Soal 8: Kontrol Perulangan dengan break**
**Deskripsi Kasus:**  
Terdapat sebuah daftar angka. Buat perulangan `for` untuk mencetak setiap angka, tetapi perulangan harus segera dihentikan (menggunakan `break`) ketika bertemu dengan angka `-1`.

```python
print("--- Soal 8 ---")
data_angka = [10, 20, 30, -1, 50, 60]

for angka in data_angka:
    if angka ______:
        ______
    print(angka)

print("Program berhenti karena angka -1 ditemukan.")
```

---

### **Soal 9: Penambahan Berkelanjutan dengan Batas**
**Deskripsi Kasus:**  
Hitung jumlah semua bilangan bulat positif, dimulai dari 1, sampai total jumlah (sum) tersebut melebihi angka 20. Gunakan perulangan `while` dan tampilkan nilai total terakhir.

```python
print("--- Soal 9 ---")
total = 0
bilangan = 1
batas = 20

while total ______ batas:
    total += bilangan
    bilangan += 1

print("Total terakhir:", total)
```

---

### **Soal 10: Perulangan Bersarang (Nested Loop) Sederhana**
**Deskripsi Kasus:**  
Anda ingin mencetak pola sederhana berupa 3 baris teks `Python`. Untuk melakukan ini, Anda dapat menggunakan perulangan luar untuk baris, dan perulangan dalam untuk mencetak kata `Python` sebanyak 1 kali per baris. Lengkapi perulangan dalam.

```python
print("--- Soal 10 ---")
jumlah_baris = 3

for baris in range(jumlah_baris):
    baris_teks = ""
    for ______:
        baris_teks += "Python "
    print(baris_teks)

# Output:
# Python
# Python
# Python
```

