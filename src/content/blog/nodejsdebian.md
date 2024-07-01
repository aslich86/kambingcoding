---
title: 'Menginstall Nodejs Pada Deepin OS (Debian)'
description: 'Langkah-langkah melakukan instalasi nodejs'
pubDate: 'Jul 02 2024'
heroImage: 'blog-placeholder-2.jpg'
---

Berikut adalah langkah-langkah cara melakukan instalasi Nodejs pada OS berbasis Debian. Saya menggunakan Deepin OS 23 (RC2) pada kesempatan ini. Sebelumnya, unduh nodejs [disini](https://nodejs.org/en). 

NB : Semua langkah di bawah dilakukan melalui terminal ya, dan saya sudah menngunduh file node-v20.15.0-linux-x64.tar.xz serta menempatkannya di direktori Downloads, apabila ada perbedaan nama file dan direktori, kamu bisa menyesuaikan sendiri.

#### Pindah ke Direktori Downloads. 
Pindah ke direktori di mana file tar.xz hasil unduhan disimpan. Biasanya, file yang diunduh disimpan di direktori Downloads.

~~~
cd ~/Downloads
~~~

#### Ekstrak File Unduhan.
Ekstrak file tar.xz yang telah kamu unduh.

~~~~
tar -xJvf node-v20.15.0-linux-x64.tar.xz
~~~

#### Pindahkan Folder Node.js
Pindahkan folder yang diekstrak ke direktori /usr/local untuk menginstalnya secara global.

~~~
sudo mv node-v20.15.0-linux-x64 /usr/local/node-v20.15.0
~~~

#### Buat Symbolic Link:
Buat symbolic link untuk memudahkan penggunaan Node.js. Dengan cara ini, kamu bisa mengakses Node.js dari mana saja di sistem.

~~~
sudo ln -s /usr/local/node-v20.15.0/bin/node /usr/local/bin/node
sudo ln -s /usr/local/node-v20.15.0/bin/npm /usr/local/bin/npm
sudo ln -s /usr/local/node-v20.15.0/bin/npx /usr/local/bin/npx
~~~

#### Verifikasi Instalasi:
Verifikasi apakah Node.js dan npm telah terinstal dengan benar.

~~~
node -v
npm -v
~~~

Perintah ini seharusnya menampilkan versi Node.js dan npm yang telah diinstal.
