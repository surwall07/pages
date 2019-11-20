# test

[分区](diskPartition.md)

| 目录           | 应放置内容                                                   |
| -------------- | ------------------------------------------------------------ |
| /boot          | The /boot/ directory contains static files required to boot the system, such as the Linux kernel. These files are essential for the system to boot properly. |
| /dev           | The /dev/ directory contains file system entries which represent devices that are attached to the system. These files are essential for the system to function properly. |
| /etc           | The /etc/ directory is reserved for configuration files that are local to the machine. No binaries are to be placed in /etc/. Any binaries that were once located in /etc/ should be placed into /sbin/ or /bin/. |
| /etc/opt(必要) | 第三方软件相关设定                                           |
| /etc/X11       | 有关于X Window设定                                           |
| /etc/skel/     | for "skeleton" user files, which are used to populate a home directory when a user is first created. |
| /lib           | 系統的函式庫非常的多，而/lib放置的則是在開機時會用到的函式庫， 以及在/bin或/sbin底下的指令會呼叫的函式庫而已。 |
| /lib/modules   | 這個目錄主要放置可抽換式的核心相關模組(驅動程式)喔           |
| /media         | The /media/ directory contains subdirectories used as mount points for removeable media, such as 3.5 diskettes, CD-ROMs, and Zip disks. |
| /mnt           | The /mnt/ directory is reserved for temporarily mounted file systems, such as NFS file system mounts. For all removeable media, use the /media/ directory. |
| /opt           | The /opt/ directory provides storage for large, static application software packages. |
| /run           | 早期的 FHS 規定系統開機後所產生的各項資訊應該要放置到 /var/run 目錄下，新版的 FHS 則規範到 /run 底下。 由於 /run 可以使用記憶體來模擬，因此效能上會好很多！ |
| /sbin          | Linux有非常多指令是用來設定系統環境的，這些指令只有root才能夠利用來『設定』系統，其他使用者最多只能用來『查詢』而已。 放在/sbin底下的為開機過程中所需要的，裡面包括了開機、修復、還原系統所需要的指令。 至於某些伺服器軟體程式，一般則放置到/usr/sbin/當中。至於本機自行安裝的軟體所產生的系統執行檔(system binary)， 則放置到/usr/local/sbin/當中了。常見的指令包括：fdisk, fsck, ifconfig, mkfs等等。 |
| /srv           | srv可以視為『service』的縮寫，是一些網路服務啟動之後，這些服務所需要取用的資料目錄。 常見的服務例如WWW, FTP等等。舉例來說，WWW伺服器需要的網頁資料就可以放置在/srv/www/裡面。 不過，系統的服務資料如果尚未要提供給網際網路任何人瀏覽的話，預設還是建議放置到 /var/lib 底下即可。 |
| /tmp           | 這是讓一般使用者或者是正在執行的程序暫時放置檔案的地方。     |