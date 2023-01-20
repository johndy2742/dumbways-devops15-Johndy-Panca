Task :
1. Jelaskan definisi distributed revision control!

distributed revision control adalah salah satu bentuk version controli di mana seluruh
basis kode, termasuk seluruh riwayatnya, ada pada setiap komputer developer.
Dibandingkan dengan centered revision control, ini memungkinkan automatic management
branching and merging, mempercepat sebagian besar operasi (kecuali push dan pull),
meningkatkan kemampuan untuk bekerja offline, dan tidak bergantung pada satu lokasi
untuk backup

2. Buat repository untuk tugas kalian di github
Format : dumbways-devops15-<nama kalian>

[1](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%204/images/image-000.png)


Buat repository baru dengan format Format : dumbways-devops15-<nama kalian>

3. Hubungkan ssh public key ke akun github

Pertama kita generate ssh key dengan command

Ssh-keygen

[2](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%204/images/image-001.png)

Lalu run command

Cat .ssh/id_rsa.pub
[2](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%204/images/image-002.png)

Copy ssh key ini dan masukan kedalam github anda

[2](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%204/images/image-003.png)

[2](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%204/images/image-004.png)

Cek koneksi dengan command

ssh -T git@github.com

[2](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%204/images/image-005.png)
Penyambungan ssh pun berhasil

4. Clone repository dumbflix-frontend & buat 3 branch (Development, Staging & Production)


Pertama kita cari repo dumbflix-frontend di github
[2](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%204/images/image-006.png)
Copy link https dan jalankan command

Git clone https://github.com/dumbwaysdev/dumbflix-frontend.git
[2](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%204/images/image-007.png)
Lalu cek branch yang ada di repo
[2](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%204/images/image-008.png)

Kita tambahkan repo development, production, dan staging
[2](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%204/images/image-009.png)
Lalu cek kembali branch yang sudah ada di repo
[2](https://github.com/johndy2742/dumbways-devops15-Johndy-Panca/blob/main/Tugas%204/images/image-010.png)
