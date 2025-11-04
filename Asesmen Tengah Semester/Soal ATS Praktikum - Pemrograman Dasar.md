# Soal Praktikum Pemrograman Dasar

**Matakuliah :** Pemrograman Dasar 

**Durasi:** 120 Menit  

---
> **Petunjuk Pengerjaan Asesmen:**  
> 1. Berdoa terlebih dahulu sebelum mengerjakan soal
> 2. Baca soal dan pahami dengan teliti
> 3. Jawablah dengan tepat
> 4. Perhatikan waktu
> 5. Kerjakan sendiri, dan dilarang keras bekerja sama
> 6. masing-masing di buat dalam satu file (.py) atau (.ipynb) Google Colab Notebook
> 7. Lalu Upload file ke **github** masing-masing dengan nama file [`ATS Praktikum_Nama/Urutan_Kelompok`]
> 7. Pastikan Nama dan NIM kelompok Terbaca dan tertulis di lembar jawaban
> 8. Pengumpulan hanya satu orang perwakilan saja
---



## 1. Percabangan / Branching
Sebuah sensor pada sistem pembangkit yang mengukur suhu air pendingin. Buatlah sebuah blok kode Python untuk:

a. Meminta input pengguna untuk suhu (bertipe float). 

b. Mencetak `"STATUS: Normal" jika suhu 90°C atau kurang`.  

c. Mencetak `"STATUS: Warning" jika suhu di atas 90°C tetapi di bawah 100°C`. 

d. Mencetak `"ALERT: SHUTDOWN" jika suhu 100°C atau lebih.` 


## 2. Fungsi / Functions
Dalam rekayasa pembangkit, efisiensi turbin dihitung dengan rumus berikut:   
`Efisiensi = (Output Energi / Input Energi) `

Buatlah fungsi Python bernama `hitung_efisiensi` untuk:

a. Menerima dua parameter:
 `input_energi` dan `output_energi`.  

b. Mengembalikan (return) nilai efisiensi (Output / Input).  

c. Bonus: Tunjukkan cara memanggil fungsi ini dengan input 500 dan output 400.


## 3. Looping `for`
Anda memiliki data hasil pembacaan vibrasi dari 5-unit mesin berbeda:
```python
vibrasi_mesin = [1.2, 0.9, 2.5, 3.1, 1.8]
```
Buatlah sebuah loop/perulangan `for` yang akan memeriksa setiap nilai dalam list tersebut. Jika nilai vibrasi melebihi `2.0`,  maka program harus mencetak:  

**`"Warning: Unit [nomor_unit] vibrasi tinggi!"`**

(Asumsikan unit dimulai dari 1).

## 4. Logika `if` Majemuk/bertingkat
Sebuah katup pengaman (safety valve) hanya boleh terbuka jika kedua kondisi berikut terpenuhi:

a. `tekanan_uap` (float) lebih besar dari `150` psi.  
b. `status_manual_override` (boolean) adalah False.  

Buatlah satu pernyataan `if` majemuk/bertingkat (menggunakan operator logika) yang akan mencetak `"Katup Terbuka"` hanya jika kedua kondisi tersebut terpenuhi.



## 5. Looping `while`

Sebuah sistem pemanas menaikkan suhu hingga mencapai target `85°C`.Mulai dengan `suhu_saat_ini = 60`.  
Loop harus berjalan selama suhu_saat_ini < 85, naikkan 5 derajat tiap iterasi, dan cetak suhu saat ini.



## 6. Variabel & Ekspresi

Sebuah generator menghasilkan tegangan `220 Volt` dan arus `15 Ampere`.  

Buatlah program Python untuk menghitung daya listrik (`P = V × I`) dan menampilkan hasil perhitunganya nya.


## 7. Percabangan / Branching
Klasifikasikan beban listrik berdasarkan persentase pemakaian terhadap kapasitas maksimum:
| Persentase (%) | Status |
|-----------------|--------|
| ≤ 60 | "Beban Ringan" |
| > 60 dan ≤ 85 | "Beban Sedang" |
| > 85 | "Beban Berat" |

Program menerima input kapasitas maksimum dan beban terpakai, lalu menampilkan status beban.


## 8. Fungsi / Modularisasi
Efisiensi termal turbin gas:
**`Efisiensi (%) = (energi keluar / energi masuk) × 100`**  
Buatlah fungsi dengan nama`hitung_efisiensi_termal()` untuk menghitung efisiensi dan menampilkan hasil perhitungannya.


## 9. Looping + List
Anda memiliki daftar hasil pembacaan suhu pada 5 titik di boiler:
```python
suhu_boiler = [92.5, 88.7, 95.1, 102.3, 97.8]
```
Gunakan loop `for` untuk menampilkan setiap nilai suhu, dan beri peringatan jika suhu di atas `100°C`.

## 10. While Loop & Logika
Simulasikan pengisian tangki bahan bakar hingga penuh (100 liter).  
Gunakan loop `while`, mulai dari `0` liter, naikkan `10` liter tiap iterasi, dan tampilkan pesan:
- `"WARNING: Hampir penuh!"` saat `80` liter.  
- `"TANGKI PENUH – Pengisian berhenti."` saat `100` liter.
--


## **Challenge**
> Buatlah sebuah program yang dapat menyelesaikan sebuah masalah di bidang energi yang mengimplementasikan percabangan `if,else,elif`, perulangan `for,while`, dan Fungsi `Function()` atau method dan fungsi lainya pada python.
  
___

> ## **Catatan:**  
> - Pastikan **Nama dan NIM** anda **Terbaca** dan tertulis di lembar jawaban.
> - Pengumpulan di classroom sesuai tanggal deadline

---
