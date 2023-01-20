Task : Web Server & Load Balancing

1. Definisi Web Server

web server adalah komputer yang menyimpan, memproses, dan mengirim file website ke
web browser. Web server terdiri dari hardware dan software yang menggunakan HTTP
(Hypertext Transfer Protocol) untuk merespons permintaan pengguna web dari World Wide
Web. Melalui proses ini, web server memuat dan mengirim halaman yang diminta untuk
disajikan di browser pengguna, misalnya Google Chrome. Web server juga menggunakan
SMTP (Simple Mail Transfer Protocol) dan FTP (File Transfer Protocol) dalam memproses
file untuk email atau penyimpanan.

2. Jalankan 2 VM (Optional)
- VM 1 = appserver
- VM 2 = nginx


3. VM1 :
- jalankan aplikasi dumbflix-frontend
 
[1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/54a4c3b5d717610b7d7c4d3d37d74ee282a1fc95/tugas%206/images/image-000.png)

[2](tugas 6/images/image-000.png)

Aplikasi berhasil dijalankan di localhost port 3000

- buat konfigurasi load balance antara VM1 dan VM2
Kita clone aplikasi di vm2 terlebih dulu dan kita run dengan npm
Jika sudah berjalan selanjutnya kita akan load balancing antar 2 vm ini
Tambahkan konfigurasi upstream ke file reverse proxy kita yang tadi dibuat
Masukan ip server dengan port tujuan
Lalu cek konfigurasi kita, jika sudah benar kita tinggal restart nginx
Setelah konfigurasi reverse proxy kita dibuat
Kita harus memasukannya di nginx.conf terlebih dahulu
Ini adalah tampilan ketika kedua server vm dimatikan
Kita coba run aplikasi di vm pertama
Ini adalah tampilannya
Lalu kita run aplikasi di server kedua terlebih dahulu
Setelah itu kita matikan aplikasi di server pertama
Dapat dilihat aplikasi masih berjalan dari server ke 2
Load balancer antara vm1 dan vm2 sudah berhasil
5. Domain bisa diakses melalui web browser kalian (edit filenya di /etc/hosts)
Note : kalau hanya bisa menjalankan 1 VM, kalian cukup jalankan task no 3 & 4 di 1 VM
tersebut

Challenge
Load Balancer dapat berjalan dengan b
