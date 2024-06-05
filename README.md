# Proxmox Backup rclone

1. #### Install rclone
```sh
  sudo -v ; curl https://rclone.org/install.sh | sudo bash
```

2. #### Konfigurasi rclone
```sh
  rclone config
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; a. 1:
```nano
      bind-address = 172.16.24.24
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; b. 2:
```vim
      server-id = 1
      log_bin = /var/log/mysql/mysql-bin.log
```
