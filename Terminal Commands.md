# Write these codes in the Terminal
wget https://www.kernel.org/pub/linux/bluetooth/bluez-5.18.tar.xz

dpkg --get-selections | grep -v deinstall | grep bluez

tar xvf bluez-5.18.tar.xz

sudo apt-get install libglib2.0-dev libdbus-1-dev libusb-dev libudev-dev libical-dev systemd libreadline-dev

cd bluez-5.18

./configure --enable-library

make -j8 && sudo make install

sudo cp attrib/gatttool /usr/local/bin/

cd

hcitool dev

sudo hcitool lescan

sudo gatttool -t random -b  -I

connect 

primary
