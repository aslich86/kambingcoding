---
title: 'Menginstall Node.Js di Solus OS'
description: 'Tutorial install Node.Js di Solus OS'
pubDate: 'Jul 17 2024'
heroImage: 'blog-placeholder-1.jpg'
---

## Tutorial Menginstall Node.js di Solus OS

Saat ini, saya menggunakan Solus OS, sebuah distribusi Linux yang mungkin kurang populer di Indonesia dibandingkan Ubuntu dan Debian.
Karena ketidak populerannya, tidak seperti sistem operasi lain, cukup sulit untuk mencari tutorial dalam menginstall tools atapun software yang kita butuhkan.
Salah satu tools yang sangat saya butuhkan diantaranya adalah Node.js. Tools ini sering saya gunakan dalam membangun sebuah website.
Berikut tutorial cara menginstall Node.js di Solus OS.

1. Download File Installer [disini](https://nodejs.org/en/)
2. Ekstrak berkas tar.xz:

~~~
cd ~/Downloads
tar -xvf node-v20.14.0-linux-x64.tar.xz
~~~

3. Verifikasi hasil ekstraksi:

~~~
ls node-v20.14.0-linux-x64
~~~

4. Pindahkan direktori hasil ekstraksi ke /usr/local:

~~~
sudo mv node-v20.14.0-linux-x64 /usr/local/
~~~

5. Verifikasi direktori di /usr/local:

~~~
ls /usr/local/node-v20.14.0-linux-x64
~~~

6. Buat symlink untuk node dan npm:

~~~
sudo ln -sf /usr/local/node-v20.14.0-linux-x64/bin/node /usr/local/bin/node
sudo ln -sf /usr/local/node-v20.14.0-linux-x64/bin/npm /usr/local/bin/npm
~~~

7. Verifikasi instalasi dengan memeriksa versi:

~~~
node -v
npm -v
~~~

Demikian tutorial menginstall Node.js di Solus OS. Semoga bermanfaat 👍.
