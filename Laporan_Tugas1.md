#**Tugas 1**

##**Pendahuluan**

&nbsp;&nbsp; &nbsp; Keamanan jaringan komputer sebagai bagian dari sebuah sistem sangat penting untuk menjaga validitas dan integritas data serta menjamin ketersediaan layanan bagi penggunaannya. Sistem keamanan jaringan komputer harus dilindungi dari segala macam serangan dan usaha-usaha penyusupan atau pemindaian oleh pihak yang tidak berhak.

&nbsp;&nbsp; &nbsp; Salah satu metode pengamanan sistem informasi yang umum diketahui oleh banyak orang adalah *password*. Tanpa disadari *password* mempunyai peranan penting dalam mengamankan informasi-informasi yang sifatnya pribadi. Pada beberapa aplikasi yang berhubungan dengan piranti lunak, seperti HP, kartu ATM, dll., ada juga sistem pengamanannya yang fungsinya mirip dengan *password*; biasa dikenal sebagai Kode PIN. Walaupun hanya terdiri dari angka, namun kegunaannya sama seperti *password*, yaitu untuk mengamankan informasi. Informasi yang disimpan tersebut biasanya sudah berbentuk digital.

&nbsp;&nbsp; &nbsp; Tetapi banyak dari para pengguna *password* yang membuat *password* secara sembarangan tanpa mengetahui kebijakan pengamanan (*password policy*) dan bagaimana membuat *password* yang kuat (*strong password*). Mereka tidak sadar dengan bahayanya para ‘penyerang’ (*attacker*) yang dapat mencuri atau mengacak-acak informasi tersebut menggunakan tehnik - tehnik tertantu.

&nbsp;&nbsp; &nbsp; Untuk itu, kami ingin membuktikan hal tersebut dengan melakukan penetrasi untuk mengetahui *password user* dengan cara melakukan tehnik *brute force* terhadap OS ubuntu server. Dalam hal ini, kami menggunakan *tools - tools* yang sudah ada yaitu THC-Hydra, Ncrack, dan Medusa.

##**Dasar Teori**

&nbsp;&nbsp; &nbsp; Ubuntu server adalah salah satu varian dari distro linux Ubuntu. Ubuntu server adalah ubuntu yang didesain untuk di *install* di server. Perbedaan mendasar, di Ubuntu Server tidak tersedia GUI. Jika anda menggunakan ubuntu server artinya anda harus bekerja dengan perintah perintah di layar hitam ayng sering disebut konsol. Jika anda datang dari windows, maka tampilan ubuntu server seperti DOS. Ubuntu server menyediakan *platform* yang terintegrasi dengan baik yang akan memudahkan anda melakukan *deploy* server dengan fasilitas layanan internet standar: *mail, web*, DNS, *file-serving* hingga manajemen *database*. Sebagai turunan dari distribusi Debian, karakter alami Ubuntu server yang diwariskan dari Debian adalah faktor keamanan (*security*). Ubuntu server tidak membiarkan keberadaan *port* yang terbuka setelah proses instalasi, dan hanya akan memuat *software-software* yang esensial dan dibutuhkan untuk membangun sebuah sistem server yang aman.

&nbsp;&nbsp; &nbsp; Kali Linux adalah distribusi berlandasan distribusi Debian GNU/Linux untuk tujuan forensik digital dan di gunakan untuk pengujian penetrasi, yang dipelihara dan didanai oleh Offensive Security. Kali juga dikembangkan oleh Offensive Security sebagai penerus BackTrack Linux. Kali menyediakan pengguna dengan mudah akses terhadap koleksi yang besar dan komprehensif untuk alat yang berhubungan dengan keamanan, termasuk *port scanner* untuk *password cracker*.

&nbsp;&nbsp; &nbsp; Hydra adalah suatu *tools* yang di gunakan untuk melakukan *bruteforcing* kepada akun tertentu di suatu jaringan atau server, contohnya FTP dan SSH. hydra adalah *tools opensource*, dan sudah bisa di install di segala platform termasuk windows, linux dan mac. *tools* ini memiliki dua versi yaitu, versi GUI dan versi CLI. Tools ini diklaim lebih cepat dibandingkan ncrack dan medusa.

##**Uji Penetrasi 1**

###**-Instalasi Ubuntu Server.**

1. Pastikan VirtualBox telah terinstal di laptop/PC.

2. Buka VirtualBox.

3. Klik Baru, maka nanti akan muncul layar kerja baru. Untuk kotak Nama isikan sesuai dengan yang diinginkan. Untuk kotak Type, pilihlah OS yang akan diinstal nantinya, selanjutnya dikotak Versi, pilihlah versi OS yang ingin diinstal. Setelah semuanya selesai dibuat klik Lanjut. 

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/1.png "")

4. Selanjutnya atur berapa kapasitas memory yang akan digunakan untuk menjalankan proses yang ada di aplikasi ini. Setelah selesai klik Lanjut. 

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/2.PNG "")

5. Selanjutnya adalah membuat harddisk virtual. Klik Buat untuk melanjutkan.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/3.PNG "")

6. Klik Lanjut saja.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/4.PNG "")
  
7. Klik Lanjut.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/5.PNG "")

8. Selanjutnya tentukan berapa kapasitas harddisk virtual yang akan digunakan untuk melakukan penginstalan nantinya. Klik Buat.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/6.PNG "")
  
9. Klik Mulai pada menu pilihan di VirtualBox untuk memulai penginstalan Ubuntu Server.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/11.png "")

10. Klik Baik.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/12.png "")

11. Pada halaman Selamat Datang di First Run Wizard! Klik Next.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/13.png "")

12. Klik tanda folder untuk memasukan iso Ubuntu Server yang baru diunduh di folder Unduhan, lalu klik Next.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/14.png "")

13. Pada halaman Risalah Klik Mulai.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/15.png "")

14. Klik Baik.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/16.png "")

15. Pilih English (pilih bahasa yang diinginkan), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/17.png "")

16. Pilih Install Ubuntu Server, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/18.png "")

17. Klik Baik.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/19.png "")

18. Pilih English, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/20.png "")

19. Pilih United States, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/21.png "")

20. Detect keyboard layout? Pilih No, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/22.png "")

21. Country of origin for the keyboard: Pilih English (US), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/23.png "")

22. Keyboard layout: Pilih English (US), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/24.png "")

23. Ketik nama di kolom Hostname sesuai yang diinginkan dan pilih (Continue) lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/25.png "")

24. Is this time zone correct? Pilih (yes), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/26.png "")

25. Partitioning method: Pilih manual, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/27.png "")

26. Pilih SCSI3 (0,0,0) (sda) – 8.6 GB ATA VBOX HARDDISK, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/28.png "")

27. Create new empty partition table on this device? Pilih (Yes), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/29.png "")

28. Pilih pri/log 8.6 GB FREE SPACE, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/30.png "")

29. How to use this free space: pilih Create a new partition, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/31.png "")

30. New partition size: ketik 5.6 GB dan (Continue), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/32.png "")

31. Type for the new partition: Pilih Primary, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/33.png "")

32. Location for the new partition: Pilih Beginning, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/34.png "")

33. Partition settings: Pilih Done setting up the partition, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/35.png "")

34. Pilih pri/log 3.0 GB   FREE SPACE, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/36.png "")

35. How to use this free space: Pilih Create a new partiion, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/37.png "")

36. Ketik 1.0 GB pada kolom New partition size, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/38.png "")

37. Type for the new partition: Pilih Logical, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/39.png "")

38. Location for the new partition: Pilih Beginning, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/40.png "")

39. Pilih swap area, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/41.png "")

40. Partition setting: Pilih Done setting up the partition, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/42.png "")

41. Pilih pri/log 2.0 GB FREE SPACE, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/43.png "")

42. How to use this free space: Pilih Create a new partition, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/44.png "")

43. New partition size: Pilih 2.0 GB, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/45.png "")

44. Type for the partition: Pilih Logical, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/46.png "")

45. Partition settings: Pilih Done setting up the partition, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/47.png "")

46. Pilih Finish partitioning and write changes to disk, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/48.png "")

47. Write the changes to disks? Pilih (Yes), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/49.png "")

48. Ketik nama pengguna yang diinginkan pada kolom Full name for the new user, pilih (Continue), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/50.png "")

49. Ketik nama akun pada kolom User for your account, lalu pilih (Continue), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/51.png "")

50. Ketik password pada kolom Choose a password for the new user, pilih (continue), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/52.png "")

51. Ketik ulang password pada kolom RE-enter password to verify, pilih (Continue), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/53.png "")

52. Use weak password? Pilih (Yes), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/54.png "")

53. Encrypt your home directory? Pilih (Yes), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/55.png "")

54. Pada kolom HTTP proxy information (blank for none): kosongkan, pilih (continue), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/56.png "")

55. How do you want to manage upgrades on this system? Pilih No automatic updates, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/57.png "")

56. Choose software to install: Pilih Manual package selection, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/58.png "")

57. Install the GRUB boot loader to the master boot record? Pilih (Yes), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/59.png "")

58. Pilih (Continue), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/60.png "")


###**- Instalasi Kali Linux**

Cara instal Kali Linux dalam VirtualBox adalah sebagai berikut:

Siapkan berkas instalasi VirtualBox dan disc Kali Linux ( ex. dalam bentuk *.iso) yang sesuai dengan platform komputer/laptop.

1. Instalasi VirtualBox

Pada kesempatan kali ini, digunakan sistem operasi Windows 64 bit. Klik kanan pada berkas aplikasi VirtualBox yang telah disiapkan dan pilih “Run as administrator”.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-02.png)](https://nodesource.com/products/nsolid)

Selanjutnya muncul layar selamat datang dalam proses instalasi VirtualBox. Silakan baca dan Klik tombol Next untuk melanjutkan.
    
[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-03.png)](https://nodesource.com/products/nsolid)

Di bagian ini, kita dapat menentukan fitur apa yang akan dipasang atau tidak, mulai dari dukungan terhadap USB, jaringan sampai script Phyton untuk VirtualBox API. Di bagian ini kita juga dapat menentukan lokasi folder VirtualBox akan dipasang. Biarkan seluruh pengaturan folder dan fitur aplikasi yang akan dipasang pada posisi bawaan sekarang. Klik tombol Next untuk melanjutkan.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-04.png)](https://nodesource.com/products/nsolid)

Di bagian ini, kita dapat menentukan apakah cara akses VirtualBox secara cepat (shortcut) akan dipasang pada bagian desktop dan Quick Launch Bar. Aktifkan Register file associations agar file dengan ekstensi terkait VirtualBox dikenal oleh sistem operasi. Klik tombol Next untuk melanjutkan.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-05.png)](https://nodesource.com/products/nsolid)

Selanjutnya muncul pemberitahuan, bahwa dalam proses instalasi, kartu jaringan yang ada pada komputer akan dinonaktifkan untuk sementara waktu. Klik tombol Yes untuk melanjutkan proses instalasi.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-06.png)](https://nodesource.com/products/nsolid)

VirtualBox sudah memiliki informasi yang diperlukan dan siap untuk dipasang. Klik tombol Install untuk memulai proses instalasi VirtualBox.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-07.png)](https://nodesource.com/products/nsolid)

Layar selanjutnya menginformasikan bahwa proses instalasi VirtualBox sedang berlangsung.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-08.png)](https://nodesource.com/products/nsolid)

Setelah seluruh proses selesai, akan muncul layar pemberitahuan berikut ini. Klik tombol Finish untuk keluar dari proses instalasi dan menjalankan aplikasi VirtualBox.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-09.png)](https://nodesource.com/products/nsolid)

Berikut Tampilan aplikasi VirtualBox yang baru dipasang.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-10.png)](https://nodesource.com/products/nsolid)

2. Membuat Virtual Mesin Di VirtualBox

Kali ini bagian Membuat Virtual Mesin Di VirtualBox untuk keperluan Kali Linux, diawali dengan meng-klik “New” sehingga tampil layar Create Virtual Machine. Pada kolom pertama, diisi nama, ex. Kali Linux, berikutnya tipe terpilih ke pilihan Linux dan Version ke pilihan, dalam hal ini, Ubuntu (64 bit), bersesuaian dengan berkas disc Kali Linux 64 bit yang telah disiapkan.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-11.png)](https://nodesource.com/products/nsolid)

Selanjutnya, tentukan besar Memory yang ingin dialokasikan untuk Kali Linux dalam VirtualBox. Dalam hal ini, dipilih besaran 1024 MB, mengingat laptop yang digunakan mempunyai memori 4 GB dan untuk sistem operasi utama yang digunakan dapat berjalan lancar pada memori 2 GB (Lihat pada Task Manager dari Komputer yang digunakan). Selanjutnya klik “Next”.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-12.png)](https://nodesource.com/products/nsolid)

 Gambar dari Task manager dari Sistem yang dipakai

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/memori.png)](https://nodesource.com/products/nsolid)

Selanjutnya pilih “Create a virtual hard drive now”, dan klik “Create”.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-13.png)](https://nodesource.com/products/nsolid)

Selanjutnya, biarkan pilihan bawaan aplikasi, yaitu “VDI (VirtualBox Disk Image)” dan klik “Next”.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-14.png)](https://nodesource.com/products/nsolid)

Selanjutnya, biarkan pilihan default, yaitu “Dynamically allocated’ dan klik “Next”.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-15.png)](https://nodesource.com/products/nsolid)

Selanjutnya, beri nama Virtual Drive dan tentukan besarnya, dalam hal ini dialokasikan sebesar 16 GB , dan klik “Create”.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-16.png)](https://nodesource.com/products/nsolid)

OK. Mesin Virtual sudah terbentuk. Sudah ada satu komputer virtual yang siap diisi. Lakukan pengaturan pada komputer virtual dengan cara klik “Settings” untuk pengaturan jumlah core prosesor, RAM, Harddisk dan lain sebagainya dari mesin virtual yang baru.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-18.png)](https://nodesource.com/products/nsolid)

Pada kesempatan kali ini, hanya dilakukan pengaturan pada bagian storage, untuk pemilihan disc Kali Linux yang telah disiapkan di awal.klik “Storage”. Kemudian klik “Empty” pada “Controller: IDE”.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-19.png)](https://nodesource.com/products/nsolid)

Selanjutnya, klik icon DVD pada bagian “Attributes”. Kemudian klik “Choose a virtual CD/DVD disk file”.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-20.png)](https://nodesource.com/products/nsolid)

Pilih file ISO Kali Linux yang telah disiapkan dan klik “Open”. Kemudian klik “OK”.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-19.png)](https://nodesource.com/products/nsolid)

Selanjutnya klik “Start” pada jendela utama Virtual Box.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-23.png)](https://nodesource.com/products/nsolid)

Selanjutnya, tekan “Enter” dengan highlight pada “Live (amd64)” untuk melakukan boot.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/gb-24.png)](https://nodesource.com/products/nsolid)

Live CD Kali linux ini dimaksudkan untuk mengetes Mesin Virtual yang telah dibuat, apakah sanggup menjalankan OS Kali Linux. Pengalaman di awal, saat langsung pilih instalasi yang berada di daftar paling bawah dan setelah selesai keseluruhan proses instalasi, Kali Linux gagal booting dan Virtual Box menampilkan peringatan error.Pengaturan saat itu mesin virtual berada pada versi linux 2.6 / 3.x dan besaran kapasitas harddisk pada posisi default: 8 GB.

3. Instalasi Kali Linux

Kali Linux berhasil jalan secara Live.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux.png)](https://nodesource.com/products/nsolid)

Setelah berada dalam Graphical Interface Kali Linux dan untuk melanjutkan pemasangan Kali Linux, klik “Applications” > “System Tools” > “Install Kali Linux”.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-01.png)](https://nodesource.com/products/nsolid)

Berikut Proses Pemasangan Kali Linux, dimulai dari pemilihan bahasa.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-02.png)](https://nodesource.com/products/nsolid)

Berikutnya pemilihan lokasi.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-04.png)](https://nodesource.com/products/nsolid)

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-05.png)](https://nodesource.com/products/nsolid)

Dilanjutkan dengan pemilihan jenis bahasa dan keyboard komputer / laptop.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-06.png)](https://nodesource.com/products/nsolid)

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-07.png)](https://nodesource.com/products/nsolid)

Installer memuat komponen-komponen instalasi.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-08.png)](https://nodesource.com/products/nsolid)

Berikut diminta nama server, boleh dikosongkan. Pada kesempatan kali ini, nama server dikosongkan.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-09.png)](https://nodesource.com/products/nsolid)

Begitu pula dengan form isian nama domain. Boleh dikosongkan.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-20.png)](https://nodesource.com/products/nsolid)

Selanjutnya pada pengaturan sandi, Silakan isi dan atur sandi untuk user Root pada sistem Kali Linux yang dipasang.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-22.png)](https://nodesource.com/products/nsolid)

Selanjutnya pemilihan time zone waktu. Dalam hal ini, Waktu Indonesia bagian Barat.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-23.png)](https://nodesource.com/products/nsolid)

Selanjutnya, installer Kali Linux memeriksa harddisk tempat pemasangan sistem nanti.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-24.png)](https://nodesource.com/products/nsolid)

Biarkan pada posisi pilihan bawaan aplikasi, : “Guided – use entire disk”. Klik “continue”.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-25.png)](https://nodesource.com/products/nsolid)

Selanjutnya konfirmasi partisi harddisk yang digunakan. Karena menggunakan seluruh kapasitas harddisk pada Mesin Virtual, cuma ada satu pilihan pada daftar. Klik “continue”.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-26.png)](https://nodesource.com/products/nsolid)

Selanjutnya, untuk pengguna pemula, biarkan pada posisi pilihan “All files in one partition (recommended for new users)”. Klik “continue”.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-27.png)](https://nodesource.com/products/nsolid)

Selanjutnya, konfirmasi partisi yang telah disiapkan dan penulisan harddisk sesuai informasi pada layar. Klik “continue”.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-28.png)](https://nodesource.com/products/nsolid)

Pada konfirmasi penulisan konfigurasi partisi ke harddsik, pilih “Yes”. Klik “continue”.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-29.png)](https://nodesource.com/products/nsolid)

Proses pemasangan kali Linux pada Mesin Virtual mulai berjalan. Silakan ditunggu atau ditinggal istirahat sebentar.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-30.png)](https://nodesource.com/products/nsolid)

Proses instalasi selesai, sistem mulai booting dan menampilkan jendela password untuk masuk ke sistem. Silakan isi dengan sandi yang dibuat pada saat proses pemasangan sistem.

[![N|Solid](https://dhaniguci.files.wordpress.com/2014/09/kali-linux-31.png)](https://nodesource.com/products/nsolid)

Proses selesai dan Kali Linux berhasil terpasang di VirtualBox




###**- Instalasi SSH Server**

1. Login user.
   
   ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/login%20ubuntu%20server.PNG "Login Ubuntu Server")

2. Ketikkan "`sudo apt-get install openssh-server`".
3. Masukkan password.
4. Ketik "y" dan tekan enter.
   
   ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/install%20openssh-server.PNG "Install openssh-server")
   
   
###**- Langkah Uji Penetrasi dengan Hydra**

1. Buat file dictionary untuk uji penetrasi.
2. Pada terminal ketikkan "`nano pass.txt`".
3. Isikan kemungkinan-kemungkinan password.
4. Simpan file.
   
   ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/dictionary%20password.PNG "Dictionary Password")
   
5. Untuk memulai uji penetrasi pada terminal ketikkan "`hydra -l ubuntu -P pass.txt 192.168.56.102 ssh`". Dengan asumsi kita sudah mengetahui nama user (ubuntu) dan ip addressnya "192.168.56.192".

####**-- Hasil Uji Penetrasi dengan Hydra**

   ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/hasil%20hydra.PNG "Hasil Hydra")


###**- Langkah Uji Penetrasi dengan Ncrack**

1. Buat file dictionary untuk uji penetrasi.
2. Pada terminal ketikkan "`nano pass.txt`".
3. Isikan kemungkinan-kemungkinan password.
4. Simpan file.
   
   ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/dictionary%20password.PNG "Dictionary Password")
   
5. Untuk memulai uji penetrasi pada terminal ketikkan "`ncrack -v 192.168.56.102 --user ubuntu -P pass.txt -p ssh`". Dengan asumsi kita sudah mengetahui nama user (ubuntu) dan ip addressnya "192.168.56.192".

####**-- Hasil Uji Penetrasi dengan Ncrack**

   ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/hasil%20ncrack.PNG "Hasil Ncrack")
   

###**- Langkah Uji Penetrasi dengan Medusa**

1. Buat file dictionary untuk uji penetrasi.
2. Pada terminal ketikkan "`nano pass.txt`".
3. Isikan kemungkinan-kemungkinan password.
4. Simpan file.
   
   ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/dictionary%20password.PNG "Dictionary Password")
   
5. Untuk memulai uji penetrasi pada terminal ketikkan "`medusa -u ubuntu -P pass.txt -h 192.168.56.102 -M ssh`". Dengan asumsi kita sudah mengetahui nama user (ubuntu) dan ip addressnya "192.168.56.192".

####**-- Hasil Uji Penetrasi dengan Medusa**

   ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/hasil%20medusa.PNG "Hasil Medusa")


##**Uji Penetrasi 2**

###**- Langkah Konfigurasi fail2ban**

1. Install fail2ban. Pada terminal server ketikkan "`sudo apt-get install fail2ban`"
2. Konfigurasi fail2ban. Pada "bantime" berisi nilai 600 yang artinya klien akan ter-banned ketika gagal autentikasi dengan benar selama 600 detik atau 10 menit. Pada "findtime" berisi nilai 600 dan "maxretry" berisi nilai 3 yang artinya fail2ban akan mem-ban klien yang gagal login 3 kali selama selang waktu 10 menit.

   ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/config%20fail2ban%20ban.PNG "Config fail2ban")

3. Konfigurasi fail2ban. Pada "action" berisi nilai "$(action_)s"_ yang artinya fail2ban akan mengatur firewall untuk me-reject traffic dari host yang menyerang selama waktu ban berjalan.

   ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/fail2ban%20setting%201.PNG "Config fail2ban")
   
4. Konfigurasi fail2ban. Pada bagian "[ssh]" ganti nilai "port" menjadi "22222" agar fail2ban melindungi port 22222 karena ssh akan diset ke port 22222.

   ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/config%20fail2ban%20port.PNG "Config fail2ban")
   
5. Restart fail2ban. Pada terminal server ketikkan "`sudo service fail2ban restart'".

   ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/restart%20fail2ban.PNG "Restart fail2ban")
   

###**- Langkah Konfigurasi SSH server**

1. Buka file config ssh server. Pada terminal server ketikkan "`sudo nano /etc/ssh/sshd_config`".
2. Edit config Port agar ssh listen port 22222. Cari config Port lalu ubah nilainya menjadi 22222.
3. Simpan file.

   ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/config%20port%20ssh.PNG "Config Port SSH")

4. Restart SSH server. Pada terminal server ketikkan "`sudo service ssh restart`".

   ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/service%20ssh%20restart.PNG "Restart SSH server")


###**- Langkah Uji Penetrasi dengan Hydra**

1. Buat file dictionary untuk uji penetrasi.
2. Pada terminal ketikkan "`nano pass.txt`".
3. Isikan kemungkinan-kemungkinan password.
4. Simpan file.
   
   ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/dictionary%20password.PNG "Dictionary Password")
   
5. Untuk memulai uji penetrasi pada terminal ketikkan "`hydra -l ubuntu -P pass.txt 192.168.56.102 ssh`". Dengan asumsi kita sudah mengetahui nama user (ubuntu) dan ip addressnya "192.168.56.192".

6. Untuk memulai uji penetrasi pada port 22222 pada terminal ketikkan "`hydra -l ubuntu -P pass.txt 192.168.56.102 -s 22222 ssh`". Dengan asumsi kita sudah mengetahui nama user (ubuntu) dan ip addressnya "192.168.56.192".

####**-- Hasil Uji Penetrasi dengan Hydra**

   ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/hydra%20fail2ban.PNG "Hasil Hydra dengan fail2ban")
   
   ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/hydra%20fail2ban%20port%20baru.PNG "Hasil Hydra dengan fail2ban port 22222")


###**- Langkah Uji Penetrasi dengan Ncrack**

1. Buat file dictionary untuk uji penetrasi.
2. Pada terminal ketikkan "`nano pass.txt`".
3. Isikan kemungkinan-kemungkinan password.
4. Simpan file.
   
   ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/dictionary%20password.PNG "Dictionary Password")
   
5. Untuk memulai uji penetrasi pada terminal ketikkan "`ncrack -v 192.168.56.102 --user ubuntu -P pass.txt -p ssh`". Dengan asumsi kita sudah mengetahui nama user (ubuntu) dan ip addressnya "192.168.56.192".

6. Untuk memulai uji penetrasi pada port 22222 pada terminal ketikkan "`ncrack -v 192.168.56.102 --user ubuntu -P pass.txt -p ssh:22222`". Dengan asumsi kita sudah mengetahui nama user (ubuntu) dan ip addressnya "192.168.56.192".

####**-- Hasil Uji Penetrasi dengan Ncrack**

   ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/ncrack%20fail2ban.PNG "Hasil Ncrack dengan fail2ban")
   
   ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/ncrack%20fail2ban%20port%20baru.PNG "Hasil Ncrack dengan fail2ban port 22222")


###**- Langkah Uji Penetrasi dengan Medusa**

1. Buat file dictionary untuk uji penetrasi.
2. Pada terminal ketikkan "`nano pass.txt`".
3. Isikan kemungkinan-kemungkinan password.
4. Simpan file.
   
   ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/dictionary%20password.PNG "Dictionary Password")

5. Untuk memulai uji penetrasi pada terminal ketikkan "`medusa -u ubuntu -P pass.txt -h 192.168.56.102 -n 22222 -M ssh`". Dengan asumsi kita sudah mengetahui nama user (ubuntu) dan ip addressnya "192.168.56.192".

####**-- Hasil Uji Penetrasi dengan Medusa**
   
   ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/medusa%20fail2ban%20port%20baru.PNG "Hasil medusa dengan fail2ban port 22222")
   

##**- Kesimpulan dan Saran**

###**-- Kesimpulan**

- openSSH-server dapat dihack secara brute force dan banyak tools yang dapat digunakan.
- fail2ban dapat menangkal serangan brute force.

###**-- Saran**

- openSSH-server dapat dikonfigurasi portnya agar lebih aman karena kecil kemungkinan hacker mengetahui port yang digunakan untuk SSH.
- fail2ban dapat dikonfigurasi maxretry dengan nilai yang kecil untuk menangkal serangan brute force.
