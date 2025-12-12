# PRAKTIKUM: Visualisasi Data

**Mata Kuliah:** Pemrograman Dasar  
**Topik:** Visualisasi  


# Pengenalan Data Visualization

Pembahasan ini merupakan salah satu pembahasan paling esensial dalam analisis data. Selain itu, kemampuan untuk memvisualisasikan data merupakan salah satu keterampilan penting yang harus dimiliki oleh seorang praktisi data.

![Pengenalan](https://assets.cdn.dicoding.com/original/academy/dos:0f6cba3720b76fe5dcbe471a29abc28120230310091635.png)

Pada siklus tersebut, data visualization merupakan tahapan yang harus kita lakukan sebelum membuat kesimpulan dan mengomunikasikan (draw conclusion & communicate) hasil dari proses analisis yang telah dilakukan. Hal ini dilakukan untuk mempermudah kita dalam memahami data dan membuat sebuah kesimpulan yang andal. Selain itu, visualisasi data juga dapat membantu kita dalam menyampaikan cerita atau temuan dari hasil analisis data kepada orang lain atau stakeholder.

Sederhananya, visualisasi data merupakan cara kita dalam menyajikan data dalam bentuk visual. Hal ini dilakukan untuk mempermudah kita dan orang lain dalam memahami data tersebut. Selain itu, visualisasi data yang baik juga akan sangat membantu kita dalam menyampaikan story dan pesan dari sebuah data.


# Prinsip-Prinsip dalam Visualisasi Data

Ketika berbicara tentang visualisasi data, kita tidak hanya membahas cara menyajikan data ke dalam bentuk visual, melainkan juga harus memahami berbagai prinsip dasar dalam membuat visualisasi data yang baik dan benar.

Sebagai permulaan, mari kita lihat berbagai contoh visualisasi data yang buruk dan tidak mengikuti prinsip desain dalam visualisasi data.

Sederhananya, visualisasi data yang buruk merupakan bentuk visual yang tidak mampu menyampaikan pesan dan informasi terkait data secara baik serta efisien. Umumnya visualisasi data yang buruk memuat salah satu dari tiga masalah berikut.

## - Misleading
Masalah pertama dalam visualisasi data yang buruk ialah misleading information yang mampu mengakibatkan kesalahan dalam pengambilan kesimpulan dari sebuah data. Berikut contoh visualisasi data yang bisa mengakibatkan misleading information

![Misleading](https://assets.cdn.dicoding.com/original/academy/dos:5d61b7e6e261f34abee21f2ba3c4136320230309140942.jpeg)

Apa yang ada di benak Anda ketika melihat visualisasi data tersebut? Tentunya Anda akan melihat bahwa terdapat gap yang cukup besar dari kedua nilai tersebut. Hal ini contoh kesalahan pengambilan kesimpulan karena buruknya sebuah visualisasi data.

Apakah Anda bisa menebak kesalahan apa yang mengakibatkan visualisasi data di atas menghasilkan kesimpulan yang salah? Yap, benar sekali visualisasi datanya tidak mulai dari nol sehingga terkesan ada gap yang cukup besar dari kedua nilai tersebut. Berikut merupakan contoh perbaikan dari visualisasi tersebut.

![misleading2](https://assets.cdn.dicoding.com/original/academy/dos:ba2d24378cadf9b558cbbf5c17992bf220230309140942.jpeg)

## - Hides
Selain misleading information, masalah lain yang umum dijumpai dalam visualisasi data yang buruk ialah menyembunyikan informasi tertentu. Berikut contoh visualisasi data yang menyembunyikan informasi penting dari sebuah data

![hides](https://assets.cdn.dicoding.com/original/academy/dos:03a1a50a1a70ff2abef992495e5fbac620230309140942.jpeg)

Berdasarkan visualisasi data di atas bisakah Anda menjawab berapa besar market share yang dimiliki supplier A? Lalu, supplier manakah yang memiliki market share terbesar? Anda mungkin akan kesulitan dalam menjawab kedua pertanyaan tersebut karena banyak sekali informasi yang disembunyikan dari visualisasi tersebut.

## Distracts
Masalah lain yang mungkin terjadi ialah distraksi. Visualisasi data yang buruk sering kali menyertakan komponen visual yang seharusnya tidak dibutuhkan dan malah mengganggu proses pengambilan kesimpulan dari sebuah visualisasi data. Berikut merupakan contoh visualisasi data yang memuat komponen visual yang tidak dibutuhkan.

![distrac1](https://assets.cdn.dicoding.com/original/academy/dos:f4d3a5d911c0c7980d5428161de3cb1220230309140942.jpeg)

Pada contoh visualisasi di atas, kita menggunakan warna untuk membedakan kategori pada data tersebut. Hal ini sebenarnya tidak dibutuhkan karena informasi terkait hal ini sudah tersedia pada sumbu x.

Warna merupakan komponen visual yang penting dalam visualisasi data. Oleh karena itu, kita bisa menggunakannya untuk menyampaikan pesan yang menarik dan mempermudah orang lain untuk memahami data yang kita miliki. Gambar di bawah ini merupakan contoh visualisasi data yang baik dalam penggunaan warna untuk menyorot bagian tertentu.

![distract2](https://assets.cdn.dicoding.com/original/academy/dos:90c67292f2a688d99fcacfd1d63d277520230309140942.jpeg)

Oke, kita telah melihat berbagai masalah beserta contohnya pada visualisasi data yang buruk. Kini saatnya kita mengenal berbagai prinsip dalam visualisasi data untuk menghindari kesalahan tersebut.

# Prinsip Desain dalam Visualisasi Data

Jika ditelisik secara mendasar, visualisasi data merupakan proses dalam mengubah data ke dalam bentuk visual menggunakan berbagai elemen visual. Berikut merupakan beberapa elemen visual yang umum digunakan untuk membuat visualisasi data.

- **Position**: elemen ini akan membantu kita merepresentasikan titik data menggunakan sumbu tertentu (seperti sumbu X, Y, dan Z) sebagai acuan.
- **Size**: ukuran (panjang atau lebar) merupakan elemen visual yang umumnya kita gunakan untuk membedakan serta membandingkan nilai dari kategori atau titik data tertentu.  
- **Shape**: bentuk merupakan salah satu elemen visual yang dapat digunakan untuk membedakan kategori atau titik data tertentu. 
- **Color**: selain bentuk, warna juga merupakan pilihan elemen visual lain yang dapat digunakan untuk membedakan kategori atau titik data tertentu. Ketika menggunakan elemen ini, kita harus ingat bahwa tidak semua orang memiliki kemampuan untuk membedakan warna dengan baik.
- **Texture**: penambahan tekstur atau pola tertentu bisa menjadi alternatif lain dalam membedakan kategori atau titik data tertentu.
- **Angle**: pada beberapa pilihan bentuk visualisasi data, sudut merupakan salah satu elemen visual yang digunakan untuk merepresentasikan nilai dari suatu data.
Oke, itulah keenam elemen visual yang biasa digunakan dalam membuat visualisasi data. Tugas kita sebagai praktisi data ialah mencari cara untuk menerapkan seluruh elemen visual tersebut secara efektif untuk menyiratkan kisah dari sebuah data.

Nah, pertanyaan selanjutnya ialah bagaimana cara menerapkan keenam elemen tersebut secara efektif. Kunci utama dalam hal ini adalah menghindari penggunaan elemen visual yang tidak perlu. Untuk memastikan penggunaan elemen visual secara efektif, Edward Tufte telah mengenalkan sebuah konsep bernama Data Ink Ratio pada bukunya yang berjudul “The Visual Display of Quantitative Data”.

Data ink ratio merupakan sebuah konsep parameter yang digunakan sebagai penentu efektivitas penggunaan visual elemen dalam sebuah visualisasi data. Ia didefinisikan sebagai perbandingan antara tinta (bisa diartikan sebagai elemen visual) yang digunakan untuk mendeskripsikan data dan total tinta yang digunakan dalam satu visualisasi data. Rasio ini dapat digunakan untuk memastikan semua elemen visual yang digunakan relevan untuk kebutuhan penyampaian pesan dari sebuah data. Jadi sederhananya, visualisasi data yang efektif haruslah memiliki nilai ink ratio yang tinggi.


![prinsip](https://assets.cdn.dicoding.com/original/academy/dos:3ea43f0e502943237cfe7c5e5b2af3db20230310091719.png)


# Prinsip Integritas dalam Visualisasi Data

Ketika membuat sebuah visualisasi data, kita tidak hanya memikirkan terkait faktor estetika (seni) saja. Melainkan, kita juga harus memastikan visualisasi data yang kita buat mampu menyampaikan berbagai informasi penting dari sebuah data tanpa menyembunyikan fakta, mengarahkan orang lain pada asumsi tertentu, serta menghindari misinterpretasi. Oleh karena itu, selain menerapkan prinsip desain kita juga menerapkan prinsip integritas dalam proses pembuatan visualisasi data.

Pada bukunya yang berjudul The Visual Display of Quantitative Data, Edward Tufte juga mengenalkan beberapa prinsip guna menjaga integritas dalam membuat visualisasi data. Berikut beberapa prinsip tersebut.

- Representasi angka pada sebuah grafik harus sebanding dengan kuantitas sebenarnya. Hal ini untuk menghindari terjadinya misinterpretasi dari sebuah visualisasi data.
- Pelabelan yang jelas, terperinci, dan menyeluruh merupakan kunci utama dalam menghindari ambiguitas dalam sebuah visualisasi data.
- Visualisasi data yang baik harus menunjukkan variasi pada data bukan variasi desain.
- Untuk menghindari asumsi, kita harus menggunakan unit yang umum digunakan (sesuai standar atau kesepakatan) dalam merepresentasikan suatu data tertentu.
- Jumlah variabel (feature/kolom) yang digambarkan tidak boleh melebihi jumlah dimensi dalam data. Sebagai contoh, untuk menggambarkan hubungan variabel X dan Y, kita disarankan untuk menggunakan plot dua dimensi ketimbang menggunakan plot tiga dimensi.
- Sebuah grafik tidak boleh menampilkan data yang di luar konteks.
  

Nah, itu dia keenam prinsip yang harus kita ikuti untuk menjaga integritas dan menghindari misinterpretasi dalam sebuah visualisasi data. Sebenarnya pada buku yang sama, Edward Tufte juga mengenalkan sebuah parameter bernama Lie Factor untuk mengukur kesalahan representasi dalam sebuah visualisasi data. Parameter ini didefinisikan sebagai rasio perbandingan ukuran yang ditampilkan pada grafik dan ukuran yang sebenarnya ada dalam data. Rasio ini tentunya akan memberikan kita gambaran sejauh mana visualisasi mendistorsi nilai dari sebuah data.

# Univariate Visualization

Sampai dengan tahap ini, Anda telah memahami berbagai konsep dasar dalam membuat visualisasi data yang efektif. Untuk melengkapi pengetahuan Anda, pada materi ini kita akan belajar cara membuat visualisasi data menggunakan library matplotlib dan seaborn. 

Seperti yang telah kita bahas sebelumnya, visualisasi data merupakan teknik yang digunakan dalam merepresentasikan atau menyajikan data ke dalam bentuk visual yang lebih mudah dipahami. Nah, berdasarkan jumlah variabel (feature/kolom) yang ingin disajikan, visualisasi data dapat dibagi menjadi tiga kategori.

- **Univariate visualization**
  
Univariate visualization merupakan bentuk visualisasi data yang hanya merepresentasikan informasi yang terdapat pada satu variabel. Jenis visualisasi ini umumnya digunakan untuk memberikan kita gambaran terkait distribusi sebuah variabel dalam suatu dataset.

- **Bivariate visualization**

Bivariate visualization merupakan bentuk visualisasi data untuk menyajikan informasi yang terdapat dalam dua variabel. Visualisasi jenis ini dapat digunakan untuk menganalisis hubungan antar dua variabel dalam sebuah dataset.

- **Multivariate visualization.**

Last but not least, multivariate visualization merupakan jenis visualisasi data untuk menggambarkan informasi yang terdapat dalam lebih dari dua variabel. Jenis visualisasi ini digunakan untuk merepresentasikan hubungan dan pola yang terdapat dalam multidimensional data.  

itulah ketiga jenis visualisasi data berdasarkan jumlah variabel yang disajikan. Nah, pada materi ini, kita akan fokus membahas tentang univariate visualization.

Secara umum, terdapat beberapa pilihan grafik yang dapat digunakan dalam univariate visualization, seperti bar chart, pie chart, histogram, box plot, dll.

Bagaimana menurut Anda? Apakah Anda penasaran kegunaan dan cara membuat seluruh pilihan grafik tersebut? Jika iya, yuk, simak penjelasan berikut.

##  Bar Chart

Bentuk visualisasi data pertama yang akan kita bahas ialah bar chart atau dikenal juga dengan sebutan diagram batang. Ia merupakan pilihan visualisasi data yang digunakan untuk menggambarkan distribusi dari suatu data kategoris (categorical data). Pada bar chart, setiap kategori akan direpresentasikan sebagai sebuah batang. Tinggi dari sebuah batang menunjukkan frekuensi atau jumlah titik data dari kategori tersebut. 

Sebagai contoh, katakanlah kita memiliki data survey dan ingin melihat distribusi responden berdasarkan gender. Nah, pada kasus ini, kita bisa menggunakan bar chart untuk merepresentasikan informasi tersebut seperti gambar di bawah ini.

![bar](https://assets.cdn.dicoding.com/original/academy/dos:b9f6278ec751791d71dda3691d63b13020230310091802.png)

Jika data kategori tersebut merupakan data nominal, kita bisa mengurutkan tampilan bar chart berdasarkan jumlahnya. Namun, ingat hal ini hanya berlaku untuk data nominal, sedangkan untuk data ordinal alangkah baiknya kita urutkan berdasarkan peringkat dari data tersebut. Hal ini dilakukan karena pada data ordinal peringkat merupakan informasi yang sangat penting untuk di informasikan.

![barchart](https://assets.cdn.dicoding.com/original/academy/dos:52937a3baf3049138b1b89c16ac63d2c20230309142246.jpeg)

Salah satu variasi bar chart yang sering Anda jumpai ialah horizontal bar chart. Pada variasi ini,  sumbu X menggambarkan kategori dan sumbu Y memuat informasi frekuensi dari tiap kategori tersebut. Variasi ini umumnya digunakan ketika kita memiliki banyak kategori atau nama kategori yang cukup panjang.

![bar](https://assets.cdn.dicoding.com/original/academy/dos:3233a18c62733d41b451c6689e3bcfbd20230310091821.png)



 sekarang kita telah memahami konsep dasar tentang bar chart. Pertanyaan selanjutnya adalah bagaimana cara membuatnya? Kabar baik untuk kita semua karena library matplotlib telah menyediakan sebuah function bernama pyplot.bar() untuk membuat sebuah bar chart. Untuk menggunakan function tersebut, kita perlu mendefinisikan parameter x dan height dari bar chart yang ingin dibuat. Berikut merupakan contoh untuk membuatnya.

 ```python
 import matplotlib.pyplot as plt
 
cities = ('Bogor', 'Bandung', 'Jakarta', 'Semarang', 'Yogyakarta', 
          'Surakarta','Surabaya', 'Medan', 'Makassar')
 
populations = (45076704, 11626410, 212162757, 19109629, 50819826, 17579085,
               3481, 287750, 785409)
 
plt.bar(x=cities, height=populations)
plt.show()
```

Kode di atas akan menghasilkan bentuk visualisasi seperti berikut.

![barchart](https://assets.cdn.dicoding.com/original/academy/dos:e77d93c192493d6d86ba18886224e08320230309143716.png)

Disclaimer: data yang digunakan pada contoh di atas bukan merupakan jumlah populasi sebenarnya. Data tersebut hanya digunakan sebagai contoh dalam pembuatan grafik menggunakan library matplotlib. 

 apakah Anda bisa membaca nama kota yang ada pada sumbu X? Tentunya tidak, bukan? Oleh karena itu, kita harus melakukan sedikit modifikasi pada plot tersebut. Untuk melakukan modifikasi ini, kita bisa menggunakan function xticks() dan mengatur besar parameter rotation. Parameter tersebut akan mengatur besar rotasi nilai kategori pada sumbu X. Contoh penggunaanya bisa Anda lihat pada contoh kode di bawah ini.

 ```python
 plt.bar(x=cities, height=populations)
plt.xticks(rotation=45)
plt.show()
 ```
Kode di atas akan menghasilkan tampilan visualisasi yang sedikit lebih baik seperti berikut.

![barchart](https://assets.cdn.dicoding.com/original/academy/dos:cef3a8395bf23689be784a4b4a14245720230309143919.png)

Hasil visualisasi di atas tentunya jauh lebih baik jika dibandingkan dengan hasil bar chart sebelumnya. Sebenarnya kita bisa merepresentasikan data ini secara lebih baik menggunakan function barh(). Untuk menggunakan function tersebut kita harus mendefinisikan parameter y dan width dari bar chart yang ingin dibuat. Berikut merupakan contoh kode untuk melakukannya.

```python
plt.barh(y=cities, width=populations)
plt.show()
```
Kode di atas akan menghasilkan bentuk visualisasi data yang lebih mudah diamati seperti berikut.

![](https://assets.cdn.dicoding.com/original/academy/dos:34419dfebee450bad527d8d48e99540320230309144110.png)

Nah, jika diperhatikan data tersebut merupakan data nominal sehingga kita boleh mengurutkan nilainya berdasarkan jumlah populasi terbanyak. Untuk melakukan hal ini, kita membutuhkan bantuan library pandas dalam mengubah data menjadi DataFrame dan mengurutkannya menggunakan function sort_values(). Berikut contoh kode yang dapat Anda gunakan.

```python
import pandas as pd
 
df = pd.DataFrame({
    'Cities': cities,
    'Population': populations,
})
 
df.sort_values(by='Population', inplace=True)
 
plt.barh(y=df["Cities"], width=df["Population"])
plt.show()
```

Berikut merupakan hasil visualisasi data dari kode di atas.

![](https://assets.cdn.dicoding.com/original/academy/dos:acadd5576fc2db7f453102ffb566277420230309144253.png)


Bagaimana menurut Anda? Hasilnya sudah cukup baik, bukan? Untuk memperjelas visualisasi data yang dibuat, kita bisa menambahkan beberapa keterangan seperti judul dan keterangan sumbu. Untuk melakukan hal ini, kita bisa menggunakan function title(), xlabel(), dan ylabel(). Kode di bawah ini merupakan contoh kode untuk menambah keterangan pada hasil plot visualisasi data.

```python
plt.barh(y=df["Cities"], width=df["Population"])
plt.xlabel("Population (Millions)")
plt.title("Population of Cities in Indonesia")
plt.show()
```

Kode di atas akan menghasilkan visualisasi data seperti berikut.

![](https://assets.cdn.dicoding.com/original/academy/dos:4cd3fbe9e248f7cd1b22ba9e5c65f58220230309144422.png)

Selain menggunakan library matplotlib, kita juga bisa membuat bar chart menggunakan library seaborn. Untuk membuat bar chart menggunakan library seaborn, kita bisa menggunakan function barplot(). Function ini akan menyediakan beberapa parameter penting seperti berikut.

- data: menampung DataFrame yang akan digunakan.
- x, y: menampung nama kolom atau data yang divisualisasikan.
- orient: orientasi dari bar chart yang akan digunakan (“v” atau “h”).
- color: mendefinisikan warna yang akan digunakan.

Berikut contoh kode untuk membuat bar chart dengan library seaborn.

```python
import seaborn as sns
 
sns.barplot(y=df["Cities"], x=df["Population"], orient="h", color='blue')
plt.xlabel("Population (Millions)")
plt.title("Population of Cities in Indonesia")
plt.show()
```

Kode di atas akan menghasilkan visualisasi data seperti gambar berikut.

![](https://assets.cdn.dicoding.com/original/academy/dos:45b8f35719945b19507c5fe598c91c8420230309144859.png)

Bagaimana menurut Anda? Cukup mudah bukan untuk membuat bar chart menggunakan matplotlib dan seaborn? Nah, selanjutnya kita akan belajar cara membuat visualisasi data untuk bentuk grafik yang lain.


## Pie Chart

Bentuk visualisasi data berikutnya yang akan kita bahas ialah pie chart. Ia merupakan bentuk visualisasi data yang dapat digunakan untuk menggambarkan perbandingan frekuensi tiap kategori pada suatu data kategoris. Pada pie chart, setiap kategori digambarkan oleh irisan dalam sebuah lingkaran dan frekuensi digambarkan sebagai luasan (area) dari irisan tersebut. Jadi pada pie chart semakin besar area dari sebuah irisan menandakan bahwa kategori tersebut memiliki jumlah titik data yang banyak. Sebaliknya, semakin sempit luasan pada sebuah irisan menandakan bahwa kategori tersebut memiliki frekuensi jumlah titik data yang sedikit.

![pie](https://assets.cdn.dicoding.com/original/academy/dos:6f13b0b58175ebf11f2237e3f8d46be420230310091836.png)

Apabila Anda perhatikan informasi yang direpresentasikan dengan pie chart ini cukup mirip dengan bar chart. Oleh karena itu, pie chart sering digunakan sebagai alternatif dari bar chart. Namun, perlu Anda ingat bahwa sebaiknya pie chart digunakan untuk merepresentasikan data yang memiliki jumlah kategori yang relatif sedikit. Hal ini dilakukan untuk mempermudah orang lain dalam memahami informasi yang ingin kita sampaikan. Bisa Anda lihat pada gambar di bawah ini, betapa sulitnya membaca nilai dari kategori lain.

![](https://assets.cdn.dicoding.com/original/academy/dos:3ab23948258dee6a328688c42a93ff4420230309142246.jpeg)

Terdapat variasi lain dari pie chart, yaitu donut plot. Sebenarnya, ia merupakan pie chart yang memiliki lubang pada bagian tengahnya sehingga membentuk donut. Selain itu, tidak ada perbedaan mendasar dalam penggunaan antara pie chart dan donut plot. Oleh karena itu, estetika merupakan alasan yang umum digunakan ketika memilih salah satu dari keduanya.

![](https://assets.cdn.dicoding.com/original/academy/dos:4a13053ea7aed1d4859195a5b31375d320230310091905.png)


Seperti biasa setelah memahami konsepnya, kini saatnya kita melihat bagaimana cara membuatnya. Untuk membuat pie chart, kita bisa memanfaatkan library andalan, yaitu matplotlib. Ia telah menyediakan sebuah function bernama pie() untuk menghasilkan grafik pie chart. Function tersebut memiliki beberapa parameter penting yaitu seperti berikut.

- x: menampung data yang akan divisualisasikan.
explode: menampung array atau list yang mengatur posisi tiap irisan lingkaran.
- labels: sekumpulan string yang digunakan untuk memberi label pada tiap irisan lingkaran.
- colors: sekumpulan warna yang akan digunakan pada tiap irisan lingkaran.
- autopct: string yang digunakan untuk memberi numerik label pada tiap irisan lingkaran.
  
Berikut contoh kode untuk membuat grafik pie chart.

```python
import matplotlib.pyplot as plt
 
flavors = ('Chocolate', 'Vanilla', 'Macha', 'Others')
votes = (50, 20, 30, 10)
colors = ('#8B4513', '#FFF8DC', '#93C572', '#E67F0D')
explode = (0.1, 0, 0, 0)
 
plt.pie(
    x=votes,
    labels=flavors,
    autopct='%1.1f%%',
    colors=colors,
    explode=explode
)
plt.show()

```

Kode di atas akan menghasilkan tampilan visualisasi data seperti berikut.

![](https://assets.cdn.dicoding.com/original/academy/dos:878d1910138f8310cb912eb135c99f3420230309150134.png)

Selain itu, kita juga bisa menggunakan parameter wedgeprops untuk menghasilkan donut plot. Parameter ini digunakan untuk mengatur ukuran dari lubang yang dihasilkan. Berikut contoh kodenya.

```python
plt.pie(
    x=votes,
    labels=flavors,
    colors=colors,
    wedgeprops = {'width': 0.4}
)
plt.show()
```

Kode di atas, akan menghasilkan tampilan visual seperti berikut.

![](https://assets.cdn.dicoding.com/original/academy/dos:067035b4230244087b941a95602a473a20230309150232.png)

## Histogram

Jika kedua grafik sebelumnya digunakan untuk data kategorik, sekarang kita kenalan dengan grafik untuk data kuantitatif yang bernama histogram. Grafik ini digunakan untuk menggambarkan distribusi dari data kuantitatif. Jika dilihat sekilas, bentuk grafik histogram mirip dengan bentuk bar chart perbedaannya hanya terdapat pada sumbu X. Pada grafik histogram, sumbu X digunakan untuk menampung range nilai dari data kuantitatif yang dikenal dengan istilah bins.

![](https://assets.cdn.dicoding.com/original/academy/dos:0f97bb835ecc6c122791dbd5304914c420230309150317.png)

Pada grafik histogram, ukuran bins akan sangat berpengaruh terhadap cara kita dalam merepresentasikan data kuantitatif. Jika menggunakan ukuran bins yang terlalu besar, kita akan kehilangan cukup banyak informasi dari data kuantitatif yang ingin divisualisasikan. Sebaliknya, apabila ukuran bins yang digunakan terlalu kecil, hal ini akan menghasilkan banyak noise yang mendistraksi distribusi data yang ingin kita amati.

![](https://assets.cdn.dicoding.com/original/academy/dos:0446839c8ed00bb37bd42b230cf9af7520230309150335.png)

Untuk membuat grafik histogram, kita bisa menggunakan function hist() yang disediakan oleh library matplotlib. Function ini menerima beberapa parameter seperti berikut.

- x: menampung data yang akan divisualisasikan.
- bins: menampung jumlah bins (sebanding dengan ukurannya) yang akan digunakan untuk membuat grafik histogram.
  
Berikut merupakan contoh kode untuk membuat grafik histogram.

```python
import matplotlib.pyplot as plt
import numpy as np
 
x = np.random.normal(15, 5, 250)
 
plt.hist(x=x, bins=15)
plt.show()
```

Pada contoh kode di atas, kita menggunakan function random.normal() yang disediakan oleh library numpy untuk menghasilkan sampel data acak yang memiliki distribusi normal. Sample data random tersebut memiliki jumlah 250 titik data dengan nilai mean sebesar 15 dan standard deviation sebesar 5. Kode di atas akan menghasilkan grafik seperti berikut.

![](https://assets.cdn.dicoding.com/original/academy/dos:12421f3b9c2db90923d22243e96f700120230309150833.png)

Selain menggunakan library matplotlib, kita juga bisa membuat grafik histogram dengan library seaborn. Library ini menyediakan function histplot() untuk membuat grafik histogram. Berikut contoh kode untuk melakukannya.

```python
import seaborn as sns
 
sns.histplot(x=x, bins=15)
plt.show()
```

Kode di atas akan menghasilkan grafik histogram seperti berikut.

![](https://assets.cdn.dicoding.com/original/academy/dos:44d91fcbbec00b34f1a37f250e158bc220230309151005.png)

Untuk mempermudah dalam mengidentifikasi distribusi dari sebuah data kuantitatif, kita bisa menambahkan parameter kde=True seperti pada contoh kode di bawah ini.

```python
sns.histplot(x=x, bins=15, kde=True)
plt.show()

```

Kode tersebut akan menghasilkan grafik histogram yang disertai sebuah garis. Garis tersebut menunjukkan densitas distribusi berdasarkan grafik histogram yang dihasilkan. Berikut merupakan visualisasi yang dihasilkan.

![](https://assets.cdn.dicoding.com/original/academy/dos:06cbb3b64458c140b8cef10cf11bfb0020230309151101.png)

## Box Plot
Bentuk visualisasi data lain yang bisa digunakan untuk mengidentifikasi distribusi pada data kuantitatif ialah box plot. Ia merupakan bentuk visual untuk merepresentasikan nilai IQR beserta ambang batas bawah dan atas dari sebuah data. Box plot ini juga bisa digunakan untuk mengidentifikasi outlier atau pencilan yang ada pada data kuantitatif.

![](https://assets.cdn.dicoding.com/original/academy/dos:424472a009560144c8e6346ba53e349220230309142246.jpeg)

Kita bisa menggunakan function boxplot() yang disediakan oleh library seaborn. Berikut contoh kode untuk menggunakannya.

```python
import matplotlib.pyplot as plt
import seaborn as sns
import numpy as np
 
x = np.random.normal(15, 5, 250)
sns.boxplot(x=x)
plt.show()
```

Kode di atas akan menghasilkan visualisasi data seperti berikut.

![](https://assets.cdn.dicoding.com/original/academy/dos:59d2c8d182c2d54c9e6d133580d3773c20230309151157.png)


# Bivariate dan Multivariate Visualization

Nah, pada materi ini, kita akan mengenal berbagai pilihan visualisasi data untuk melakukan bivariate dan multivariate visualization.

Sederhananya, bivariate visualization merupakan bentuk visualisasi data untuk menyajikan informasi dari dua variabel dalam suatu dataset. Di lain sisi, multivariate visualization merupakan jenis visualisasi data untuk menggambarkan informasi yang terdapat dalam lebih dari dua variabel. Keduanya sering digunakan untuk mendeskripsikan hubungan antar variabel dalam suatu dataset.

Terdapat beberapa pilihan visualisasi data yang umum digunakan dalam bivariate dan multivariate visualization, seperti scatter plot, line chart, dan clustered bar chart. Selain itu, sebenarnya kita juga bisa menggunakan komponen visual tambahan, yaitu color, shape, dan texture untuk mendeskripsikan lebih banyak variabel. Nah, pada materi ini, kita akan belajar seluruh hal tersebut satu per satu.

## Scatter Plot

Bentuk visualisasi data pertama yang akan kita bahas ialah scatter plot. Ia merupakan bentuk visualisasi data yang digunakan untuk melihat hubungan antara dua atau lebih variabel data kuantitatif. Pada scatter plot sumbu X, Y, atau Z digunakan untuk menampung nilai dari setiap variabel yang akan divisualkan. Titik pada scatter plot merupakan titik temu data dari setiap sumbu yang digunakan. Gambar di bawah ini merupakan contoh tampilan scatter plot untuk dua variabel data.

![](https://assets.cdn.dicoding.com/original/academy/dos:5c64022558142feae8e218f44c1bb67320230310092003.png)

Untuk membuat scatter plot, kita bisa menggunakan library matplotlib. Ia telah menyediakan sebuah function bernama scatter() untuk membantu kita membuat scatter plot secara lebih mudah. 

Berikut contoh kode untuk menggunakannya.

```python

import matplotlib.pyplot as plt
 
lemon_diameter = [6.44, 6.87, 7.7, 8.85, 8.15, 
                  9.96, 7.21, 10.04, 10.2, 11.06]
lemon_weight = [112.05, 114.58, 116.71, 117.4, 128.93, 
                132.93, 138.92, 145.98, 148.44, 152.81]
 
plt.scatter(x=lemon_diameter, y=lemon_weight)
plt.show()
```

Kode di atas akan menghasilkan visualisasi data seperti berikut.

![](https://assets.cdn.dicoding.com/original/academy/dos:7286084cee047c2831a001a2342ddf6120230309155435.png)

Bagaimana cukup mudah, bukan? Nah, selain menggunakan library matplotlib, kita juga bisa menggunakan function scatterplot() yang disediakan oleh library seaborn untuk membuat scatter plot.
Berikut contoh kode untuk menggunakan function tersebut.

```python
import matplotlib.pyplot as plt
import seaborn as sns
 
sns.scatterplot(x=lemon_diameter, y=lemon_weight)
plt.show()
```

Berikut tampilan visualisasi data yang dihasilkan.

![](https://assets.cdn.dicoding.com/original/academy/dos:daf676bcf819464a0cde376284bba2e820230309155715.png)

Nah, untuk mempermudah dalam melihat korelasi atau hubungan antar variabel, kita bisa menggunakan function regplot() yang disediakan oleh library seaborn. Function tersebut memadukan scatter plot dan regression function (metode statistik untuk memperkirakan korelasi antar independent dan dependent variable) untuk melihat tren serta korelasi antar variabel. 

```python
sns.regplot(x=lemon_diameter, y=lemon_weight)
plt.show()
```

Kode di atas akan menghasilkan tampilan visualisasi data seperti berikut.

![](https://assets.cdn.dicoding.com/original/academy/dos:b59f8ecd4f8d9c7066538387b101b7bd20230309155836.png)


Pada visualisasi data di atas, garis biru menunjukkan garis korelasi dari hasil regression sedangkan pita di sekitar garis tersebut menunjukkan confidence level dari hasil regression tersebut. Semakin kecil bentuk pita yang dihasilkan menandakan tingkat confidence level yang tinggi.

Selain itu, kita juga bisa membuat scatter plot untuk menggambarkan hubungan antar tiga variabel. Namun, untuk kebanyakan kasus kita harus menghindari penggunaan plot tiga dimensi karena sulit diamati dan dipahami.


## Line Chart

Bentuk visualisasi data yang selanjutnya akan kita bahas ialah line chart. Ia merupakan bentuk grafik yang umum digunakan untuk menggambarkan tren nilai dari suatu variabel terhadap variabel lain. 

![](https://assets.cdn.dicoding.com/original/academy/dos:2485ca916bcb8e825ad94b50f739db9e20230310092017.png)

Kita bisa membuat line chart menggunakan function plot() yang disediakan oleh matplotlib. Berikut merupakan contoh kode untuk melakukannya.

```python
import matplotlib.pyplot as plt
 
lemon_diameter = [6.44, 6.87, 7.7, 8.85, 8.15, 
                  9.96, 7.21, 10.04, 10.2, 11.06]
lemon_weight = [112.05, 114.58, 116.71, 117.4, 128.93, 
                132.93, 138.92, 145.98, 148.44, 152.81]
 
plt.plot(lemon_diameter, lemon_weight)
plt.show()
```

Kode di atas akan menghasilkan visualisasi data seperti berikut.

![](https://assets.cdn.dicoding.com/original/academy/dos:aa7a7e3a1a928019dc8619d6461c57c620230309160017.png)

Bentuk visualisasi data ini umumnya digunakan untuk melihat trend dari data berbentuk time series (data yang direkam dalam interval waktu yang konsisten). Berikut contoh kode untuk menampilkan plot harga saham Bank Central Asia dengan kode saham BBCA.

```python
import yfinance as yf
import matplotlib.pyplot as plt
 
# Unduh data historis saham BBCA.JK
ticker = yf.Ticker("BBCA.JK")
df = ticker.history(period="6mo", interval="1d")  # atau bisa diubah ke "1y", dll
 
# Reset index agar tanggal menjadi kolom
df.reset_index(inplace=True)
 
# Visualisasi harga penutupan
plt.figure(figsize=(12, 5))
plt.plot(df['Date'], df['Close'], color='red')
plt.xlabel('Date', fontsize=15)
plt.ylabel('Close Price (IDR)', fontsize=15)
plt.title('Harga Saham BBCA.JK', fontsize=16)
plt.grid(True)
plt.tight_layout()
plt.show()
```

Pada contoh kode di atas, kita memvisualkan data saham yang diperoleh dari Yahoo Finance. Agar tampilan visualnya enak dilihat, pada contoh ini, kita mengatur ukuran plot-nya dengan argumen figsize pada function figure(). Berikut merupakan visualisasi data yang dihasilkan.

![](https://assets.cdn.dicoding.com/original/academy/dos-7884ecf7212076252aae792bafe9e54b20250731145438.png)

![](https://assets.cdn.dicoding.com/original/academy/dos-09dee78537998f7f6843bbbcc10337e320250731145423.png)

Catatan: Jika terdapat kesalahan yfinance belum terinstal, silakan gunakan perintah berikut untuk menginstallnya. pip install yfinance


## Clustered Bar Chart

Clustered bar chart merupakan bentuk modifikasi dari bar chart yang sebelumnya kita kenal dengan menambahkan variabel kategoris lain. Modifikasi ini memungkinkan untuk melihat distribusi serta hubungan antar dua atau lebih variabel kategoris. 

Untuk membuat clustered bar chart, kita bisa menggunakan parameter hue pada function barplot() yang disediakan oleh library seaborn. Berikut contoh kode untuk membuatnya.

```python
import seaborn as sns
import matplotlib.pyplot as plt
 
penguins = sns.load_dataset("penguins")
 
sns.barplot(data=penguins, x="species", y="body_mass_g", hue="sex", errorbar=None)
plt.show()
```

Pada contoh kode di atas, kita membuat bar chart untuk melihat distribusi berat badan dari setiap spesies penguin. Selanjutnya distribusi tersebut dikelompokkan berdasarkan jenis kelamin. Berikut tampilan visualisasi data yang diperoleh.

![](https://assets.cdn.dicoding.com/original/academy/dos:d6a13fbded044ee73aab761b44cf753f20230309160401.png)


### Menggunakan Komponen Visual Tambahan

Selain menggunakan scatter plot, line chart, dan clustered bar chart, kita juga bisa memodifikasi bentuk visualisasi data dengan menambahkan komponen visual tambahan seperti color, shape, serta texture untuk mendeskripsikan lebih banyak variabel. 

Sebagai contoh, Anda bisa membuat lebih dari satu boxplot untuk menggambarkan distribusi nilai numerik dari beberapa variabel. Hal ini bisa Anda gunakan dengan memasukkan DataFrame yang akan divisualisasikan pada parameter data dalam function boxplot(). Selain itu, Anda juga bisa menggunakan parameter palette untuk mengatur palet warna yang akan digunakan. Berikut contoh kode untuk melakukannya.


```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
 
url = 'https://query1.finance.yahoo.com/v7/finance/download/BBCA.JK?period1=1644796800&period2=1676332800&interval=1d&events=history&includeAdjustedClose=true'
df = pd.read_csv(url)
df['Date'] = pd.to_datetime(df['Date'])
 
df_boxplot = df[["Open", "High", "Low", "Close", "Adj Close"]]
 
sns.boxplot(data=df_boxplot, palette="rocket")
plt.ylabel('Price',size=15)
plt.show()
```

Sederhananya, pada contoh kode di atas, kita memvisualkan seluruh data yang ada di dalam df_boxplot. Selain itu, pada kode tersebut, kita menggunakan palet warna bernama “rocket” (dokumentasi palet warna: [Choosing color palettes](https://seaborn.pydata.org/tutorial/color_palettes.html)). Berikut merupakan tampilan visualisasi data yang dihasilkan.

![](https://assets.cdn.dicoding.com/original/academy/dos:f5b42049cfe2b8145fecf2ea4463708b20230309160544.png)

Nah, dengan visualisasi data tersebut, kita dapat membandingkan berbagai variabel yang digunakan untuk mendeskripsikan harga saham. Namun, perlu diingat bahwa hal ini hanya boleh dilakukan untuk membandingkan nilai variabel yang merepresentasikan unit atau satuan ukur yang sama (contoh di atas sama-sama menggambarkan harga saham).

Selain itu, kita juga bisa memodifikasi scatter plot menggunakan shape atau color yang berbeda guna menampilkan hubungan lebih dari dua variabel data. Seperti pada contoh berikut.


```python
import seaborn as sns
 
penguins = sns.load_dataset("penguins")
 
sns.scatterplot(data=penguins, x="body_mass_g", y="flipper_length_mm", hue="species", style="species")
plt.show()

```

Pada contoh kode di atas, kita menampilkan hubungan antara berat badan dan flipper length dari setiap spesies penguin yang dibedakan menggunakan warna (hue) serta bentuk (style). Berikut hasil visualisasi data dari kode tersebut.

![](https://assets.cdn.dicoding.com/original/academy/dos:61dd7ce81928eeb88a9c3c579d5a10c720230309160753.png)

itulah berbagai pilihan bentuk visualisasi dan teknik yang dapat Anda gunakan untuk merepresentasikan dua atau lebih variabel dalam suatu dataset. Nah, pada materi berikutnya, kita akan melihat berbagai hal dan best practice dalam melakukan explanatory analysis.