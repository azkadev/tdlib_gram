# Tdlib Gram (Untuk Bahan Belajar)

Sebuah bahan dasar untuk kamu yang ingin membuat / berinteraksi dengan telegram api terutama menggunakan tdlib, karena sampai saat ini tdlib adalah awalan yang bagus karena kamu tidak hanya bisa membuat bot melainkan applikasi telegram sungguhan.

applikasi ini tidak di design bagus dalam arti ini hanyalah contoh simple penggunaan library [Telegram Client](https://github.com/azkadev)

walaupun ini design tidak bagus, tapi saya membuat ini selain karena ingin membuat contoh penggunaan library saya [Telegram Client](https://github.com/azkadev), saya ingin
mematahkan perkataan seseorang flutter lag apalagi ketika menggunakan ffi

> Ini hanya untuk bahan belajar tidak akan ada update design ui yang mewah / animasi

> Di karenakan kemudahan tdlib, saya tidak bisa update hal hal lebih hanya fitur sederhana saja, karena api telegram sering disalah gunakan

- [Indonesia](README.md)
- [English](README_EN.md)

## Screenshot

ini adalah screenshot di buat pada tanggal 24-juli-2025 mungkin tampilan berbeda jika kamu menggunakan versi open source

| 1                                   | 2                                   | 3                                   |
|-------------------------------------|-------------------------------------|-------------------------------------|
| ![](./screenshots/tdlib_gram/1.png) | ![](./screenshots/tdlib_gram/2.png) | ![](./screenshots/tdlib_gram/3.png) |
| ![](./screenshots/tdlib_gram/4.png) | ![](./screenshots/tdlib_gram/5.png) | ![](./screenshots/tdlib_gram/6.png) |
| ![](./screenshots/tdlib_gram/7.png) |                                     |                                     |

## Applikasi yang sudah di compile dan sudah bisa di jalankan

saya sudah mencoba dan menjalankan pada perangkat saya, tetapi tidak semua arsitektur, 
**mobile hanya arch64 desktop hanya intel dan amd**, selain itu ya bisa saja akan tetapi kamu perlu **compile ulang** termasuk **tdlib**

1. [x] [Android]()
2. [x] [Ubuntu 24 Linux]()
3. [x] [Windows 11]()

## Fakta Menarik

berikut ini adalah beberapa fakta yang mungkin menarik untuk kamu

1. [x] Tidak memakai state management / widget pihak 3 semuanya langsung dari flutter
2. [x] Tidak terikat banyak dependencies / library pihak 3

## Pengembangan

Untuk mengembangkan project ini pastikan kamu memiliki pengetahuan tentang bahasa code [dart](https://dart.dev) dan juga framework [flutter](https://flutter.dev)

setelah mengetahui dasar pastikan kamu memahami library [Telegram Client]()

setelah itu cobalah buka project ini di flutter dan rubah code mana yang kamu ingin rubah

- [Blog Website]()
  jika kamu masih bingung dan ingin tahu bagaimana saya mengembangkan program ini check website diatas


## Masih Kurang

tidak puas karena applikasi ini minimalist ingin fitur lebih? 

Baca ini [Versi Lebih Lengkap](https://)

## Masih Terasa Lag?

sebenernya di katakan **lag** tidak juga, tapi jika kamu **berhasil memodif library** ini dan ya kamu menggunakan banyak client sekaligus, memang kamu benar terkait pernyataan ini. itu **bukan** karena **flutter / ffi**. melainkan **TDLIB** yang memang boros sumber daya apalagi untuk **membuat user dalam jumlah besar**, secara default **TDLIB** memang menyimpan **memory** dan sering menulis ke **disk**, ini yang membuat lag, karena tdlib di design sangat mudah.

> Jika kamu ingin menggunakan tdlib, gunakan hanya satu client saja untuk 1 program, karena jika lebih penggunaan memory akan sulit turun, terutama jika kamu masih pemula

Jika kamu masih merasa tdlib tidak cocok untuk project kamu, coba beralih ke repository [Azkadev Telegram]() yang akan datang disana walaupun saya menggunakan tdlib, saya berhasil memodif tdlib sehingga bisa berjalan dengan sangat baik


## Bantu Saya

Jika kamu merasa program ini berguna, kamu bisa support saya [GITHUB AZKADEV](https://github.com/azkadev) di link itu tersedia social media dan sponsor saya. saya tidak keberatan jika kamu hanya follow / donasi uang sedikit


Terimakasih


Azkadev - 18-07-2025


## 