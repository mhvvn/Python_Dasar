# Soal Teori Asesmen Tengah Semester 

**Matakuliah :** Pemrograman Dasar 

**Jumlah Soal:** 30  

**Bentuk Soal:** Pilihan Ganda dan Esai

**Durasi:** 90 Menit  
---



> **Petunjuk Pengerjaan Asesmen:**  
> 1. Berdoa terlebih dahulu sebelum mengerjakan soal
> 2. Baca soal dan pahami dengan teliti
> 3. Jawablah soal dengan tepat
> 4. Perhatikan waktu pengerjaan soal
> 5. Kerjakan secara mandiri
> 6. Dilarang mencontek, bekerja sama, dan atau membuka sumber belajar
> 7. Pastikan Nama dan NIM anda Terbaca dan tertulis di lembar jawaban
> 8. Kumpulkan tepat waktu
> 9. Jawablah pertanyaan dengan **Ditulis tangan** hanya **Soal dan Jawban yg Benar** saja.
---

## A. Creating and Using Variables (1–5)

1. **Manakah pembuatan nama variabel yang valid dalam bahasa Python?**  
   - A. `2jumlah`  
   - B. `nama_siswa`   
   - C. `nama siswa`  
   - D. `_nilaiMahasiswa`  

2. **Perhatikan kode berikut:**
   ```python
   umur = 20
   print("Umur saya adalah", umur)
   ```
   Output yang benar dari program di atas adalah...  
   - A. `Umur saya adalah umur`  
   - B. `Umur saya adalah 20`  
   - C. `Umur saya adalah umur = 20`  
   - D. `Umur saya adalah 0`  

3. **Berikut ini yang **bukan** dari  contoh pemberian nilai variabel yang benar dalam bahasa Python adalah...**  
   - A. `x = 5`  
   - B. `nama = 'Andi'`  
   - C. `nilai = 90`  
   - D. `True = 1`  

4. **Jika `a = 10` dan `b = 3`, maka hasil dari `a // b` adalah...**  
   - A. `3`  
   - B. `3.33`  
   - C. `10/3`  
   - D. `0.3`  

5. **Perhatikan kode berikut:**
   ```python
   x = 5
   x = x + 2
   print(x)
   ```
   Output yang benar dari program di atas adalah...  
   - A. `5`  
   - B. `7`  
   - C. `x + 2`  
   - D. `2`  

---

## B. String Formatting & Expressions (6–8)

6. **Output yang benar dari kode program berikut adalah:**
   ```python
   nama = "Budi"
   print(f"Halo {nama}, selamat belajar Python!")
   ```
   - A. `Halo {nama}, selamat belajar Python!`  
   - B. `Halo Budi, selamat belajar Python!`  
   - C. `Halo , selamat belajar Python!`  
   - D. `Halo 'nama', selamat belajar Python!`  

7. **Jika `a = 7` dan `b = 3`, maka nilai `f"hasil = {a*b}"` adalah...**  
   - A. `hasil = 21`  
   - B. `hasil = 7*3`  
   - C. `hasil = 10`  
   - D. `hasil = a*b`  

8. **Lengkapi potongan kode berikut agar dapat mencetak panjang string yang dimasukkan oleh pengguna:**
   ```python
   kata = input("Masukkan kata: ")
   print(____(kata))
   ```
   - A. `len`  
   - B. `sum`  
   - C. `type`  
   - D. `str`  

---

## C. Comparing Numbers & Logical (9–11)

9. **Jika `x = 8`, maka ekspresi berikut `x > 5 and x < 10` akan menghasilkan...**  
   - A. `True`  
   - B. `False`  
   - C. `8`  
   - D. `None`  

10. **Output yang benar dari kode berikut ini adalah:**
    ```python
    a = 5
    b = 5
    print(a is b)
    ```
    - A. `True`  
    - B. `False`  
    - C. `5`  
    - D. `SyntaxError`  

11. **Pernyataan yang benar dari logika berikut, **kecuali**...**  
    - A. `not True` menghasilkan False  
    - B. `True or False` menghasilkan True  
    - C. `True and False` menghasilkan False  
    - D. `not False` menghasilkan False  

---

## D. Flow Control (12–14)

12. **Output yang benar dari kode berikut ini adalah:**
    ```python
    nilai = 75
    if nilai >= 70:
        print("Lulus")
    else:
        print("Gagal")
    ```
    Output:  
    - A. `Lulus`  
    - B. `Gagal`  
    - C. `Tidak ada output`  
    - D. `Kesalahan logika`  

13. **Jika `x = 3`, berapa output dari kode berikut ini:**
    ```python
    if x > 5:
        print("A")
    elif x > 2:
        print("B")
    else:
        print("C")
    ```
    - A. `A`  
    - B. `B`  
    - C. `C`  
    - D. `B dan C`  

14. **Manakah potongan kode yang salah dalam penulisan indentasinya?**  
    - A. 
      ```python
      if True:
      print("OK")
      ```
    - B. 
      ```python
      if True:
          print("OK")
      ```
    - C. 
      ```python
      if True:
            print("OK")
      ```
    - D. 
      ```python
      if True:
          print("OK")
      print("Done")
      ```

---

## E. List, Tuple, Dictionary, Set (15–19)

15. **Manakah cara yang benar dalam membuat variabel list di Python?**  
    - A. `data = (1,2,3)`  
    - B. `data = [1,2,3]`  
    - C. `data = {1,2,3}`  
    - D. `data = "1,2,3"`  

16. **Jika `angka = [10,20,30]`, maka `angka[1]` bernilai...**  
    - A. `10`  
    - B. `20`  
    - C. `30`  
    - D. `Error Index`  

17. **Manakah cara yang benar dalam membuat variabel dictionary di Python?**  
    - A. `data = {'nama':'Budi', 'umur':20}`  
    - B. `data = ['nama':'Budi']`  
    - C. `data = ('nama','Budi')`  
    - D. `data = {Budi:'nama'}`  

18. **Output yang benar dari kode programa berikut ini adalah:**
    ```python
    set_a = {1,2,3}
    set_b = {3,4,5}
    print(set_a & set_b)
    ```
    - A. `{3}`  
    - B. `{1,2,3,4,5}`  
    - C. `{1,2}`  
    - D. `[]`  

19. **Jika `t = (1,2,3)` maka pernyataan berikut yang salah adalah...**  
    - A. `t[0]` menghasilkan 1  
    - B. `t.append(4)` menambah elemen  
    - C. `len(t)` menghasilkan 3  
    - D. `t[2]` menghasilkan 3  

---

## F. Function & Loop (20–25)

20. **Lengkapi kode program berikut agar dapat mendefinisikan fungsi dengan benar:**
    ```python
    ____ sapa():
        print("Halo Dunia")
    ```
    - A. `func`  
    - B. `define`  
    - C. `def`  
    - D. `declare`  

21. **Fungsi berikut ini akan menghasilkan output:**
    ```python
    def kali(a,b):
        return a*b

    print(kali(2,3))
    ```
    - A. `a*b`  
    - B. `5`  
    - C. `6`  
    - D. `2*b`  

22. **Hasil yang benar dari program berikut ini adalah:**
    ```python
    for i in range(1,4):
        print(i, end=' ')
    ```
    - A. `1 2 3`  
    - B. `0 1 2 3`  
    - C. `1 2 3 4`  
    - D. `Error`  

23. **Lengkapi bagian kode programa berikut ini agar dapat menampilkan jumlah semua angka pada sebuah variabel list:**
    ```python
    angka = [1,2,3,4]
    total = 0
    for a in angka:
        total += a
    print(____)
    ```
    - A. `angka`  
    - B. `a`  
    - C. `total`  
    - D. `sum(angka)`  

24. **Diketahui fungsi seperti berikut ini:**
    ```python
    def luas_persegi(sisi):
        return sisi * sisi
    ```
    Jika `sisi = 5`, maka output dari `print(luas_persegi(5))` adalah...  
    - A. `10`  
    - B. `25`  
    - C. `5 * sisi`  
    - D. `20`  

25. **Seorang teknisi ingin membuat program untuk mengecek apakah suhu boiler yang aman. Jika suhu lebih dari 100°C, akan menampilkan pesan “Bahaya!”, selain itu ,menampilkan pesan “Aman.”**
    - A. 
      ```python
      if suhu > 100:
          print("Bahaya!")
      else:
          print("Aman")
      ```
    - B. 
      ```python
      if suhu >= 100:
          print("Bahaya!")
      else:
          print("Aman")
      ```
    - C. 
      ```python
      if suhu < 100:
          print("Aman")
      else:
          print("Bahaya!")
      ```
    - D. 
      ```python
      if suhu == 100:
          print("Suhu normal")
      ```

---

## G. Esai Isian Singkat (26-30)

1. Jelaskan perbedaan fundamental antara operator logika **and** dan **or** dalam Python!  Bagaimana Anda menggunakannya untuk menggabungkan dua kondisi dalam sebuah pernyataan **if**?.
    
2. Apa dua alasan utama mengapa menggunakan **fungsi (functions)** dalam pemrograman? Jelaskan secara singkat perbedaan antara **parameter** dan **return value** dalam sebuah **fungsi**.
    
3. Dalam bahasa Python memungkinkan penggunaan struktur data seperti **list, tuple, dictionary, dan set**. Jelaskan perbedaan mendasar antara keempat struktur data tersebut dari segi **sifat penyimpanan, kemampuan diubah (mutable/immutable), dan penggunaan praktisnya** dalam pemrograman teknik. Sertakan satu **contoh kasus** penggunaan nyata untuk salah satu struktur data tersebut.
    
4. Ketika menjalankan program Python, terkadang terjadi **kesalahan (error)** seperti **SyntaxError, ValueError, atau TypeError**. Jelaskan **perbedaan antara ketiga jenis error** tersebut dan bagaimana pendekatan berpikir seorang programmer dalam menemukan serta memperbaiki kesalahan tersebut agar program dapat berjalan dengan benar.
    
5. Apa tujuan dari pernyataan **elif** dalam struktur percabangan **if-elif-else**? Mengapa tidak bisa hanya menggunakan beberapa pernyataan **if** yang terpisah?

---

> ## **Catatan:**  
> - Jawablah pertanyaan dengan **Ditulis tangan** hanya **Soal dan Jawban yg Benar** saja.
> - Pastikan **Nama dan NIM** anda **Terbaca** dan tertulis di lembar jawaban.
> - Pengumpulan di **classroom** sesuai tanggal deadline
