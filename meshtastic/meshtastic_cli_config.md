# Meshtastic node setup using command line interface

`pip install meshtastic` or `pip3 install meshtastic`

Download the node's firmware here: https://github.com/meshtastic/firmware/releases/ select file based on your node model

- For the Seeed Studio Xiao Kit: `firmware-esp32s3-2.7.26.54e0d8d` is most recent at time of this writing (03.07.2026)

- Unzip the file and you have a folder with the same name

From terminal, change directory using `cd` into that folder of firmware files. In my case it was `cd Downloads/firmware-esp32s3-2.7.26.54e0d8d`

Use command `ls -a /dev/tty*` to find port name where your node is plugged into usb port

Run `./device-install.sh -f firmware-seeed-xiao-s3-2.7.26.54e0d8d.factory.bin -p /dev/tty.usbmodem2101` or other port name to run flasher. may need to run twice, can try first without port flag

`meshtastic --info` to test if it worked, try with phone, or use CLI to set params

All together in one command (change the name for each)
`meshtastic --set lora.region EU_868 --set security.admin_key base64:zhSuVvaywubn9tTUoVwRFaSYZEYH7joeLE0I0JY0hH0= --ch-index 2 --ch-set psk base64:cWpuRGhrQlZYbEYwUHNnTnlHRmNwVUprQkNWaVVWZ3A= --ch-set name khmesh --ch-set module_settings.position_precision 32 --set-owner 'CSXX' --set-owner-short 'CSXX'`

`meshtastic --info` again to test if it worked, try with phone

Here are the individual commands:

`meshtastic --set lora.region EU_868 --set security.admin_key base64:zhSuVvaywubn9tTUoVwRFaSYZEYH7joeLE0I0JY0hH0=` to set the region and remote admin ability

`meshtastic --set-owner 'CSXX' --set-owner-short 'CSXX'` to set the new name (replace XXs with number of node)

`meshtastic --ch-index 2 --ch-set psk base64:cWpuRGhrQlZYbEYwUHNnTnlHRmNwVUprQkNWaVVWZ3A= --ch-set name khmesh --ch-set module_settings.position_precision 32` to set channel attributes (psk is the encryption key)

`meshtastic --ch-index 3 --ch-set psk base64:JO8zmnnMnPeLCzFgAUPEr+6bbdwTR/DS9fi+EQ4JRi0= --ch-set name codeship --ch-set module_settings.position_precision 32` 

`meshtastic --ch-index XX psk random --ch-set name "My Channel"` to set additional channels. get the key from another node where it's been set and use `base64:KEY`, or create it using `psk random` which has high level encryption



