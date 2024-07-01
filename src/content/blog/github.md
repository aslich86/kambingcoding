---
title: 'Install Git dan Github pada Solus OS'
description: 'Tutorial install Git dan Github pada Solus OS'
pubDate: 'Jun 18, 2024'
heroImage: 'blog-placeholder-2.jpg'
---

Berikut adalah cara menginstall Git dan Github pada Solus OS (semua langkah dilakukan melalui terminal)

#### 1. Menginstall Git
Solus OS menggunakan eopkg sebagai package manager. Kamu bisa menginstal Git dengan menjalankan perintah berikut di terminal:

```
sudo eopkg install git
```

#### 2. Mengkonfigurasi Git
Setelah Git terinstall, kamu perlu mengkonfigurasinya dengan nama pengguna dan email yang akan kamu gunakan untuk commit. Jalankan perintah berikut di terminal, ganti namamu dan emailmu@example.com dengan informasimu sendiri:

```
git config --global user.name "namamu"
git config --global user.email "emailmu@example.com"
```

#### 3. Memeriksa Instalasi Git
Untuk memastikan bahwa Git telah terinstal dengan benar, kamu bisa menjalankan perintah berikut untuk melihat versi Git yang terinstall:

```
git --version
```

#### 4. Membuat SSH Key (Opsional, tetapi Direkomendasikan)
Jika kamu ingin menggunakan SSH untuk berinteraksi dengan GitHub, kamu perlu membuat SSH key dan menambahkannya ke akun GitHubmu. Jalankan perintah berikut untuk membuat SSH key:

```
ssh-keygen -t rsa -b 4096 -C "emailmu@example.com"
```

Ikuti petunjuk di terminal untuk menyimpan key. Biasanya, key akan disimpan di ~/.ssh/id_rsa.

Kemudian, tambahkan SSH key ke ssh-agent:

```
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa
```

#### 5. Menambahkan SSH Key ke GitHub
Salin SSH key ke clipboard:

```
cat ~/.ssh/id_rsa.pub
```

Salin output yang ditampilkan, kemudian ikuti langkah berikut untuk menambahkan SSH key ke GitHub:

- Masuk ke akun GitHub .
- Pergi ke Settings.
- Di menu SSH and GPG keys, klik New SSH key.
- Masukkan judul untuk key, lalu paste key yang telah disalin tadi.
- Klik Add SSH key.

#### 6. Mengkloning Repository dari GitHub
Sekarang kamu bisa mengkloning repository dari GitHub menggunakan SSH. Misalnya:

```
git clone git@github.com:username/repository.git
```

Atau, jika menggunakan HTTPS:

```
git clone https://github.com/username/repository.git
```

#### 7. Menggunakan Git
Berikut adalah beberapa perintah dasar yang sering digunakan dengan Git:

- git status : Melihat status dari repository.
- git add . : Menambahkan semua perubahan pada staging area.
- git commit -m "Pesan commit" : Membuat commit dengan pesan.
- git push origin branch-name : Mengirim perubahan ke remote repository.
