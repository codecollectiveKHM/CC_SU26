## Why Reticulum?

[Brief intro](https://pad.puscii.nl/p/reticulum_introduction)

## Part 1: How to Reticulum

0. Optional: Create a conda environment

Best practice for all projects. 

At the terminal run the following:

`conda create -n mesh python=3.13`

`conda activate mesh`

1. Install and run reticulum tool

Install Reticulum utilities: `pip3 install rns` (or try `pip` instead of `pip3` everywhere, depending on which version of python you have installed)

Run Reticulum network: `rnsd` 

If you get an error that says `lxmf` is missing (that's the chat module), you may also need to install it: 

`pip3 install lxmf`

Then try running `rnsd` again. You should have a message saying that it has started.

2. Update config file

Copy text from `config` file into your own harddrive's `USERNAME/.reticulum/config` (on Mac, may be [elsewhere](https://reticulum.network/manual/gettingstartedfast.html) on linux/win)

Update any settings as necessary. Optional: You can run `rnsd --exampleconfig > ~/.reticulum/example-config.txt` to generate a well-commented config file for reference.

Restart. Hit the `cntrl` key + `C` to kill the running process, then run `rnsd` again to start Reticulum with your updated configuration. 

In another terminal window, check `rnstatus` to see if you're up and running. You should see at least list of at least a couple Reticulum interfaces that have the status 'up'.

3. Optional: Flash your LoRa Rnode if you have one

Use the firmware flash utility to run:

`rnodeconfig --autoinstall`

You may also need to append the physical location of your device by finding its port. Find your device's port by typing into the terminal: 

`ls /dev/tty*`

Then look in the list for the item that sounds most like your device. Try running the config again with the specific device location.

You may also need to run it twice or add a `--baud-flash 125000` flag in order to complete the flashing process successfully. 

Your command may end up looking like this, for example:

`rnodeconfig /dev/tty.USB1101 --autoinstall --baud-flash 125000` 

Follow the onscreen instructions to choose your model and your correct bandwidth (in EU 868 mH). 

===

## Part 2: How to Nomadnet

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






