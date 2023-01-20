<h1>TASK</h1>

<h2>1. Menjalankan aplikasi Webserver (apache2)</h2>

Pertama saya akan menginstall apache2 terlebih dahulu, setelah apache2 terinstall kita
bisa mengaktifkannya di localtunnel tetapi kita harus mematikan dulu server nginx
Jika sudah maka hasilnya akan seperti ini

![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%203/images/image-000.png)

![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%203/images/image-001.png)

Server apache2 sudah berhasil di run di local tunnel


<h2>2. Menjalankan 3 aplikasi "hello world" menggunakan nodejs, golang dan python </h2>
<h3> NODEJS </h3>
Pertama kita harus menginstall node.js terlebih dahulu
![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%203/images/image-002.png)

Disini saya sudah pernah menginstall nvm jadi selanjutnya saya akan menginstall node,js
version 16

![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%203/images/image-003.png)

![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%203/images/image-004.png)
Lalu jalankan command npm init -y untuk mengnisiasi projek

![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%203/images/image-005.png)
Lalu jalankan command npm install express –save
Lalu buat file index.js dengan command
Nano index.js
Dan tambahkan script didalamnya

![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%203/images/image-006.png)
Lalu run command index.js untuk menjalankan aplikasi

![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%203/images/image-007.png)

Karena saya menggunakan virtual machine saya tidak bisa langsung mengaksesnya melalui
localhost melainkan melalui ip vm saya jadi hasilnya menjadi seperti ini

![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%203/images/image-008.png)

<h3>GOLANG</h3>

![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%203/images/image-009.png)


Lalu kita masukan path go pada .bashrc
![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%203/images/image-010.png)

Untuk golang pertama kita harus menginstalnya terlebih dahulu

![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%203/images/image-011.png)

Lalu buatlah sebuah direktori untuk menyimpan file testing kita
Lalu run command nano index.go

Didalam index go masukan script ini

package main
import "fmt"
func main() {
fmt.Println("Hello World!")
}

![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%203/images/image-012.png)

Lalu save dan coba run aplikasi dengan command
go run index.go
Dan build aplikasi dengan command
Go build index.go
Aplikasi yang telah dibuild bisa dirun dengan command

./index

<h3>Python </h3>

Pertama kita akan menginstall python3 dahulu, biasanya python3 secara default terinstall di
ubuntu dan dapat kita check dahulu dengan command
Python3 -v

![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%203/images/image-013.png)

Dapat dilihat python sudah ada di sistem kita
Selanjutnya kita akan menginstall package manager python3 dengan command

sudo apt install python3-pip

![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%203/images/image-014.png)

Setelah command ini selesai dirun lanjutkan dengan command
Pip install flask

![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%203/images/image-015.png)

Dan python3 pun siap digunakan kita coba dengan membuat sebuah app sederhana
Pertama buat direktori untuk testing


![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%203/images/image-016.png)

Lalu buat file dengan nama index .py dan masukan script ini
from flask import Flask
app = Flask(__name__)
@app.route("/")
def helloworld():
return "Hello World"
if __name__ == "__main__":
app.run()

![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%203/images/image-017.png)

![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%203/images/image-018.png)

Setelah itu run command

python3 index.py

![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%203/images/image-019.png)

Untuk di python3 kita tidak bisa membukanya di browser secara langsung, untuk melihat
hasil kita buka terminal baru dan curl alamat ip yang diberikan oleh sistem disini alamat yang
diberikan adalah 127.0.0.1:5000

![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%203/images/image-020.png)

Jika muncul hello world maka python3 kita sudah berjalan



<h1>3. Gunakan localtunnel untuk menjalankan "Hello world!" nodejs</h1>

Untuk localtunnel pertama kita harus run aplikasi node js kita terlebih dahulu

![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%203/images/image-021.png)

Setelah di run, buka terminal baru dan masukan command
Lt –port 3000

![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%203/images/image-022.png)

Sekarang kita bisa mengakses aplikasi kita melalui localtunnel

![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%203/images/image-023.png)

<h1>Challenge :
Jalankan "Hello world" di python3 melalui port 5000 (gunakan flask), lalu akses dengan
localtunnel
Gunakan PM2</h1>


Python3 dijalankan melalui local tunnel

![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%203/images/image-024.png)

![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%203/images/image-025.png)




![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%203/images/image-026.png)
Pm2

Pertama kita install dulu pm2 nya
Lalu kita run aplikasi python dengan pm2 menggunakan command
pm2 start index.py --interpreter=/usr/bin/python3



![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%203/images/image-027.png)
![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%203/images/image-028.png)

Lalu jalankan locatunnel dengan port 5000
![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%203/images/image-029.png)
![1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%203/images/image-030.png)

Aplikasi python pun berhasil dijalankan dengan pm2


