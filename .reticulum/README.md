## Why Reticulum?

[Brief intro](https://pad.puscii.nl/p/reticulum_introduction)

## How to Reticulum

0. Optional: Create a conda environment

Best practice for all projects. 

At the terminal run the following:
`conda create -n mesh python=3.13`

`conda activate mesh`

1. Install and run reticulum tool

`pip install rnsd`

`rnsd`

2. Update config file

Copy text from example `config` file into `USERNAME/.reticulum/config`

Update any settings as you see fit. You can run `rnsd --exampleconfig > ~/.reticulum/example-config.txt` to generate a well-commented config file for reference.

3. Optional: Flash your LoRa Rnode if you have one

Find your device's port: `$ ls /dev/tty*`

Use the flash utility to run an  
`$ pip install rnodeconf`
`$ rnodeconfig --autoinstall`

Follow the onscreen instructions. You may need to run it twice or add a `--baud-rate 125000` flag in order to complete the flashing process successfully.

## How to Nomadnet

1. Install and start nomadnet from terminal, or another messaging client

`$ pip install nomadnet`

`$ nomadnet`

2. Share your address with other users
   
   You can find your address under the `Network` tab, at the bottom left hand size of the interface.

   Change your name from `Anonymous Peer` to a new name of your preference.

   Copy the `LXMF Address` and share with your pals.

4. Experiment with the different sections, including `Conversations` and `Networks` reading the guide.
   
5. Make a Page to introduce yourself to your network.

6. Try out other clients like Sideband or MeshChatX if you prefer.






