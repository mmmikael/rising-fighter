# rising-fighter

### OS Installation
* Download RASPBIAN JESSIE LITE https://www.raspberrypi.org/downloads/raspbian/
* Copy to sd card `xzcat 2017-06-21-raspbian-jessie-lite.img.xz | sudo dd bs=4m of=/dev/disk2`
* Add empty file `ssh` in the root directory of the sdcard.
* Boot
* Connect to pi: `ssh pi@192.168.8.106` (default pwd: `raspberry`)

### Wifi setup
Follow instructions: https://www.raspberrypi.org/documentation/configuration/wireless/wireless-cli.md

### Camera setup
* Enable with `sudo raspi-config`
* Test with `raspistill -f -k`

### Docker installation
(Taken from official doc https://docs.docker.com/engine/installation/linux/debian/#install-using-the-repository)
```bash
$ sudo apt-get install apt-transport-https ca-certificates curl gnupg2 software-properties-common
$ curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -
$ echo "deb [arch=armhf] https://download.docker.com/linux/debian \
      $(lsb_release -cs) stable" | \
      sudo tee /etc/apt/sources.list.d/docker.list
$ sudo apt-get install docker-ce
```
Test: `sudo docker run armhf/hello-world`
