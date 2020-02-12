1. What is the different between IaaS, SaaS, and PaaS ?
- IaaS(Infrastruktur sebagai layanan) yaitu Perangkat keras, perangkat lunak, dan kode aplikasi Anda harus dikelola.
Anda memilih server untuk diaktifkan (baik fisik atau virtual), menginstal OS dan tumpukan perangkat lunak, lalu akhirnya menyebarkan aplikasi Anda.
Beberapa penyedia menawarkan kontrol tingkat sangat rendah sehingga Anda dapat membangun pusat data Anda sendiri di cloud.

- SaaS(Perangkat Lunak sebagai layanan) Ini adalah level abstraksi tertinggi dan berarti Anda hanya menggunakan aplikasi web dan tidak pernah melihat tumpukan perangkat keras dan lunak yang membuatnya berjalan.

- PaaS(Platform sebagai layanan) Jenis layanan ini memisahkan semua keputusan perangkat keras. Hanya tumpukan perangkat lunak dan kode aplikasi Anda yang harus dikelola.
Server, jaringan, dan penyimpanan yang sebenarnya semuanya diurus secara otomatis oleh platform.

2. SaaS Platform Architecture
SaaS adalah model pengiriman umum untuk banyak aplikasi bisnis, termasuk perangkat lunak perkantoran dan pesan, perangkat lunak manajemen, virtualisasi dll.
Ini adalah bagian dari nomenklatur komputasi awan, bersama dengan infrastruktur sebagai layanan (IaaS), platform sebagai layanan (PaaS), desktop sebagai layanan (DaaS).
Ada dua varietas utama SaaS:
- SaaS Vertikal
	- Perangkat Lunak yang menjawab kebutuhan industri tertentu (mis. Perangkat lunak untuk kesehatan, pertanian, real estat, industri keuangan)
- SaaS Horisontal
	- Produk-produk yang berfokus pada kategori perangkat lunak (pemasaran, penjualan, alat pengembang, SDM) tetapi agnostik industri.

* Manfaat SAAS
Ini menawarkan peluang besar bagi organisasi dari semua ukuran untuk mengalihkan risiko akuisisi perangkat lunak,
dan untuk memindahkan TI dari pusat biaya reaktif menjadi bagian perusahaan yang proaktif dan bernilai tambah.

3. SaaS(Software as a Service) Platform itecture
SaaS juga merupakan salah satu pilar utama komputasi awan.
Sebuah ledakan dalam komputasi Cloud, didorong oleh penyedia cloud seperti Microsoft dengan Azure atau Amazon dengan AWS,
telah melihat pertumbuhan produk dan layanan lain yang disampaikan melalui internet seperti:
* Infrastruktur sebagai Layanan
* Platform sebagai Layanan
* Pembelajaran Mesin sebagai Layanan
* …dan banyak lagi!

- Dari sisi konsumen
Dari perspektif konsumen, produk SaaS adalah salah satu cara termudah untuk menggunakan layanan atau produk digital.
Dalam beberapa tahun terakhir kita telah melihat munculnya ribuan produk SaaS yang ditargetkan untuk konsumen seperti:
* Netflix
* Microsoft Office 365
* Amazon Prime
* Facebook
* …dan masih banyak lagi

- Dari sisi bisnis
Dari perspektif bisnis, produk perangkat lunak yang dikirimkan “sebagai layanan” memungkinkan perusahaan untuk menawarkan produk mereka dalam skala global.
Beberapa manfaat lain dari penerapan arsitektur SaaS dalam bisnis termasuk, tetapi tidak terbatas pada:
* Mengurangi waktu ke pasar
* Biaya perawatan lebih rendah
* Pembaruan yang lebih mudah

**Capabilities of SaaS Solutions**
Solusi SaaS dapat digunakan untuk lingkungan ini dan, secara teori, menawarkan semua jenis layanan yang dapat dikembangkan sebagai aplikasi perangkat lunak yang dapat mencakup, tetapi tidak terbatas pada:
* Aplikasi kantor
* Email dan pesan instan
* Media sosial
* Keamanan dan otentikasi
* Pembelajaran mesin
* Kecerdasan buatan
* Layanan lokasi
* Streaming data dan layanan pencarian

**Kerugian dari Platform SaaS**
* Kurang kontrol
	Karena aplikasi SaaS di-host di server web vendor, Anda memiliki sedikit atau tidak ada kontrol atas perangkat lunak yang Anda gunakan.
* Ekosistem terbatas
	Tidak dapat dipungkiri bahwa SaaS adalah tren yang berkembang sebagai saluran distribusi perangkat lunak. Yang mengatakan, masih banyak aplikasi yang tidak menawarkan versi yang di-host.
* Performa
	Aplikasi internal, klien kental, atau lokal akan selalu berjalan lebih cepat daripada produk yang dikirim melalui internet.
* Kekhawatiran Data
	Saat memilih produk SaaS, dan misalnya, dengan munculnya GDPR, bisnis harus memberikan perhatian khusus dalam hal di mana implementasi SaaS menyimpan data di cloud.
	Setiap yurisdiksi memiliki kebijakan legislatif sendiri dan bertindak ketika data sensitif diproses atau disimpan.

4. How to build a cloud-based SaaS Application
# Pemilihan bahasa pemrograman
	Selain kemampuan dan keterampilan pribadi, pilihan bahasa pemrograman Anda akan dipengaruhi oleh kemungkinan masing-masing bahasa. Ada berbagai bahasa pemrograman (modern) di luar sana sehingga sulit untuk memilih yang benar.
# Bahasa pemrograman Python
	Python adalah bahasa pemrograman yang banyak digunakan, dirancang untuk menekankan keterbacaan kode-nya.
	Python dapat melakukan banyak hal. Apa pun aplikasi web yang ingin Anda bangun, kemungkinan ada kerangka untuknya dengan Python.
# Pemilihan basis data
	salah satu hal pertama dalam daftar Anda akan mencakup pemasangan basis data. Kami merekomendasikan penggunaan basis data berorientasi dokumen . Database dokumen sangat berbeda dengan konsep tradisional database relasional.
* Basis data berorientasi dokumen
Database dokumen mendapatkan informasi tipenya dari data itu sendiri. Ini memungkinkan lebih banyak fleksibilitas, terutama ketika berhadapan dengan perubahan. Dan sering mengurangi ukuran basis data.
# MongoDB
MongoDB adalah database berorientasi dokumen yang memberikan kinerja tinggi, ketersediaan tinggi, dan skalabilitas mudah.
Skalabilitas adalah faktor terpenting bagi kami sebagai bisnis SaaS global. Banyak pendiri SaaS bertujuan untuk meningkatkan skala bisnis mereka.
Dengan sharding otomatis, Anda dapat mendistribusikan data di berbagai mesin. Sharding adalah metode untuk menyimpan data Anda di beberapa mesin. Dan MongoDB menggunakan sharding untuk mendukung penyebaran dengan dataset besar.
# RabbitMQ
RabbitMQ adalah sistem antrian sumber terbuka yang berjalan pada semua sistem operasi utama.
# AWS & EC2
AWS memungkinkan Anda untuk meng-host dan menjalankan aplikasi web Anda serta melakukan pekerjaan batch berkinerja tinggi. Dengan Elastic Compute Cloud (EC2) AWS menyediakan server virtual yang dapat diskalakan untuk setiap bisnis.
# EC2
server-server EC2 tersebar di seluruh dunia. Bergantung pada kebutuhan Anda untuk mengukur dan pasar geografis mana yang menjadi target pertama, Anda dapat memilih di antara berbagai lokasi EC2 Anda.
Dengan EC2 terinstal, sangat mudah untuk terus menambahkan server dan sumber daya baru.
# Jaringan pengiriman konten
Sebuah jaringan pengiriman konten (CDN) pada dasarnya adalah sebuah sistem server didistribusikan yang memungkinkan Anda untuk melayani konten dengan pengguna aplikasi Anda dengan kinerja tinggi dan ketersediaan tinggi.
# Mengatur aplikasi SaaS
Dengan Python, MongoDB - sebagai basis data yang berorientasi pada dokumen, perangkat lunak RabbitMQ sebaiknya dilakukan dengan pengaturan dasar.