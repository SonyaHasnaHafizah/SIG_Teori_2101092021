1. Membuat Peta Kampung (Layout 1)

- Unduh dan ekstrak data Kit Mulai Cepat Natural Earth. Buka QGIS. Temukan folder di panel Browser . Perluas folder untuk menemukan proyek. Ini adalah file proyek yang berisi lapisan bergaya dalam format Dokumen QGIS. Klik dua kali proyek untuk membukanya. Natural Earth quick startNatural_Earth_quick_start_for_QGIS_v3
- Gunakan kontrol geser dan zoom di Bilah Alat Navigasi Peta dan perbesar ke daerah Kampung (Kota Padang).
- Kita dapat menonaktifkan beberapa lapisan peta untuk data yang tidak kami perlukan untuk peta ini. Perluas folder dan hapus centang pada kotak di sebelah dan lapisan. Sebelum kita membuat peta yang cocok untuk dicetak, kita perlu memilih proyeksi yang sesuai. CRS default untuk proyek diatur ke . Ini adalah CRS yang populer digunakan untuk pemetaan web dan merupakan pilihan yang layak untuk tujuan kita, sehingga kita dapat membiarkannya pada nilai defaultnya. Pergi ke Proyek Tata Letak Cetak Baru .z5 - 1:18mne_10m_geography_marine_polysne_10m_admin_0_disputed_areasEPSG:3857 Pseudo-Mercator.
-Kita akan diminta untuk memasukkan judul untuk tata letak. Kita dapat membiarkannya kosong dan klik Ok.
- Di jendela Print Layout, klik tombol Zoom full untuk menampilkan seluruh Layout.
- Kita harus membawa tampilan peta yang kita lihat di Kanvas QGIS ke tata letak. Pergi ke Tambah Item Tambah Peta.
- Setelah mode Tambah Peta aktif, tahan tombol kiri mouse dan seret persegi panjang di mana Anda ingin menyisipkan peta.
- Kita akan melihat bahwa jendela persegi panjang akan ditampilkan dengan peta dari kanvas QGIS utama. Peta yang diberikan mungkin tidak mencakup seluruh area minat kami. Gunakan opsi Edit Pilih/Pindahkan item dan Edit Pindahkan Konten untuk menggeser peta di jendela dan memusatkannya di komposer.
- Mari kita juga menyesuaikan tingkat zoom untuk peta. Klik pada tab Item Properties dan masukkan 10000000sebagai nilai Scale.
- Tambahkan inset peta yang menunjukkan tampilan yang diperbesar untuk area Kota Padang. Sebelum kita membuat perubahan pada lapisan di jendela utama QGIS, centang kotak Kunci lapisan dan Gaya kunci untuk lapisan . Ini akan memastikan bahwa jika kita mematikan beberapa lapisan atau mengubah gayanya, tampilan ini tidak akan berubah.
- Beralih ke jendela QGIS utama. Matikan grup layer dan aktifkan grup. Grup lapisan ini memiliki gaya yang lebih sesuai untuk tampilan yang diperbesar. Gunakan kontrol pan dan zoom di Map Navigation Toolbar dan zoom di sekitar Kota Padang.z5 - 1:18mz7 - 1: 4m.
- Siap untuk menambahkan inset peta. Ganti jendela Print Layout . Pergi ke Tambah Item Tambah Peta .
- Seret persegi panjang di tempat yang kita ingin menambahkan inset peta. Anda sekarang akan melihat bahwa kami memiliki 2 objek peta di Tata Letak Cetak. Saat membuat perubahan, pastikan Anda memilih peta yang benar.
- Pilih objek yang baru saja kita tambahkan dari panel Items . Pilih tab Properti item . Gulir ke bawah ke panel Frame dan centang kotak di sebelahnya. Anda dapat mengubah warna dan ketebalan batas bingkai sehingga mudah dibedakan dengan latar belakang peta.Map 2
- Salah satu fitur rapi dari Tata Letak Cetak adalah ia dapat secara otomatis menyorot area dari peta utama yang diwakili di sisipan. Pilih objek dari panel Item . Di tab Properti item , gulir ke bawah ke bagian Ikhtisar . Klik tombol Tambahkan ikhtisar baru .Map 1
- Pilih sebagai Bingkai Peta . Ini memberitahu Tata Letak Cetak untuk menyorot objek saat ini dengan tingkat peta yang ditampilkan di objek.Map 2Map 1Map 2
- Siapkan inset peta, kita akan menambahkan grid ke peta utama. Pilih objek dari panel Item . Di tab Properti item , gulir ke bawah ke bagian Kisi . Klik tombol Add a new grid , diikuti dengan Modify grid… .Map 1
- Secara default, garis kisi menggunakan unit dan proyeksi yang sama dengan proyeksi peta yang dipilih saat ini. Namun, lebih umum dan berguna untuk menampilkan garis kisi dalam derajat. Kita dapat memilih CRS yang berbeda untuk grid. Klik tombol Change… di sebelah CRS .
- Dalam dialog Pemilih Sistem Referensi Koordinasi4326 , masukkan dalam kotak Filter . Dari hasil, pilih sebagai CRS. Klik Oke .WGS84 EPSG:4326
- Pilih nilai Interval sebagai 5derajat dalam arah X dan Y. Anda dapat menyesuaikan Offset untuk mengubah tempat munculnya garis kisi.
- Gulir ke bawah ke bagian Bingkai kisi dan centang kotak Gambar koordinat . Format defaultnya adalah Degreestetapi muncul sebagai angka. Kita dapat menyesuaikan adalah dengan menambahkan simbol °. Pilih Customdan klik tombol Ekspresi di sebelahnya.
- Masukkan ekspresi berikut untuk membuat string yang mengambil nomor grid dan menambahkan simbol ° ke dalamnya.
concat(to_string(@grid_number), '°    ')
- Tambahkan bingkai Rectangluar untuk menampung elemen peta lainnya seperti panah utara, skala, dan label. Pergi ke Add Item Add Shape Add Rectangle.
- Kita dapat mengubah Gaya persegi panjang agar sesuai dengan latar belakang peta.
- Tambahkan Panah Utara ke peta. Klik Add Item Add Picture .
- Sambil menahan tombol kiri mouse kita, gambarlah sebuah persegi panjang. Di panel sebelah kanan, klik pada tab Item Properties dan perluas bagian Search directory dan pilih gambar yang Anda sukai.
- Menambahkan bilah skala. Klik Add Item Add Scalebar.
- Memberi label pada peta kita. Klik Add Item Add Lable
- Untuk mengekspor menjadi gambar, klik Tata Export as Image, lalu pilih format yang diinginkan.

2. Bekerja dengan Atribut (Layout 2)

- Cari ne_10m_populated_places_simple.zipfile di QGIS Browser dan perluas. Pilih ne_10m_populated_places_simple.shpfile dan seret ke kanvas.
- Lapisan baru ne_10m_populated_places_simplesekarang akan dimuat di QGIS dan Kita akan melihat banyak titik yang mewakili tempat-tempat berpenduduk di dunia. Tampilan default di kanvas QGIS menunjukkan geometri lapisan GIS. Setiap titik juga memiliki atribut terkait. Mari kita lihat mereka. Temukan Bilah Alat Atribut . Toolbar ini berisi banyak alat yang berguna untuk memeriksa, melihat, memilih, dan memodifikasi atribut dari sebuah lapisan.
- Klik tombol Identifikasi pada Bilah Alat Atribut . Setelah alat dipilih, klik titik mana pun di kanvas. Atribut terkait dari titik itu akan ditampilkan di panel Identifikasi Hasil baru. Setelah Anda selesai menjelajahi atribut dari titik yang berbeda, Anda dapat mengklik tombol Tutup .
- Daripada melihat atribut satu fitur pada satu waktu, kita dapat melihat semuanya bersama-sama sebagai sebuah tabel. Klik tombol Buka Tabel Atribut pada Bilah Alat Atribut . Anda juga dapat mengklik kanan ne_10m_populated_places_simplelayer dan memilih Open Attribute Table .
- Anda dapat menggulir secara horizontal dan menemukan kolom pop_max . Bidang ini berisi populasi tempat terkait. Anda dapat mengklik dua kali pada tajuk bidang untuk mengurutkan kolom dalam urutan menurun.
- Sekarang kita siap untuk melakukan query kita pada atribut-atribut ini. QGIS menggunakan ekspresi seperti SQL untuk melakukan query. Klik Pilih fitur menggunakan tombol ekspresi .
- Di jendela Select By Expression , perluas bagian Fields and Values dan klik dua kali pop_maxlabelnya. Anda akan melihat bahwa itu ditambahkan ke bagian ekspresi di bagian bawah. Jika Anda tidak yakin tentang nilai bidang, Anda dapat mengklik tombol Semua Unik untuk melihat nilai atribut apa yang ada dalam kumpulan data. Untuk latihan ini, kami mencari semua fitur yang memiliki populasi lebih dari 1 juta. Jadi lengkapi ekspresi seperti di bawah ini dan klik Select Features lalu Close .
"pop_max" > 1000000
- Tutup jendela tabel atribut dan kembali ke jendela utama QGIS. Anda akan melihat bahwa subset poin sekarang dirender dengan warna kuning. Ini adalah hasil dari kueri kami dan titik yang dipilih adalah titik yang memiliki pop_maxnilai atribut lebih besar dari 1000000.
- Mari kita perbarui kueri kita dengan menyertakan syarat bahwa tempat itu juga harus menjadi ibu kota selain memiliki populasi lebih dari 1 juta. Untuk membuka editor ekspresi dengan cepat, Anda dapat menggunakan tombol Select Features by Expression di Attributes Toolbar .
- Bidang yang berisi data tentang huruf kapital adalah adm0cap . Nilai tersebut 1 menunjukkan bahwa tempat tersebut adalah ibukota. Kita dapat menambahkan kriteria ini ke ekspresi kita sebelumnya menggunakan operator and . Masukkan ekspresi seperti di bawah ini dan klik Select Features lalu Close .
"pop_max" > 1000000 and "adm0cap" = 1
- Kembali ke jendela utama QGIS. Sekarang Anda akan melihat subset yang lebih kecil dari poin yang dipilih. Ini adalah hasil dari kueri kedua dan menunjukkan semua tempat dari kumpulan data yang merupakan ibu kota negara serta memiliki populasi lebih dari 1 juta.
- Sekarang kita akan mengekspor fitur yang dipilih sebagai layer baru. Klik kanan ne_10m_populated_places_simplelayer dan pergi ke Export Save Selected Features As…
- Kita dapat memilih format apa pun yang Anda sukai sebagai Format . Untuk latihan ini, kita akan memilih GeoJSON. GeoJSON adalah format berbasis teks yang digunakan secara luas dalam pemetaan web. Klik tombol … di sebelah Nama file dan masukkan populated_capitals.geojsonsebagai file output.
- Data input memiliki banyak kolom. Kita hanya dapat memilih sebagian dari kolom asli untuk diekspor. Perluas bagian Pilih bidang yang akan diekspor dan opsi ekspornya . Klik Deselect All dan centang kolom nameand pop_max. Klik Oke .
- Sebuah layer baru populated_capitalsakan dimuat di QGIS. Anda dapat menghapus centang pada ne_10m_populated_places_simplelayer untuk menyembunyikannya dan melihat poin dari layer yang baru diekspor.

 3. Mengimpor file Spreadsheet atau CSV
 
 - Download dataset gempa bumi antara tahun 1900-2000 dari National Geophysical Data Center NOAA
 -  Klik tombol Buka Pengelola Sumber Data pada Bilah Alat Sumber Data Open Data Source.
 - Dalam kotak dialog Pengelola Sumber Data , alihkan ke tab Teks Dibatasi . Klik tombol di sebelah nama File.
 - Pilih file yan telah diunduh, dan klik Open.
 - Di kotak dialog Pengelola Sumber Data , jalur ke file akan tersedia di Nama File . Ubah nama Lapisan menjadi 1900_2000_earthquakes. Di bagian Format file , pilih Pembatas khusus dan centang Tab. Di bagian Definisi geometri , pilih Koordinat titik . Secara default , nilai bidang X dan bidang Y akan terisi secara otomatis jika menemukan bidang nama yang sesuai di input. Dalam kasus kami, mereka adalah Longitudedan Latitude. Kita dapat mengubahnya jika impor memilih bidang yang salah. Anda dapat membiarkan Geometry CRS ke defaultEPSG:4326 - WGS 84CRS. Jika file Anda berisi koordinat dalam CRS yang berbeda, Anda dapat memilih CRS yang sesuai di sini. Klik Tambahkan.
 - Data akan diimpor dan ditampilkan di kanvas QGIS sebagai layer baru yang disebut 1900_2000_earthquakesdengan CRS EPSG:4326.
