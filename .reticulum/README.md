## Why Reticulum?

## How to Reticulum

0. Optional: Create a conda environment

Best practice for all projects. 

`$ conda create -n mesh python=3.13`
`$ conda activate mesh`

1. Install reticulum tool

`$ pip install rnsd`

2. Update config file

Copy `config` file into `USERNAME/.reticulum/`

Update any settings as you see fit, or run `rnsd --exampleconfig` to generate a well-commented config file

3. Optional: Flash your LoRa Rnode if you have one

Find your device's port: `$ ls /dev/tty`

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

3. Experiment with the different sections, including `Conversations` and `Networks` reading the guide.
   
4. Make a Page to introduce yourself to your network.

5. Try out other clients like Sideband or MeshChatX if you prefer.






