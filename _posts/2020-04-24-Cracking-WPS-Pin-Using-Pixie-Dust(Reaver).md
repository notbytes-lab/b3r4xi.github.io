---
title: Cracking WPS Pin Using Pixie Dust (Reaver)
published: true
categories: Ethical Hacking
---

Well hello gaiss apa kabar ? jenuh kan self quarantine, sama aing juga
So kali ini mau sedikit kasih tutorial gimana cara cracking WPS Pin.

nah buat kalian yang belum tau apa itu WPS Pin, kita sedikit pelajari dulu aja, mulai dari apa itu WPS Pin sama cara kerja nya gimana.

```Disclaimer
Disclaimer
Jadi Tulisan ini ane buat, semata-mata hanya untuk Education Purpose Only. 
Jadi mohon digunakan sebaik mungkin ya !
```
Oke, lanjut ke pembahasan apa itu WPS PIN ?
Jadi, Singkatnya gini WPS adalah atau Wi-Fi Protected Setup sebuah metode yang digunakan untuk sebuah perangkat dapat terkoneksi secara otomatis kepada router atau access point

Nah buat lebih lanjut lagi kalian bisa baca artikel dibawah ini

[How WPS Pin Works](https://www.digitalcitizen.life/simple-questions-what-wps-wi-fi-protected-setup)

Untuk sekarang, Kita sudah tau kan gimana WPS Pin itu berkerja, disamping dapat melakukan koneksi terhadap Router Wifi tanpa harus memasukan password, namun di sisi lain terdapat sebuah `vulnerability` atau kerentanan yang mana memungkinkan seseorang dapat melakukan Attacking dengan cara melakukan **Cracking** pada wi-Fi Router tersebut.

Nah jika Pin tersebut dapat dilakukan proses Cracking maka tidak menutup kemungkinan Password yang ada pada Wi-Fi Router tersebut dapat diperoleh. Banyak metode dan tools yang dapat digunakan untuk melakukan proses tersebut.
Kali ini saya akan memberikan sebuah cara dengan menggunakan salah satu Tools yang dapat kalian download dan gunakan, berikut link tools tersebut :

[airgeddon by v1s1t0r1sh3r3](https://github.com/v1s1t0r1sh3r3/airgeddon)

Perlu diingat jika Airgeddon membutuhkan **Essential Tools** dan **Optional Tools** agar dapat dijalankan, untuk proses instalasi Tools kalian dapat membaca dokumentasi yang ada pada Github airgeddon tersebut.

### [](#header-3)Langkah Pertama

Jadi pertama kalian masuk pada folder atau direktori, Tools itu berada. berikut ini adalah lokasi saya menyimpan tools tersebut :

![](https://user-images.githubusercontent.com/62985891/80211827-9a2f6080-8660-11ea-95ef-5d8fd78a2f32.png)

pada folder tersebut terdapat sebuah file `bash` yang dapat dijalakan dengan perintah `./` perlu diingat jika menjalakan file tersebut membutuhkan hak akses `root` sehingga kalian dapat menambahkan `sudo ./namafile` lalu masukan password root kalian.

### [](#header-3)Langkah Kedua

Nah sekarang setelah menjalakan file `bash` tadi, airgeddon akan mengecek mulai dari `root permission` hingga jenis `system` yang kalian gunakan, seperti gambar berikut ini :

![](https://user-images.githubusercontent.com/62985891/80211841-9f8cab00-8660-11ea-93a9-03947d52835c.png)

Kalian tekan `enter` saja buat melanjutkan.

### [](#header-3)Langkah Ketiga

Oke sekarang akan dilakukan pengecekan apakah tools yang dibutuhkan oleh `airgeddon` tersebut tersedia dan dapat digunakan, jika tidak maka proses akan berhenti dan kalian harus melakukan setup terhadap `tools` yang airgeddon butuhkan.
buat kalian yang mengalami `error` terhadap beberapa tools yang dibutuhkan airgeddon dapat melakukan installasi seperti yang ada pada tutorial web berikut :
[Instalasi Airgeddon](https://miloserdov.org/?p=1)

Jika semua nya berjalan normal, kalian akan masuk pada menu untuk memilih Wi-Fi adapter yang akan kalian gunakan, saya menggunakan `wlp2s0`

![](https://user-images.githubusercontent.com/62985891/80211927-c9de6880-8660-11ea-8096-f9965d03a2b2.png)

### [](#header-3)Langkah Keempat

Pada langkah ini kalian harus merubah `mode` dari wi-fi adapter kalian yang asalnya `Mode : Managed` ke `Mode : Monitor`

Kalian tinggal pilih Nomor `2` saja

![](https://user-images.githubusercontent.com/62985891/80211882-b16e4e00-8660-11ea-948f-2d9942508a07.png)

### [](#header-3)Langkah Keempat

Setelah itu kalian tinggal pilih menu nomer `8` untuk melakukan WPS Cracking.

![](https://user-images.githubusercontent.com/62985891/80211919-c64ae180-8660-11ea-8daa-c56529432a1d.png)

Kenapa nomer 8, karena metode yang kita gunakan adalah `Pixie Dust (Reaver)` pastikan mode wireless adapater kalian sudah `Mode : Monitor`

### [](#header-3) Langkah kelima

Kalian harus melakukan explorasi SSID mana yang akan menjadi target

![](https://user-images.githubusercontent.com/62985891/80211851-a4515f00-8660-11ea-83f1-434909ef92b9.png)

Pilih nomer `4`

### [](#header-3) Langkah keenam

Setalah itu maka akan muncul windows dari daftar SSID yang menggunakan WPS PIN, perlu diingat Daftar SSID ini hanya terdeteksi yang menggunakan WPS PIN saja, sehingga yang tidak terkonfigurasi PIN nya tidak akan terdeteksi, mungkin kalian bisa menggunakan metode lain untuk melakukan cracking tersebut.

![](https://user-images.githubusercontent.com/62985891/80212627-09f21b00-8662-11ea-84b9-78cf988b70f0.png)

### [](#header-3) Langkah ketujuh

Close windows tersebut dan akan menuju menu berikut ini :

![](https://user-images.githubusercontent.com/62985891/80212621-0199e000-8662-11ea-97dd-d47c7473a3fc.png)

Disini saya coba untuk melakukan WPS Pin Cracking pada SSID `QIONS FAMS`.

### [](#header-3) Langkah kedelapan

Setelah menentukan SSID target, kalian akan kembali ke menu berikut ini :

![](https://user-images.githubusercontent.com/62985891/80211909-c1862d80-8660-11ea-98f3-b1ca6100c230.png)

langkah selanjutnya kalian hanya perlu melakukan cracking dengan memilih `nomer 8` dan konfigurasi penyimpanan file.txt hasil capture pin tersebut

![](https://user-images.githubusercontent.com/62985891/80211913-c3e88780-8660-11ea-976a-5e68de751d74.png)

Dan akan muncul sebuah windows terminal proses Cracking Pin tersebut.

![](https://user-images.githubusercontent.com/62985891/80212605-f9da3b80-8661-11ea-878d-420819169366.png)

**See What We Get** some stuff yang mana kalian pengin kan. 

Jadi sesimple itu sih gais, kesimpulannya gini 

```conclusion
WPS PIN menawarkan kemudahan bagi kita pengguna Wi-Fi.
Terlebih jika itu Wi-Fi pribadi yang mana tanpa harus melakukan proses input sebuah password.
kalian dapat dengan mudah terkoneksi.
Namun disisi lain terdapat sebuah celah yang mana dapat menjadi sebuah masalah. 
Yaitu Password kita dapat diketahui oleh orang lain.
```
***Makasih yang udah baca*** Mohon digunakan dengan bijak yak, dan jadikan media pembelajaran.
