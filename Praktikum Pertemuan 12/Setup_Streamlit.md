# Pengembangan Dashboard

## Pengenalan Dashboard
Di dunia industri, keahlian dalam membuat dashboard merupakan salah satu skill yang harus dimiliki oleh seorang praktisi data. Nah, bagi Anda yang belum pernah mendengar tentang dashboard, jangan khawatir karena pada materi ini kita akan membahasnya dari dasar.

### Apa itu Dashboard?
Pernahkah Anda mengendarai mobil atau motor? Jika pernah, tentunya Anda sudah tidak asing lagi dengan gambar di bawah ini, bukan?
![](https://assets.cdn.dicoding.com/original/academy/dos:615499b4087daebba07b5b024fa28d4520230314201042.png)


Bagi Anda yang belum tahu, gambar di atas merupakan tampilan dashboard mobil. Seperti yang Anda lihat, ia terdiri dari berbagai panel indikator serta speedometer, odometer, fuel meter, dll. Seluruh hal tersebut mampu memberikan kita gambaran terkait keadaan dari kendaraan tersebut. Nah, itulah contoh sederhana dari sebuah dashboard. 

Sama halnya dengan contoh di atas, dashboard juga banyak digunakan sebagai media untuk memonitori berbagai metrik yang dianggap penting untuk perkembangan sebuah perusahaan. Selain itu, ia juga merupakan salah satu komponen penting dalam kultur data-driven decision making. Umumnya, sebuah dashboard terdiri dari beberapa visualisasi data yang interaktif dan saling berhubungan satu sama lain.

apa yang dimaksud dengan visualisasi data yang interaktif?” Sederhananya, visualisasi data yang interaktif akan memungkinkan pengguna untuk mengontrol hal yang ingin ditampilkan dalam sebuah visualisasi data. Hal ini tentunya memberikan kebebasan terhadap user untuk fokus ke bagian yang menurut mereka penting.

materi ke depan kita akan belajar cara membuat sebuah dashboard. Namun, sebelum itu, mari kita lihat berbagai hal yang perlu dipertimbangkan sebelum membuat sebuah dashboard.


### Pertimbangan dalam Membuat Dashboard
Saat ini, kita telah memahami apa itu dashboard. Namun, sebelum belajar cara membuat dashboard, kita perlu memahami berbagai hal penting dalam membuat dashboard yang efektif.

Dashboard yang efektif merupakan kunci utama dalam kultur data-driven decision making. Ia umumnya memiliki atau menampilkan metrik yang jelas serta mampu menyampaikan informasi yang relevan dengan kebutuhan audiens atau pengguna. Berikut merupakan beberapa hal yang harus diperhatikan dalam membuat dashboard yang efektif.

- ### Memahami audiens
Untuk membuat dashboard yang efektif, kita harus mempertimbangkan audiens dan kebutuhannya. Oleh karena itu, pada proses pembuatan dashboard kita harus memahami siapa target user atau audiens serta goals atau kebutuhan yang ingin mereka capai dari dashboard tersebut.

- ###  Pertimbangkan ukuran tampilan
Sejalan dengan poin pertama, kita juga harus mempertimbangkan ukuran tampilan dashboard yang sesuai dengan device atau perangkat yang sering digunakan oleh target user atau audiens untuk melihat dashboard yang Anda buat.

- ###  Manfaatkan sweet spot
Anda bisa menggunakan sweet spot untuk menampilkan informasi penting dari sebuah dashboard. Tentunya Anda perlu melakukan riset terlebih dahulu untuk mengetahui sweet spot yang tepat untuk kebutuhan Anda. Sebagai contoh, umumnya, bagian kiri atas merupakan spot pertama yang dilihat dalam sebuah halaman web. Nah, kita bisa menempatkan informasi terkait metrik penting seperti KPI (key performance indicators) pada spot tersebut.

- ###  Pertimbangkan load time
Load time merupakan salah satu hal yang penting untuk kita pertimbangkan guna menjaga pengalaman user atau audiens. Oleh karena itu, kita harus memastikan dashboard yang dibuat memiliki load time yang relatif singkat.

- ###  Batasi komponen visual yang ditampilkan
Sama halnya ketika kita membuat visualisasi data, pada proses pengembangan dashboard juga harus mempertimbangkan jumlah komponen visual yang akan ditampilkan. Komponen visual yang terlalu banyak tentunya akan mengganggu fokus dan perhatian user. Secara umum, kita disarankan untuk hanya menampilkan dua atau tiga visualisasi data. Selain itu, kita juga perlu menghindari penggunaan komponen visual yang tidak mendukung dalam penyampaian informasi penting.


itulah kelima poin yang harus kita pertimbangkan guna membuat dashboard yang efektif. Semoga paparan tersebut dapat membantu Anda ketika membuat sebuah dashboard nantinya.



## Pengenalan Streamlit
![](https://assets.cdn.dicoding.com/original/academy/dos:7609ab4d164bb007ad316fefc029016620230310100714.jpeg)

Streamlit merupakan salah satu open-source web app framework untuk bahasa pemrograman Python. Ia memungkinkan kita membuat web app yang baik dan interaktif dalam waktu yang singkat. Selain itu, ia juga kompatibel dengan berbagai library populer seperti NumPy, pandas, matplotlib, dll. Inilah yang menjadi alasan streamlit sering digunakan oleh oleh para praktisi data dan machine learning


### Menjalankan Streamlit
Cukup banyak cara untuk menjalankan streamlit, merujuk pada dokumentasinya https://docs.streamlit.io/ yakni :

1. Menggunakan Playgrount : https://docs.streamlit.io/get-started/installation/streamlit-playground, yang bisa di akses langung pada halaman berikut ini : https://streamlit.io/playground?
![alt text](/Praktikum%20Pertemuan%2012/images/image.png)
Tanpa harus menginstall di komputer sudah bisa menjalankan streamlit, Cara ini hanya untuk belajar atau percobaan.

2. Install Streamlit using command line : https://docs.streamlit.io/get-started/installation/command-lin, Installasi langsung ke komputer/laptop dengan menjalankan virtual enviroment Python. (membutuhkan Code Editor)
![alt text](/Praktikum%20Pertemuan%2012/images/image-2.png)

3. Install Streamlit using Anaconda Distribution : https://docs.streamlit.io/get-started/installation/anaconda-distribution: ![alt text](/Praktikum%20Pertemuan%2012/images/image-1.png) Sama hal nya dengan cara sebelumnya hanya saja menggunakan anaconda sebagai paket python, sehingga tidak perlu install python lagi karena sudah satu paket (membutuhkan Code Editor) **Akan Menggunakan Cara ini**

4. GitHub Codespaces : https://docs.streamlit.io/get-started/installation/community-cloud : ![alt text](/Praktikum%20Pertemuan%2012/images/image-3.png)
Dengan memanfaatkan server codespace github dan langung terkoneksi dengan platfrom streamlit : https://share.streamlit.io/, Sehingga langung bisa di akses secara online, tidak ada yang perlu di install, semua berjalan secara online mulai dari Code Editor dan Python 

5. Snowflake  : https://docs.streamlit.io/get-started/installation/streamlit-in-snowflake
![alt text](/Praktikum%20Pertemuan%2012/images/image-4.png) Cara ini hampir mirip dengan Github Codespace, akan tetapi fitur gratis hanya bisa di gunakan selama 30 hari saja.

# Skipp Langkah ini
## Menjalankan Streamlit di Github Codespace 
1. Buat akun share streamlit pada link berikut ini : https://share.streamlit.io/ Bisa langsung mengguakan akun github atau email (jika menggunakan github tidak perlu menghubungkan streamlit dengan github)
2. Jika sudah terbuat akun nya. Pastikan akun github sudah terhubung dengan streamlit ![alt text]/Praktikum%20Pertemuan%2012/images/(image-5.png) Seperti gambar di atas, Jika belum lakukan koneksi antara keduanya.
3. Membuat Project ![alt text](/Praktikum%20Pertemuan%2012/images/image-6.png), Klik create app pada pojok kanan
4. Deploy a public app from a template ![alt text](/Praktikum%20Pertemuan%2012/images/image-7.png)
5. Pilih Template : ![alt text](/Praktikum%20Pertemuan%2012/images/image-8.png) ada beberapa pilihan template yang di sediakan, untuk kali ini Pilih  basik (**Blank App**), lalu sesuaikan **nama dan url** dengan nim dan nama
6. Centang Pilihan Open Github Codespace
![alt text](/Praktikum%20Pertemuan%2012/images/image-9.png) lalu klik **Deploy** 

Akan tampil tab baru seperti gambar berikut  ini : 
![alt text](/Praktikum%20Pertemuan%2012/images/image-10.png)
Tampilan code editor Visual Studio Code online yang siap pakai.
di sebelah kiri struktur file, lalu ada code editor tempat untuk menuliskan code, dan di sebelah kanan sudah di jalankan liver server untuk langsung melihat hasil streamlit yang sedang di buat/edit.

- Untuk memahami Konsep Dasar Streamlit : baca pada link berikut ini :https://docs.streamlit.io/get-started/fundamentals/main-concepts
- Untuk Fitur Advance pada link berikut ini : https://docs.streamlit.io/get-started/fundamentals/advanced-concepts
- Dan Fitur tambahan : https://docs.streamlit.io/get-started/fundamentals/additional-features

## Membuat "Hello, world!" App dengan Streamlit
- Klik file ``streamlit_app.py`` lalu ganti dengan code berikut ini

```python
import streamlit as st 
 
st.write(
    """
    # My first app
    Hello, Ini Project Streamlit Saya [Gani Nama & Nim]!
    """
)
```

Jika liver server di sebelah kanan tidak otomatis berubah klik **Always Rerun** 
![alt text](/Praktikum%20Pertemuan%2012/images/image-11.png) Jika sudah berhasil selamat! Anda berhasil membuat web app pertama menggunakan streamlit.



# langsung ke sini

## Pastikan di Komputer sudah terinstall 
- Visual Studio Code
- Miniconda (Jika belum, download di link beirkut https://repo.anaconda.com/miniconda/Miniconda3-latest-Windows-x86_64.exe) Lalu Install

- Selanjutnya :
    - klik start menu (logo windows) lalu ketik **anaconda prompt** seperti berikut ini 
    ![alt text](/Praktikum%20Pertemuan%2012/src/image.png) 
    - **Klik**  lalu akan tampil jendela terminal seperti berikut ini :
    
    ![alt text](/Praktikum%20Pertemuan%2012/src/image-1.png)
    - Setelah itu buat folder dengan cara mengetik command berikut ini **mkdir spasi nama folder** ``mkdir streamlit_veven``
    - masuk ke dalam folder yang sudah di buat sebelumnya dengan cara mengetikan **cd nama folder yg di buat** ``cd streamlit_veven``
    - pastikan line pada terminal menunjukan nama folder anda ``(base) C:\Users\vvn\streamlit_veven>``
    - berikut ini tampilanya
    
    ![](/Praktikum%20Pertemuan%2012/src/Screenshot%202025-12-22%20135504.png)

    - pastikan apakah library **streamlit** sudah terinstall atau belum dengan cara mengetikan perintah ``pip list``

    ![alt text](/Praktikum%20Pertemuan%2012/src/image-2.png)

    scroll dan cari streamlit pada list tersebut, jika belum ada
    - Install library streamlit dengan mengetikan printah berikut ini ``pip install streamlit`` tampilanya seperti gambar berikut ini, tunggu hingga selesai.
    ![alt text](/Praktikum%20Pertemuan%2012/src/image-3.png)
    - untuk memverifikasi apakah streamlit sudah bisa di jalankan maka jalankan perintah berikut ini ``streamlit hello``, tekan enter jika di minta memasukan email.

    ![alt text](/Praktikum%20Pertemuan%2012/src/image-5.png)

    - Akan terbuka tab baru pada web browser dengan tampilan seperti berikut ini 

     ![alt text](/Praktikum%20Pertemuan%2012/src/image-4.png)
    jika seprti berikut ini maka streamlit sudah siap untuk jalankan di komputer lokal
    - jika kembali ke terminal maka akan tampil ip untuk mengakses streamlit seperti gambar berikut

    ![alt text](/Praktikum%20Pertemuan%2012/src/image-6.png)

    - Hentika proses streamlit yg berjalan dengan menetak tomnol ``ctrl + c``
    ![alt text](/Praktikum%20Pertemuan%2012/src/image-7.png)
    sehingga tampilan terminal akan seperti gambar di atas



   
    





## Basic Element dalam Streamlit

Sebagai sebuah web app framework yang andal, streamlit telah menyediakan banyak pilihan element, widget, layout serta container untuk memastikan kita dapat membuat web app atau dashboard yang menarik dan interaktif. Nah, pada materi ini, kita hanya akan fokus pada bagian basic element dalam streamlit yang terdiri dari write, text, data display, dan chat. Yuk, kita bahas satu per satu!

### Write
Basic element pertama yang akan kita bahas ialah write. Ia merupakan elemen streamlit yang digunakan untuk menampilkan sebuah output.  Untuk menggunakan element ini, kita hanya perlu memanggil function ``write()`` dan diikuti inputan yang ingin ditampilkan.

Pada contoh pembuatan ``“Hello, world!”`` app, kita telah menggunakan function ``write()`` untuk menampilkan output dari argument markdown.  Sebenarnya function ini dapat digunakan untuk menampilkan hal lain, seperti DataFrame, visualisasi data, dll. Berikut merupakan contoh penggunaannya untuk menampilkan DataFrame.

```python 
import streamlit as st
import pandas as pd
 
st.write(pd.DataFrame({
    'c1': [1, 2, 3, 4],
    'c2': [10, 20, 30, 40],
})) 
```

Kode di atas akan menghasilkan tampilan web app seperti berikut.

![alt text](https://assets.cdn.dicoding.com/original/academy/dos:74ff12a48a358afb5e3a37bcadb2535e20230310105317.jpeg)

Untuk melihat contoh lain dalam penggunaan function write(), Anda dapat mengunjungi dokumentasi berikut: st.write().

## Text
Elemen lain yang ada dalam streamlit ialah text (dokumentasi: https://docs.streamlit.io/library/api-reference/text ). Sesuai dengan namanya, ia merupakan elemen yang digunakan untuk menampilkan sebuah output berupa text. Elemen ini memiliki banyak function yang bisa digunakan sesuai kebutuhan. Berikut merupakan beberapa pilihan yang tersedia saat ini. 

- # markdown()
Function ini digunakan untuk menampilkan output dari argument markdown. Berikut merupakan contoh kode untuk menggunakannya.

```python
import streamlit as st 
 
st.markdown(
    """
    # My first app
    Hello, para calon praktisi data masa depan!
    """
)
```
- # title()
Ini merupakan function yang digunakan untuk menampilkan teks dalam format judul. Kode yang dapat Anda gunakan untuk menerapkan function tersebut adalah seperti di bawah ini

```python
import streamlit as st
 
st.title('Belajar Analisis Data')
```

- # header()
Function ini digunakan untuk menampilkan output teks sebagai format header. Berikut contoh penulisan kode untuk menggunakannya

```python
import streamlit as st
 
st.header('Pengembangan Dashboard')
```

- # subheader()
Ini merupakan function yang digunakan untuk menampilkan output teks sebagai format subheader
```python
import streamlit as st
 
st.subheader('Pengembangan Dashboard')

```

- # caption()
Function berikutnya ialah caption(). Ia merupakan function yang digunakan untuk menampilkan output teks dalam ukuran kecil. Function ini biasanya digunakan untuk menampilkan caption, footnotes, dll. Contoh penggunaannya seperti di bawah ini.
```python
import streamlit as st
 
st.caption('Copyright (c) 2023')
```
- # code()
Pada beberapa case, kita harus menampilkan potongan kode ke dalam streamlit app (web app yang dibuat menggunakan streamlit). Untuk menjawab hal ini, streamlit telah menyediakan sebuah function bernama code(). Kode di bawah ini merupakan contoh penggunaan dari function tersebut.

```python
import streamlit as st
 
code = """def hello():
    print("Hello, Streamlit!")"""
st.code(code, language='python')
```
Kode di atas akan menghasilkan tampilan seperti berikut.
![](https://assets.cdn.dicoding.com/original/academy/dos:b738f09dc5ea883cc513982a82261bb920230310105318.jpeg)


- # text()
Function selanjutnya ialah text(). Function ini digunakan untuk menampilkan sebuah normal teks. Berikut merupakan contoh kode untuk menggunakannya.

```python
import streamlit as st
 
st.text('Halo, calon praktisi data masa depan.')
```
- # latex()
Function terakhir yang dapat digunakan untuk menampilkan elemen teks ialah ``latex()``. Sesuai namanya, function tersebut digunakan untuk menampilkan mathematical expression yang ditulis dalam format
 [LaTeX](https://katex.org/docs/supported.html). Berikut contoh kode untuk menggunakan function ``latex()``

```python
import streamlit as st
 
st.latex(r"""
    \sum_{k=0}^{n-1} ar^k =
    a \left(\frac{1-r^{n}}{1-r}\right)
""")
```
Kode tersebut akan menghasilkan tampilan mathematical expression seperti berikut.
![](https://assets.cdn.dicoding.com/original/academy/dos:b4c10746687a2d7b82a59a62ecee0ecd20230310111310.jpeg)

## Data Display
Basic element selanjutnya yang akan kita bahas ialah data display (dokumentasi: data display). Ia merupakan elemen yang digunakan untuk menampilkan data secara cepat dan interaktif ke dalam streamlit app yang kita buat. Elemen ini memiliki beberapa function seperti berikut.


- #  dataframe()
Function pertama yang bisa kita gunakan untuk menampilkan data ke dalam streamlit app ialah dataframe(). Ia merupakan function yang digunakan untuk menampilkan DataFrame sebagai sebuah tabel interaktif. Pada function ini, kita bisa mengatur ukuran dari table yang ingin ditampilkan menggunakan parameter width dan height. Berikut merupakan contoh kode untuk menampilkan data menggunakan function dataframe().

```python
import pandas as pd
import streamlit as st 
 
df = pd.DataFrame({
    'c1': [1, 2, 3, 4],
    'c2': [10, 20, 30, 40],
})
 
st.dataframe(data=df, width=500, height=150)
```


- #  table()
Selain dataframe(), kita juga bisa menggunakan function table()untuk menampilkan data ke dalam streamlit app. Ia dapat digunakan untuk menampilkan data dalam bentuk static table. Berikut merupakan contoh penggunaannya.


```python
import pandas as pd
import streamlit as st 
 
df = pd.DataFrame({
    'c1': [1, 2, 3, 4],
    'c2': [10, 20, 30, 40],
})
st.table(data=df)
```

- # metric()
Ketika membuat dashboard, terkadang kita perlu menampilkan sebuah metrik tertentu. Untuk melakukan hal ini, kita bisa memanfaatkan function metric(). Function ini dapat membantu kita untuk menampilkan sebuah metrik tertentu beserta detailnya seperti label, value serta besar perubahan nilainya. Berikut merupakan contoh kode untuk menggunakannya.

```python
import streamlit as st
 
st.metric(label="Temperature", value="28 °C", delta="1.2 °C")
```
Kode di atas akan menghasilkan tampilan berikut.

![](https://assets.cdn.dicoding.com/original/academy/dos:eb8182ad7316976a1127338d5b668b3a20230310105318.jpeg)

- # json()
Selain bentuk DataFrame atau tabel, terkadang kita juga perlu menampilkan data dalam format JSON. Streamlit telah menyediakan function json() untuk menampilkan data dalam format JSON. Berikut merupakan contoh penggunaannya.

```python

import streamlit as st
 
st.json({
    'c1': [1, 2, 3, 4],
    'c2': [10, 20, 30, 40],
})
```
Kode di atas akan menghasilkan tampilan berikut.

![](https://assets.cdn.dicoding.com/original/academy/dos:5bea6f0e37cdbc6aec9fbed5992f4f7b20230310111741.jpeg)


Chart
Basic element terakhir yang perlu kita ketahui ialah chart. Sesuai namanya, elemen ini dapat digunakan untuk menampilkan grafik visualisasi data ke dalam streamlit app. Elemen inilah yang akan sering kita gunakan untuk membuat dashboard nantinya. Sebenarnya streamlit telah menyediakan banyak sekali function untuk mendukung berbagai library visualisasi data (dokumentasi: [chart](https://docs.streamlit.io/library/api-reference/charts)). Namun, pada materi ini, kita hanya akan fokus pada function pyplot().

Function pyplot() dapat digunakan untuk menampilkan grafik visualisasi data yang dibuat menggunakan matplotlib. Berikut merupakan contoh kode untuk menggunakannya.

```python

import matplotlib.pyplot as plt
import numpy as np
import streamlit as st
 
x = np.random.normal(15, 5, 250)
 
fig, ax = plt.subplots()
ax.hist(x=x, bins=15)
st.pyplot(fig)
```

Kode di atas akan menampilkan grafik visualisasi data berikut di dalam streamlit app.

![](https://assets.cdn.dicoding.com/original/academy/dos:0abca0b15e5395dd8dc918fa8d4d8e7a20230310105318.jpeg)

itulah berbagai basic element yang ada dalam streamlit. Pemahaman terhadap basic element ini sangat penting untuk mendukung Anda dalam membuat sebuah dashboard nantinya. 



## Basic Widgets dalam Streamlit

pada materi ini, kita akan berkenalan dengan berbagai basic widget yang telah disediakan oleh streamlit. Untuk membantu kita menghasilkan web app yang interaktif, streamlit telah menyediakan banyak sekali pilihan widget yang bisa disesuaikan dengan kebutuhan. Agar lebih mudah dalam memahami seluruh widget tersebut, pada materi ini kita akan membaginya ke dalam dua kategori, yaitu input widget dan button widget. 


### Input Widget
Kategori widget yang akan kita bahas ialah input widget. Ia merupakan kategori widget yang memungkinkan pengguna untuk memberikan input ke dalam streamlit app. Terdapat beberapa widget yang termasuk kategori ini, seperti text input, number input, date input, dll. Yuk, kita bahas satu per satu!

- #  Text input
Text input merupakan widget yang digunakan untuk memperoleh inputan berupa single-line text. Kita bisa menggunakan function text_input() untuk membuat widget ini. Berikut merupakan contoh kode untuk membuatnya.

```python
import streamlit as st
 
name = st.text_input(label='Nama lengkap', value='')
st.write('Nama: ', name)

```
Kode di atas akan menghasilkan sebuah widget seperti berikut.
![](https://assets.cdn.dicoding.com/original/academy/dos:2f842f1453d93a7268ca2c51a9a3e6e320230310112559.jpeg)


- # Text-area
Text area merupakan widget yang memungkinkan pengguna untuk menginput multi-line text. Untuk membuat widget ini, streamlit telah menyediakan function bernama text_area(). Kode di bawah ini merupakan contoh kode untuk menggunakan function tersebut.

```python
import streamlit as st
 
text = st.text_area('Feedback')
st.write('Feedback: ', text)
```
Berikut merupakan tampilan widget yang diperoleh dari kode di atas.

![](https://assets.cdn.dicoding.com/original/academy/dos:204e96706e079f8cdfad7e5031a06d6820230310112559.jpeg)

- # Number input
Widget berikutnya yang akan kita bahas ialah number input . Ia merupakan widget yang digunakan untuk memperoleh inputan berupa angka dari pengguna. Anda dapat menggunakan contoh kode berikut untuk membuat number input widget menggunakan function number_input().

```python
import streamlit as st
 
number = st.number_input(label='Umur')
st.write('Umur: ', int(number), ' tahun')
```
Gambar di bawah ini merupakan tampilan widget yang dihasilkan dari contoh kode tersebut. 

![](https://assets.cdn.dicoding.com/original/academy/dos:4b06606bbf99ac30c95e7a5ca2ffb36b20230310112559.jpeg)

- # Date input
Selain inputan berupa angka dan teks, pada beberapa kasus kita juga membutuhkan input berupa tanggal dari pengguna melalui date input widget. Kita dapat membuat widget tersebut menggunakan function date_input(). Berikut merupakan contoh kode untuk menggunakannya.     


```python
import datetime
import streamlit as st
 
date = st.date_input(label='Tanggal lahir', min_value=datetime.date(1900, 1, 1))
st.write('Tanggal lahir:', date)
```
Kode tersebut akan menghasilkan tampilan widget seperti berikut.

![](https://assets.cdn.dicoding.com/original/academy/dos:b08b81434d2606e2dbf32bdeb793763720230310112559.jpeg)


- # File uploader
Widget selanjutnya yang akan kita bahas ialah file uploader. Widget ini memungkinkan kita meminta pengguna untuk meng-upload sebuah berkas tertentu ke dalam web app. Kita dapat membuat file uploader widget menggunakan function file_uploader() seperti pada contoh kode berikut. 

```python
import streamlit as st
import pandas as pd
 
uploaded_file = st.file_uploader('Choose a CSV file')
 
if uploaded_file:
    df = pd.read_csv(uploaded_file)
    st.dataframe(df)

```
Kode di atas akan menghasilkan widget seperti berikut.

![](https://assets.cdn.dicoding.com/original/academy/dos:a0176d67ac8f9b6820218330d577ac8b20230310112559.jpeg)


- # Camera input
Selain file uploader, streamlit juga menyediakan camera input widget yang dapat digunakan untuk meminta user mengambil gambar melalui webcam sekaligus mengunggahnya.  Hal ini tentunya dilakukan dengan persetujuan pengguna. Berikut merupakan contoh kode untuk membuat camera input widget menggunakan function camera_input().

```python

import streamlit as st
picture = st.camera_input('Take a picture')
if picture:
    st.image(picture)
```

Berikut merupakan tampilan widget yang akan diperoleh ketika menjalankan kode di atas.

![](https://assets.cdn.dicoding.com/original/academy/dos:7c6477ceea2c6d8d69b30208c119d0ba20230310112559.jpeg)

## Button Widgets 
kategori widget selanjutnya yang akan kita bahas ialah button widget. Ia merupakan kategori widget yang terdiri dari button, checkbox, radio button, dll.


- # Button
Button merupakan widget untuk menampilkan tombol interaktif. Tombol tersebut dapat digunakan pengguna untuk melakukan aksi tertentu. Untuk membuat widget ini, kita bisa menggunakan function button() seperti contoh berikut.

```python
import streamlit as st
 
if st.button('Say hello'):
    st.write('Hello there')
```
Berikut merupakan button widget yang dihasilkan dari kode di atas.
![](https://assets.cdn.dicoding.com/original/academy/dos:481a22315719a1e9b5f23545648f56c720230310112559.jpeg)


- # Checkbox
Checkbox merupakan widget yang digunakan untuk menampilkan sebuah checklist untuk pengguna. Kita bisa menggunakan function checkbox() untuk membuat dan menampilkan checklist dalam streamlit app. Berikut contoh kode untuk melakukannya.


```python
import streamlit as st
 
agree = st.checkbox('I agree')
 
if agree:
    st.write('Welcome to MyApp')
```

Kode di atas akan menghasilkan tampilan berikut.

![](https://assets.cdn.dicoding.com/original/academy/dos:ed937e3ea27353979046a2753b2b8f2c20230310112559.jpeg)


- # Radio button
Selain button dan checkbox, terkadang kita juga membutuhkan radio button untuk menghasilkan web app yang interaktif. Ia merupakan widget yang memungkinkan pengguna untuk memilih satu dari beberapa pilihan yang ada. Untuk membuat widget ini, kita bisa menggunakan function radio() seperti pada contoh kode berikut.

```python
import streamlit as st
 
genre = st.radio(
    label="What's your favorite movie genre",
    options=('Comedy', 'Drama', 'Documentary'),
    horizontal=False
)
```

Berikut merupakan tampilan widget yang dihasilkan dari kode di atas.
![](https://assets.cdn.dicoding.com/original/academy/dos:0e1be5ea9ae7d52e69c4a17e8255aa1820230310112559.jpeg)


- # Select Box
Select box merupakan widget yang memungkinkan pengguna untuk memilih salah satu dari beberapa pilihan yang ada. Ia merupakan opsi alternatif dari radio button. Streamlit telah menyediakan function selectbox() untuk membuat select box widget. Berikut contoh penggunaannya.

```python
import streamlit as st
 
genre = st.selectbox(
    label="What's your favorite movie genre",
    options=('Comedy', 'Drama', 'Documentary')
)
```
Berikut merupakan tampilan select box dari kode di atas.
![](https://assets.cdn.dicoding.com/original/academy/dos:cbae72beac30b15c215c595457ad906920230310112559.jpeg)

- # Multiselect
Widget lain yang harus kita ketahui ialah multiselect. Ia merupakan widget yang digunakan agar user dapat memilih lebih dari satu pilihan dari sekumpulan pilihan yang ada. Untuk mempermudah kita dalam membuat multiselect widget, streamlit telah menyediakan function bernama multiselect(). Berikut contoh kode untuk menggunakan function tersebut.


```python
import streamlit as st
 
genre = st.multiselect(
    label="What's your favorite movie genre",
    options=('Comedy', 'Drama', 'Documentary')
)
```
Kode di atas akan menghasilkan tampilan multiselect widget seperti berikut.

![](https://assets.cdn.dicoding.com/original/academy/dos:fdfa0a615cc6e3162612946b7096361e20230310112559.jpeg)

- #    Slider
Slider merupakan widget yang memungkinkan pengguna untuk memilih nilai (atau range nilai) dari sebuah range nilai yang telah ditentukan. Streamlit telah menyediakan function slider() untuk membuat slider widget. Berikut merupakan contoh penggunaannya.

```python
values = st.slider(
    label='Select a range of values',
    min_value=0, max_value=100, value=(0, 100))
st.write('Values:', values)
```

Kode di atas akan menghasilkan widget seperti berikut.
![](https://assets.cdn.dicoding.com/original/academy/dos:01c449ea37df8981905497e8d6aff26620230310112559.jpeg)

Nah, itulah beberapa pilihan widget yang disediakan oleh streamlit. Anda dapat melihat lebih banyak pilihan widget pada dokumentasi berikut: [widgets in streamlit](https://docs.streamlit.io/library/api-reference/widgets). Pengetahuan terkait basic widget ini akan sangat membantu Anda dalam membuat dashboard yang interaktif nantinya. 




## Upload Streamlit project

### Sebelumnya silahkan uplaod file streamlit ke github masing-masing.
- Buat repository baru
- lalu jalankan ketiga printah berikut pada termianl VSCode anda 
```bash
git init
git remote add origin https://github.com/mhvvn/new-streamlit.git
git branch -M main
git push -u origin main
```
- sehingga pada repository anda terupload file streamlit nya
  ![alt text](/Praktikum%20Pertemuan%2012/src/image-12.png)

## setup akun streamlit share

- Daftar akun streamlit sahre : https://share.streamlit.io/
  ![alt text](/Praktikum%20Pertemuan%2012/src/image-8.png)
- Silahkan daftar menggunakan gmail atau github 
  ![alt text](/Praktikum%20Pertemuan%2012/src/image-9.png)
- (di rekomendasikan github karena nanti file yg akan di upload via github)
- Jika sudah masuk, Klik icon foto lalu masuk ke setting, untuk mensinkronkan akun github dengan streamlit
  ![alt text](/Praktikum%20Pertemuan%2012/src/image-10.png)
- isilah Source control dengan github anda
  ![alt text](/Praktikum%20Pertemuan%2012/src/image-11.png)
- klik create app pada pojok kanan
- lalu pilih source from github
  ![alt text](/Praktikum%20Pertemuan%2012/src/image-13.png)
- Lalu cari nama reposiotry github yg baru saja di buat sebelumnya
  ![alt text](/Praktikum%20Pertemuan%2012/src/image-14.png)
- biarkan semua terisi secara default
- untuk App URL bisa di atur sesuai dengan kemauan
- Terakhir klik deploy untuk menjalankan project streamlit
  ![alt text](/Praktikum%20Pertemuan%2012/src/image-15.png)
- maka akan terbuka tab baru yang menampilkan halaman project streamlit anda dengan url sesuai yg di isi sebelumnya
![alt text](/Praktikum%20Pertemuan%2012/src/image-16.png)