Idea based from Morrolinux's Pirate radio


# Sources
https://github.com/jobpassion/raspberryPi/blob/master/BluetoothSpeaker.md
http://www.instructables.com/id/Turn-your-Raspberry-Pi-into-a-Portable-Bluetooth-A/
https://github.com/morrolinux/mpradio

simple-agent

bluetooth connect 
pactl list sources short
/bin/su pi -c "parec -d bluez_source.68_C4_4D_A7_BF_1C.a2dp_source | sox -t raw -v 1.3 -G -b 16 -e signed -c 2 -r 44100 - -t wav - | sudo /home/pi/PiFmRds/src/pi_fm_rds -ps 'BLUETOOTH' -rt 'A2DP BLUETOOTH' -freq 103.8 -audio -"
