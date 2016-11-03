# Tugas 3
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

#### -Survey and Poll
&nbsp;&nbsp; &nbsp;&nbsp;&nbsp; &nbsp;Survey and Poll merupakan plugin yang menyediakan berbagai macam pilihan untuk mendapatkan informasi apapun dan menampilkannya dengan mengesankan, grafik animasi. Semua jajak pendapat anonim, tidak perlu login untuk mengisi, karena plugin menggunakan cookies untuk menghindari duplikasi.


## Instalasi

### -Instalasi dan Menggunakan Cuckoo Malware Analisis Sandbox

##### Pengantar

&nbsp; &nbsp; &nbsp; &nbsp; Dalam artikel ini kita akan mengeksplorasi Cuckoo Sandbox, kerangka analisis malware otomatis. Saat memasang Cuckoo untuk pertama kalinya, kita dapat dengan cepat menentukan bahwa itu tidak semua yang mudah untuk menginstal Cuckoo. Oleh karena itu, untuk meringankan rasa sakit kita sudah dijelaskan proses cara menginstal Cuckoo pada sistem operasi Debian bersama-sama akan semua dependensi.

##### Instalasi Cuckoo
&nbsp; &nbsp; &nbsp; &nbsp; Untuk menginstal Cuckoo, pertama kita harus menginstal semua dependensi, yang dijelaskan pada situs Cuckoo resmi. Pada dasarnya kita perlu menjalankan perintah berikut untuk menginstal dependensi yang paling dasar yang dibutuhkan untuk menjalankan Cuckoo.

~~~~
# apt-get install python python-sqlalchemy python-bson python-dpkt python-jinja2 python-magic python-pymongo python-gridfs python-libvirt python-bottle python-pefile bridge-utils python-pyrex
# pip install jinja2 pymongo bottle pefile cybox maec django chardet
~~~~
Untuk mengendus paket dari kawat, kita harus menginstal tcpdump dan memastikan Cuckoo mampu menggunakannya tanpa memerlukan akses root.

~~~~
# apt-get install tcpdump
# setcap cap_net_raw,cap_net_admin=eip /usr/sbin/tcpdump
# getcap /usr/sbin/tcpdump
~~~~
Kita mungkin juga ingin menginstal Yara / Pydeep:
~~~~

# wget http://sourceforge.net/projects/ssdeep/files/ssdeep-2.12/ssdeep-2.12.tar.gz
# tar xvzf ssdeep-2.12.tar.gz
# cd ssdeep-2.12/
# ./configure && make && make install
# git clone https://github.com/kbandla/pydeep
# cd pydeep
# python setup.py build
# python setup.py install

# wget https://yara-project.googlecode.com/files/yara-1.7.tar.gz
# tar xvzf yara-1.7.tar.gz
# cd yara-1.7/
# ./configure && make && make install
# echo "/usr/local/lib" >> /etc/ld.so.conf
# ldconfig

# wget https://yara-project.googlecode.com/files/yara-python-1.7.tar.gz
# tar xvzf yara-python-1.7.tar.gz
# cd yara-python-1.7/
# python setup.py build
# python setup.py install
~~~~
Kita juga dapat menginstal Volatilitas, yang membutuhkan sebuah perpustakaan DiStorm disassembler tambahan. Perhatikan bahwa Cuckoo versi terbaru 1.2 (pada saat tulisan ini) tidak memerlukan DiStorm perpustakaan, tetapi menggunakan Capstone disassembler perpustakaan. Namun demikian Volatilitas masih menggunakan DiStorm, itulah sebabnya mengapa kita perlu menginstalnya jika kita ingin menggunakan Volatilitas.
~~~~
# Wget https://distorm.googlecode.com/files/distorm3.zip
# Unzip distorm3.zip
# Cd distorm3 /
# Python setup.py membangun
# Python setup.py menginstal

# Wget https://volatility.googlecode.com/files/volatility-2.3.1.tar.gz
# Tar xvzf volatilitas-2.3.1.tar.g
# Cd volatilitas-2.3.1 /
# Python setup.py membangun
# Python setup.py menginstal
~~~~
Akhirnya, saatnya untuk menginstal Cuckoo.
~~~~
# adduser cuckoo
# usermod -G vboxusers cuckoo
# git clone git://github.com/cuckoobox/cuckoo.git
~~~~

##### Instalasi VirtualBox
&nbsp; &nbsp; &nbsp; &nbsp; Setup VirtualBox, pertama kita harus menginstal header Linux yang sesuai dan GCC / G ++ compiler, yang dapat dilakukan dengan menjalankan perintah di bawah ini. Kita tidak harus menginstal VirtualBox dengan hanya menjalankan "apt-get install virtualbox", karena sering menyebabkan pemasangan VirtualBox usang dengan modul kernel yang tidak dapat dimuat. Untuk mencegah masalah dengan VirtualBox, pilihan terbaik adalah dengan menginstal header kernel dan kemudian secara manual men-download versi VirtualBox terbaru dan menginstalnya.
~~~~
# apt-get install build-essential linux-headers-`uname -r` libvpx1
~~~~
Next, we have to download the appropriate version of VirtualBox manually from official VirtualBox website.
~~~~
# wget http://download.virtualbox.org/virtualbox/4.3.18/virtualbox-4.3_4.3.18-96516~Debian~wheezy_amd64.deb
# dpkg -i virtualbox-4.3_4.3.18-96516~Debian~wheezy_amd64.deb
~~~~
Sejak Cuckoo mengharapkan untuk menggunakan alamat IP 192.168.56.1, yang termasuk VirtualBox, kita harus membuat antarmuka jaringan. Jika antarmuka jaringan tidak hadir ketika memulai Cuckoo, program akan mencetak kesalahan kritis tentang menjadi tidak dapat mengikat 192.168.56.1:2042 dan mengakhiri. Untuk membuat antarmuka jaringan yang tepat, kita dapat menjalankan perintah berikut.
~~~~
# VBoxManage hostonlyif buat
# Ip link set vboxnet0 up
# Ip addr add 192.168.56.1/24 dev vboxnet0
~~~~
Selanjutnya kita bisa memulai Cuckoo biasanya dengan menjalankan skrip cuckoo.py seperti yang ditunjukkan di bawah ini. Perhatikan bahwa script mulai mendengarkan pada IP 192.168.56.1 dan port 2042.
    ![alt text](https://www.proteansec.com/images/2015/02/cuckoo1.png "")
Jika kita ingin antarmuka vboxnet0 yang akan dibuat pada saat startup sistem kita harus menjalankan VBoxManage selama booting sistem, yang secara otomatis akan membuat vboxnet * interface. Pada dasarnya, kita harus menambahkan "daftar VBoxManage VMS" perintah ke /etc/rc.local, yang akan secara otomatis dijalankan pada setiap sistem startup. Tambahkan baris berikut ke file rc.local sebelum "exit 0" line.

~~~~
daftar VBoxManage VMS 2> & 1 >> / dev / null
~~~~
##### Membuat Mesin Virtual
&nbsp; &nbsp; &nbsp; &nbsp; Ketika kami datang sejauh ini, saatnya untuk membuat mesin virtual pada host yang sama di mana Cuckoo diinstal. Ini diperlukan untuk Cuckoo untuk dapat memulai / menghentikan / melanjutkan mesin virtual setelah sampel malware telah dieksekusi. Karena kita sedang memasang Cuckoo dalam lingkungan server, yang tidak memiliki antarmuka GUI, yang terbaik jika kita mengkonfigurasi dan menginstal sistem operasi dari baris perintah. Kami akan memasang sistem operasi Windows XP SP3 ke dalam mesin virtual yang akan digunakan oleh sandbox Cuckoo.

&nbsp; &nbsp; &nbsp; &nbsp;Pertama kita harus membuat XML baru mesin virtual file definisi dengan menggunakan perintah createvm. Perintah membutuhkan argumen --name diperlukan menetapkan nama mesin virtual. Opsi --register digunakan untuk mendaftarkan XML dibuat dari VM dengan instalasi VirtualBox.
    ![alt text](https://www.proteansec.com/images/2015/02/cuckoo2.png "")
    
&nbsp; &nbsp; &nbsp; &nbsp; Setelah itu tambahkan 256MB RAM untuk mesin virtual, menonaktifkan ACPI, menandai DVD sebagai pilihan booting pertama, mendefinisikan host-satunya antarmuka jaringan dan menyatakan sistem operasi untuk Windows XP.
    ![alt text](https://www.proteansec.com/images/2015/02/cuckoo3.png "")
&nbsp; &nbsp; &nbsp; &nbsp;Selanjutnya, kita harus membuat penyimpanan VDI, yang akan diserang untuk mesin virtual yang dibuat sebelumnya. Penyimpanan 10GB disimpan di / srv / VMs / direktori dapat dibuat dengan menggunakan perintah createhd.
    ![alt text](https://www.proteansec.com/images/2015/02/cuckoo4.png "")
&nbsp; &nbsp; &nbsp; &nbsp;Untuk benar-benar memasang gambar VDI untuk mesin virtual, perintah berikut harus dijalankan.
    ![alt text](https://www.proteansec.com/images/2015/02/cuckoo5.png "")
&nbsp; &nbsp; &nbsp; &nbsp; Kita mungkin juga perlu instalasi iso Windows untuk mesin virtual, sehingga kita akan dapat menginstal sistem operasi.
    ![alt text](https://www.proteansec.com/images/2015/02/cuckoo6.png "")
&nbsp; &nbsp; &nbsp; &nbsp; Setelah iso tersebut telah ditambahkan, kita dapat memulai mesin virtual dengan menggunakan perintah startvm.
    ![alt text](https://www.proteansec.com/images/2015/02/cuckoo7.png "")
&nbsp; &nbsp; &nbsp; &nbsp; Pada titik ini, VirtualBox harus mendengarkan koneksi RDP masuk pada port 3389. Jika itu tidak terjadi, kita mungkin lupa untuk menginstal VirtualBox Ekstensi Pack, yang dapat diinstal dengan perintah extpack disajikan di bawah ini. Perhatikan bahwa Oracle Ekstensi Pack diperlukan untuk diinstal pada host agar VRDP untuk bekerja.
~~~~
# Wget http://download.virtualbox.org/virtualbox/4.3.18/Oracle_VM_VirtualBox_Extension_Pack-4.3.18-96516.vbox-extpack
# VBoxManage extpack menginstal Oracle_VM_VirtualBox_Extension_Pack-4.3.18-96516.vbox-extpack
~~~~
&nbsp; &nbsp; &nbsp; &nbsp; Setelah restart mesin virtual dengan VboxHeadless, kita dapat mengamati komentar tambahan membiarkan kita tahu bahwa VirtualBox sekarang mendengarkan pada port 3389 untuk koneksi RDP masuk.
![alt text](https://www.proteansec.com/images/2015/02/cuckoo8.png "")

&nbsp; &nbsp; &nbsp; &nbsp; Kita dapat terhubung ke server host pada port 3389 dengan rdesktop RDP klien setelah yang kita akan disajikan dengan prosedur instalasi seperti yang terlihat di bawah ini.
![alt text](https://www.proteansec.com/images/2015/02/cuckoo9.png "")
&nbsp; &nbsp; &nbsp; &nbsp; Kita harus menginstal sistem operasi biasanya dengan mengikuti semua langkah, yang merupakan langkah yang normal diperlukan ketika menginstal sistem operasi Windows. Ketika sistem operasi Windows XP diinstal, seharusnya terlihat seperti disajikan di bawah ini.
![alt text](https://www.proteansec.com/images/2015/02/cuckoo10.png "")
&nbsp; &nbsp; &nbsp; &nbsp; Sekarang adalah waktu untuk menginstal agen Cuckoo python dalam mesin virtual. Karena kita telah host-only networking diaktifkan, kita tidak dapat terhubung ke internet dalam mesin virtual dan download paket yang kita butuhkan. Kami sementara dapat menambahkan kartu antarmuka jaringan NAT sekunder dan download semua paket yang dibutuhkan.
![alt text](https://www.proteansec.com/images/2015/02/cuckoo11.png "")

&nbsp; &nbsp; &nbsp; &nbsp; Setelah menambahkan antarmuka jaringan sekunder, kita akan memiliki akses ke internet. Sekarang kita harus mengkonfigurasi mesin virtual dengan tepat.

1. Instal Python: kita harus mengunjungi http://python.org/download/ dan men-download Python, yang merupakan komponen wajib ketika ingin menggunakan Cuckoo tamu analyzer. Selain itu, kami juga dapat menginstal perpustakaan PIL Python digunakan untuk mengambil screenshot dari desktop Windows selama analisis.

2. Disable Auto Update: di Control Panel, kita bisa klik pada Automatic Updates dan menonaktifkannya tidak mengganggu analisis malware.

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![alt text](https://www.proteansec.com/images/2015/02/cuckoo12.png "")

3. Nonaktifkan Windows Firewall: di Control Panel, kita bisa klik pada Windows Firewall dan menonaktifkannya tidak mengganggu analisis malware.

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![alt text](https://www.proteansec.com/images/2015/02/cuckoo13.png "")

4. Komponen Software tambahan: tergantung pada jenis malware kita akan menganalisis, kami juga mungkin menginstal komponen perangkat lunak lain ke dalam mesin virtual, seperti Adobe Reader, Microsoft Office, dll

5. Instalasi Agen: Cuckoo memiliki agen yang berjalan dalam mesin virtual tamu, dan menangani komunikasi dan transfer data antara tamu dan tuan rumah. Untuk memulai agen, kita perlu menyalin agen / agent.py untuk tamu VM dan menjalankannya, yang akan mulai server XMLRPC mendengarkan koneksi masuk pada port 8000.

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![alt text](https://www.proteansec.com/images/2015/02/cuckoo14.png "")

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Karena kita ingin memulai agent.py secara otomatis pada startup, kita dapat menambahkan &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; "HKLMSOFTWAREMicrosoftWindowsCurrentVersionRunAgent" kunci registri dengan nilai  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; "C: agent.py".

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![alt text](https://www.proteansec.com/images/2015/02/cuckoo15.png "")

6. Menghapus NIC: ketika kita sudah download dan diinstal segala sesuatu yang diperlukan oleh mesin virtual, kita harus menghapus antarmuka jaringan NAT kami sebelumnya telah menambahkan. Pada dasarnya kita harus poweroff mesin virtual, remote NIC sekunder dan restart VM, yang dapat dilakukan dengan menggunakan perintah disajikan di bawah ini.

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![alt text](https://www.proteansec.com/images/2015/02/cuckoo16.png  "")

7. Mengambil Snapshot: jika kita restart tamu VM pada titik ini, VM otomatis akan memanggil script agent.py untuk mulai mendengarkan pada port 8080. Sejak persyaratan yang telah puas, kita dapat mengambil snapshot dari mesin virtual, yang akan menyelamatkan negara dari mesin virtual. Setelah itu kita dapat menutupnya dan mengembalikannya lagi. Dengan menggunakan snapshot kita bisa menyelamatkan keadaan sistem sebelum menginfeksi dengan sampel malware berbahaya. Setelah analisis dilakukan, kita hanya bisa mengembalikan perubahan dengan mengembalikan dari snapshot.

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![alt text](https://www.proteansec.com/images/2015/02/cuckoo17.png  "")

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Mesin virtual sekarang siap untuk digunakan oleh Cuckoo Sandbox untuk menganalisa sampel malware. Pada bagian ini artikel kita hanya mengkonfigurasi mesin virtual tanpa melihat Cuckoo Sandbox. Oleh karena itu, penting bahwa kita mengkonfigurasi Cuckoo tepat dalam rangka untuk itu untuk dapat menggunakan mesin virtual yang dikonfigurasi.

##### Konfigurasi Cuckoo
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; File konfigurasi conf / virtualbox.conf berisi pengaturan untuk VirtualBox virtualisasi backend Cuckoo akan menggunakan. Gambar di bawah menyajikan semua opsi konfigurasi, di mana komentar dan baris kosong telah dihapus. Modus menentukan modus VirtualBox di mana kita ingin menjalankan mesin virtual: pada dasarnya kita perlu memilih antara gui, SDL atau tanpa kepala; ketika menginstal pada sistem remote tanpa X server kita harus menggunakan modus tanpa kepala. Variabel path menentukan path mutlak untuk program VBoxManage, sedangkan mesin direktif mendefinisikan daftar dipisahkan koma mesin virtual yang tersedia untuk digunakan. Karena kita telah menginstal hanya "WindowsXPSP3" mesin virtual yang adalah satu-satunya yang terdaftar. Setelah itu, masing-masing mesin virtual memiliki itu bagian konfigurasi sendiri disajikan sebagai "[WindowsXPSP3]", yang berisi variabel konfigurasi yang berbeda. label berisi nama mesin virtual seperti yang ditentukan dalam konfigurasi VirtualBox. Platform ini mendefinisikan sistem operasi dari mesin virtual, yang dapat jendela, darwin atau linux. ip mendefinisikan alamat IP dari mesin virtual, yang harus dicapai oleh tuan rumah, jika analisis akan gagal.

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![alt text](https://www.proteansec.com/images/2015/02/cuckoo18.png  "")

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Pada titik ini kita juga harus memverifikasi apakah tuan rumah memiliki akses ke mesin virtual tamu. Pertama kita dapat menjalankan ipconfig di cmd.exe untuk memverifikasi apakah mesin virtual memiliki alamat IP yang benar 192.168.56.101 sebagaimana ditentukan dalam file konfigurasi virtualbox.conf.

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![alt text](https://www.proteansec.com/images/2015/02/cuckoo19.png  "")

Dari tuan rumah kita harus terhubung ke IP 192.168.56.101 pada port 8000 di mana agent.py mendengarkan untuk koneksi masuk. Jika koneksi berhasil, itu berarti tuan rumah berhasil dapat berkomunikasi dengan mesin virtual tamu dengan menggunakan Agen Cuckoo. Pada gambar di bawah ini kita dapat melihat bahwa sambungan bekerja, tetapi server merespon dengan pesan kesalahan, yang normal, karena tidak berbicara protokol HTTP. Yang penting adalah kenyataan bahwa komunikasi bekerja, yang dengan jelas menyatakan bahwa host dapat menggunakan mesin virtual untuk analisis.

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![alt text](https://www.proteansec.com/images/2015/02/cuckoo20.png  "")

Sekarang adalah saat yang tepat untuk me-restart cuckoo.py untuk melihat apakah mesin virtual telah berhasil terdeteksi. Pada gambar di bawah, kita dapat melihat bahwa manajer virtualbox mesin virtual telah perlu berhasil digunakan untuk memuat 1 mesin virtual dan Cuckoo menunggu tugas analisis.

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![alt text](https://www.proteansec.com/images/2015/02/cuckoo21.png  "")

Selain itu, Cuckoo memiliki file-file konfigurasi di conf / direktori, yang disajikan dan dijelaskan dalam tabel di bawah.

Masalah yang sering terjadi ketika menggunakan Cuckoo dengan VirtualBox disajikan di bawah ini, yang menyatakan bahwa analisis mesin virtual tidak dapat mengakses resultserver IP. Masalahnya adalah "[resultserver] ip" direktif di cuckoo.conf, yang harus menentukan alamat IP dari antarmuka host terhubung ke tamu.

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![alt text](https://www.proteansec.com/images/2015/02/cuckoo22.png  "")

Untuk mengatasi masalah ini, kita perlu memastikan mesin virtual tamu dapat mengakses alamat IP tertentu pada port dikonfigurasi. Contoh berhasil menghubungkan ke http://192.168.56.1:2042/ dapat dilihat pada gambar di bawah, di mana sambungan didirikan, tetapi tidak ada data yang diterima.

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![alt text](https://www.proteansec.com/images/2015/02/cuckoo23.png  "")

Hal ini membuktikan bahwa mesin virtual dapat mengakses hasil Server. Dalam kasus VirtualBox, kita harus memastikan antarmuka jaringan yang digunakan oleh mesin virtual tamu terserah sebelum memulai Cuckoo, jika kesalahan tersebut akan ditampilkan di stdout. Untuk memastikan antarmuka, kita dapat secara manual memulai dan menghentikan mesin virtual sebelum menjalankan Cuckoo.

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![alt text](https://www.proteansec.com/images/2015/02/cuckoo24.png  "")

#### Menganalisis Sampel Malware
Sekarang akan menjadi saat yang tepat untuk menyerahkan sampel malware ke Cuckoo untuk analisis. Ada beberapa cara sampel malware dapat disampaikan kepada Cuckoo untuk analisis dan disajikan di bawah ini.

##### Membuat Contoh Malware yang Berbahaya 
Mari kita pertama membuat sampel berbahaya dengan msfpayload untuk menganalisis. Sampel berbahaya dapat dihasilkan dengan perintah di bawah ini, yang menghasilkan executable biner meterpreter.exe siap untuk dijalankan pada sistem operasi Winows.

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![alt text](https://www.proteansec.com/images/2015/02/cuckoo25.png  "")

Kami juga harus membuat script meter.rc yang secara otomatis akan memulai handler meterpreter untuk mendengarkan koneksi meterpreter masuk. script harus dipanggil dengan "msfconsole r meter.rc" perintah, yang akan memulai pendengar.df

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![alt text](https://www.proteansec.com/images/2015/02/cuckoo26.png  "")

Kita juga harus memulai program meterpreter.exe dari sistem operasi Windows untuk mengkonfirmasi bahwa itu bekerja seperti yang diharapkan dan dapat terhubung kembali ke pawang. Setelah kami memastikan program ini bekerja saatnya untuk mengirimkannya ke Cuckoo untuk analisis.

##### Menggunakan Command Line Interface
Perintah di bawah ini yang pertama kali menciptakan direktori baru untuk menahan malware sampel / srv / malware /, setelah itu malware meterpreter.exe dipindahkan ke direktori tersebut. Akhirnya submit.py disebut dengan berbagai parameter untuk menganalisis sampel malware pada platform Windows pada mesin virtual WindowsXPSP3.

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![alt text](https://www.proteansec.com/images/2015/02/cuckoo27.png  "")

Setiap pilihan konfigurasi util submit.py dapat dilihat di bawah ini dan disajikan untuk kelengkapan.

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![alt text](https://www.proteansec.com/images/2015/02/cuckoo28.png  "")

##### Menggunakan Web Interface
Untuk memulai antarmuka web, kita harus menjalankan util / web.py utilitas, yang akan mulai mendengarkan pada port 8080.

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![alt text](https://www.proteansec.com/images/2015/02/cuckoo29.png  "")

Untuk memulai antarmuka web, semua yang perlu kita lakukan adalah menjalankan web.py, tapi kami opsional dapat membuatnya mengikat ke port sewenang-wenang dengan menggunakan argumen --port. Setelah itu, kita dapat terhubung ke port 8080 dengan web browser, yang akan menampilkan antarmuka Cuckoo web seperti yang ditunjukkan di bawah ini. Kita bisa memilih file meterpreter.exe dan mengirimkannya untuk analisis dengan cara yang sama seperti yang kita lakukan dengan script submit.py.

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![alt text](https://www.proteansec.com/images/2015/02/cuckoo30.png  "")

Setelah analisis selesai, kita bisa melihat hasilnya di antarmuka web. Salah satu yang paling detail yang paling menarik adalah "Detail File" bagian dari laporan yang disajikan di bawah, di mana kita bisa melihat nama file, ukuran file dan banyak hal lain yang berguna, seperti apakah sampel meterpreter terdeteksi oleh Yara atau PEiD.

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![alt text](https://www.proteansec.com/images/2015/02/cuckoo31.png  "")

Atau, kita harus lebih menggunakan Apache untuk server halaman web Cuckoo, yang bisa kita lakukan dengan menciptakan / etc / apache2 / sites-enabled / Cuckoo dan menggunakan perintah konfigurasi berikut. The WSGIScriptAlias ​​peta URL ke lokasi filesystem dan menandai target sebagai script WSGI: setiap kali kita meminta http: // analyzemalware / di web browser kita, server akan menjalankan aplikasi WSGI didefinisikan dalam naskah wsgi.py. WSGIDaemonProcess menentukan proses daemon distrint untuk aplikasi, yang dapat dijalankan di bawah usernams berbeda Apache. Sisa dari pilihan di VirtualHost direktif harus jelas.

~~~~
<VirtualHost *: 443>
ServerAdmin admin@company.com
ServerName analyzemalware
WSGIDaemonProcess web user = cuckoo kelompok = proses cuckoo = 1 thread = 5
WSGIScriptAlias ​​/ /srv/cuckoo/web/web/wsgi.py
<Directory / srv / cuckoo / web / web />
AllowOverride Semua
Order menyangkal, memungkinkan
Izinkan dari semua
</ Directory>
Alias ​​/ static / srv / cuckoo / web / statis
<Directory / srv / cuckoo / web / statis>
AllowOverride Semua
Order menyangkal, memungkinkan
Izinkan dari semua
</ Directory>
ErrorLog /var/log/cuckoo/web-error.log
CustomLog /var/log/cuckoo/web-access.log dikombinasikan
loglevel memperingatkan
ServerSignature Off

# SSL
SSLEngine di
SSLCertificateFile /etc/ssl/certs/ssl-cert-snakeoil.pem
SSLCertificateKeyFile /etc/ssl/private/ssl-cert-snakeoil.key
</ VirtualHost>
Ketika restart web server Apache dan mengunjungi alamat web Cuckoo sebagaimana ditentukan dalam file konfigurasi, antarmuka web Cuckoo akan ditampilkan.
~~~~

##### Menjalankan Cuckoo sebagai Pengguna normal
Setelah kami telah dikonfigurasi dan diuji segala sesuatu, kita harus menjalankan Cuckoo sebagai pengguna Cuckoo biasa tanpa akses root: kita tidak boleh mengeksekusi malware sebagai root, karena malware entah bagaimana bisa keluar dari lingkungan virtualisasi dan mengeksekusi kode di bawah software virtualisasi pengguna menjalankan . Pertama kita harus mengubah mesin virtual yang sebelumnya dibuat untuk Cuckoo pengguna direktori home / home / kukuk / dan mendaftarkannya dengan pengguna cuckoo. Kami juga harus menjalankan perintah registervm dengan VBoxManage, yang akan memberitahu VirtualBox tentang mesin virtual yang dibuat sebelumnya. Kita harus menjalankan perintah disajikan di bawah ini:

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![alt text](https://www.proteansec.com/images/2015/02/cuckoo32.png "")

Setelah itu kita dapat mengeksekusi ./cuckoo.py biasanya seperti yang ditunjukkan pada gambar di bawah, yang akan dapat mengimpor mesin virtual yang dibuat sebelumnya tanpa masalah.

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![alt text](https://www.proteansec.com/images/2015/02/cuckoo33.png "")

Kami juga dapat memverifikasi bahwa Cuckoo benar-benar berjalan di bawah nama pengguna kukuk, yang ditunjukkan di bawah ini.

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![alt text](https://www.proteansec.com/images/2015/02/cuckoo34.png "")

##### Paket Analisis Cuckoo
Cuckoo berisi paket analisis beberapa, yang memandu analisa Cuckoo ketika melakukan analisis.

Paket analisis pada dasarnya hanya modul yang memberitahu Cuckoo bagaimana file upload perlu diuji. Untuk file executable, exe.py tampak seperti disajikan di bawah, di mana argumen parameter diambil dari permintaan dan ditambahkan ke nama program.

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![alt text](https://www.proteansec.com/images/2015/02/cuckoo35.png "")

Dari potongan kode di atas, kita dapat melihat bahwa fungsi start () pada dasarnya memanggil fungsi mengeksekusi (), yang merupakan bagian dari kelas Paket didefinisikan dalam file ./analyzer/windows/lib/common/abstracts.py Python.

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![alt text](https://www.proteansec.com/images/2015/02/cuckoo36.png "")

Kita bisa melihat di fungsi self.options.get panggilan untuk menentukan argumen itu menerima. Argumen gratis digunakan untuk mengaktifkan log perilaku, argumen argumen yang digunakan untuk menentukan argumen baris perintah untuk diteruskan ke sampel malware. procmemdump yang memungkinkan dump memori dari proses dimonitor secara aktif, sedangkan dll menentukan nama DLL opsional yang akan disuntikkan ke dalam proses bukannya cuckoomon.dll.

Untuk menggunakan paket tertentu, kita harus memilih ketika mengirimkan sampel malware baru untuk analisis.

##### Menganalisis Cuckoo ini DLL Injection
Cuckoo menyuntikkan DLL perpustakaan cuckoomon.dll ke dalam proses dengan menggunakan inject () fungsi didefinisikan dalam analyzer / jendela / lib / api / process.py.

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![alt text](https://www.proteansec.com/images/2015/02/cuckoo37.png "")

Cuckoo kemudian akan mencoba untuk menyuntikkan DLL ke dalam proses dengan menggunakan fungsi-fungsi berikut: VirtualAllocEx, WriteProcessMemory, CreateEventA dan CreateRemoteThread.

VirtualAllocEx
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![alt text](https://www.proteansec.com/images/2015/02/cuckoo38.png "")

WriteProcessMemory
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![alt text](https://www.proteansec.com/images/2015/02/cuckoo39.png "")

QueueUserAPC
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![alt text](https://www.proteansec.com/images/2015/02/cuckoo40.png "")

CreateEventA
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![alt text](https://www.proteansec.com/images/2015/02/cuckoo41.png "")

CreateRemoteThread
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![alt text](https://www.proteansec.com/images/2015/02/cuckoo42.png "")


Jika kita melihat kode, kita dapat melihat mereka adalah standar fungsi API Win32 yang dapat digunakan untuk mengalokasikan memori dalam proses lain, menulis DLL ke dalam memori yang dialokasikan dan membuat thread baru dalam proses terpencil yang mengeksekusi DLL disuntikkan. Oleh karena itu, eksekusi kode di dalam sebuah proses remote sewenang-wenang dapat dilakukan dengan hanya memanggil beberapa fungsi dan melewati DLL, yang akan dijalankan.

##### Kesimpulan
Pada artikel ini kita sudah melihat di Cuckoo malware analis sandbox. Kami telah mendekati masalah dari awal dan pertama kali diinstal dan dikonfigurasi Cuckoo dari awal. Lalu kami sudah menyiapkan mesin virtual yang menjalankan Windows XP, yang akan digunakan untuk menjalankan sampel malware.

Karena ada segudang sampel malware yang didistribusikan di Internet setiap hari, penting untuk menganalisis mereka dengan cepat dan efisien dan ini adalah di mana Cuckoo datang. Sejak Cuckoo adalah open-source siapa saja dapat menginstal secara gratis dan yang paling penting berkontribusi fitur baru yang mungkin membuat analisis malware lebih dapat diandalkan.

Saya mendorong Anda untuk mencoba dan menginstal Cuckoo, karena proses ini cukup mudah dan jika ada sesuatu yang tidak jelas jangan lupa untuk komentar di bawah ini.

##### Referensi
[1] Instalasi Cuckoo, http://docs.cuckoosandbox.org/en/latest/installation/.

## Analisis Malware

Kita akan menganalisis 3 malware pdf yang sudah didapatkan dengan cara submit ke alamat localhost:8000. Malware yang akan dianalisis antara lain :
- bad.pdf
- PO.pdf
- Tax invoice - INV 400093889265.pdf

Pilih file yang akan di submit pada alamat localhost:8000

![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/localhost.PNG  "")

Hasil report analisis yang pernah dilakukan


![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/hasil%20report.PNG  "")

#### - Hasil Analisa Malware bad.pdf

Malware ini membuka file dan juga menulis sebuah file seperti gambar dibawah:

![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/file%20bad%20pdf.PNG  "")

Malware ini juga membuka dan mengubah registry seperti gambar dibawah:

![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/registry%20bad%20pdf.PNG  "")

![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/registry2%20bad%20pdf.PNG  "")

Malware ini membuat beberapa direktori seperti gambar dibawah:

![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/direktori%20bad%20pdf.PNG  "")

Malware ini melakukan proses seperti gambar dibawah:

![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/proses%20bad%20pdf.PNG  "")

#### - Hasil Analisa Malware PO.pdf

Malware ini membuka file dan juga menulis sebuah file seperti gambar dibawah:

![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/file%20po%20pdf.PNG  "")

![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/file2%20po%20pdf.PNG  "")

Malware ini hanya membuka registry saja, tidak sampai merubah seperti malware sebelumnya. Gambarnya seperti dibawah ini:

![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/registry%20po%20pdf.PNG  "")

Malware ini melakukan proses seperti gambar dibawah:

![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/proses%20po%20pdf.PNG  "")

#### - Hasil Analisa Malware Tax invoice - INV 400093889265.pdf

Malware ini membuka file dan juga menulis sebuah file seperti gambar dibawah:

![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/file%20tax%20pdf.PNG  "")

![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/file2%20tax%20pdf.PNG  "")

Sama dengan malware PO.pdf, malware ini hanya membuka registry saja, tidak sampai merubah registrinya. Gambarnya seperti dibawah ini:

![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/registry%20tax%20pdf.PNG  "")

Malware ini melakukan proses seperti gambar dibawah:

![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/proses%20tax%20pdf.PNG  "")

## Kesimpulan dan Saran
1. Untuk menghindari serangan malware, sebaiknya kita selalu melakukan update terhadap OS kita maupun software - software yang ada didalamnya. Hal ini dilakukan untuk mencegah serangan malware menyusup ke dalam OS dan software kita.
2. Install Antivirus untuk memproteksi komputer atau laptop kita dari serangan malware. Kita juga harus selalu melakukan update terhadap antivirus secara berkala.
3. Sebaiknya kita lebih berhati - hati saat membuka file dikarenakan saat ini malware sudah semakin beragam jenisnya dan memiliki ekstensi yang bervariasi.
