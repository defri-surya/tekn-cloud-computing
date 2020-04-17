# Praktikum TCC Minggu 9 (Docker For Beginners - Linux)
-------------------------------------------------------
## Login ke akun Docker Hub
-------------------------------------------------------
![Login Akun Docker Hub](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-09/Screenshot_0.png)

supaya kita dapat mengakses terminal maka dilakukan login pada akun Docker Hub

-----------------------------------------------------------------------
## Task 0: Prerequisites
-----------------------------------------------------------------------

Pada *Prerequisites* ini dilakukan clone repo github untuk mendapatkan linux_tweet_app kemudian dilanjutkan dengan langkah selanjutnya yaitu pada **Task 1: Run some simple Docker containers** untuk memulai container baru dengan menggunakan image alphine dan mengecek daftar image yang tersedia.
Yang ditunjukkan pada hasil dibawah.

![Clone linux_tweet_app](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-09/Screenshot_1.png)

**Run an interactive Ubuntu container**

Mengakses image ubuntu untuk menjalankan terminal dari ubuntu, kemudian dilakukan perintah :
```
$ ls /
$ ps aux
$ cat /etc/issue
```
> perintah $ ls / digunakan untuk melihat file yang ada pada direktori ubuntu
> perintah $ ps aux digunakan untuk melihat container yang sedang berjalan saat ini
> perintah $ cat /etc/issue digunakan untuk menampilkan container yang digunakan saat ini

dengan hasil pada gambar dibawah

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-09/Screenshot_2.png)

kemudian dilakukan perintah exit untuk keluar dari image ubuntu yang sedang dijalankan dan kemudian mengetikkan perintah *cat /etc/issue* untuk menampilkan versi VM yang digunakan setelah keluar dari ubuntu
dengan hasil gambar dibawah

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-09/Screenshot_3.png)

**Run a background MySQL container**

Yang pertama dilakukan yaitu menjalankan MySQL container baru

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-09/Screenshot_4.png)

Selanjutnya melihat proses yang sedang berjalan pada container

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-09/Screenshot_5.png)

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-09/Screenshot_6.png)

Selanjutnya yaitu melihat versi MySQL container yg sedang berjalan kemudian Menjalankan perintah untuk memberikan shell interaktif ( sh) di dalam MySQL container dan mengetikkan perintah *mysql --user=root --password=$MYSQL_ROOT_PASSWORD --version* kemudian ketikkan perintah *exit* untuk keluar dari terminal

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-09/Screenshot_7.png)

--------------------------------------------------------------------------

## Task 2: Package and run a custom app using Docker
--------------------------------------------------------------------------

Pertama, berpindah pada direktori *linux_tweet_app* yang diawal tadi sudah diclone kemudian menampilkan isi Dockerfile

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-09/Screenshot_8.png)

Selanjutnya melakukan Ekspor variabel ke DockerId untuk mendapatkan akses gratis dari variabel ini kemudian dilanjutkan dengan menampilkan isi DockerId

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-09/Screenshot_9.png)

Selanjutnya yaitu membuat Image Docker baru

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-09/Screenshot_10.png)

Selanjutnya memulai container baru dari image yang telah dibuat
![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-09/Screenshot_11.png)

Untuk melihat hasil [Klik Disini Untuk Melihat Hasil](ip172-18-0-74-bqcjndaosm4g00f4due0-80.direct.labs.play-with-docker.com)

![Gambar Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-09/Screenshot_12.png)

Mematikan dan menghapus web yang telah dijalankan

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-09/Screenshot_13.png)

![Hasil Setelah dimatikan dan dihapus](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-09/Screenshot_14.png)

--------------------------------------------------------------------------
## Task 3: Modify a running website
--------------------------------------------------------------------------

Memulai aplikasi web dan pasang direktori saat ini ke dalam container

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-09/Screenshot_15.png)

Menjalankan situs web [Klik Disini Untuk Melihat Hasil](ip172-18-0-74-bqcjndaosm4g00f4due0-80.direct.labs.play-with-docker.com)

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-09/Screenshot_16.png)

**Modify the running website**

Menyalin yang baru *index.html* ke dalam container dengan mengetikkan perintah *cp index-new.html index.html* dan hasilnya dengan menjalankan
[Klik Disini Untuk Melihat Hasil](ip172-18-0-74-bqcjndaosm4g00f4due0-80.direct.labs.play-with-docker.com)

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-09/Screenshot_17.png)

Hentikan dan hapus container yang sedang berjalan, kemudian menjalankan kembali versi saat ini tanpa bind mount, kemudian lihat hasilnya [Klik Disini Untuk Melihat Hasil](ip172-18-0-74-bqcjndaosm4g00f4due0-80.direct.labs.play-with-docker.com)

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-09/Screenshot_18.png)

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-09/Screenshot_19.png)

Berhenti dan lepaskan container yang berjalan saat ini

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-09/Screenshot_20.png)

**Update the image**

Membuat image baru dengan versi 2.0

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-09/Screenshot_21.png)

Melihat daftar image

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-09/Screenshot_22.png)

**Test the new version**

Menjalankan container baru dari versi image yang baru [Klik Disini Untuk Melihat Hasil](ip172-18-0-74-bqcjndaosm4g00f4due0-80.direct.labs.play-with-docker.com)

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-09/Screenshot_23.png)

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-09/Screenshot_24.png)

Menjalankan container baru lain, kali ini dari versi image yang lama
[Klik Disini Untuk Melihat Hasil](ip172-18-0-74-bqcjndaosm4g00f4due0-80.direct.labs.play-with-docker.com)

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-09/Screenshot_25.png)

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-09/Screenshot_26.png)

**Push your images to Docker Hub**

Melihat daftar image pada host Docker

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-09/Screenshot_27.png)

Login ke Docker Hub

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-09/Screenshot_28.png)

Melakukan push image *linux_tweet_app versi 1.0 dan versi 2.0* ke akun Docker Hub

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-09/Screenshot_29.png)

Hasil Setelah dilakukan push image ke akun Docker Hub

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-09/Screenshot_30.png)
