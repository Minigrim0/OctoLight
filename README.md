# OctoLight
A simple project to add an RGB strip Led to an Ender5 printer, using an OrangePI with OctoPrint

# Installation

The next commands are following adafruit's [official documentation](https://learn.adafruit.com/circuitpython-on-orangepi-linux/orange-pi-pc-setup)

### Install libgpiod
```bash
# As Root
cd ~
wget https://raw.githubusercontent.com/adafruit/Raspberry-Pi-Installer-Scripts/master/libgpiod.sh
chmod +x libgpiod.sh
./libgpiod.sh
```

### Make sure the board is up-to-date
```bash
sudo apt update
sudo apt upgrade
```

### Upgrade python packages
In adafruit's tutorial they seem to do it globally, I'll just do it in my virtualenv
```bash
python3 -m venv ve
source ve/bin/activate
pip install --upgrade setuptools
pip freeze - local | grep -v '^\-e' | cut -d = -f 1 | xargs -n1
pip install -U
```

### Enable UART, I2C and SPI
```bash
sudo apt-get install -y python-smbus python-dev i2c-tools
sudo adduser pi i2c
```

# MQTT
...
