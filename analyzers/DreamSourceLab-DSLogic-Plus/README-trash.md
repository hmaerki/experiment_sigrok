# Experiment without success

https://sigrok.org/wiki/DreamSourceLab_DSLogic#Firmware
Install firmware
sudo ./sigrok-fwextract-dreamsourcelab-dslogic.sh 
[sudo] password for maerki: 
Installing into: /usr/local/share/sigrok-firmware

then
sigrok-cli --driver=dreamsourcelab-dslogic -l 5 --scan
