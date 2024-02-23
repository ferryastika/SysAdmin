# TUGAS 1

**DAFTAR ISI**

- [SOAL 1](#1-langkah-langkah-instalasi-sistem-operasi-debian)
  - [Requirements](#persyaratan-sistem)
  - [Persiapan](#persiapan)
  - [Mulai](#langkah-langkah)

- [SOAL 2](#2-perbedaan-debian-12--bookworm--dengan-debian-11--bullseye-)

- [SOAL 3](#3-fungsi-file-etcgroups-dan-formatnya)
- [SOAL 4](4-perbedaan-su-dan-su-)
  - [COMMAND SU](#a-su)
  - [COMMAND SU-](#b-su--)
- [SOAL 5](#5-fungsi-sudo-command)
- [soal 6](#6jelaskan-langkah-langkah-penambahan-user-anda-sebagai-user-sudo--gunakan-perintah-su---lalu-setelah-masuk-sebagai-root-jalankan-perintah-visudo-tambahkan-user-anda-di-bawah-user-root-pada-bagian---user-privilege-specification)


## 1. Langkah-langkah Instalasi Sistem Operasi Debian

Instalasi sistem operasi Debian dapat dilakukan menggunakan berbagai aplikasi virtualisasi seperti VirtualBox, VMWare Player, atau Vmware Fusion (untuk MAC). Berikut adalah langkah-langkah instalasi Debian dengan menggunakan VirtualBox.


------------



### Persyaratan Sistem:
- CPU: Minimal 2 core.
- RAM: Minimal 4096 MB (4 GB).
- HDD: Minimal 25 GB dengan partisi sebagai berikut:
  - / (root): 20 GB
  - /storage: 5 GB
  - swap: 1,5 GB
- Hostname: SysAdmin-NRP


### Persiapan:
   - Unduh file ISO Debian dari Repo resmi [DISINI](https://kartolo.sby.datautama.net.id/debian-cd/12.5.0/amd64/iso-cd/).
   [TUTORIAL DOWNLOAD](#download)
   - Unduh dan instal aplikasi VirtualBox dari web resmi [DISINI](https://www.virtualbox.org/wiki/Downloads).
   [TUTORIAL INSTALL](#download)



### LANGKAH LANGKAH

1. **Membuat Virtual Machine**
   - Buka VirtualBox dan klik tombol "New" untuk membuat mesin virtual baru.
   - Beri nama mesin virtual SysAdmin-3122500024.
     
   ![CREATE](https://github.com/Reza1290/SysAdmin-3122500024/assets/70069286/411502a5-8282-4e85-ac03-59b31a322b0e)

   - **Pastikan Centang Kotak ** Supaya dapat melakukan Custom Install.
     
   - Atur alokasi RAM minimal 4096 MB. Disini saya alokasi 8GB
   - Atur alokasi core CPU minimal 2 Core, disini saya alokasi 6 Core dari 12 Core
     
   ![SPEK](https://github.com/Reza1290/SysAdmin-3122500024/assets/70069286/f8dcbcba-39e2-45af-9896-c70f6b26c257)
    
   - Buat hard disk virtual baru dengan ukuran minimal 25 GB.
     
   ![DISK SIZE](https://github.com/Reza1290/SysAdmin-3122500024/assets/70069286/5d2bd9a7-7e5b-41d2-bae9-7a65e0c05abc)



2. **Instalasi OS Debian**
   
Setelah kita melakukan setup pada bagian VM, selanjutnya Machine dapat kita jalankan dengan menekan tombol Start, setelah VM Menyala maka akan disuguhkan tampilan HOME dari Debian OS.

![HOME DEBIAN](https://github.com/Reza1290/SysAdmin-3122500024/assets/70069286/5933edad-5a74-458a-98f3-d38ad5ba25ca)

  **A. PILIHAN INSTALL**
  
  Note: Masukkan Angka Lalu tekan **ENTER** atau Gunakan _Panah Navigasi_ untuk memilih Menu
  
  1. Kita disini akan disuguhkan opsi install dengan CLI, Untuk Bagian Bahasa Sesuaikan Preferensi Masing Masing,
      Kemudian Pastikan **HOST : SysAdmin-NRP** disini saya SysAdmin-3122500024
      
     ![Screenshot (1291)](https://github.com/Reza1290/SysAdmin-3122500024/assets/70069286/984652d6-352b-450d-9027-4afacc1ace84)

  2. Sesuaikan password untuk user **root** anda lalu buatlah satu akun pengguna untuk anda disini saya beri nama *user*

     ![image](https://github.com/Reza1290/SysAdmin-3122500024/assets/70069286/172be2b1-6fc2-4a2e-b3f9-8e634c332e49)

  **PARTISI PART**
  
  3. Kemudian kita masuk ke bagian Pembagian Partisi Pilih **MANUAL METHOD** Kemudian Pilih Partisinya disini saya memilih **SCSI3 (0,0,0) (sda) - 37.6 GB ATA VBOX HARDDISK**
      
     ![image](https://github.com/Reza1290/SysAdmin-3122500024/assets/70069286/f22f4aaf-6f6e-4200-b31b-4563c603c1e8)

  4. Kemudian muncul prompt Ya Tidak, Pada Bagian ini bisa dijawab Tidak Setelah itu Akan Muncul Partisi Kosong **(FREE SPACE)** Masukkan Angka kemudian tekan enter

     ![image](https://github.com/Reza1290/SysAdmin-3122500024/assets/70069286/dfe5ac12-adfe-42ad-9406-851b158515d9)

  5. Setelah Memilih Create New Partition, Masukkan Maximum Size dari disk yang akan dibagi

     ![image](https://github.com/Reza1290/SysAdmin-3122500024/assets/70069286/5b629cb0-bcf4-4c19-8488-5cc2a8ebc3ab)

  6. Disini kita pilih Logical -> Beginning ( diatas ) End ( dibawah )

     ![image](https://github.com/Reza1290/SysAdmin-3122500024/assets/70069286/c555220b-7f7e-49c7-9145-560095e28308) Hasil

  7. Karena 5GB untuk Mount Point /storage maka kita pilih angka 3 untuk mengganti mount point, Kemudian Pilih Enter Manual (10)

     ![image](https://github.com/Reza1290/SysAdmin-3122500024/assets/70069286/cbc907cb-15cf-4f0b-828e-373c45fce928)

  8. Setelah itu kita simpan dengan memilih angka 11

     ![image](https://github.com/Reza1290/SysAdmin-3122500024/assets/70069286/6c3a9592-9b8b-4fb9-8a50-0af53a495ea1)

  9. Lakukan langkah yang sama untuk SWAP dan Root Directory, **Khusus Swap perhatikan langkah berikut**

     ![image](https://github.com/Reza1290/SysAdmin-3122500024/assets/70069286/0e071126-e6be-41fc-8e99-fa93bed9d5d6)

     Pilih OPSI SWAP
     
     ![image](https://github.com/Reza1290/SysAdmin-3122500024/assets/70069286/4f86ad7a-4e4e-420a-b207-5b39a8f76e57)

  10. Untuk Opsi / (root) pastikan mount point adalah "/" Lakukan Simpan
  11. Setelah Tersimpan Kita Lakukan WRITE DISK PARTITION, Pastikan YES
      
      ![image](https://github.com/Reza1290/SysAdmin-3122500024/assets/70069286/583d8f0a-9a77-4e36-8dc0-d47d76ed59c8)

  12. Secara Otomatis Sistem akan Menginstall BASE SYSTEM tunggu beberapa saat
      
      ![image](https://github.com/Reza1290/SysAdmin-3122500024/assets/70069286/af1f62fc-64c7-4b97-9ced-0c32d3a7a422)

  13. Setelah Terinstall User diminta memasukan **REPOSITORY UNTUK MENDOWNLOAD SOFTWARE**
      Saya Menyarankan menggunakan Mirror https://kartolo.sby.datautama.net.id/ Karena Mirror berada di Indonesia dan up to date.

  14. Jika Muncul Bagian ini silahkan di Enter Saja (DEFAULT OPTION)
      
      ![image](https://github.com/Reza1290/SysAdmin-3122500024/assets/70069286/dab1eab5-205d-4669-83d2-0a3916bc45ca)

  15. Pastikan Tersambung Ke INTERNET, kemudian ditunggu hingga selesai maka DEBIAN 12.5 AKAN TERINSTALL SEMPURNA.

  **B. PILIHAN GRAPHICAL INSTALL**

  DEBIAN memudahkan kita dalam Menginstall OS mereka dengan menyediakan GRAPHICAL INSTALLER!

  1. Pilih Bahasa sesuai preferensi
     
     ![Screenshot (1319)](https://github.com/Reza1290/SysAdmin-3122500024/assets/70069286/55b24f48-41c8-4ab4-89a2-a10194487730)

  2. Masukkan Hostname Berupa SysAdmin-3122500024

     ![image](https://github.com/Reza1290/SysAdmin-3122500024/assets/70069286/ed69ee94-87a8-4c47-89ac-d7036ff1a21a)
    
  3. Isilah Beberapa Credentials Yang diwajibkan untuk diisi, root password, akun pengguna dsb.

     ![Screenshot (1322)](https://github.com/Reza1290/SysAdmin-3122500024/assets/70069286/5717b8c0-4bb5-461b-8a44-21b0876d008f)

  4. Setting Partisi seperti dibawah

     ![Screenshot (1324)](https://github.com/Reza1290/SysAdmin-3122500024/assets/70069286/57702346-9075-4bce-87c0-6287a7b360a5)

  5. Pada Bagian Ini Lakukan Klik Menggunakan Mouse Ke Partisi lalu Buat Partisi Baru Pastikan Mount Point telah sama
  6. jika belum dapat diubah, dan pastikan use as benar

     ![Screenshot (1325)](https://github.com/Reza1290/SysAdmin-3122500024/assets/70069286/151b6f65-10e1-4a97-976b-1dbb0b0f5468)

  7. Jalankan Installer Menekan Continue.
  8. Tunggu Hingga Terinstall Sempurna.


------------

## 2. PERBEDAAN DEBIAN 12 ( BOOKWORM ) DENGAN DEBIAN 11 ( BULLSEYE )

Buat ringkasan tentang perbedaan dari Debian 12 (bookworm) dengan Debian 11 (bullseye) : versi kernel, kebutuhan sistem, penerapan systemd dan perbedaan packagenya (dalam bentuk tabel) !

|Jenis |Debian 12 (bookworm)|Debian 11 (bullseye)| Sumber |
|-----|--------|---------------------------------| ------ |
|Versi Kernel| Linux Kernel 6.1 LTS| Linux Kernel 5.10 LTS | [LIST](https://docs-cortex.paloaltonetworks.com/r/Linux-Kernel-Versions/Debian-11-x86_64) |
| | + support untuk Rust, Intel Meteor Lake, dan ARM SoC. | - | |
| | + Kernel Concurrency Sanitizer + Kernel Control Flow Integrity (KCFI) support (KCSAN) |         | |
|Kebutuhan Sistem  |   No desktop	RAM 256Mb - 512Mb	DISK 4 GB With Desktop	RAM 1 GB- 2 GB DISK 10 GB   |   No desktop	RAM 256Mb - 512Mb	DISK 4 GB With Desktop	RAM 1 GB- 2 GB DISK 10 GB    | [BOOKWORM](https://www.debian.org/releases/bookworm/amd64/ch03s04.en.html) [BULLSEYE](https://www.debian.org/releases/bullseye/amd64/ch03s04.en.html)  |
| Penerapan Systemd | Versi 252 | Versi 247 | [LINK](https://www.debian.org/releases/stable/amd64/release-notes/ch-whats-new.html) |
| |Resolvectl menampilkan informasi lokasi host resolved jika komunikasi terenkripsi | - | [ARTIKEL](https://www.debian.org/releases/stable/arm64/release-notes/ch-information.en.html#systemd-resolved) |
| Package | 64419 packages (11089 new) | 53330 packages | [LINK](https://www.debian.org/releases/stable/amd64/release-notes/ch-whats-new.en.html#newdistro) |
| | non-free firmware packages dipindahkan dari non-free ke non-free-firmware | Manual diubah "4.1.8 bullseye: recommended to add non-free-firmware" dan 5.1.1. | [BOOKWORM 2.2](https://www.debian.org/releases/stable/i386/release-notes/ch-whats-new.en.html#newdistro) [BULLSEYE 4.1.8](https://www.debian.org/releases/stable/amd64/release-notes/ch-upgrading.en.html#non-free-firmware) [BULLSEYE 5.1.1](https://www.debian.org/releases/stable/amd64/release-notes/ch-information.en.html#non-free-split) |
| Filesystems | NTFS sudah ada (bulit in) -> ikut kernel 5.15, + ntfs2btrfs | harus menggunakan third party | |


## 3. FUNGSI FILE "etc/groups" DAN FORMATNYA

  Bersumber dari manual books linux ( dapat menggunakan command "man"). "etc/groups" sebuah file teks yang berisi definisi dari groups yang ada pada system. 

  Untuk satu group di tulis dalam satu baris dengan format sebagai berikut

        group_name:password:GID:user_list
      


  Dengan rincian sebagai berikut:

        group_name  



  nama dari grup.

        password



  password dari group yang terenkripsi.  Jika kosong maka groups tidak berpassword.

        GID  


       
  GROUP ID bersifat numerik.

        user_list



  list dari username user yang berada pada grup, dipisahkan dengan koma.

## 4. PERBEDAAN SU dan SU-

  Sebelumnya berikut adalah format pattern dari command su di linux :
  
        su [options] [-] [user [argument...]]

### a. "su"

  Perintah su tanpa options atau param nama digunakan untuk melakukan superuser user sekarang (root shell saat ini).
    
  contoh :


### b. "su -"

  (-) strip, adalah opsi yang dapat digunakan pada command su, digunakan untuk berpindah dengan root di environtement baru dengan menginisialisasi lingkungan shell baru.
    jadi seperti halaman login awal.


## 5. FUNGSI "SUDO" COMMAND

  Secara singkat, Sudo merupakan singkatan dari superuser do. Dengan menggunakan ini, pengguna non-root dapat menjalankan perintah yang hanya bisa dilakukan oleh hak istimewa superuser. Ini memungkinkan pengguna dapat melakukan tugas administratif tanpa membuka resiko keamanan yang terkait dengan penggunaan root. Memudahkan membedakan environtment sendiri dan environtment administrator tanpa harus menggunakan kredensial sendiri maupun root.

  Penggunaannya saat kita menggunakan akun kita misal user lalu terdapat command yang mengharuskan permission diatas kita, kita dapat melakukan sudo tanpa perlu masuk ke root dengan masuk sebagai superuser atau user lain.
  

## 6.	Jelaskan langkah-langkah penambahan user anda sebagai user sudo ! Gunakan perintah "su -" lalu setelah masuk sebagai root, jalankan perintah "visudo". Tambahkan user anda di bawah user root pada bagian " # User privilege specification"

  Sebelumnya kita akan mencoba melakukan sudo dengan username "user" (belum ditambahkan ke sudoers file).

  ![image](https://github.com/Reza1290/SysAdmin-3122500024/assets/70069286/ac7da5bb-8367-4196-bd0c-508fa349393b)
  
  disini gagal.

  ### SETUP VISUDO ( SUDOERS FILE )

  lakukan su - untuk masuk ke dalam root sehingga kita memiliki privilage superuser

  ![image](https://github.com/Reza1290/SysAdmin-3122500024/assets/70069286/cd8926b1-124a-46e7-b1b9-8929eeb817fc)
  
  setelah itu ketikan visudo, dan kita lakukan edit pada bagian User Privilage
  
  ![image](https://github.com/Reza1290/SysAdmin-3122500024/assets/70069286/3079725c-0d59-49dd-bb14-aee4bca41a82)

  setelah mendapat privilage username user dapat menggunakan sudo command
  
  ![image](https://github.com/Reza1290/SysAdmin-3122500024/assets/70069286/23168c6f-fb3a-4eec-9cf7-5272af3bcb99)
