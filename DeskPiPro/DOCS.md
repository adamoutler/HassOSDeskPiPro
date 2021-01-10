# Configuration

![image](https://raw.githubusercontent.com/adamoutler/HassOSDeskPiPro/main/gitResources/Configuration.png)

## Celcius or Farenheit

Choose Celcius or Farenheit.

- **CorF** - Configures Celcius or Fahrenheit.

## Temperature Ranges

![image](https://raw.githubusercontent.com/adamoutler/HassOSDeskPiPro/main/gitResources/FanRangeExplaination.png)

Set your fan ranges appropriately.

- **LowRange** Minimum Temperature to turn on 33%. Temperatures less than this value will turn the fan off.
- **MediumRange** to be the temperature divider between 33 and 66%.
- **HighRange** to be the maximum temperature before 100% fan.

# Enable Serial

In order to enable Serial, you must add `dtoverlay=dwc2,dr_mode=host` to your config.txt. You can do this from a computer, a terminal addon, or from the hassio main terminal.

## Edit config.txt method

plug your sdcard or memory stick into a computer and modify the config.txt file.

```
dtoverlay=dwc2,dr_mode=host
```

## Terminal Addon method

If you have a terminal addon, you can disable protection mode and execute the following.

### Built-in hard drive

```mount /dev/sda1 /mnt
echo 'dtoverlay=dwc2,dr_mode=host' >> /mnt/config.txt
```

### SDCard

```mount /dev/mmcblk0p1 /mnt
echo 'dtoverlay=dwc2,dr_mode=host' >> /mnt/config.txt
```

## Hassio Main Terminal

Login to the main terminal, then at the ha> prompt, type "login".

```
echo 'dtoverlay=dwc2,dr_mode=host' >> /mnt/boot/config.txt
```

If problems are encountered please get all "Karen" in the foums and make sure to display attitude, because developers love that. Alternatively, you can provide a log and tell us the problem, what you did, the model of your device, and what happened differently than what you expected.
