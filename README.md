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
echo "dtoverlay=diarmuid_dac" | sudo tee -a /boot/config.txt 
echo "dtdebug=on" | sudo tee -a /boot/config.txt 
echo "dtparam=i2c_arm=on" | sudo tee -a /boot/config.txt 
echo "dtparam=i2s=on" | sudo tee -a /boot/config.txt 

```

## Debug
```
sudo vcdbg log msg
sudo i2cdetect -y 1

```
