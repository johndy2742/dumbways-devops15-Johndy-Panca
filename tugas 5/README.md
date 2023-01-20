<h1>Task : Manage Server with Terminal</h1>

<h2>1. Apa itu terminal?</h2>
Terminal adalah sebuah command prompt dimana kita bisa mengontrol file,
membuat folder, membuat akses, merubah akses ataupun membaca, membuat,
merubah file, dan masih banyak lagi fungsi yang lainnya.


<h2>2. BASH script untuk update dan upgrade server, lalu install nginx/apache2 (salah satu)
Pertama kita akan membuat sebuah file script dengan command</h2>

[1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/tugas%205/images/image-000.png)


Nano script.sh

Lalu diisi dengan script berikut
echo "==================================="

echo "running apt update"

echo "==================================="

sudo apt update

echo "==================================="

echo "running apt upgrade"

echo "==================================="

sudo apt upgrade

echo "==================================="

echo "running install apache2"

echo "==================================="

sudo apt install apache2

Save dan run script dengan command

Bash script.sh

[1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/tugas%205/images/image-001.png)

Script pun akan berjalan secara otomatis

[1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/tugas%205/images/image-002.png)

Dan apache2 pun berhasil diinstall

3. BASH script untuk memberi akses ke port 22,80,443
Pertama kita aktifkan dulu firewall dengan command

Sudo ufw enable

[1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/tugas%205/images/image-003.png)

Setelah firewall aktif kita tidak akan bisa mengakses server (default port adalah 80)
karena belum ada konfigurasi

Lalu kita memberi akses ke port 22,80,443 dengan command

sudo ufw allow 22
sudo ufw allow 80
sudo ufw allow 443

[1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/tugas%205/images/image-004.png)

Server pun bisa diakses kembali karena kita telah allow port 80 untuk diakses

[1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/tugas%205/images/image-005.png)

4. Tugas text manipulation
- contoh penggunaan cat, grep, echo & sort
Untuk cat kita bisa menggunakan beberapa function seperti
Cat <filename> berfungsi untuk melihat apa yang tertulis didalam file tanpa harus masuk
melalui text editor
  
[1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/tugas%205/images/image-006.png)
  
Cat > <filename> berfungsi untuk menghapus semua text di dalam file dan
menggantikannya dengan text yang kita masukan

[1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/tugas%205/images/image-007.png)  
  
Cat >> <filename> berfungsi untuk menyisipkan text kedalam file tanpa menghapus isi
didalamnya

[1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/tugas%205/images/image-008.png)
  
Untuk grep kita bisa menggunakan beberapa function seperti
  
Grep <kata kunci> <filename> berfungsi untuk mencari kata kunci dalam file

  [1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/tugas%205/images/image-009.png)
  
Grep -c <kata kunci> <filename> berfungsi untuk menghitung berapa kali muncul kata kunci
dalam file

  [1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/tugas%205/images/image-010.png)

  Untuk echo kita bisa menggunakan beberapa function seperti
  
echo <text> berfungsi untuk mencetak string yang dimasukan
  
[1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/tugas%205/images/image-011.png)
  
  Echo <text> > <filename> befungsi sama seperti cat > <filename> yaitu untuk menghapus
semua text difile dan menggantikannya dengan text yang kita masukan

  [1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/tugas%205/images/image-012.png)
  
  Echo <text> >> <filename> befungsi sama seperti cat > <filename> yaitu untuk menyisipkan
text kedalam file tanpa menghapus isi didalamnya

  [1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/tugas%205/images/image-013.png)
  
  Untuk sort kita bisa menggunakan beberapa function seperti

  Sort <filename> Berfungsi untuk mengurutkan data
Disini saya sudah membuat sebuah file dengan nomor acak
Jika kita jalankan perintah sort maka data akan diurutkan
  [1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/tugas%205/images/image-014.png)
  
Sort -r <filename> Berfungsi untuk mengurutkan data secara menurun

  [1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/tugas%205/images/image-015.png)
  
  5. Gunakan nmon untuk tampilkan CPU usage, RAM usage, Disk dan Resources OS & Proc
Untuk menggunakan nmon kita harus menginstalnya terlebih dahulu
  [1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/tugas%205/images/image-016.png)

  Lalu jalankan command nmon

  [1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/tugas%205/images/image-017.png)
  
  Disini terdapat list function dari nmon karena yang kita butuhkan adalah CPU usage, RAM
usage, Disk dan Resources OS & Proc

  [1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/tugas%205/images/image-018.png)
  
  Maka kita dapat menekan C M D R
C untuk cpu usage
M untuk ram usage
D untuk disk usage
R untuk resource Os dan processor
  
  [1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/tugas%205/images/image-019.png)
  
Challenge
- Buat script instalasi node version manager menggunakan BASH
Buat sebuah file script lalu isi dengan
  
sudo apt update
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash

  [1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/tugas%205/images/image-020.png)
  Save dan jalankan script

  Lalu check dengan command

  Nvm --version

  [1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/tugas%205/images/image-021.png)
  
  Nvm pun berhasil diinstal dengan script
- Jalankan aplikasi pilihan kalian (nodejs/python) dengan kondisi ufw enable
Pertama kita aktifkan dulu firewall dengan command
  
Sudo ufw enable
  
[1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/tugas%205/images/image-022.png)
  
  Pertama kita coba jalankan aplikasi nodejs kita terlebih dahulu

  [1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/tugas%205/images/image-023.png)
  
  Jika kita mencoba untuk mengakses aplikasi kita maka akan muncul pesan seperti berikut
  
  [1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/tugas%205/images/image-024.png)

  Agar bisa menjalankan aplikasi kita, kita harus terlebih dahulu mengallow port yang akan
kita akses dalam kasus ini adalah port 3000
  
  [1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/tugas%205/images/image-025.png)

  Setelah itu kita coba lagi untuk membuka webserver kita
  
  [1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/tugas%205/images/image-026.png)

  Dan aplikasi nodejs pun berhasil dibuka dengan firewall akti
