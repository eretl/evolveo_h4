# evolveo_h4
Remote control mappings for Evolveo H4 CoreELEC/LibreELEC

# How to install
SSH in to the Evolveo H4

Stop kodi  
`systemctl stop kodi`  
`systemctl stop eventlircd`  

Save [evolveo_h4.txt](evolveo_h4.txt) to `/storage/.config/rc_keymaps/`  
Add at the end of `/storage/.config/rc_maps.cfg` contents of [rc_maps.cfg](rc_maps.cfg)   

Load new configuration `ir-keytable -a /storage/.config/rc_maps.cfg -s rc0`  

Start kodi  
`systemctl start eventlircd`  
`systemctl start kodi`  

# How to generate remote codes
SSH in to the Evolveo H4

Stop kodi  
`systemctl stop kodi`  
`systemctl stop eventlircd`  

`ir-keytable -t`
Start pressing buttons on remote, HEX codes will be displayed.

Create your txt file with key mapings. All keycodes are in [keycodes.txt](keycodes.txt).  


# Source
https://forum.libreelec.tv/thread/11643-le9-0-remote-configs-ir-keytable-amlogic-devices/  
