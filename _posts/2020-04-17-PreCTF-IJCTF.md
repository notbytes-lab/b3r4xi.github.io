---
title: PreCTF - IJCTF 2020
published: true
categories: CTF
---

Hai...
Nah jadi kemarin ada tuh `event` PreCTF dari salah satu penyelenggaran CTF yang bakal di mulai pada _25-04-2020_ mendatang, nah jika kalian pen daftar juga ini link nya [https://www.ijctf.ml](https://www.ijctf.ml). Nah berhubung preCTF udah beres, saya mau nulis dikit dari beberapa challenge yang udah ke solve. gabanyak sih tapi ya lumayan lah buat bahan bacaan.

# [](#header-3) Dig.zip (MISC)

Judulnya sebenernya bukan dig.zip tapi itu file yang ada dichallenge ini, berhubung ane lupa gak langsung nulis writeup selesai solve, jadi gini dah repot kalo pen nulis. 
jadi langsung aja gimana solve nya, 
nah kan di challenge ini ane dapet file `dig.zip` dari namanya aja udh ngasih tau kalo ini tuh kayak nge _digging_ buat yang ndak tau digging itu macul nyak gais, atau ngegali gitu.

Oh iya ini file zipnya bisa Download [disini nih](https://github.com/linuxjustin/IJCTF/blob/master/Misc/Dig.zip).

Setelah didownload, dan menganalisi dengan perintah **file** pada terminal.
untuk memastikan bahwa file tersebut tidak corrupt dan sesuai dengan formatnya

![1](https://user-images.githubusercontent.com/62985891/79568774-aa839080-80e0-11ea-9b6e-fe4e92a131ac.jpeg)

setelah dicek, langsung saya unzip dengan perintah berikut. `unzip dig.zip`

Dan berikut ini yang dihasilkan dari proses decompress tadi :

![2](https://user-images.githubusercontent.com/62985891/79568526-30eba280-80e0-11ea-8902-474ac1989123.jpeg)

Dari gambar diatas, dapat dilihat bahwa file **flag.txt** tersembunyi pada sub-sub folder yang sangat dalam, makannya kan kata aing juga ini mah kaya macul daksss.
nah buat sampe kesana kalian harus buka satu-satu foldernya atau, dengan :

```python
cd U/p/D/V/E/Z/7/V/G/g/z/X/3/A/w/d/z/N/y/X/z/B/m/Z/l/9/o/M/W/R/k/M/2/5/f/e/j/F/w/X/3/c/x/d/G/h/f/Y/m/F/z/Z/T/Y/0/f/Q
```

Setelah masuk ke folder `Q` yang paling ujung akan terdapat `Flag.txt` kalian tinggal baca aja pake perintah `cat` `flag.txt` dan akan muncul strings berikut 

![4](https://user-images.githubusercontent.com/62985891/79569800-845ef000-80e2-11ea-9a51-8e773685b364.jpeg)

nah udah keliatan kan flagnya, gitu doang udah cape-cape macul ampe dalem cuma dikasih `==%` gajelas :(
eh tapi jangan salah paham dulu, kalo kalian cermat dan paham struktur `base64` yang ditampilkan `flag.txt` adalah sebuah padding dari pada base64 itu, jadi artinya kalian harus ambil masing-masing huruf yang dijadikan nama folder dan sub-folder tadi.

Setelah itu tinggal kalian decode deh dengan perintah berikut :

![5](https://user-images.githubusercontent.com/62985891/79568542-36e18380-80e0-11ea-93e3-80bcdf6a1a6e.jpeg)

nah dapet dah tuh flag buat solve ini soal :)

`IJCTF{Th3_pow3r_0ff_h1dd3n_z1p_w1th_base64}`

udah gitu doang, makasih loh udah baca ampe akhir.

semoga bermanfaat. **BYE!!!**

