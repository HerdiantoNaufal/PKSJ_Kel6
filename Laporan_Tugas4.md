# Tugas 4

## Pendahuluan

## Dasar Teori

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

&nbsp; 2. Install dan Konfigurasi PHP Sandbox
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

## Uji Penetrasi Web Honeypot Glastopf

## Kesimpulan dan Saran
