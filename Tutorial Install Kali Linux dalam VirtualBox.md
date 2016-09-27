# Instalasi Kali Linux 

Cara instal Kali Linux dalam VirtualBox adalah sebagai berikut:

Siapkan berkas instalasi VirtualBox dan disc Kali Linux ( ex. dalam bentuk *.iso) yang sesuai dengan platform komputer/laptop.

1. Instalasi VirtualBox

Pada kesempatan kali ini, digunakan sistem operasi Windows 64 bit. Klik kanan pada berkas aplikasi VirtualBox yang telah disiapkan dan pilih “Run as administrator”.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-02.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Selanjutnya muncul layar selamat datang dalam proses instalasi VirtualBox. Silakan baca dan Klik tombol Next untuk melanjutkan.
    
[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-03.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Di bagian ini, kita dapat menentukan fitur apa yang akan dipasang atau tidak, mulai dari dukungan terhadap USB, jaringan sampai script Phyton untuk VirtualBox API. Di bagian ini kita juga dapat menentukan lokasi folder VirtualBox akan dipasang. Biarkan seluruh pengaturan folder dan fitur aplikasi yang akan dipasang pada posisi bawaan sekarang. Klik tombol Next untuk melanjutkan.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-04.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Di bagian ini, kita dapat menentukan apakah cara akses VirtualBox secara cepat (shortcut) akan dipasang pada bagian desktop dan Quick Launch Bar. Aktifkan Register file associations agar file dengan ekstensi terkait VirtualBox dikenal oleh sistem operasi. Klik tombol Next untuk melanjutkan.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-05.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Selanjutnya muncul pemberitahuan, bahwa dalam proses instalasi, kartu jaringan yang ada pada komputer akan dinonaktifkan untuk sementara waktu. Klik tombol Yes untuk melanjutkan proses instalasi.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-06.png?w=300&h=205)](https://nodesource.com/products/nsolid)

VirtualBox sudah memiliki informasi yang diperlukan dan siap untuk dipasang. Klik tombol Install untuk memulai proses instalasi VirtualBox.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-07.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Layar selanjutnya menginformasikan bahwa proses instalasi VirtualBox sedang berlangsung.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-08.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Setelah seluruh proses selesai, akan muncul layar pemberitahuan berikut ini. Klik tombol Finish untuk keluar dari proses instalasi dan menjalankan aplikasi VirtualBox.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-09.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Berikut Tampilan aplikasi VirtualBox yang baru dipasang.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-10.png?w=300&h=205)](https://nodesource.com/products/nsolid)

2. Membuat Virtual Mesin Di VirtualBox

Kali ini bagian Membuat Virtual Mesin Di VirtualBox untuk keperluan Kali Linux, diawali dengan meng-klik “New” sehingga tampil layar Create Virtual Machine. Pada kolom pertama, diisi nama, ex. Kali Linux, berikutnya tipe terpilih ke pilihan Linux dan Version ke pilihan, dalam hal ini, Ubuntu (64 bit), bersesuaian dengan berkas disc Kali Linux 64 bit yang telah disiapkan.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-11.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Selanjutnya, tentukan besar Memory yang ingin dialokasikan untuk Kali Linux dalam VirtualBox. Dalam hal ini, dipilih besaran 1024 MB, mengingat laptop yang digunakan mempunyai memori 4 GB dan untuk sistem operasi utama yang digunakan dapat berjalan lancar pada memori 2 GB (Lihat pada Task Manager dari Komputer yang digunakan). Selanjutnya klik “Next”.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-12.png?w=300&h=205)](https://nodesource.com/products/nsolid)

 Gambar dari Task manager dari Sistem yang dipakai

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/memori.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Selanjutnya pilih “Create a virtual hard drive now”, dan klik “Create”.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-13.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Selanjutnya, biarkan pilihan bawaan aplikasi, yaitu “VDI (VirtualBox Disk Image)” dan klik “Next”.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-14.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Selanjutnya, biarkan pilihan default, yaitu “Dynamically allocated’ dan klik “Next”.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-15.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Selanjutnya, beri nama Virtual Drive dan tentukan besarnya, dalam hal ini dialokasikan sebesar 16 GB , dan klik “Create”.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-16.png?w=300&h=205)](https://nodesource.com/products/nsolid)

OK. Mesin Virtual sudah terbentuk. Sudah ada satu komputer virtual yang siap diisi. Lakukan pengaturan pada komputer virtual dengan cara klik “Settings” untuk pengaturan jumlah core prosesor, RAM, Harddisk dan lain sebagainya dari mesin virtual yang baru.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-18.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Pada kesempatan kali ini, hanya dilakukan pengaturan pada bagian storage, untuk pemilihan disc Kali Linux yang telah disiapkan di awal.klik “Storage”. Kemudian klik “Empty” pada “Controller: IDE”.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-19.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Selanjutnya, klik icon DVD pada bagian “Attributes”. Kemudian klik “Choose a virtual CD/DVD disk file”.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-20.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Pilih file ISO Kali Linux yang telah disiapkan dan klik “Open”. Kemudian klik “OK”.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-19.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Selanjutnya klik “Start” pada jendela utama Virtual Box.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-23.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Selanjutnya, tekan “Enter” dengan highlight pada “Live (amd64)” untuk melakukan boot.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-24.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Live CD Kali linux ini dimaksudkan untuk mengetes Mesin Virtual yang telah dibuat, apakah sanggup menjalankan OS Kali Linux. Pengalaman di awal, saat langsung pilih instalasi yang berada di daftar paling bawah dan setelah selesai keseluruhan proses instalasi, Kali Linux gagal booting dan Virtual Box menampilkan peringatan error.Pengaturan saat itu mesin virtual berada pada versi linux 2.6 / 3.x dan besaran kapasitas harddisk pada posisi default: 8 GB.

3. Instalasi Kali Linux

Kali Linux berhasil jalan secara Live.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Setelah berada dalam Graphical Interface Kali Linux dan untuk melanjutkan pemasangan Kali Linux, klik “Applications” > “System Tools” > “Install Kali Linux”.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-01.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Berikut Proses Pemasangan Kali Linux, dimulai dari pemilihan bahasa.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-02.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Berikutnya pemilihan lokasi.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-04.png?w=300&h=205)](https://nodesource.com/products/nsolid)

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-05.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Dilanjutkan dengan pemilihan jenis bahasa dan keyboard komputer / laptop.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-06.png?w=300&h=205)](https://nodesource.com/products/nsolid)

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-07.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Installer memuat komponen-komponen instalasi.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-08.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Berikut diminta nama server, boleh dikosongkan. Pada kesempatan kali ini, nama server dikosongkan.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-09.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Begitu pula dengan form isian nama domain. Boleh dikosongkan.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-20.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Selanjutnya pada pengaturan sandi, Silakan isi dan atur sandi untuk user Root pada sistem Kali Linux yang dipasang.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-22.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Selanjutnya pemilihan time zone waktu. Dalam hal ini, Waktu Indonesia bagian Barat.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-23.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Selanjutnya, installer Kali Linux memeriksa harddisk tempat pemasangan sistem nanti.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-24.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Biarkan pada posisi pilihan bawaan aplikasi, : “Guided – use entire disk”. Klik “continue”.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-25.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Selanjutnya konfirmasi partisi harddisk yang digunakan. Karena menggunakan seluruh kapasitas harddisk pada Mesin Virtual, cuma ada satu pilihan pada daftar. Klik “continue”.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-26.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Selanjutnya, untuk pengguna pemula, biarkan pada posisi pilihan “All files in one partition (recommended for new users)”. Klik “continue”.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-27.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Selanjutnya, konfirmasi partisi yang telah disiapkan dan penulisan harddisk sesuai informasi pada layar. Klik “continue”.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-28.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Pada konfirmasi penulisan konfigurasi partisi ke harddsik, pilih “Yes”. Klik “continue”.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-29.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Proses pemasangan kali Linux pada Mesin Virtual mulai berjalan. Silakan ditunggu atau ditinggal istirahat sebentar.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-30.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Proses instalasi selesai, sistem mulai booting dan menampilkan jendela password untuk masuk ke sistem. Silakan isi dengan sandi yang dibuat pada saat proses pemasangan sistem.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-31.png?w=300&h=205)](https://nodesource.com/products/nsolid)

Proses selesai dan Kali Linux berhasil terpasang di VirtualBox

