#**Tugas 1**

##**Pendahuluan**

##**Dasar Teori**

&nbsp;&nbsp; &nbsp; Ubuntu server adalah salah satu varian dari distro linux Ubuntu. Ubuntu server adalah ubuntu yang didesain untuk di install di server. Perbedaan mendasar, di Ubuntu Server tidak tersedia GUI. Jika anda menggunakan ubuntu server artinya anda harus bekerja dengan perintah perintah di layar hitam ayng sering disebut konsole. Jika anda datang dari windows, maka tampilan ubuntu server seperti DOS. Ubuntu server menyediakan platform yang terintegrasi dengan baik yang akan memudahkan anda melakukan deploy server dengan fasilitas layanan internet standar: mail, web, DNS, file-serving hingga manajemen database. Sebagai turunan dari distribusi Debian, karakter alami Ubuntu server yang diwariskan dari Debian adalah faktor keamanan (security). Ubuntu server tidak membiarkan keberadaan port yang terbuka setelah proses instalasi, dan hanya akan memuat software-software yang esensial dan dibutuhkan untuk membangun sebuah sistem server yang aman.

&nbsp;&nbsp; &nbsp; Kali Linux adalah distribusi berlandasan distribusi Debian GNU/Linux untuk tujuan forensik digital dan di gunakan untuk pengujian penetrasi, yang dipelihara dan didanai oleh Offensive Security. Kali juga dikembangkan oleh  Offensive Security sebagai penerus BackTrack Linux. Kali menyediakan pengguna dengan mudah akses terhadap koleksi yang besar dan komprehensif untuk alat yang berhubungan dengan keamanan, termasuk port scanner untuk password cracker.

&nbsp;&nbsp; &nbsp; Hydra adalah suatu tools yang di gunakan untuk melakukan bruteforcing kepada akun tertentu di suatu jaringan atau server, contohnya FTP dan SSH. hydra adalah tools opensource, dan sudah bisa di install di segala platform termasuk windows, linux dan mac. tools ini memiliki dua versi yaitu, versi GUI dan versi CLI. Tools ini diklaim lebih cepat dibandingkan ncrack dan medusa.

##**Uji Penetrasi 1**

###**-Instalasi Ubuntu Server.**

1. Pastikan VirtualBox telah terinstal di laptop/PC.

2. Buka VirtualBox.

3. Klik Baru.

   ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/1.png "")

4. Klik Next.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/2.png "")

5. Ketik Ubuntu Server pada kolom Nama, lalu klik Next.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/3.png "")

6. Pilih jumlah memori dasar (RAM) dalam megabytes untuk dialokasikan pada mesin virtual, lalu klik Next.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/4.png "")

7. Start-up Disk: Pilih Create new hard disk, lalu klik Next.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/5.png "")

8. File type (tipe berkas): Pilih VDI (VirtualBox Disk Image), lalu Klik Next.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/6.png "")

9. Stronge details: Pilih Dynamically allocated, lalu Klik Next.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/7.png "")

10. Pilihlah Virtual disk file location and size (lokasi dan ukuran) sesuai keinginan anda, lalu Klik Next.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/8.png "")

11. Pada halaman Risalah Klik Create.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/9.png "")

12. Pada halaman Risalah berikutnya Klik Create.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/10.png "")

13. Klik Mulai pada menu pilihan di VirtualBox untuk memulai penginstalan Ubuntu Server.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/11.png "")

14. Klik Baik.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/12.png "")

15. Pada halaman Selamat Datang di First Run Wizard! Klik Next.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/13.png "")

16. Klik tanda folder untuk memasukan iso Ubuntu Server yang baru diunduh di folder Unduhan, lalu klik Next.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/14.png "")

17. Pada halaman Risalah Klik Mulai.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/15.png "")

18. Klik Baik.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/16.png "")

19. Pilih English (Pilih Bahasa Yang Anda Inginkan), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/17.png "")

20. Pilih Install Ubuntu Server, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/18.png "")

21. Klik Baik.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/19.png "")

22. Pilih English, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/20.png "")

23. Pilih United States, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/21.png "")

24. Detect keyboard layout? Pilih No, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/22.png "")

25. Country of origin for the keyboard: Pilih English (US), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/23.png "")

26. Keyboard layout: Pilih English (US), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/24.png "")

27. Ketik nama di kolom Hostname sesuai keinginan anda dan pilih (Continue) lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/25.png "")

28. Is this time zone correct? Pilih (yes), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/26.png "")

29. Partitioning method: Pilih manual, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/27.png "")

30. Pilih SCSI3 (0,0,0) (sda) – 8.6 GB ATA VBOX HARDDISK, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/28.png "")

31. Create new empty partition table on this device? Pilih (Yes), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/29.png "")

32. Pilih pri/log 8.6 GB FREE SPACE, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/30.png "")

33. How to use this free space: pilih Create a new partition, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/31.png "")

34. New partition size: ketik 5.6 GB dan (Continue), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/32.png "")

35. Type for the new partition: Pilih Primary, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/33.png "")

36. Location for the new partition: Pilih Beginning, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/34.png "")

37. Partition settings: Pilih Done setting up the partition, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/35.png "")

38. Pilih pri/log 3.0 GB   FREE SPACE, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/36.png "")

39. How to use this free space: Pilih Create a new partiion, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/37.png "")

40. Ketik 1.0 GB pada kolom New partition size, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/38.png "")

41. Type for the new partition: Pilih Logical, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/39.png "")

42. Location for the new partition: Pilih Beginning, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/40.png "")

43. Pilih swap area, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/41.png "")

44. Partition setting: Pilih Done setting up the partition, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/42.png "")

45. Pilih pri/log 2.0 GB FREE SPACE, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/43.png "")

46. How to use this free space: Pilih Create a new partition, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/44.png "")

47. New partition size: Pilih 2.0 GB, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/45.png "")

48. Type for the partition: Pilih Logical, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/46.png "")

49. Partition settings: Pilih Done setting up the partition, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/47.png "")

50. Pilih Finish partitioning and write changes to disk, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/48.png "")

51. Write the changes to disks? Pilih (Yes), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/49.png "")

52. Ketik nama pengguna yang anda inginkan pada kolom Full name for the new user, misal: indonesia, pilih (Continue), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/50.png "")

53. Ketik nama dari akun anda pada kolom User for your account, misal: indonesia lalu pilih (Continue), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/51.png "")

54. Ketik password pada kolom Choose a password for the new user, pilih (continue), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/52.png "")

55. Ketik ulang password pada kolom RE-enter password to verify, pilih (Continue), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/53.png "")

56. Use weak password? Pilih (Yes), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/54.png "")

57. Encrypt your home directory? Pilih (Yes), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/55.png "")

58. Pada kolom HTTP proxy information (blank for none): kosongkan, pilih (continue), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/56.png "")

59. How do you want to manage upgrades on this system? Pilih No automatic updates, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/57.png "")

60. Choose software to install: Pilih Manual package selection, lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/58.png "")

61. Install the GRUB boot loader to the master boot record? Pilih (Yes), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/59.png "")

62. Pilih (Continue), lalu enter.

  ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Instalasi%20Ubuntu%20Server/60.png "")

63. Menampilkan GUI / Desktop Ubuntu Server:

$ sudo apt-get update

$ sudo apt-get upgrade

$ sudo apt-get install ubuntu-desktop

$ sudo reboot


###**- Instalasi Kali Linux**




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


##**Uji Penetrasi 2**

###**- Langkah Konfigurasi fail2ban**

1. Install fail2ban. Pada terminal server ketikkan "`sudo apt-get install fail2ban`"
2. Konfigurasi fail2ban. Pada "bantime" berisi nilai 600 yang artinya klien akan ter-banned ketika gagal autentikasi dengan benar selama 600 detik atau 10 menit. Pada "findtime" berisi nilai 600 dan "maxretry" berisi nilai 3 yang artinya fail2ban akan mem-ban klien yang gagal login 3 kali selama selang waktu 10 menit.

   ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/config%20fail2ban%20ban.PNG "Config fail2ban")

3. Konfigurasi fail2ban. Pada "action" berisi nilai "$(action_)s"_ yang artinya fail2ban akan mengatur firewall untuk me-reject traffic dari host yang menyerang selama waktu ban berjalan.

   ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/fail2ban%20setting%201.PNG "Config fail2ban")
   
4. Restart fail2ban. Pada terminal server ketikkan "`sudo service fail2ban restart'".

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

####**-- Hasil Uji Penetrasi dengan Hydra**

   ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/hydra%20fail2ban.PNG "Hasil Hydra dengan fail2ban")


###**- Langkah Uji Penetrasi dengan Ncrack**

1. Buat file dictionary untuk uji penetrasi.
2. Pada terminal ketikkan "`nano pass.txt`".
3. Isikan kemungkinan-kemungkinan password.
4. Simpan file.
   
   ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/dictionary%20password.PNG "Dictionary Password")
   
5. Untuk memulai uji penetrasi pada terminal ketikkan "`ncrack -v 192.168.56.102 --user ubuntu -P pass.txt -p ssh`". Dengan asumsi kita sudah mengetahui nama user (ubuntu) dan ip addressnya "192.168.56.192".

####**-- Hasil Uji Penetrasi dengan Ncrack**

   ![alt text](https://github.com/HerdiantoNaufal/PKSJ_Kel6/blob/master/Gambar/hasil%20ncrack.PNG "Hasil Ncrack dengan fail2ban")


##**- Kesimpulan dan Saran**

###**-- Kesimpulan**

- openSSH-server dapat dihack secara brute force dan banyak tools yang dapat digunakan.
- fail2ban dapat menangkal serangan brute force.

###**-- Saran**

- openSSH-server dapat dikonfigurasi portnya agar lebih aman karena kecil kemungkinan hacker mengetahui port yang digunakan untuk SSH.
- fail2ban dapat dikonfigurasi maxretry dengan nilai yang kecil untuk menangkal serangan brute force.
