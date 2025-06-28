+++
date = '2025-06-28T09:55:09+07:00'
draft = false
title = 'Mari Mulai Instal Hugo di Laptop'
+++

## Buat Folder Spesifik
Aku membuat folder pada direktori ini:
- /home/qw/Project/Hugo *(sebelum bikin situs baru bernama 'moveup')*
- /home/qw/Project/Hugo/moveup

## ketahui alamat ip Laptop
- Ketik *ip a*
nanti akan muncul alamat ip misanya *192.168.1.11* tambahkan port *1313* menjadi http://192.168.1.11:1313/ 

## Install App Pendukung
1. sudo apt install git
2. sudo snap install go --classic

## Install Hugo
- sudo apt install hugo

## Buat Situs Baru
- *hugo new site moveup*

Aku membuat situs baru bernama **moveup**, ini berarti ada folder baru bernama moveup.

## Tambahkan Tema
- *git init*
- *git add module git submodule add --depth=1 https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod*

Ini berarti aku mengunduh tema bernama *PaperaMod* dari *themes.gohugo.io*

Terkadang ada tema yang gagal unduh, sehingga harus pastikan untuk melakukan trial-error.

## Terapkan Tema
- *nano hugo.toml*
- tambahkan baris *theme = "PaperMod"*

Jika berhasil, tidak akan muncul error saat membuat postingan baru atau saat melakukan *hugo server*
Ini disebut file config, jadi akan diload saat memulai proses.

## Menambah Artikel
- *hugo new content posts/Mulai.md*
- *nano content/posts/Mulai.md*
- Pastikan *draft = false*

Konsepnya sama persis seperti Obsidian, jadi aku bsia mengeditnya langsung dengan nano. Bisa juga dengan mengunjungi direktori *content/post* lalu mengeditnya langsung dengan *markdown editor*.

## Akses via Browser Laptop
- *hugo server*
- pada browser cukup ketik alamat *http://localhost:1313*

Blog hanya bisa diakses melalui broser laptop saja, sangat cepat, uptodate.
**Pastikan terminal yang menjalankan perintah *hugo server* tidak ditutup**

## Bikin dia Bisa Diakses via Ponsel
- hugo server -D --bind 0.0.0.0 --baseURL http://192.168.1.11:1313/

Ip yang tampil adalah ip yang didapat dari perintah *ip a*. Pastikan melakukan cek IP setelah restart karena router telkom menggunakan ip dinamis yang selalu berubah.


