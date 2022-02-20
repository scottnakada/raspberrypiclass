# How to setup your Raspberry Pi

# Setup your Raspberry Pi without a monitor (must have microSD 32Gb)
https://www.tomshardware.com/reviews/raspberry-pi-headless-setup-how-to,6028.html

# Setup your Raspberry Pi if you have a monitor to connect thru your PC/Mac
https://pimylifeup.com/raspberry-pi-vnc-server/

# Install Docker (if you don't have a raspberry pi)
https://www.docker.com/get-started

# Enable ssh to raspberry pi
https://phoenixnap.com/kb/enable-ssh-raspberry-pi

# Updating OS on raspberry pi (takes a long time)
https://jamesjdavis.medium.com/how-to-update-raspberry-pi-just-follow-these-easy-steps-ac507cf70238#:~:text=To%20update%20the%20Raspberry%20Pi,Raspberry%20Pi's%20library%20of%20applications.

sudo apt upgrade
sudo apt update
sudo apt dist-upgrade -y
sudo apt clean
sudo reboot

sudo rpi-update -y

sudo nano /etc/apt/sources.list
  Find this line in the file, and change stretch to buster:

    deb http://raspbian.raspberrypi.org/raspbian/ stretch main contrib non-free rpi

  Press Ctrl + X to save and exit
  
sudo apt-get remove apt-listchanges -y
sudo apt update
sudo apt --fix-broken install
sudo apt dist-upgrade -y
    <This will take some time>
    <answer No, when asked about DHCP Wins Servers>
    <answer Yes, when asked about restart services during package upgrades>
    <answer No, to installing a new playmouth version>
    <answer No, to the lightdm question>
sudo apt autoremove -y
sudo apt autoclean
sudo rebooot

