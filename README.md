# Klavaro-Indonesia-Translation
Program berlatih mengetik

For **English** version of this README.md see _README.en.md_

Klavaro adalah aplikasi untuk berlatih ketrampilan mengetik dan ini adalah versi bahasa Indonesianya. Saat ini hanya baru ada versi Linux dan terbukti bisa berjalan di Ubuntu versi 18.04 (_Bionic Beaver_)
Sebelum menginstalasi program ini periksa apakah library-library berikut sudah ada di komputer anda dengan menjalankan perintah berikut di terminal
```
$ sudo apt update
$ sudo apt install libgtk-3-dev
$ sudo apt install libcurl4-gnutls-dev
$ sudo apt install intltool
$ sudo apt install libtool
```

Sementara untuk GtkDatabox (https://gtkdatabox.sourceforge.io/):
```
$ sudo apt install libgtkdatabox-dev
$ sudo ldconfig
```

Unduh source file ke home directory anda dengan menggunakan perintah ini:
`$ git clone https://github.com/Blantranderozari/Klavaro-Indonesia-Translation.git`

Untuk menginstalasi program .
```
$ ./configure
$ make
$ sudo make install
$ export LANGUAGE=id
$ klavaro
```

Dan tampilan ini yang akan muncul:

![image](https://user-images.githubusercontent.com/35718731/135736567-0ef08ea5-b1fc-4d03-af9d-cfb898a69c15.png)
