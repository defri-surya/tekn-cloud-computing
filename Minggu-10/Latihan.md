# Docker Network - Pertemuan 10

---------------------------------------------------------------

Sebelum menjalankan perintah memlalui terminal kita melakukan login pada akun docker hub terlebih dahulu

![Login Akun Docker Hub](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S1.tcc-1.png)

---------------------------------------------------------------

## Bagian 1

Mengetikkan perintah *docker network* untuk mengkonfigurasi dan mengelola jaringan kontainer

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S1.tcc-2.png)

Selanjutnya, mengetikkan perintah *docker network ls* digunakan untuk melihat jaringan container yang ada pada host docker saat ini

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S1.tcc-3.png)

Untuk melihat rincian konfigurasi jaringan bridge yang meliputi : nama, ID, driver, driver IPAM, info subnet, wadah terhubung, dan banyak lagi dengan mengetikkan perintah *docker network inspect bridge*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S1.tcc-4.png)

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S1.tcc-4%60.png)

Dengan mengetikkan perintah *docker info* untuk menunjukkan banyak informasi tentang instalasi docker dan menemukan dafatr plugin jaringan

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S1.tcc-5.png)

---------------------------------------------------------------

## Bagian 2

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S2.tcc-1.png)

Pada hasil diatas menunjukkan bahwa jaringan bridge dicakup secara lokal dan jaringan hanya terdapat pada host docker ini
Untuk membuat bridge Linux di host docker dapat menggunakan perintah *apk update dan apk add bridge*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S2.tcc-2.png)

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S2.tcc-3.png)

Untuk melihat detail bridge pada **docker0** dengan menggunakan perintah *ip a*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S2.tcc-4.png)

Selanjutnya kita akan membuat container baru dengan menjalankan perintah *docker run -dt ubuntu sleep infinity*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S2.tcc-5.png)

Untuk melihat container yang sedang berjalan dengan menggunakan perintah *docker ps*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S2.tcc-6.png)

Lalu kita akan melihat antarmuka yang terhubung pada **docker0** setelah pembuatan container baru

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S2.tcc-7.png)

pada hasil diatas dapat dilihat bahwa setelah pembuatan container baru maka antarmuka akan terhubung pada **docker0**
Selanjutnya, memeriksa jaringan bridge kembali dengan meengetikkan perintah *docker network inspect bridge*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S2.tcc-8.png)

Selanjutnya, melakukan Ping pada alamat IP container dengan menjalankan perintah *ping -c5 172.17.0.2*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S2.tcc-9.png)

Lalu memeriksa kembali container yang sedang berjalan

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S2.tcc-10.png)

Selanjutnya, kita menjalankan shell ubuntu dengan menggunakan perintah *docker exec -it 63c376343001 /bin/bash*, Setelah masuk pada shell ubuntu kemudian melakukan instalasi program ping dengan menggunakan perintah *apt-get update && apt-get install -y iputils-ping*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S2.tcc-11.png)

Setelah proses instalasi program ping selesai maka dilanjutkan dengan melakukan PING pada www.guthub.com dengan menggunakan perintah *ping -c5 www.github.com*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S2.tcc-12.png)

Setelah itu menjalankan perintah *docker stop 63c376343001* untuk menghentikan container yang berjalan

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S2.tcc-13.png)

Selanjutnya, menjalanakan container baru yaitu container NGINX dengan menjalankan perintah *docker run --name web1 -d -p 8080:80 nginx*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S2.tcc-14.png)

Melihat kembali container yang sedang berjalan

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S2.tcc-15.png)

Jika tidak dapat menjalankan sesi menggunakan web browser maka dapat menjalankan perintah *curl 127.0.0.1:8080* maka kita dapat terhubung dari host docker

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S2.tcc-16.png)

---------------------------------------------------------------

## Bagian 3

Pada bagian ini hal pertama yang dilakukan yaitu melakukan analisis pada swarm dengan menggunakan printah *docker swarm init --advertise-addr $(hostname -i)*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S3.tcc-1.png)

Untuk melakukan verifikasi bahwa kedua node adalah bagian dari swarm, dengan menggunakan perintah *docker node ls*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S3.tcc-2.png)

Selanutnya, membuat jaringan Overlay baru yang disebut "overnet" dengan menggunakan perintah *docker network create -d overlay overnet* dan melihat bahwa jaringan telah berhasil dibuat atau tidak dengan menggunakan perintah *docker network ls*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S3.tcc-3.png)

Untuk melihat informasi lebih rinci mengenai jaringan "overnet" dengan menggunakan perintah *docker network inspect overnet*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S3.tcc-5.png)

Selanjutnya, membuat layanan baru dengan nama **myservice** pada jaringan "overnet" dengan replika, menggunakan perintah
*docker service create --name myservice \
--network overnet \
--replicas 2 \
ubuntu sleep infinity*
dan memeriksa bahwa layanan sudah berhasil dibuat dan berhasil dijalankan atau belum dengan menggunakan perintah *docker service ls*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S3.tcc-6.png)

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S3.tcc-7.png)

Memeriksa bahwa replika yang dibuat telah berjalan pada masing-masing node swarm

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S3.tcc-8.png)

Perintah *docker network ls* untuk memeriksa jaringan overnet

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S3.tcc-9.png)

Untuk mendapatkan informasi lebih rinci tentang jaringan "overnet" dengan menggunakan perintah *docker network inspect overnet*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S3.tcc-10.png)

Perintah *docker ps* disini digunakan untuk mendapatkan ID container

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S3.tcc-11.png)

Menggunakan perintah *docker exec -it a3c8b870e2ec /bin/bash* untuk menampilkan shell dan melakukan instalasi *iputils-ping* Setelah itu dilanjutkan dengan melakukan *ping -c5 10.0.0.3*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S3.tcc-12.png)

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S3.tcc-13.png)

Kemudian mengetikkan perintah *cat /etc/resolv.conf* lalu dilanjutkan dengan melakukan ping pada layanan dengan menggunakan perintah *ping -c5 myservice*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S3.tcc-14.png)

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S3.tcc-15.png)

Melakukan konfigurasi layanan

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S3.tcc-16.png)

Yang terakhir yaitu melakukan penghapusan layanan **myservice** dengan menggunakan perintah *docker service rm myservice* kemudian dilanjutkan dengan melihat daftar container yang berjalan

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S3.tcc-17.png)

Melakukan penghapusan node

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-10/S3.tcc-18.png)