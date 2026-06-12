## Why Reticulum?

[Brief intro](https://pad.puscii.nl/p/reticulum_introduction)

## How to Reticulum

0. Optional: Create a conda environment

Best practice for all projects. 

At the terminal run the following:
`conda create -n mesh python=3.13`

`conda activate mesh`

1. Install and run reticulum tool

Install Reticulum utilities: `pip install rns`

Run Reticulum network: `rnsd -v` 

The `-v` flag is for 'verbose', which helps if there's troubleshooting to do, and otherwise you can leave it off.

2. Update config file

Copy text from `config-example.text` file into your own harddrive's `USERNAME/.reticulum/config` (on Mac, may be [elsewhere](https://reticulum.network/manual/gettingstartedfast.html) on linux/win)

Update any settings as necessary. Optional: You can run `rnsd --exampleconfig > ~/.reticulum/example-config.txt` to generate a well-commented config file for reference.

Restart. Hit the `cntrl` key + `C` to kill the running process, then run `rnsd` again to start Reticulum with your updated configuration. 

In another terminal window, check `rnstatus` to see if you're up and running.

3. Optional: Flash your LoRa Rnode if you have one

Find your device's port: `$ ls /dev/tty*`

Use the flash utility to run an  

`$ pip install rnodeconf`

`$ rnodeconfig --autoinstall`

Follow the onscreen instructions. You may need to run it twice or add a `--baud-flash 125000` flag in order to complete the flashing process successfully. You may need to designate the device port.

## How to Nomadnet

1. Install and start nomadnet from terminal, or another messaging client

`$ pip install nomadnet`

`$ nomadnet`

2. Share your address with other users
   
   You can find your address under the `Network` tab, at the bottom left hand size of the interface.

   Change your name from `Anonymous Peer` to a new name of your preference.

   Copy the `LXMF Address` or QR code and share with your pals.

4. Experiment with the different sections, including `Conversations` and `Networks` reading the guide.
   
5. Make a Page to introduce yourself to your network. See instructions in the `Config` section

6. Try out other clients like Sideband or MeshChatX if you prefer.






