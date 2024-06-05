# Proxmox Backup rclone

1. #### Install rclone
```sh
  sudo -v ; curl https://rclone.org/install.sh | sudo bash
```

2. #### Konfigurasi rclone
```sh
  rclone config
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; a. ketik n untuk membuat remote baru dan beri nama:
<br />
![alt text](./rclone2.png)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; b. ketik 13:
<br />
![alt text](./rclone3.png)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; c. tekan enter:
<br />
![alt text](./rclone4.png)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; d. ketik 1:
<br />
![alt text](./rclone5.png)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; e. tekan enter:
<br />
![alt text](./rclone6.png)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; f. ketik n dan y:
<br />
![alt text](./rclone7.png)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; g. lakukan tunnel ssh ke 127.0.0.1, buka browser dan lakukan verifikasi allow gdrive:
<br />
![alt text](./tunnelssh.png)

3. #### Download rclone.sh dan upload ke server
   

5. #### Beri hak akses chmod eksekusi ke file rclone.sh
```sh
  chmod +x rclone.sh
```

6. #### Buat crontab penjadwalan dan tambahkan baris perintah crontab (dalam contoh ini crontab dijalankan setiap hari selasa jam 2 pagi)
```sh
  crontab -e
  0 2 * * TUE /root/rclone.sh
```

7. #### Restart crontab
```sh
  /etc/init.d/cron reload
```

