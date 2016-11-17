# Tugas 4

## Pendahuluan

&nbsp; Belakangan ini tengah marak hacking pada web. dimana hacker menyerang sistem web dengan cara mencari celah yang bisa ditembus. oleh karena itu untuk mengamankan sistem kita, honeypot salah satu tools yang dapat kita digunakan. sistem kerja honeypot sendiri dengan cara menjebak sang hacker dan kita bisa memantau gerak-gerik maupun apa yang diinginkan hacker. laporan ini berisi bagaimana cara instalasi dan penggunaan dari honeypot beserta hasil uji nya.

## Dasar Teori

&nbsp; 1. Honeypot adalah sebuah sistem palsu yang dirancang untuk menjebak penyerang, seolah-olah yang diserang adalah sistem yang asli

&nbsp; 2. Glastopf adalah *low interaction web application* honeypot yang memiliki kemampuan untuk mengemulasikan tibuan *vulnerabilities* untuk mengumpulkan data dari serangan yang ditujukan ke aplikasi web. Prinsip dasar dari kerja Glastopf adalah membalas serangan dengan memberikan jawaban sesuai dengan tujuan penyerang menyerang aplikasi web. Glastopf menyediakan *vulnerability* emulator yang membuat Glastopf dapat membalas semua serangan tanpa harus memodifikasi template aplikasi web.

&nbsp; 3. ZAP Proxy adalah tools untuk pengujian penetrasi yang mudah digunakan dalam menemukan celah pada aplikasi web. Hal ini dirancang untuk digunakan oleh orang - orang dengan berbagai pengalaman keamanan dan dengan demikian sangat ideal untuk pada pengembang dan pentester yang baru untuk melakukan kegiatan pentest. ZAP menyediakan scanner otomatis serta satu set alat yang memungkinkan untuk menemukan kerentanan keamanan website secara manual.

## Instalasi Glastopf

&nbsp; 1. Install dependencies
```
sudo apt-get update
sudo apt-get install python2.7 python-openssl python-gevent libevent-dev python2.7-dev build-essential make
sudo apt-get install python-chardet python-requests python-sqlalchemy python-lxml
sudo apt-get install python-beautifulsoup mongodb python-pip python-dev python-setuptools
sudo apt-get install g++ git php5 php5-dev liblapack-dev gfortran libmysqlclient-dev
sudo apt-get install libxml2-dev libxslt-dev
sudo pip install --upgrade distribute
```

&nbsp; 2. Install dan konfigurasi PHP sandbox
```
cd /opt
sudo git clone git://github.com/mushorg/BFR.git
cd BFR
sudo phpize
sudo ./configure --enable-bfr
sudo make && sudo make install
```

&nbsp; 3. Buka php.ini dan tambahkan bfr.so pada "/etc/php/7.0/cli/php.ini" (Ubuntu 16.04 LTS)
```
zend_extension = /usr/lib/php/20151012/bfr.so
```

&nbsp; 4. Install glastopf
```
sudo pip install glastopf
```
Atau install manual dengan cara :
```
cd /opt
sudo git clone https://github.com/mushorg/glastopf.git
cd glastopf
sudo python setup.py install
```

&nbsp; 5. Konfigurasi honeypot
```
cd /opt
sudo mkdir myhoneypot
cd myhoneypot
sudo glastopf-runner
```

&nbsp; 6. Cek apakah honeypot berjalan atau tidak dengan cara mengetikkan perintah :
```
sudo glastopf-runner
```
Jika honeypot berhasil jalan, maka akan menampilkan hasil seperti dibawah ini:

![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/glastopf%20running.PNG "")


## Uji Penetrasi Web Honeypot Glastopf

&nbsp; 1. Jalankan glastopf. Masuk ke folder honeypot lalu jalankan glastopf
```
cd /opt
sudo mkdir honeeyphot
cd honeeyphot
sudo glastopf-runner
```
&nbsp; Hasil pada terminal bila glastopf berjalan
![alt text](https://raw.githubusercontent.com/HerdiantoNaufal/PKSJ_Kel6/master/Gambar/glastopf%20running.PNG "")

&nbsp; 2. Jalankan ZAP Proxy dari Kali Linux. Lalu masukkan ip server honeypot pada form yang ada.
![alt text](https://raw.githubusercontent.com/HerdiantoNaufal/PKSJ_Kel6/master/Gambar/zap%20attack.PNG "")

&nbsp; Setelah itu ZAP Proxy akan meluncurkan "Spider" untuk memeriksa direktori pada server honeypot. Setelah itu ZAP Proxy akan mencoba menyerang server honepot. Hasil uji serang penetrasi:
![alt text](https://raw.githubusercontent.com/HerdiantoNaufal/PKSJ_Kel6/master/Gambar/zap%20hasil.png "")
&nbsp; Dapat dilihat bahwa server memiliki 10 jenis celah keamanan.

&nbsp; Pada server, dapat dilihat log dari honeypot.
![alt text](https://raw.githubusercontent.com/HerdiantoNaufal/PKSJ_Kel6/master/Gambar/log%20glastopf.PNG "")
&nbsp; Dapat dilihat bahwa server honeypot banyak sekali diakses oleh satu alamat.

### Hasil Penetrasi

* Cross Site Scripting
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/cross%20glastopf.PNG "")
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/cross%20zap.PNG "")

* Path Traversal
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/path%20glastopf.PNG "")
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/path%20zap.PNG "")

* SQL Injection-Oracle
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/oracle%20glastopf.PNG "")
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/oracle%20zap.PNG "")

* SQL Injection
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/sql%20glastopf.PNG "")
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/sql%20zap.PNG "")


## Kesimpulan dan Saran

### Kesimpulan
* Tools-tools honeypot dapat digunakan mendeteksi serangan.
* Tools-tools penetrasi tidak dapat membedakan mana yang server honeypot atau bukan.

### Saran
* Untuk memancing hacker dapat menggunakan honeypot.
* Tools-tools penetrasi dapat digunakan untuk menguji keamanan sebuah sistem.
