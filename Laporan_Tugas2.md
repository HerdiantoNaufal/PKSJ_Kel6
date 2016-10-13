# Tugas 2
## Pendahuluan
&nbsp;&nbsp; &nbsp;&nbsp;&nbsp; &nbsp;Belakangan ini sangat marak sekali kejahatan di dalam dunia maya, salah satunya adalah hacking. Dimana seseorang meretas suatu sistem yang dia kehendaki guna mengambil alih kontrol dalam sistem tersebut. Tentu ini bukanlah suatu kegiatan yang dilegalkan. Maka dari itu sangat penting sekali membangun keamanan dari sistem yang telah ada.

&nbsp;&nbsp; &nbsp;&nbsp;&nbsp; &nbsp;Salah salah satu jenis hacking yaitu SQL Injection. Hacking ini merupakan jenis aksi hacking pada keamanan komputer di mana seorang penyerang bisa mendapatkan akses ke basis data di dalam sistem. Dengan masuknya hacker ke dalam database sistem tersebut maka dia bebas untuk mengutak-atik data pada sistem.

&nbsp;&nbsp; &nbsp;&nbsp;&nbsp; &nbsp;Maka dari itu pada kesempatan kali ini kelompok kami belajar untuk menggunakan SQL Injection dalam meretas suatu sistem yang kali ini kami menggunakan CMS Wordpress. Dengan tujuan jika kita mengetahui celah yang bisa diretas maka kedepan kita bisa mengetahiu bagaimana mengamankan sistem kita jika di hack dengan metode SQL Injection ini.


## Dasar Teori

#### -Ubuntu
&nbsp;&nbsp; &nbsp; &nbsp;&nbsp; &nbsp;Ubuntu merupakan salah satu distribusi Linux yang berbasiskan Debian dan didistribusikan sebagai software bebas. nama Ubuntu berasal dari filosofi dari Afrika Selatan yang berarti “Kemanusiaan kepada sesama”. Ubuntu didesain untuk kepentingan penggunaan personal, namun versi server Ubuntu juga tersedia, dan telah dipakai secara luas.

&nbsp;&nbsp; &nbsp;&nbsp;&nbsp; &nbsp;Proyek Ubuntu resmi disponspori oleh Canonical Ltd. yang merupakan sebuah perusahaan yang dimiliki oleh pengusaha Afrika Selatan Mark Shuttleworth. Tujuan dari distribusi Linux Ubuntu adalah membawa semangat yang terkandung di dalam Filosofi Ubuntu ke dalam dunia perangkat lunak. Ubuntu adalah sistem operasi lengkap berbasis Linux, tersedia secara bebas dan mempunyai dukungan baik yang berasal dari komunitas maupun tenaga ahli profesional.

&nbsp;&nbsp; &nbsp;&nbsp;&nbsp; &nbsp;Selain itu, Ubuntu juga bersifat Open Source.

&nbsp;&nbsp; &nbsp;&nbsp;&nbsp; &nbsp;Open source adalah Kekuatan komunitas seluruh dunia yang sangat ahli terampil yang membangun, berbagi dan meningkatkan perangkat lunak yang sangat terbaru bersama – kemudian membuatnya tersedia untuk semua orang.

#### -Wordpress

&nbsp;&nbsp; &nbsp;&nbsp;&nbsp; &nbsp;WordPress adalah sebuah aplikasi sumber terbuka (open source) yang sangat populer digunakan sebagai mesin blog (blog engine). WordPress dibangun dengan bahasa pemrograman PHP dan basis data (database) MySQL. PHP dan MySQL, keduanya merupakan perangkat lunak sumber terbuka (open source software). Selain sebagai blog, WordPress juga mulai digunakan sebagai sebuah CMS (Content Management System) karena kemampuannya untuk dimodifikasi dan disesuaikan dengan kebutuhan penggunanya. 

&nbsp;&nbsp; &nbsp;&nbsp;&nbsp; &nbsp;WordPress adalah penerus resmi dari b2/cafelog yang dikembangkan oleh Michel Valdrighi. Nama WordPress diusulkan oleh Christine Selleck, teman Matt Mullenweg. WordPress saat ini menjadi platform content management system (CMS) bagi beberapa situs web ternama seperti CNN, Reuters, The New York Times, TechCrunch, dan lainnya.

#### -Plug-in
&nbsp;&nbsp; &nbsp;&nbsp;&nbsp; &nbsp;Plug-in adalah sebuah modul program computer atau alat yang berinteraksi dengan yang lain untuk menambahkan fungsi tambahan yang spesifik, atau mendukung format file atau alat yang spesifik.

&nbsp;&nbsp; &nbsp;&nbsp;&nbsp; &nbsp;WordPress Plugin: adalah sebuah atau seperangkat program aplikasi tambahan yang berisi fungsi script dalam bahasa PHP yang memberikan fitur-fitur atau layanan yang spesifik untuk meningkatkan fungsi dalam penggunaan blog wordpress, yang dapat digabungkan dengan blog menggunakan akses poin dan metode yang disediakan oleh wordpress.

#### -WPScan

&nbsp;&nbsp; &nbsp;&nbsp;&nbsp; &nbsp;WPScan merupakan tools vulnerability scanner untuk CMS Wordpress yang ditulis dengan menggunakan bahasa pemrograman ruby, WPScan mampu mendeteksi kerentanan umum serta daftar semua plugin dan themes yang digunakan oleh sebuah website yang menggunakan CMS Wordpress.

#### -SQLMap
&nbsp;&nbsp; &nbsp;&nbsp;&nbsp; &nbsp;SQLMap adalah tool open source yang di jalankan menggunakan command dan support untuk data base MySQL, Oracle, PostgreSQL, Microsoft SQL Server, Microsoft Access, IBM DB2, SQLite, Firebird, Sybase and SAP MaxDB.

##**Instalasi**

###**-Instalasi Wordpress.**

&nbsp; 1. Install Apache dengan perintah:

> sudo apt-get update

> sudo apt-get install apache2

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/foto/setelah%20install%20apache2.PNG "")

&nbsp; 2. Install Mysql dengan perintah: sudo apt-get install mysql-server php5-mysql

&nbsp; Selama instalasi, anda diminta untuk memilih sebuah password untuk MYSQL “root” user. Ini adalah sebuah akun administrator dalam MySQL.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/foto/install%20mysql.PNG "")
  
&nbsp; Setelah instalasi selesai, kita harus menjalankan beberapa perintah tambahan untuk membuat lingkungan MySQL menjadi aman. Ketik perintah: sudo mysql_install_db

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/foto/mysql_install_db.PNG "")
  
&nbsp; Setelah itu, kita menjalankan sebuah kemanan untuk menghapus beberapa default berbahaya dan mengunci akses ke system database kita. Ketik perintah: sudo mysql_secure_installation

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/foto/mysql_secure_installation.PNG "")
  
  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/foto/mysql_secure_installation_1.PNG "")
  
  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/foto/mysql_secure_installation_2.PNG "")
  
  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/foto/mysql_secure_installation_3.PNG "")
  
&nbsp; Anda kemudian akan ditanya tentang password untuk akun root MySQL. Jika anda setuju dengan password yang sudah anda buat dilangkah sebelumnya, ketik “n” pada command prompt terminal. Tekan “Enter” untuk pertanyaan-pertanyaan berikutnya sebagai default instalasi. Sampai dengan tahap ini anda telah menginstall MySQL.
  
&nbsp; 3. Install php dengan perintah: sudo apt-get install php5 libapache2-mod-php5 php5-mcrypt

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/foto/install%20php5.PNG "")

&nbsp; Kita ingin memodifikasi bahwa Apache melayani file ketika sebuah direktori diminta. Dasarnya, jika sebuah user meminta sebuah direktori dari server, Apache pertamakali akan melihat sebuah file dengan nama  index.html.

&nbsp; Kita ingin web server untuk menggunakan file PHP, sehingga Apache akan melihat pertama kali pada file index.php. Untuk melakukan ini, kita harus membuka file dir.conf pada teks editor, ketik perintah: sudo nano /etc/apache2/mods-enabled/dir.conf

&nbsp; Edit bagian ini:

~~~~
<IfModule mod_dir.c>
    DirectoryIndex index.html index.cgi index.pl index.php index.xhtml index.htm
</IfModule>
~~~~

&nbsp; Menjadi :

~~~~
<IfModule mod_dir.c>
    DirectoryIndex index.php index.html index.cgi index.pl index.xhtml index.htm
</IfModule>
~~~~

&nbsp; Kemudian restart apache dengan perintah: sudo service apache2 restart

&nbsp; 4. Setelah anda meginstall MySql, log into MySQL root dengan perintah: mysql -u root -p

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/foto/bikin%20database.PNG "")

&nbsp; Pertama, buat database WordPress contohnya dengan nama wordpress. Ketikkan perintah: CREATE DATABASE wordpress;

&nbsp; Buat akun dengan nama wordpressuser dan buat password dengan nama  password. Catatan: akun dan password dapat anda pilih terserah anda. Ketikkan perintah: CREATE USER wordpressuser@localhost IDENTIFIED BY 'password';

&nbsp; Untuk memberikan akses pada user ke database yang tadi telah dibuat, ketikkan perintah: GRANT ALL PRIVILEGES ON wordpress.\* TO wordpressuser@localhost;

&nbsp; User telah punya akses ke database. Kita perlu flush privileges sehingga MySQL mengetahui perubahan privileges yang telah kita buat , dengan mengetikkan perintah: FLUSH PRIVILEGES;

&nbsp; kemudian exit mysql: exit;

&nbsp; 5. Download wordpress, ketik perintah: wget http://wordpress.org/latest.tar.gz

&nbsp; Esktraksi file wordpress yang dikompres ke direktori home, ketik perintah: tar xzvf latest.tar.gz

&nbsp; Beberapa package yang perlu diinstall agar wordpress berkerja dengan images, install plugin dan update website dengan login SSH, maka kita ketikkan perintah:

> sudo apt-get update

> sudo apt-get install php5-gd libssh2-php

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/foto/install%20php5-gd.PNG "")

&nbsp; 6. Konfigurasi wordpress, ketik perintah: cd ~/wordpress

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/foto/config%20wp.PNG "")

&nbsp; Kita harus menyalin sample configuration ke default configuration supaya WordPress mengenali file. Ketikkan perintah: cp wp-config-sample.php wp-config.php

&nbsp; Kita ubah default configuration, ketik perintah: sudo nano wp-config.php

&nbsp; Kita harus menemukan settings untuk DB_NAME, DB_USER, and DB_PASSWORD supaya WordPress dapat terhubung dan terotentikasi dengan database yang telah kita buat. Masukkan nilai dari parameters dengan infromasi untuk database yang telah anda buat sebelumnya. Tampilannya harusnya seperti ini:

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/foto/config%20wp-1.PNG "")

&nbsp; 7. Setelah kita konfigurasi WordPress, selanjutnya kita menyalin ke Apache’s Document Root agar pengunjung dapat mengunjungi website kita

&nbsp; Salah satu cara untuk transfer file dari direktori ke direktori dengan perintah rsync

&nbsp; Lokasi dari Apache’s document root di var/www/html.  Kita dapat menyalin direktori Wordpres yang diunpack di langkah sebelumnya ke direktori var/www/html, ketik perintah: sudo rsync -avP ~/wordpress/ /var/www/html/

&nbsp; Kepemilikan grup kita akan berikan ke proses web server dalam hal ini yaitu www-data. Hal ini akan mengijinkan Apache untuk berinteraksi dengan konten seperlunya. Ketik: sudo chown -R demo:www-data *

&nbsp; Kemudian kita akan merubah kepemilikan untuk direktori upload. Buat direktori uploads di dalam direktori wp-content pada dokumen root. Ketik perintah: mkdir /var/www/html/wp-content/uploads

&nbsp; Kita saat ini telah mempunyai sebuah direktori upload file, namun permission masih ketat. Kita harus mengijinkan web server untuk menulis ke dalam direktori. Ketik perintah: sudo chown -R :www-data /var/www/html/wp-content/uploads 

&nbsp; Hal ini akan mengijinkan web server untuk membuat file dan direktori di dalam direktori uploads dan mengijinkan kita untuk upload konten ke server.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/foto/salin%20file%20ke%20document%20root.PNG "")
  
&nbsp; 8. Isi informasi yang ada di site dan akun admin yang ingin anda buat. Ketik selesai, klik install button di bawahnya.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/foto/install%20wordpress%20web.PNG "")
  
&nbsp; WordPress akan konfirmasi instalasi dan meminta anda login ke akun yang telah anda buat

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/foto/install%20wordpress%20web-1.PNG "")