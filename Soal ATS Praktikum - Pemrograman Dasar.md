# Soal Praktikum Pemrograman Dasar (Python)

## 1. Percabangan / Branching
Sebuah sensor pada sistem pembangkit mengukur suhu air pendingin. Buatlah sebuah blok kode Python untuk:
a. Meminta input pengguna untuk suhu (sebagai float).  
b. Mencetak "STATUS: Normal" jika suhu 90°C atau kurang.  
c. Mencetak "STATUS: Warning" jika suhu di atas 90°C tetapi di bawah 100°C.  
d. Mencetak "ALERT: SHUTDOWN" jika suhu 100°C atau lebih.  

---

## 2. Fungsi / Functions
Dalam rekayasa pembangkit, efisiensi turbin sederhana dihitung dengan rumus:  
**Efisiensi = (Output Energi / Input Energi)**  

Buatlah fungsi Python bernama `hitung_efisiensi` untuk:
a. Menerima dua parameter: `input_energi` dan `output_energi`.  
b. Mengembalikan (return) nilai efisiensi (Output / Input).  
c. Bonus: Tunjukkan cara memanggil fungsi ini dengan input 500 dan output 400.

---

## 3. Looping for
Anda memiliki data pembacaan vibrasi dari 5-unit mesin berbeda:
```python
vibrasi_mesin = [1.2, 0.9, 2.5, 3.1, 1.8]
```
Buatlah loop `for` yang akan memeriksa setiap nilai dalam list tersebut. Jika nilai vibrasi melebihi 2.0, program harus mencetak:  
**"Warning: Unit [nomor_unit] vibrasi tinggi!"**  
(Asumsikan unit dimulai dari 1).

---

## 4. Logika Majemuk
Sebuah katup pengaman (safety valve) hanya boleh terbuka jika kedua kondisi berikut terpenuhi:
a. `tekanan_uap` (float) lebih besar dari 150 psi.  
b. `status_manual_override` (boolean) adalah False.  

Buat satu pernyataan if majemuk (menggunakan operator logika) yang mencetak "Katup Terbuka" hanya jika kedua kondisi tersebut terpenuhi.

---

## 5. Looping while
Sebuah sistem pemanas menaikkan suhu hingga mencapai target 85°C.  
Mulai dengan `suhu_saat_ini = 60`.  
Loop harus berjalan selama suhu_saat_ini < 85, naikkan 5 derajat tiap iterasi, dan cetak suhu saat ini.

---

## 6. Variabel & Ekspresi
Sebuah generator menghasilkan tegangan 220 Volt dan arus 15 Ampere.  
Buatlah program Python untuk menghitung daya listrik (`P = V × I`) dan menampilkan hasilnya.

---

## 7. Percabangan / Branching
Klasifikasikan beban listrik berdasarkan persentase pemakaian terhadap kapasitas maksimum:
| Persentase (%) | Status |
|-----------------|--------|
| ≤ 60 | "Beban Ringan" |
| > 60 dan ≤ 85 | "Beban Sedang" |
| > 85 | "Beban Berat" |

Program menerima input kapasitas maksimum dan beban terpakai, lalu menampilkan status beban.

---

## 8. Fungsi / Modularisasi
Efisiensi termal turbin gas:
**Efisiensi (%) = (energi keluar / energi masuk) × 100**  
Buat fungsi `hitung_efisiensi_termal()` untuk menghitung efisiensi dan menampilkan hasilnya.

---

## 9. Looping + List
Anda memiliki daftar pembacaan suhu pada 5 titik di boiler:
```python
suhu_boiler = [92.5, 88.7, 95.1, 102.3, 97.8]
```
Gunakan loop `for` untuk menampilkan setiap nilai suhu, dan beri peringatan jika suhu di atas 100°C.

---

## 10. While Loop & Logika
Simulasikan pengisian tangki bahan bakar hingga penuh (100 liter).  
Gunakan loop `while`, mulai dari 0 liter, naikkan 10 liter tiap iterasi, dan tampilkan pesan:
- "WARNING: Hampir penuh!" saat 80 liter.  
- "TANGKI PENUH – Pengisian berhenti." saat 100 liter.
