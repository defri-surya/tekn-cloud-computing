# Praktikum TCC Pertemuan 11 - Application Containerization and Microservice Orchestration

Melakukan login ke akun Docker Hub untuk menampilkan terminal

![Login Docker Hub](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/1.png)

----------------------------------------------------------------------------------------------------------------------------------------------------------------

## Step-0

Melakukan clone repository untuk mendapaktan kode demo, mengubah direktory, dan memeriksa demo

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/2.png)

Memeriksa daftar file yang ada didalam **step0**

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/3.png)

Melihat script python yang ada pada file *linkextractor.py*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/4.png)

Ketika menjalankan perintah *./linkextractor.py http://example.com/* terdapat hasil output **bash: ./linkextractor.py: Permission denied**, Maka dilakukan pemeriksaan izin pada file dengan menggunakan perintah *ls -l linkextractor.py*, Supaya skrip dapat dieksekusi dapat dilakuakn dengan menggunakan perintah *chmod a+x linkextractor.py* atau dengan menggunakan perintah *python linkextractor.py*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/5.png)

----------------------------------------------------------------------------------------------------------------------------------------------------------------

## Step-1

Memeriksa daftar file yang terdapat didalam **step1**

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S1.1.png)

Melihat isi dari Dockerfile

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S1.2.png)

Membuat Image Docker yang diberi nama *linkextractor:step1*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S1.3.png)

Melihat dafatr image dan menjalankan container dan meng-ekstrak tautan dari beberapa halaman web

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S1.4.png)

Melihat halaman web dengan lebih banyak tautan

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S1.5.png)

----------------------------------------------------------------------------------------------------------------------------------------------------------------

## Step-2

Memeriksa daftar file yang terdapat didalam **step2**

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S2.1.png)

Melihat script *linkextractor.py* yang sudah diperbaharui

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S2.2.png)

Membuat Docker image baru

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S2.3.png)

Melihat daftar image yang berjalan

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S2.4.png)

Menjalankan container *linkextractor:step2*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S2.5.png)

Menjalankan container *linkextractor:step1*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S2.6.png)

----------------------------------------------------------------------------------------------------------------------------------------------------------------

## Step-3

Memeriksa daftar file yang ada didalam **step3** dan Melihat isi Dockerfile

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S3.1.png)

Melihat isi dari file *main.py*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S3.2.png)

Membuat Docker image baru dengan nama *linkextractor:step3*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S3.3.png)

Menjalankan container, kemudian melihat daftar container, dilanjutkan dengan membuat request HTTP dan mengambil respon yang berisi tautan yang diekstrak, Lalu melihat log container yang sedang berjalan

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S3.4.png)

Menghapus container

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S3.5.png)

----------------------------------------------------------------------------------------------------------------------------------------------------------------

## Step-4

Melihat daftar file yang ada didalam **step4**

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S4.1.png)

Melihat isi dari file *docker-compose.yml*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S4.2.png)

Melihat isi dari file *www/index.php*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S4.3.png)

Membuat layanan yang terpisah

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S4.4.png)

Melihat daftar container yang sedang berjalan, Mengakses interface dari web, Melakukan modifikasi pada **www/index.php** untuk mengganti link yang awalnya **Link Extractor** menjadi **Super Link Extractor**, Mereset perubahan, Menghentikan layanan

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S4.5.png)

----------------------------------------------------------------------------------------------------------------------------------------------------------------

## Step-5

Melihat daftar file yang ada didalam **step5** dan melihat isi dari *www/Dockerfile*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S5.1.png)

Melihat isi dari *api/main.py*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S5.2.png)

Melihat isi dari file *docker-compose.yml* yang telah diperbaharui

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S5.3.png)

Membuat layanan

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S5.4.png)

Mengekstran tautan dari beberapa halaman web menggunakan interface web, Melihat perubahan dalam layanan yang berjalan dan memverifikasi bahwa perubahan yang dibuat secara lokal tidak mencerminkan dalam layanan yang berjalan, Me-Reset perubahan

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S5.5.png)

Menghentikan layanan yang berjalan

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S5.6.png)

----------------------------------------------------------------------------------------------------------------------------------------------------------------

## Step-6

Melihat daftar file yang ada didalam **step6**

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S6.1.png)

Melihat isi dari *api/linkextractor.rb*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S6.2.png)

Melihat isi dari *api/Dockerfile* dan isi dari file *docker-compose.yml*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S6.3.png)

Membuat layanan baru

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S6.4.png)

Mengakses API, Menghentikan layanan yang berjalan, Melihat log

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-11/S6.5.png)