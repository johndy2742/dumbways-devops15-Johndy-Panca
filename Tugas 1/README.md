<h1>Tugas 1</h1>
 
<h2>1. Definisi DevOps</h2>
   DevOps merupakan singkatan dari dua kata yaitu Development dan Operation. Di mana
kedua kata tersebut bermakna “operasional pengembang”. Seperti yang disebutkan
sebelumnya, DevOps adalah sebuah prinsip developer untuk mengkoordinasikan antar tim
yaitu tim development dengan tim operations dengan efektif dan efisien.

<h2>2. sebutkan lifecycle DevOps (Continuous ...) dan Jelaskan definisi-definisinya! </h2>

Continuous Development
    Continuous Development ini melibatkan perencanaan dan pengkodean dalam pengembangan
perangkat lunak. Di sini, seluruh proses pengembangan dipecah menjadi siklus
pengembangan yang lebih kecil / dipecah - pecah. Proses ini memudahkan tim DevOps untuk
mempercepat proses pengembangan perangkat lunak secara keseluruhan.
Pada perencanaan tidak ada tools DevOps yang diperlukan, tapi sangat banyak Version
Control Tools digunakan untuk maintain kode. Untuk proses maintain code kita sebut Source
Code Maintenance.
Tool - tool populer yang digunakan untuk Source Code Maintenance adalah diantaranya
JIRA, Git, Mercurial, dan SVN.

Continuous Integration
Continuous integration (CI) adalah langkah-langkah yang berkaitan dengan fase pengujian
atau testing. Pada fase ini, Klien juga memberikan informasi yang akan dimasukkan untuk
menambahkan fitur baru ke aplikasi. Pada fase ini juga sebagian besar perubahan terjadi pada
kode. CI adalah pusat dimana perubahan pada kode yang sering terjadi setiap hari maupun
bulan.
Kode yang dibangun ini adalah kombinasi antara Unit Test, Code Review, Integration dan
Packaging. Pada fase ini developer sangat sering melakukan perubahan, mereka akan sangat
cepat menemukan masalah yang terjadi (jika ada) dan menyelesaikannya pada tahap

Continuous Development.
Pada fase ini, akan terjadi penggabungan fungsi dari kode baru dengan kode yang lama. Pada
proses tersebut kita harus memperbarui kode yang ada pada seluruh sistem secara mulus.
Salah satu tools populer yang dapat digunakan adalah Jenkins.

Continuous Testing
Continuous Testing adalah sebuah fase dimana kode akan diuji untuk bug dan kesalahan yang
ada pada kode. Disinilah Quality Analysis (QA) memiliki peran utama untuk memastikan
kode yang dikembangkan tidak terdapat bug.
Automation Tools seperti JUnit, Selenium dan TestNG sering digunakan untuk pengujian.
Tools ini dapat membantu QA menganalisa kode secara bersamaan. Hal ini dilakukan agar
tidak ada kekurangan dalam fungsionalitas aplikasi.

Continuous Deployment
Continuous Deployment memastikan bahwa publish aplikasi dapat dilakukan tanpa
mempengaruhi kinerja dari aplikasi tersebut. Sangat penting untuk memastikan bahwa kode
telah diterapkan pada semua server pada fase ini. Proses ini menghilangkan kebutuhan untuk
merilis aplikasi secara manual.

Continuous Monitoring
Fase ini memproses informasi penting tentang aplikasi yang dikembangkan. Melalui
Continuous Monitoring, developer dapat mengidentifikasi pola umum dan area abu-abu di
aplikasi yang perlu di optimize.
Continuous Monitoring adalah fase operasional yang bertujuan untuk meningkatkan efisiensi
keseluruhan aplikasi. Selain itu, Continuous Monitoring juga membantu kinerja aplikasi.
Oleh karena itu, ini adalah salah satu fase paling penting dari DevOps Lifecycle.
Kesalahan sistem seperti ‘server not reachable’, ‘low memory’ dan yang lainnya, diselesaikan
pada fase Continuous Monitoring. Continuous Monitoring juga menjada ketersediaan dan
keamanan layanan. Masalah jaringan dan masalah lainnya karena secara otomatis diperbaiki
selama fase ini pada saat kesalahan dideteksi.

Continuous Feedback
Continuous Feedback sangat penting untuk memastikan dan menganalisis hasil akhir dari
sebuah aplikasi. Fase ini kita akan mendapatkan feedback untuk meningkatkan versi saat ini
dan melakukan release versi terbaru berdasarkan feedback yang diberikan dari Customer dan
yang lainnya.
Keseluruhan proses pengembangan aplikasi hanya dapat ditingkatkan dengan menganalisa
hasil dari operasi aplikasi. Feedback tidak lain adalah informasi yang dikumpulkan dari
client. Di sini akan mendapatkan informasi penting, karena membawa semua data tentang
kinerja aplikasi dan masalah yang terjadi pada aplikasi tersebut. Pada fase ini juga berisi
saran yang diberikan oleh pengguna dari aplikasi.
Continuous operations
Ini adalah fase terakhir dari DevOps Lifecycle, fase ini adalah yang terpendek dan termudah
untuk dipahami. Continuity adalah inti dari semua operasi DevOps yang membantu untuk
mengotomatiskan proses rilis, memungkinkan developer mendeteksi masalah dengan cepat
dan membangun versi produk aplikasi yang lebih baik. Continuous adalah kunci untuk
menghilangkan langkah tambahan lainnya yang menghambat pengembangan pada sebuah
aplikasi.


<h2>3.Instalasi Ubuntu Server menggunakan VMWare</h2>

Pertama kita harus mendownload file file yang dibutuhkan seperti ubuntu live server dan
vmware


Setelah vmware terinstall, kita bisa langsung membuat virtual machine kita

![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%201/images/1.jpg)

![2](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%201/images/2.jpg)<br>
Dipilihan ini pilih custom configuration agar kita bisa membuat konfigurasi sesuai dengan
kebutuhan

![2](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%201/images/3.jpg)<br>
Pada page ini browse file live server ubuntu yang didownload tadi


![2](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%201/images/4.jpg)<br>
Masukan nama, username, dan password, informasi ini akan digunakan setiap kali kita ingin
login ke live server kita

![2](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%201/images/5.jpg)<br>
Pilih lokasi untuk penginstalan vm

![2](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%201/images/5.jpg)<br>
Pilihlah jumlah core sesuai kebutuhan disini saya memakai 2 core

![2](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%201/images/6.jpg)<br>
Lalu pilih memory yang ingin dipakai disini saya memlih 1GB

![2](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%201/images/7.jpg)<br>
Untuk koneksi pilihlah option NAT

![2](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%201/images/8.jpg)<br>
Untuk disk pilih Create a new virtual disk

![2](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%201/images/9.jpg)<br>
Setelah itu kita tinggal membuild virtual machine yang sudah kita konfigurasi

![2](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%201/images/10.jpg)<br>
Setelah virtual machine telah selesai di build kita harus melakukan beberapa konfigurasi lagi

![2](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%201/images/11.jpg)<br>
Untuk konfigurasi koneksi kita akan memakai static configuration

![2](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%201/images/12.jpg)<br>
Lalu kita masukan ip address, subnet, dan default getaway sesuai dengan adapter apa yang
kita gunakan di vmware, untuk mengecek adapter apa yang digunakan bisa melalui command
prompt

Pada command prompt masukan command ipconfig

![2](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%201/images/13.jpg)<br>
Disini terlihat ip address dan subnet kita, masukan ip address sesuai dengan informasi disini

![2](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%201/images/14.jpg)<br>
Pada konfigurasi storage pilih custom storage layout

![2](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%201/images/15.jpg)<br>
Kita akan membuat partisi yaitu root dan swap
root adalah tempat dimana sistem kita itu ter-install.
swap adalah suatu memori cadangan yang akan digunakan untuk server kita apabila memori1
utama sudah penuh

![2](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%201/images/16.jpg)<br>
Untuk swap cukup 1GB saja

![2](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%201/images/17.jpg)<br>
Untuk root gunakan semua memori yang tersisa

![2](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%201/images/18.jpg)<br>
Lalu masukan nama, nama server dan password untuk server yang dibuat

![2](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%201/images/19.jpg)<br>
Pada ssh setup pilih install openssh server
Setelah selesai diinstall
Coba lah untuk ping ke google.com atau 8.8.8.8

![2](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%201/images/20.jpg)<br>

![2](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%201/images/21.jpg)<br>
Jika berhasil maka koneksi server sudah berhasil


