# Pi-Tail Komplett
> auf Deutsch
***

(hier die anleitung auf englisch:
https://whitedome.com.au/re4son/pi-tail/)

re4son kernel und image funktionieren auf den raspberry pi zero.. hier eine anleitung...

***

Image: Pi-Tail.img von dem Entwickler "re4son"
letztes update 2018
> Pi-Tail-180925.img.xz (2,2G)

..nicht das aktuellste .img, dennoch funktioniert noch alles, solange man nicht updatet:
- nicht apt-get update/upgrade
***
re4son sein kernel sorgt dafür das Raspberry pi's in den monitor mode
gehen können, ohne eine zusatz w-lan karte... 
> ladet hierfür folgende datei herrunter und kopiert sie
> per "Raspberry Pi Imager" auf eine SD-Karte
https://whitedome.com.au/re4son/download/pi-tail/

https://downloads.raspberrypi.org/imager/imager_latest.exe
"Raspberry Pi Imager"

steckt diese nun in ein Raspberry Pi zero und startet ihn
indem ihr euer gerät strom gebt

***
***

stellt nun euer android ein:
(WiFi-Hotspot einstellen &ConnectBot)

# https://youtu.be/HwUJdM0aFXw

# Hier zeige ich euch was ihr tun müsst, nachdem ihr das Image herruntergeladen habt, und es auf eine SD-karte mit hilfe von Raspberry Pi Imager, kopiert habt.
Dieses Image, was von "re4son" zur verfügung gestellt wurde, ist komplett und bedarf KEIN "apt-get update/upgrade".. dieser vorgang würde dafür sorgen das eucher Pi-Tail nicht mehr funktioniert wie gewohnt
***
Hotspot Name:
- sepultura

und das Passwort:
- R4t4m4h4tt4
***
***
in ConnectBot:
- root@192.168.43.254

ssh/root Passwort:
- toor
***
- mon0up
- wifite
> (crtl+c =beenden // mon0down beendet monitor mode)

***
___________________________
***

# Tipp: VNC kontrolle:
wenn ihr im "Pi-Tail" seid
gebt folgenden befehl ein:
- vncserver
***
oben rechts auf die 3punkte klicken und auf "Port-weiterleitung" gehen
- nickname: localhost
- type: local
- source port: 5901
- destination: 127.0.0.1:5901
***
öffnet eine VNC app und fügt eine neue Verbindung hinzu:
- name: PiTail0
- adresse: 127.0.0.1:5901
- user: root
- passwort: toortoor

__________________________
***

***

# Es gibt eine Pi-Tail version von "kali.org"
> (momentan kali-linux-2021.3-rpi0w-pitail-armel.img.xz)
dieses ist zwar aktueller, bedarf doch mehr konfigurationen


***
> !!!
ihr müsst als Root-User unter kali-tail unterwegs sein, damit alle skripte wie gewohnt funktionieren..
kali.org hat das img. zwar auf den neusten stand gebracht und alle Skripte mit importiert, nun ist es aber so das man bei der kali 2018 version komplett als root-user unterwegs ist, was seit der neusten 2020 version unter kali NICHT mehr der fall ist.. 
entweder passt ihr alle befehle mit "sudo" an,{dazu müsst ihr auch teils die skripte bearbeiten} 
oder ihr wendet eines, der von mir gegebenden "Tricks" an um das problem zu lösen
> !!!
***

***
# [Trick 1]
> ersetzt bei ConnectBot..
> root@192.168.43.254 mit..
- kali@192.168.43.254 

> euer ssh passwort lautet:
- kali 
> (statt toor)

damit alles wie gewohnt funktioniert, geht wie folgt vor:
verbinden mit 
- kali@192.168.43.254
- kali
> [jetzt seid ihr ein normaler user der immer sudo eingeben müsste !!]
> 
***
> um wieder root-user zu sein, tut folgendes..
befehl:
- sudo passwd root
> [da die neue kali version gar kein root passwort hat, fragt er euch direkt nach einem neuen]
- toor
- toor     (..als bestätigung)
> [euer passwort ist nun wieder "toor"]
- su
- toor
> jetzt seit ihr wieder der gewohnte Root-User
***

***
# [Trick 2]
---> wenn ihr euch bei diesem img, über ConnectBot mit root einloggen wollt, tut folgendes !!! <---
verbinden mit: 
- kali@192.168.43.254
> passwort: 
- kali
***
- passwd
> [er fragt euch nach eurem kali passwort was zur Zeit noch "kali" ist (ssh passwort).. also:]
- kali
- toortoor 
> [neues kali passwort]
- toortoor 
> [zum bestätigen]
***
> trennt die aktive verbindung und erstellt einen neuen host:
- root@192.168.43.254
***
> verbindet euch mit root@192.168.43.254
> und gebt 
- toortoor
> als passwort ein
***
***

***
ihr müsst als Root-User unter kali-tail unterwegs sein, damit alle skripte wie gewohnt funktionieren..
kali.org hat das img. zwar auf den neusten stand gebracht und alle Skripte mit importiert, nun ist es aber so das man bei der kali 2018 version komplett als root-user unterwegs ist, was seit der neusten 2020 version unter kali NICHT mehr der fall ist.. 
entweder passt ihr alle befehle mit "sudo" an,{dazu müsst ihr auch teils die skripte bearbeiten} 
oder ihr wendet eines, der von mir gegebenden "Tricks" an um das problem zu lösen
***

https://github.com/trendy77/kaliPiBOOT
https://github.com/Re4son/
