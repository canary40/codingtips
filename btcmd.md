bluetooth & cmd

----------------------------------------------------------------------

btcom

https://bluetoothinstaller.com/bluetooth-command-line-tools
https://gist.github.com/joshjm/69dcef304386e928c10c9534c73c3a04

00:bb:43:99:ed:40

btcom -b "XX:XX:XX:XX:XX:XX" -c

connect:
btcom -r -b aa:bb:cc:dd:ee:ff -s110b
btcom -c -b aa:bb:cc:dd:ee:ff -s110b

disconnect:
btcom -r -b aa:bb:cc:dd:ee:ff -s110b

ahk & btcom

connect:
#c::
  Run, %ComSpec% /c btcom.exe -r -b "aa:bb:cc:dd:ee:ff" -s111e , ,Min
  RunWait, %ComSpec% /c btcom.exe -r -b "aa:bb:cc:dd:ee:ff" -s110b , ,Min
  Run, %ComSpec% /c btcom.exe -c -b "aa:bb:cc:dd:ee:ff" -s110b , ,Min
Return

disconnect:
 #+c::
  Run, %ComSpec% /c btcom.exe -r -b "aa:bb:cc:dd:ee:ff" -s111e , ,Min
  Run, %ComSpec% /c btcom.exe -r -b "aa:bb:cc:dd:ee:ff" -s110b , ,Min
Return

----------------------------------------------------------------------

btpair

btpair -n "devicename"
btpair -b "XX:XX:XX:XX:XX:XX"
for PIN: btpair -p 1234 -n "devicename"

--------------------------------------------------------------------

https://superuser.com/questions/408302/how-can-i-script-a-bluetooth-device-to-connect-disconnect
https://www.reddit.com/r/DS4Windows/comments/xjq714/ds4_auto_connect_using_btpair_from_bluetooth/

----------------------------------------------------------------------

