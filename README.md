# audio_dac

## Install
```
sudo apt-get install -y i2c-tools

```

## Compiling
```
dtc -@ -Hepapr -I dts -O dtb -o diarmuid_dac.dtbo diarmuid-dac-overlay.dts 
sudo cp diarmuid_dac.dtbo /boot/overlays/
```
## Add to config
```
sudo echo "dtoverlay=diarmuid_dac" >> /boot/config.txt 
sudo echo "dtdebug=on" >> /boot/config.txt 
```

## Debnug
```
sudo vcdbg log msg

```
