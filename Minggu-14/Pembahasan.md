# Praktikum Pertemuan 14 - Kubernetes For Beginners

Melakukan login ke akun Docker Hub supaya dapat menampilkan terminal

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-14/kubernetes%201.jpg)

Menjalankan perintah *ls* kemudian menjalankan perintah *kubeadm init --apiserver-advertise-address $(hostname -i)* untuk menginisialisasi gugus pada terminal pertama

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-14/kubernetes%202.jpg)

Setelah melakukan inisialisasi dilanjutkan dengan menjalankan perintah *kubeadm join 192.168.0.33:6443 --token bdk9eq.z3q1b4rhpbuyhlw5 \ --discovery-token-ca-cert-hash sha256:315c1a287b01338b26c0131a9d0cd81fd1db18197fe3f779d099207191c7a68b*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-14/kubernetes%203.jpg)

Yang terakhir untuk mengatur cluster yaitu dengan menjalankan perintah *kubectl apply -n kube-system -f \ "https://cloud.weave.works/k8s/net?k8s-version=$(kubectl version | base64 |tr -d '\n')"*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-14/kubernetes%204.jpg)

Menjalankan perintah *git clone https://github.com/dockersamples/dockercoins* untuk melakukan clone repository Dockercoins

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-14/kubernetes%206.jpg)

Setelah proses clone selesai dilanjutkan dengan membuka direktori Dockercoins yang telah didiclone dengan menjalankan perintah *cd ~/dockercoins* dan dilanjutkan kembali dengan menjalankan container Dockercoins dengan menjalankan perintah *docker-compose up*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-14/kubernetes%207.jpg)

Setelah itu bisa melihat hasil dengan menggunakan link [Klik Disini Untuk Melihat Hasil](http://ip172-18-0-8-brgro7rmjflg00d8b3r0-8000.direct.labs.play-with-k8s.com/)

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-14/kubernetes%205.jpg)

Untuk melihat komposisi dari Cluster dapat menjalankan perintah *kubectl get node*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-14/kubernetes%208.jpg)

Untuk melihat info lebih lanjut mengenai node dapat menjalankan perintah *kubectl get nodes -o wide*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-14/kubernetes%209.jpg)

Untuk menampilkan info berupa YAML dapat dilakukan dengan menjalankan perintah *kubectl get no -o yaml*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-14/kubernetes%2010.jpg)

Menampilkan kapasitas semua node sebagai aliran objek JSON dengan menjalankan perintah *kubectl get nodes -o json | jq ".items[] | {name:.metadata.name} + .status.capacity"*

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-14/kubernetes%2011.jpg)

Melihat daftar layanan Cluster

![Hasil](https://github.com/defri-surya/tekn-cloud-computing/blob/master/Minggu-14/kubernetes%2012.jpg)