# Klavaro-Indonesia-Translation
Klavaro is a typing tutor application and this is the version for Indonesian language.
For **Indonesian** version of this README.md see _README.id.md_. There is also a more detail instruction in Bahasa Indonesia on [YOUTUBE](https://youtu.be/uUxak2vBh_8)

## Libraries required

Before compile and linking the source code, check whether these libraries are installed on your system.  
```
$ sudo apt update
$ sudo apt install libgtk-3-dev
$ sudo apt install libcurl4-gnutls-dev
$ sudo apt install intltool
$ sudo apt install libtool
```

## Install gtkdatabox library

Meanwhile for libgtkdatabox (https://gtkdatabox.sourceforge.io/), you have to ensure that it is installed with the right version. Klavaro requires at least libgtkdatabox version 1.0.0

First use the following command:

`$ sudo apt-cache policy libgtkdatabox-dev`

and examine the output if libgtkdatabox-dev is installed with version greater or equal to 1.0.0. If this condition is satisfied go directly to Installing Klavaro below.

![image](https://user-images.githubusercontent.com/35718731/136917081-148f2a8b-945e-46b3-be81-8b7bd6638e5c.png)

**Installed : (None)** means that libgtkdatabox-dev is not installed in your system.
**Candidate: 1:0.9.3.1-1** means there is only 1 candidate with version 0.9.3.1-1

Here we have version 0.9.3.1-1 which below the required version. Therefore we need to download it directly from the source. Open your browser and get the source code from. https://sourceforge.net/projects/gtkdatabox/files/latest/download. Extract this file with:

`$ tar xzvf gtkdatabox-1.0.0.tar.gz`

and build the source code using GNU Make as shown below:
```
$ cd gtkdatabox-1.0.0/
$ ./configure
$ make
$ sudo make install
$ sudo ldconfig
```
 

## Installing Klavaro

Clone my repository using this command:

`$ git clone https://github.com/Blantranderozari/Klavaro-Indonesia-Translation.git`

... and go straightly build the source. 
```
$ cd Klavaro-Indonesia-Translation
$ ./configure
$ make
$ sudo make install
$ export LANGUAGE=id
$ klavaro
```


You should see this window poping up:

![image](https://user-images.githubusercontent.com/35718731/135736567-0ef08ea5-b1fc-4d03-af9d-cfb898a69c15.png)



Congratulation you have succeed building and installing Klavaro! Happy Typing...
