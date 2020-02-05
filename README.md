# BuggyCart a customization of OpenCart

## Overview

BuggyCart is a customization of OpenCart (a free open source ecommerce platform for online merchants) with the following implanted vulnerabilities.

   1. Sql inject in admin login
   2. Sql inject in customer login
   3. Disable password retry limit
   4. Allow passwords with len <8
   5. Allow XSS in customer name edit page
   6. Store CVV in DB
   7. Show unmasked PAN
   8. Use hardcoded key for encrypting PAN
   9. Store plaintext PAN (Set ENCRYPT_PAN to false in the config.php)
  10. Store unsalted customer passwords
  11. Store plaintext passwords for admins

## Install from docker

Download the docker image from [this URL](http://yaogroup.cs.vt.edu/softwares/buggycart.v1/buggycart.v1.tar) and run the following commands.

   1. `sudo docker load --input buggycart.v1.tar` (load the docker image)
   2. `sudo docker run -it buggycart.v1:latest bash` (run an instance with an interactive bash)
   3. `/opt/lampp/xampp startapache` (Start Apache with the buggycart installation)
   4. `/opt/lampp/xampp startmysql` (Start Mysql with the buggycart installation)
   5. `cd pci-checker && ./run.sh` (run [pci-checker](https://github.com/sazzad114/pci-checker) on the installed instance)

## Install from scratch

To install from scratch, please read the installation instructions included in the repository or download file.

## License

[GNU General Public License version 3 (GPLv3)](https://github.com/opencart/opencart/blob/master/license.txt)

