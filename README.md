# Command-Central
Install dan Config Command Central


## Download

  Linux
  ```console
  wget -O https://empowersdc.softwareag.com/ccinstallers/cc-def-10.7-fix1-lnxamd64.sh
  ```
  Windows
  ```console
  http://empowersdc.softwareag.com/ccinstallers/cc-def-10.2-fix2-w64.zip
  ```

## Install 
  Linux
  ```console
  chmod +x cc-def-10.7-fix1-lnxamd64.sh
  ./cc-def-10.7-fix1-lnxamd64.sh --accept-license -d /appl/cc -p admin123 -c 8200 -s 8202 -S 8203
  sudo firewall-cmd --add-port=8200/tcp --permanent
  sudo firewall-cmd --add-port=8202/tcp --permanent
  sudo firewall-cmd --add-port=8203/tcp --permanent
  sudo firewall-cmd --add-port=8091/tcp --permanent
  sudo firewall-cmd --reload
  sudo firewall-cmd --list-all
  ```

  ```desciption
    Argument  Value
    --accept-license  Indicates that you accept the Software AG product license.
    -d path           (-d C:\CCE)   Full path to the installation directory in which you are going to install Command Central.
    -p password       (-p manage123) Password to use for the Command Central Administrator user account.
    -C port number    (-C 8201) HTTPS port to use for Command Central.
    -c port number    (-c 8200) HTTP port to use for Command Central.
    -S port number    (-S 8203) HTTPS port for Command Central to communicate with the local Platform Manager.
    -s port number    (-s 8202) HTTP port for Command Central to communicate with the local Platform Manager.
  ```

  ```desciption
    Setelah install, nyalakan dulu SPM nya, baru nyalakan CCE nya.
    dan di server tujuan harus nyala juga SPM nya
    untuk mengakses web console command central nya di https://<ip>:8091
  ```



#### Install IS dari CCE
  - Pastikan dulu IS CCE bisa mengkases server yg akan di install IS
  - File Instalasi nya harus bernama image-`LNXAMD64`.zip , harus ada nama `LNXAMD64` di belakang nya
  - Setelah Install IS via CCE berhasil, nyalakan SPM nya terlebih dahulu karena `CCE dan server tujuan berkomunikasi mnenggunakan SPM`
 
