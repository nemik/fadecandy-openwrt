This is a port of Micah "scanlime"'s fcserver for OpenWRT. The awesome Fadecandy project is here: http://github.com/scanlime/fadecandy

fcserver provides a websocket server interface for interacting with Micah's Fadecandy or Teensy3 (running fadecandy firmware)  devices over USB.

To install this to use it on your OpenWRT buildroot, just add "src-git fadecandy git://github.com/nemik/fadecandy-openwrt.git" to your feeds.conf.default file in your buildroot. Then run "./scripts/feeds update -a" then "./scripts/feeds install -a". Then run "make menuconfig" and to install "fcserver" from the Utilities menu option.

The default config for fcserver is "fserver.config" and resides in /etc/ on the filesystem. It listens for websocket and HTTP requests on port 7890 from any remote host. An init file for it is also provided so that fcserver can automatically run on startup.
