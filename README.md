# Klavaro-Indonesia-Translation
Program berlatih mengetik

For **English** version of this README.md see _README.en.md_

Klavaro adalah aplikasi untuk berlatih ketrampilan mengetik dan ini adalah versi bahasa Indonesianya. Saat ini hanya baru ada versi Linux dan terbukti bisa berjalan di Ubuntu versi 18.04 (_Bionic Beaver_)

## Instalasi library-library yang diperlukan

Sebelum menginstalasi program ini periksa apakah library-library berikut sudah ada di komputer anda dengan menjalankan perintah berikut di terminal
```
$ sudo apt update
$ sudo apt install libgtk-3-dev
$ sudo apt install libcurl4-gnutls-dev
$ sudo apt install intltool
$ sudo apt install libtool
```

## Instalasi library gtkdatabox

Sementara untuk libgtkdatabox (https://gtkdatabox.sourceforge.io/), anda harus memastikan terlebih dahulu apakah library tersebut sudah terinstal  atau belum dan versinya masing-masing. Perlu dicatat bahwa versi terendah yang diperlukan adalah libgtkdatabox versi 1.0.0
Untuk itu gunakan perintah berikut:

`$ sudo apt-cache policy libgtkdatabox-dev`

dan perhatikan baris berikut

![image](https://user-images.githubusercontent.com/35718731/136917081-148f2a8b-945e-46b3-be81-8b7bd6638e5c.png)

**Installed : (None)** artinya libgtkdatabox-dev belum terinstal di komputer anda

**Candidate: 1:0.9.3.1-1** artinya hanya ada 1 kandidat yang akan diinstal dengan versi 0.9.3.1-1

Karena versi yang akan diinstall adalah 0.9.3.1-1 lebih rendah dari versi yang disyaratkan (1.0.0) maka kita perlu mengkompilasi library gtkdatabox langsung dari _source file_-nya.
Sebaliknya bila versi yang akan diinstall sudah lebih besar atau sama dengan 1.0.0, anda cukup melanjutkan dengan perintah berikut:

```
$ sudo apt install libgtkdatabox-dev
$ sudo ldconfig
```

Perintah-perintah berikut ini berlaku apabila versi yang diinstal < 1.0.0. 

Buka browser (Firefox atau chrome) dan masukan link berikut https://sourceforge.net/projects/gtkdatabox/files/latest/download. Ekstrak file yang baru didownload _gtkdatabox-1.0.0.tar.gz_ dengan perintah berikut

`$ tar xzvf gtkdatabox-1.0.0.tar.gz`

dan instal libgtkdatabox dengan perintah-perintah berikut:
```
$ cd gtkdatabox-1.0.0/
$ ./configure
$ make
$ sudo make install
$ sudo ldconfig
```
 

## Instalasi Klavaro

Unduh source file ke home directory anda dengan menggunakan perintah ini:

`$ git clone https://github.com/Blantranderozari/Klavaro-Indonesia-Translation.git`

Untuk menginstalasi program .
```
$ cd Klavaro-Indonesia-Translation
$ ./configure
$ make
$ sudo make install
$ export LANGUAGE=id
$ klavaro
```


Dan tampilan ini yang akan muncul:

![image](https://user-images.githubusercontent.com/35718731/135736567-0ef08ea5-b1fc-4d03-af9d-cfb898a69c15.png)



Selamat anda telah berhasil menginstall klavaro! Silahkan mulai berlatih mengetik...
