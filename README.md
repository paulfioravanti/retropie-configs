### RetroPie custom config files

These are the config files I am using for my [RetroPie](http://blog.petrockblock.com/retropie/) and [Emulation Station](http://emulationstation.org/) setup on my [Raspberry Pi Model B+](http://www.raspberrypi.org/products/model-b-plus/).

The config files reflect that I am using XBox 360 wireless controllers with a XBox 360 wireless gaming receiver for the emulators.

### Installation

Assumption is that the [RetroPie-Setup](https://github.com/petrockblog/RetroPie-Setup) instructions have been followed, especially the content in the repo's [wiki](https://github.com/petrockblog/RetroPie-Setup/wiki).  For me, this also meant: 

- [Overclocking the Raspberry Pi](https://github.com/petrockblog/RetroPie-Setup/wiki/Advanced-Configuration#sound-issues-and-overclocking) in order to get speed and sound working on some emulators.  My B+, using a 32GB Sandisk memory card, passed the stress test script included in the wiki section on overclocking. (Heatsinks seem to be recommended for overclocking, and since [my Raspberry Pi kit](http://www.canakit.com/raspberry-pi-starter-ultimate-kit.html) came with one I'm using it, but opinion varies as to whether they're actually needed). 
- Setting up the config for the XBox 360 controllers via petrockblog's [init script](https://github.com/petrockblog/RetroPie-Setup/wiki/Setting-up-the-XBox360-controller#3---init-script)

These files go under the `/opt/retropie/configs/` directory, where all custom config needs to go ([more info](http://blog.petrockblock.com/2014/07/01/major-update-for-retropie/)):

    $ cd /opt/retropie/configs
    $ git clone git@github.com:paulfioravanti/retropie-configs.git . 
    # dot on the end specifies current directory as the checkout directory,
    # which should also be empty

### Notable Deviations from default

- The default config for XBox 360 controllers on the NES emulator has the A and B buttons around the wrong way (it's unnatural to me, at least), so those buttons are switched for NES games 

### Other notes

- Resolution of screen can be set on a per-emulator basis by changing the values in `/etc/emulationstation/es_systems.cfg` (values for the `runcommand.sh` script are 0, 1, or 4. ([more info](https://github.com/petrockblog/RetroPie-Setup/blob/master/supplementary/runcommand.sh))
