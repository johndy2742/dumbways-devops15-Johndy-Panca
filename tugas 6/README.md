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


Aplikasi berhasil dijalankan di localhost port 3000
[1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/54a4c3b5d717610b7d7c4d3d37d74ee282a1fc95/tugas%206/images/image-001.png)

gunakan pm2 (challenge)
[1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/54a4c3b5d717610b7d7c4d3d37d74ee282a1fc95/tugas%206/images/image-002.png)

Aplikasi berhasil dijalankan menggunakan pm2

[1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/54a4c3b5d717610b7d7c4d3d37d74ee282a1fc95/tugas%206/images/image-003.png)

4. VM2 :
- jalankan nginx
[1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/54a4c3b5d717610b7d7c4d3d37d74ee282a1fc95/tugas%206/images/image-004.png)

[1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/54a4c3b5d717610b7d7c4d3d37d74ee282a1fc95/tugas%206/images/image-005.png)

buat konfigurasi reverse proxy dengan domain (gunakan nama kalian) mengarah ke app di vm1

[1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/54a4c3b5d717610b7d7c4d3d37d74ee282a1fc95/tugas%206/images/image-006.png)

[1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/54a4c3b5d717610b7d7c4d3d37d74ee282a1fc95/tugas%206/images/image-007.png)


- buat konfigurasi load balance antara VM1 dan VM2
Kita clone aplikasi di vm2 terlebih dulu dan kita run dengan npm

[1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/54a4c3b5d717610b7d7c4d3d37d74ee282a1fc95/tugas%206/images/image-008.png)

[1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/54a4c3b5d717610b7d7c4d3d37d74ee282a1fc95/tugas%206/images/image-009.png)

[1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/54a4c3b5d717610b7d7c4d3d37d74ee282a1fc95/tugas%206/images/image-010.png)


Jika sudah berjalan selanjutnya kita akan load balancing antar 2 vm ini
Tambahkan konfigurasi upstream ke file reverse proxy kita yang tadi dibuat
Masukan ip server dengan port tujuan
[1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/54a4c3b5d717610b7d7c4d3d37d74ee282a1fc95/tugas%206/images/image-011.png)

Lalu cek konfigurasi kita, jika sudah benar kita tinggal restart nginx
[1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/54a4c3b5d717610b7d7c4d3d37d74ee282a1fc95/tugas%206/images/image-012.png)

Setelah konfigurasi reverse proxy kita dibuat
Kita harus memasukannya di nginx.conf terlebih dahulu
[1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/54a4c3b5d717610b7d7c4d3d37d74ee282a1fc95/tugas%206/images/image-013.png)

Ini adalah tampilan ketika kedua server vm dimatikan
[1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/54a4c3b5d717610b7d7c4d3d37d74ee282a1fc95/tugas%206/images/image-014.png)
Kita coba run aplikasi di vm pertama
[1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/54a4c3b5d717610b7d7c4d3d37d74ee282a1fc95/tugas%206/images/image-015.png)
Ini adalah tampilannya

Lalu kita run aplikasi di server kedua terlebih dahulu
[1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/54a4c3b5d717610b7d7c4d3d37d74ee282a1fc95/tugas%206/images/image-017.png)
Setelah itu kita matikan aplikasi di server pertama
[1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/54a4c3b5d717610b7d7c4d3d37d74ee282a1fc95/tugas%206/images/image-018.png)
Dapat dilihat aplikasi masih berjalan dari server ke 2
Load balancer antara vm1 dan vm2 sudah berhasil


5. Domain bisa diakses melalui web browser kalian (edit filenya di /etc/hosts)
[1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/54a4c3b5d717610b7d7c4d3d37d74ee282a1fc95/tugas%206/images/image-019.png)
Note : kalau hanya bisa menjalankan 1 VM, kalian cukup jalankan task no 3 & 4 di 1 VM
tersebut

Challenge
Load Balancer dapat berjalan dengan b
