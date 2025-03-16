---
title: Ubuntu
---

```{=org}
#+STARTUP: overview
```
# Getting Started

## Install Softwares

-   snap

``` example
   $ sudo snap install namasoftware
```

-   apt

``` example
   $ sudo apt-get install namasoftware
```

-   deb

``` example
   $ sudo dpkg -i $DEB
```

\$DEB adalah path ke instalasi file (deb).

## Uninstall Softwares

**apt**

``` example
   $ sudo apt-get purge <program name>
```

**snap**

``` example
   $ sudo snap remove <software name>
```

## Installed Softwares

**apt**

``` example
   $ apt list --installed
```

**snap**

``` example
   $ snap list
```

## Vim

-   install: sudo apt-get install vim
-   [vimrc](https://github.com/yohanfs/.vim)

## Git

-   Command:

``` example
$ sudo apt-get update
$ sudo apt-get install git
$ git --version
```

-   [Install](https://www.digitalocean.com/community/tutorials/how-to-install-git-on-ubuntu-18-04)
-   [SSH](https://wiki.paparazziuav.org/wiki/Github_manual_for_Ubuntu)

Enable ssh di Ubuntu:

``` example
sudo apt-get install openssh-server
sudo systemctl status ssh
```

## Pandoc

-   Install

    -   [download
        installer](https://github.com/jgm/pandoc/releases/tag/2.9.2.1)
    -   Command:

``` example
     $ sudo dpkg -i $DEB
```

-   \$DEB adalah path ke instalasi file (deb)
-   [Referensi](https://pandoc.org/installing.html)

## Python

-   Sudah terinstall secara default
-   Cek di terminal: python3 ---version
-   Install pip: sudo apt-get -y install python3-pip

## Inkscape

-   [Web: inkscape](https://inkscape.org/release/)
-   Go to the "Ubuntu Software" atau

``` example
$ sudo add-apt-repository ppa:inkscape.dev/stable
$ sudo apt update
$ sudo apt install inkscape
```

## Make

-   Install: sudo apt-get install make

## Markdown Editor (ReText)

-   Command: sudo apt-get install -y retext
-   [Referensi](https://www.hiroom2.com/2017/05/16/ubuntu-16-04-write-markdown-with-retext/)

## Latex

-   [Texlive](https://www.tecrobust.com/insta-latex-ubuntu-texmaker-linux-ubuntu-latest/)

``` example
   $ sudo apt-get install texlive-full
```

-   [MiKTeX](https://miktex.org/download)

Isu saat menjalankan `sudo apt-get update`{.verbatim}:

> Skipping acquire of configured file
> \'universe/binary-i386/Packages\'...

Ini terjadi karena MiKTeX untuk Linux tidak support arsitektur i386.
Solusinya adalah dengan mengedit:

``` example
$ sudo vim /etc/apt/sources.list.d/miktex.list
```

Tambahkan \[arch=amd64\] sehingga menjadi:

``` example
$ deb [arch=amd64] http://miktex.org/download/ubuntu focal universe
```

## Google Chrome

-   Google Chrome tidak tersedia di Ubuntu Software
-   [Install Google Chrome](https://itsfoss.com/install-chrome-ubuntu/)

``` example
$ wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
$ sudo dpkg -i google-chrome-stable_current_amd64.deb
```

## Terminal PDF

-   [merge pdf:
    pdfunite](http://manpages.ubuntu.com/manpages/bionic/man1/pdfunite.1.html)
-   Example: pdfunite sample1.pdf sample2.pdf sample.pdf
-   [extract pdf: qpdf](http://qpdf.sourceforge.net/)
-   [pdftk](https://www.pdflabs.com/docs/pdftk-cli-examples/)

## Tree

*Directory tree* bisa diprint di terminal dengan tree command. Command
tersebut adalah built-in di Windows. Sedangkan di ubuntu harus diinstall
terlebih dahulu:

``` example
   sudo apt-get install tree
```

Selanjutnya bisa digunakan dengan mengetikkan tree command sebagai
berikut:

``` example
   tree
```

Hasilnya:

![](images/tree.png)

## reStructuredText

-   [rst2html](https://pypi.org/project/rst2html/) : sudo pip3 install
    rst2html
-   [rst2pdf](https://pypi.org/project/rst2pdf/) : sudo pip3 install
    rst2pdf

## Shotwell

Shotwell adalah image viewer dan editor.

## Inotifywait

Inotifywait berguna untuk memantau aktivitas sebuah folder atau file.

``` example
   $ sudo apt-get install inotify-tools
```

## Zathura

Simple pdf viewer.

``` example
   $ sudo apt-get install zathura 
```

## Install Printer

### Canon

Printer canon diinstall di ubuntu dengan cara sebagai berikut:

-   Tambahkan repositori

``` example
   sudo add-apt-repository ppa:michael-gruz/canon
   sudo apt-get update
```

-   Install printer sesuai dengan versinya. Contohnya adalah printer
    MP540.

``` example
   sudo apt-get install cnijfilter-mp540series
```

**Referensi**

-   [Askubuntu: Canon
    Printer](https://askubuntu.com/questions/75014/how-can-i-install-a-canon-printer-or-scanner-driver)

## Terminal Multiplexer

Tmux adalah *terminal multiplexer* yang memungkinkan untuk membuka
banyak tab dalam satu terminal.

**Install**

``` example
   sudo apt-get install tmux
```

**Run**

-   open terminal, kemudian ketik: tmux

-   split terminal:

    -   horizontal: `Ctrl+b+"`{.verbatim}
    -   vertikal: `Ctrl+b+%`{.verbatim}

-   berpindah antar terminal:

    -   next terminal: `Ctrl+b+o`{.verbatim}
    -   previous terminal: `Ctrl+b+;`{.verbatim}

-   menutup current terminal: `Ctrl+b+x`{.verbatim}

-   buka last session: open normal terminal, kemudian ketik:
    `tmux attach`{.verbatim}

-   kembali normal terminal: `Ctrl+b+d`{.verbatim}

-   list terminal: `tmux list-sessions`{.verbatim}

**Referensi**

-   [github: tmux](https://github.com/tmux/tmux/wiki)
-   [linuxize: getting started with
    tmux](https://linuxize.com/post/getting-started-with-tmux)

## Only Office

Alternatif untuk Microsoft Office.

-   Install via Snap (setting juga file permission di snap page)
-   Untuk menambahkan font, simpan .ttf format di:

``` example
   /usr/share/fonts/truetype
```

Buatlahlah folder baru dengan nama onlyoffice pada path di atas untuk
menyimpan font-nya.

-   [Download fonts](https://github.com/justrajdeep/fonts)

## SoftMaker FreeOffice

Alternatif untuk Microsoft Office. Download di
[www.freeoffice.com](https://www.freeoffice.com/en/).

# Hieararki Filesystem

Sistem folder di ubuntu dan deskripsinya:

  Direktori   Deskripsi
  ----------- -----------------------------------------------
  /           root directory
  /bin        command binaries misalnya: cat, ls, cp
  /boot       boot loader
  /dev        device files, misalnya /dev/null, /dev/sda1
  /etc        file konfigurasi (text based)
  /home       home direktori
  /lib        library untuk /bin dan /sbin
  /media      mount point untuk removable media (usb drive)
  /mnt        mounting drive
  /proc       vitual filesystem
  /root       home directory untuk root user
  /run        run-time variable data
  /sbin       system binaries, misalnya fsck, init, route
  /srv        serve folder. ex untuk ftp, rsync, www, cvs
  /tmp        temporary space
  /usr        programs, libraries, dan dokumentasi
  /var        tempat penyimpanan untuk semua variable files

**Referensi**

-   [Wikipedia - Fileystem Hierarchy
    Standard](https://en.wikipedia.org/wiki/Filesystem_Hierarchy_Standard)
-   Tldp - General Overview of The Linux File System
-   [Understanding the linux directory
    layout](https://www.nixtutor.com/linux/understanding-the-linux-directory-layout/)

# Bootable Flash Drive

Berikut ini adalah langkah-langkah untuk membuat bootable usb. Bootable
usb ini diperuntukkan untuk menginstall sebuah operating system (OS)
misalnya ubuntu dan windows melalui usb.

-   Colokkan flaskdisk (usb drive) ke usb port di komputer.
-   Buka **Startup Disk Creator**.
-   Klik other untuk memilih ISO file.
-   Pilih flaskdisk dan kemudian klik **Make Startup Disk**.

![](images/bootable.png)

**Referensi**

-   [Bootable flash drive for
    ubuntu](https://askubuntu.com/questions/876058/bootable-flash-drive-for-ubuntu)

# Partisi Hardisk

**Gparted**

Partisi hardisk di Ubuntu tidak bisa dilakukan ketika Ubuntu sedang
dioperasikan. Partisi dapat dilakukan dengan cara menjalankan instalasi
ubuntu dari usb kemudian pilih **live ubuntu**. Selanjutnya, partisi
dapat dilakukan dengan program yang bernama Gparted.

Contoh hardisk sebelum partisi adalah:

![](images/sebelumpartisi.png)

Dengan memilih menu **Partition**, maka hasil partisinya adalah sbb:

![](images/setelahpartisi.png)

**Daftar Partisi**

``` example
   $ ls -l /dev/disk/by-label
```

atau

``` example
   $ ls -l /dev/disk/by-id
```

atau

``` example
   $ ls -l /dev/disk/by-uuid
```

uuid = *universal unique identifier*

# Cloning Disk

Cloning disk bisa menggunakan dd command. Disk tujuan harus sama atau
lebih besar dari disk yang dicloning. Apabila menggunakan disk tujuan
yang lebih besar, maka nanti kelebihan storagenya akan menjadi
*unaloccated space*. Selanjutnya *unaloccated space* dapat digabungkan
ke disk yang sudah ada dengan menggunakan gparted.

``` example
   $ dd if=<source-disk> of=<destination-disk> [option}
```

-   if adalah input file
-   of adalah output file
-   option misalnya status=progress untuk melihat proses pengkopian data

Contoh:

``` example
   $ dd if=/dev/sda of=/dev/sdb status=progress
```

**Referensi**

[How to clone your linux harddrive with
dd](https://snapshooter.io/blog/how-to-clone-your-linux-harddrive-with-dd)

# Basic Command

Berikut ini adalah basic command ubuntu yang sering saya gunakan:

  Task                                Command
  ----------------------------------- -----------------------------------------------------
  update ubuntu package               sudo apt-get update
  install package                     sudo apt-get install \<Package\>
  menggunakan super user              sudo su
  open terminal                       CTRL + ALT + T
  membuat file baru                   touch filenamedotextension (contoh touch README.md)
  membuat folder baru                 mkdir namafolder
  berpindah ke subfolder              cd namafolder
  memindah sebuah file                mv asalFile tujuanFile
  exit dari terminal                  exit
  rename file                         mv file.ext1 file.ext2
  install deb packages                sudo dpkg -i filenamedotdeb
  berpindah ke path sebelumnya        cd ..
  menampilkan isi file                cp filenamedotextension
  menampilkan isi direktori           ls atau ls -a (memunculkan hidden files)
  delete file                         rm filenamedotextension
  delete semua dengan nama tertentu   rm **filename**
  open file dengan default program    start filenamedotextension
  clear terminal                      clear atau CTRL + L
  manual command                      man ls (manual dari command ls)
  view beberapa baris csv data        head contoh.csv
  list disk                           lsblk

# Akses Network Drive

Ada 2 metode untuk akses network drive di ubuntu.

1.  GUI (file explorer)

    -   Install samba
    -   Other Locations \>\> Connect to Server \>\> Enter server address
    -   Server address format= <smb://ip-address>

2.  Terminal

    -   Install smbclient
    -   *Command*: smbclient -L=ip-address

Untuk cara 2, masih ada isu. Setelah daftar shared hardisk muncul,
kemudian ketik smbclient //ip-address/L, maka akan muncul pesan:

``` example
   tree connect failed: NT_STATUS_REQUEST_NOT_ACCEPTED
```

# Mounting Drive

## Manual

Buat sebuah folder sebagai *mount point*, misalnya
`/mnt/Data`{.verbatim}.

``` example
   $ sudo mkdir /mnt/Data
   $ sudo mount /dev/sdb6 /mnt/Data
```

Sekarang data bisa diakses di `/mnt/Data`{.verbatim}.

Alamat /dev/sdb6, dapat dilihat dari:

``` example
   $ lsblk
```

## Auto Mounting

File yang harus diedit adalah `/etc/fstab`{.verbatim}. Sebelumnya cari
terlebih dahulu UUID dari drive yang akan dimounting.

``` example
   $ ls -al /dev/disk/by-uuid
```

Kemudian editlah `/etc/fstab`{.verbatim}, misalnya:

### untuk internal drive

1.  Ubuntu

    ``` example
       UUID=xxxxxxx /mnt/Data   ext4    defaults        0       0        
    ```

2.  Ubuntu Mate

    ``` example
       UUID=xxxxxxx /mnt/Data   ext4    defaults        0       2
    ```

    Jika ada issue dengan file permission, jalankan command berikut
    setelah restart komputer.

    ``` example
       sudo chown -R name(user):name(user) /mnt/Data        
    ```

### untuk ekternal usb drive

``` example
   UUID=xxxxxxx /mnt/usb    ntfs    uid=1000,gid=1000,umask=022 0 1  
```

Note

Jika format storage-nya adalah ntfs, maka install:

``` example
   $ sudo apt-get update
   $ sudo apt-install ntfs-3g
```

Jika tidak di-install, maka akan ada issue dengan file permission.

-   Test Fstab

Sebelum rebooting, cek terlebih dengan cara:

``` example
  sudo mount -a
```

-   Unmounting drive dengan umount

``` example
   sudo umount /mnt/Data
```

Referensi:

-   [automatic mounting
    drive](https://confluence.jaytaala.com/display/TKB/Mount+drive+in+linux+and+set+auto-mount+at+boot)

# Mounting Shared Drive

-   Buatlah mount point, misalnya `/mnt/Data`{.verbatim}

``` example
   $ sudo mkdir /mnt/Data
```

-   Install cifs-utils

``` example
   $ sudo apt install cifs-utils
```

-   Buatlah sebuah file `/root/.smbcredentials`{.verbatim} dengan isi:

``` example
   username=user
   password=pass
```

-   Ganti permission agar hanya root yang bisa baca smbcredentials

``` example
   $ sudo chmod 700 /root/.smbcredentials
```

-   Edit `/etc/fstab`{.verbatim}

``` example
   $ sudo vim /etc/fstab
```

Tambahkan line berikut:

**Owner drive adalah root**

``` example
   //192.168.1.120/storage /mnt/Data    cifs credentials=/root/.smbcredentials,file_mode=0777,dir_mode=0777 0 0
```

**Owner drive adalah user**

``` example
   //192.168.1.120/storage /mnt/Data    cifs uid=1000,gid=1000,credentials=/root/.smbcredentials,file_mode=0777,dir_mode=0777 0 0
```

-   Test Fstab

Sebelum rebooting, cek terlebih dengan cara:

``` example
   $ sudo mount -a
```

Referensi:

-   [Mount a network shared
    drive](https://linuxize.com/post/how-to-mount-cifs-windows-share-on-linux/)

# Change Permission

Untuk melihat permission dari file atau folder:

``` example
   $ ls -l 
```

atau dengan ditambah opsi **-t** apabila file ingin diurutkan
berdasarkan waktu.

``` example
   $ ls -lt
```

Misalnya `ls -lt`{.verbatim} diterapkan pada folder demo, hasilnya
adalah:

![](images/seepermission.png)

Pada gambar di atas ada nama `fajar fajar`{.verbatim} yang secara
berurutan. Itu maksudnya adalah nama user dan nama grup. Selanjutnya ada
kode berikut:

``` example
   -rw-rw-r--
```

dan

``` example
   drwxrwxr-x
```

Tanda (-) di awal kode tersebut menandakan itu adalah sebuah file.
Sedangkan (d) menandakan sebuah direktori. Kemudian rwx adalah kode
untuk:

-   r=read
-   w=write
-   x=executable

Kode rwx di atas bisa dinyatakan dengan huruf seperti contoh di atas
atau dengan huruf sebagai berikut:

-   r=4
-   w=2
-   x=1

Kode `-rw-rw-r--`{.verbatim}, dapat dibaca sebagai berikut:

  Tipe   user   grup   other
  ------ ------ ------ -------
  \-     rw-    rw-    r--
  File   6      6      4

Jadi apabila ingin mengubah permission dari sebuah file atau folder,
bisa menggunakan *command* berikut:

``` example
   sudo chmod 664 namaFile.extension
```

-   [change
    permission](https://opensource.com/article/19/6/understanding-linux-permissions)

# Change Password

Ganti password:

``` example
   $ passwd
```

Ganti password root user:

``` example
   $ sudo passwd
```

# UID dan GID

Mencari uid user:

``` example
   $ id -u <username>
```

Mencari gid:

``` example
   $ id -g <username>
```

Mencari semua grup dari seorang user:

``` example
   $ id -G <username>
```

Mencari uid dan gid sebuah user:

``` example
   $ id <username>
```

Menambah user ke grup:

``` example
   $ sudo usermod -aG <groupname> <username>
```

-   (-a) adalah shortcut dari --append
-   (-G) adalah shortcut dari --groups

**Referensi**

-   [Linux sysadmin basics: uid and
    gid](https://www.redhat.com/sysadmin/user-account-gid-uid)
-   [Find uid and gid](https://kb.iu.edu/d/adwf)
-   [Sudo
    usermod](https://medium.com/@dhananjay4058/what-does-sudo-usermod-a-g-group-user-do-on-linux-b1ab7ffbba9c)

# Umask

Umask (user file-creation mode mask) digunakan untuk menentukan file
permission dari file yang baru dibuat.

Berikut ini adalah notasi untuk umask:

  Bit   File permission
  ----- --------------------------
  0     read, write, and execute
  1     read and write
  2     read and execute
  3     read only
  4     write and execute
  5     write only
  6     execute only
  7     no permissions

Untuk umask=077, pengertiannya adalah:

  Bit   Target   File permission
  ----- -------- --------------------------
  0     owner    read, write, and execute
  7     group    no permission
  7     others   no permission

**Referensi**

-   [What is
    umask?](https://www.cyberciti.biz/tips/understanding-linux-unix-umask-value-usage.html)

# Kapasitas Disk

``` example
   df -h
```

# Disk Size

``` example
du -sh /path
```

# Rsync

Berguna untuk sinkronisasi file atau folder antara 2 lokasi di internal
komputer atau ke remote. Rync juga hanya akan mengkopi data yang berbeda
dari 2 lokasi tersebut sehingga lebih efisien.

**Install**

``` example
   $ sudo apt-get install rsync
```

**Syntax**

``` example
   Local to local: $ rsync [OPTION} [SRC] [DEST]
       Local to remote: $ rsync [OPTION] [SRC] [USER@HOST:DEST]
       Remote to local: $ rsync [OPTION] [USER@HOST:DEST] [DEST]
```

\- OPTION

:   -   -a: archive mode
    -   -z: compress
    -   -P: partial/progress
    -   --delete: delete extra file di destination folder (untuk mirror)
    -   -q: quite (non-error messages)

-   SRC: source directory
-   DEST: destination directory
-   USER: Remote username
-   HOST: Remote hostname or IP Address

**Contoh**

``` example
   $ rsync -a /home/data /mnt/data
```

``` example
   $ rsync -a /home/data user@hostname:/mnt/data
```

``` example
   $ rsync -avh --progress --delete /source /destination
```

**Referensi**

-   [Rsync command in
    linux](https://linuxize.com/post/how-to-use-rsync-for-local-and-remote-data-transfer-and-synchronization/)

# Memory

Untuk melihat status penggunaan memory:

``` example
   $ vmstat -s
```

# Networking

## Share Folders

-   [Install
    Samba](https://ubuntu.com/tutorials/install-and-configure-samba#2-installing-samba)

``` example
   $ sudo apt-get update
   $ sudo apt-get install samba
```

-   Pilih folder yang akan dishare, misalnya:

``` example
   /mnt/data
```

-   Aturlah file berikut:

``` example
   $ sudo vim /etc/samba/smb.conf
```

Tambahkan *script* berikut pada bagian akhir smb.conf

``` example
[namashare]
path = /mnt/data
writeable = Yes
create mask = 0777
directory mask = 0777
public = no
```

**Referensi**

-   Akses komputer dalam network: <smb://IP-Address/>
-   [Referensi: Share a folder in
    ubuntu](http://ubuntuhandbook.org/index.php/2019/11/share-folder-ubuntu-18-04-step-by-step-guide/)
-   [Referensi: Setting LAN in
    ubuntu](https://linuxconfig.org/how-to-configure-static-ip-address-on-ubuntu-18-04-bionic-beaver-linux)

## Mapping IP Addresses

Untuk mapping ip-address:

``` example
   sudo vim /etc/hosts
```

Cara ini hanya berlaku untuk mesin komputer tersebut. Agar bisa
digunakan oleh komputer lain dalam network yang sama, perlu menggunakan
DNS server. DNS server bisa diinstall di Raspberry Pi.

# Untar

``` example
   $ tar -xzf filename.tar.gz
```

# CPU Info

``` example
   $ cat /proc/cpuinfo
```

# Kopi ke Clipboard

**Install**

``` example
   $ sudo apt-get install xclip
```

**Kopi pwd**

``` example
   $ pwd | xclip
```

**Output**

``` example
   $ xclip -o 
```

# Scanner

Gunakan aplikasi simple scan.

``` example
sudo apt-get install simple-scan
```

# Crash

Tekan Ctrl + Alt + F3. Kemudian jalankan:

``` example
sudo systemctl restart gdm3
```

# Issues

-   broken installation

``` example
   $ sudo apt-get install --fix-broken
```
