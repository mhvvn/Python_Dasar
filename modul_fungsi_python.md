# MODUL PRAKTIKUM: PEMBUATAN FUNGSI LANJUTAN PYTHON

**Mata Kuliah:** Dasar-Dasar Pemrograman  
**Dosen Pengampu:** [Nama Anda]

---

## Pendahuluan
Tujuan dari modul praktikum ini adalah untuk melatih kemampuan mahasiswa dalam mendefinisikan dan menggunakan fungsi (`def`) dalam bahasa pemrograman Python. Fungsi merupakan blok kode yang terorganisir dan dapat digunakan kembali untuk menjalankan tugas tertentu, sebuah konsep fundamental dalam pemrograman prosedural dan berorientasi objek.

Mahasiswa diharapkan dapat mengisi bagian yang dikosongkan (`______`) agar kode dapat berjalan sesuai dengan deskripsi kasus.

---

## Soal Latihan Pembuatan Fungsi

### **Soal 1: Fungsi Sederhana Tanpa Parameter (Inisialisasi)**
**Narasi Kasus:**  
Anda diminta untuk membuat fungsi inisialisasi pada sistem program yang bertugas memberikan sambutan awal. Fungsi ini tidak memerlukan input apapun dari luar (tanpa parameter).

**Tugas:**  
Lengkapi definisi fungsi bernama `sapa_praktikan` dan isi argumennya.

```python
# SOAL 1: Fungsi Inisialisasi Sederhana
def sapa_praktikan(______):
    """Mencetak pesan sambutan dasar."""
    print("Sistem siap. Selamat datang kembali di sesi praktikum.")

# Pemanggilan:
sapa_praktikan()
```

**Alternatif Modifikasi (Tingkat Lanjut):** Tambahkan docstring yang lebih deskriptif pada fungsi tersebut, menjelaskan tujuan dan tanggal pembuatannya.

---

### **Soal 2: Fungsi dengan Parameter Primitif (Matematika)**
**Narasi Kasus:**  
Sebagai bagian dari modul perhitungan geometris, Anda perlu mendefinisikan fungsi untuk menghitung volume dari sebuah kubus. Volume kubus dihitung dari sisi pangkat tiga (`s³`).

**Tugas:**  
Lengkapi parameter fungsi `hitung_volume_kubus` dan operasi aritmatika yang sesuai.

```python
# SOAL 2: Menghitung Volume Kubus
def hitung_volume_kubus(sisi):
    """Menghitung volume kubus dari panjang sisinya."""
    return sisi ______ 3

# Pemanggilan:
panjang_sisi = 5
print(f"Volume kubus dengan sisi {panjang_sisi} adalah: {hitung_volume_kubus(panjang_sisi)}")
```

**Alternatif Modifikasi (Tingkat Lanjut):** Ubah fungsi agar dapat menghitung volume balok dengan menerima tiga parameter: panjang, lebar, dan tinggi.

---

### **Soal 3: Fungsi dengan Parameter Non-Primitif (list) dan Perulangan (for)**
**Narasi Kasus:**  
Anda memiliki data nilai ujian mahasiswa dalam bentuk list. Buat fungsi yang menerima list nilai tersebut. Fungsi harus menggunakan perulangan `for` untuk menjumlahkan semua nilai, lalu mengembalikan nilai rata-ratanya.

**Tugas:**  
Lengkapi perulangan `for` untuk mengiterasi daftar nilai dan hitung panjang list untuk pembagian rata-rata.

```python
# SOAL 3: Menghitung Rata-rata dari List Nilai
def hitung_rata_rata(data_nilai):
    """Menghitung rata-rata dari list angka menggunakan perulangan for."""
    total = 0
    
    # Perulangan untuk menjumlahkan nilai
    for nilai in ______:
        total += nilai
    
    # Pembagian untuk rata-rata
    if total > 0:
        return total / ______
    return 0

# Pemanggilan:
nilai_praktikan = [85, 78, 92, 65, 90]
print(f"Nilai rata-rata kelas adalah: {hitung_rata_rata(nilai_praktikan)}")
```

**Alternatif Modifikasi (Tingkat Lanjut):** Tambahkan pengecekan menggunakan percabangan `if` di dalam perulangan `for` untuk mengabaikan atau memberikan penalti jika ada nilai di bawah 0 atau di atas 100.

---

### **Soal 4: Fungsi dengan Percabangan (if, elif, else)**
**Narasi Kasus:**  
Dalam sistem penilaian, Anda perlu membuat fungsi `tentukan_predikat` yang menentukan predikat (A, B, C, D, E) berdasarkan skor numerik (0–100).

**Tugas:**  
Lengkapi kondisi `elif` untuk predikat B dan `return` untuk predikat C.

| Skor | Predikat |
|------|-----------|
| ≥ 85 | A |
| 70 - 84 | B |
| 60 - 69 | C |
| 50 - 59 | D |
| < 50 | E |

```python
# SOAL 4: Sistem Penentuan Predikat Nilai
def tentukan_predikat(skor):
    """Menentukan predikat (A, B, C, D, E) berdasarkan skor."""
    if skor >= 85:
        return "A"
    elif skor ______:
        return "B"
    elif skor >= 60:
        return ______
    elif skor >= 50:
        return "D"
    else:
        return "E"

# Pemanggilan:
print(f"Skor 75 mendapat predikat: {tentukan_predikat(75)}")
print(f"Skor 48 mendapat predikat: {tentukan_predikat(48)}")
```

**Alternatif Modifikasi (Tingkat Lanjut):** Implementasikan pengecekan tipe data agar hanya menerima input numerik (int/float).

---

### **Soal 5: Fungsi dengan Implementasi Perulangan while**
**Narasi Kasus:**  
Buatlah fungsi yang dapat menghitung faktorial dari sebuah bilangan bulat positif `n` (`n! = n × (n−1) × ... × 1`). Proses pengurangan bilangan harus diimplementasikan menggunakan perulangan `while`.

**Tugas:**  
Lengkapi kondisi perulangan `while` dan operasi pengurangan pada variabel `n`.

```python
# SOAL 5: Menghitung Faktorial dengan Loop While
def hitung_faktorial(n):
    """Menghitung faktorial dari bilangan positif n."""
    hasil = 1
    
    # Perulangan berjalan selama n lebih besar dari 1
    while ______:
        hasil *= n
        n ______ 1  # Kurangi n
    return hasil

# Pemanggilan:
bilangan_n = 4
print(f"Faktorial dari {bilangan_n} adalah: {hitung_faktorial(bilangan_n)}")  # Output: 24
```

**Alternatif Modifikasi (Tingkat Lanjut):** Tambahkan percabangan `if` untuk menangani kasus khusus seperti `n = 0` atau `n < 0`.

---

### **Soal 6: Fungsi Komprehensif (Gabungan Perulangan dan Percabangan)**
**Narasi Kasus:**  
Anda ditugaskan untuk menganalisis data sensor suhu harian dalam sebuah list (`data_suhu`). Buat fungsi yang menghitung jumlah hari dengan suhu ekstrem: hari dianggap **Panas** jika suhu ≥ 35°C dan **Dingin** jika suhu ≤ 15°C.

**Tugas:**  
Lengkapi inisialisasi penghitung dan implementasikan percabangan `if` untuk menghitung hari "Dingin".

```python
# SOAL 6: Analisis Data Suhu Ekstrem (for dan if/elif)
def analisis_suhu(data_suhu):
    """Menghitung jumlah hari Panas dan Dingin dari data_suhu."""
    panas_count = 0
    dingin_count = ______
    
    for suhu in data_suhu:
        if suhu >= 35:
            panas_count += 1
        elif suhu ______:
            dingin_count += 1
            
    return panas_count, dingin_count

# Pemanggilan:
suhu_mingguan = [36, 30, 14, 25, 38, 16, 28]
jumlah_panas, jumlah_dingin = analisis_suhu(suhu_mingguan)
print(f"Jumlah hari Panas (>=35°C): {jumlah_panas}")
print(f"Jumlah hari Dingin (<=15°C): {jumlah_dingin}")
```

**Alternatif Modifikasi (Tingkat Lanjut):** Tambahkan parameter opsional pada fungsi seperti `batas_panas` dan `batas_dingin` dengan nilai default 35 dan 15.

---

## Kunci Jawaban

### **Soal 1**
```python
def sapa_praktikan():
    """Mencetak pesan sambutan dasar."""
    print("Sistem siap. Selamat datang kembali di sesi praktikum.")
```

### **Soal 2**
```python
def hitung_volume_kubus(sisi):
    """Menghitung volume kubus dari panjang sisinya."""
    return sisi ** 3
```

### **Soal 3**
```python
def hitung_rata_rata(data_nilai):
    """Menghitung rata-rata dari list angka menggunakan perulangan for."""
    total = 0
    for nilai in data_nilai:
        total += nilai
    if len(data_nilai) > 0:
        return total / len(data_nilai)
    return 0
```

### **Soal 4**
```python
def tentukan_predikat(skor):
    """Menentukan predikat (A, B, C, D, E) berdasarkan skor."""
    if skor >= 85:
        return "A"
    elif skor >= 70:
        return "B"
    elif skor >= 60:
        return "C"
    elif skor >= 50:
        return "D"
    else:
        return "E"
```

### **Soal 5**
```python
def hitung_faktorial(n):
    """Menghitung faktorial dari bilangan positif n."""
    hasil = 1
    while n > 1:
        hasil *= n
        n -= 1
    return hasil
```

### **Soal 6**
```python
def analisis_suhu(data_suhu):
    """Menghitung jumlah hari Panas dan Dingin dari data_suhu."""
    panas_count = 0
    dingin_count = 0
    for suhu in data_suhu:
        if suhu >= 35:
            panas_count += 1
        elif suhu <= 15:
            dingin_count += 1
    return panas_count, dingin_count
```

