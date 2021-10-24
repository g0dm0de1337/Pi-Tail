# Pi-Tail
re4son kernel und image funktionieren auf den raspberry pi zero.. hier eine anleitung

hier die anleitung auf englisch:
https://whitedome.com.au/re4son/pi-tail/

Image: Pi-Tail.img von dem Entwickler "re4son"
letztes update 2018
was nicht schlimm ist, da immernoch alles funktioniert, solange nicht updatet:
-nicht apt-get update/upgrade

re4son sein kernel sorgr dafür das Raspberry pi's in den monitor mode
gehen können, ohne eine zusatz w-lan karte
ladet hierfür folgende datei herrunter und kopiert sie
per Raspberry Pi Imager auf eine SD-Karte
https://whitedome.com.au/re4son/download/pi-tail/

https://downloads.raspberrypi.org/imager/imager_latest.exe
Raspberry Pi Imager

steckt diese nun in ein Raspberry Pi zero und startet ihn
indem ihr euer gerät strom gebt

stellt nun euer androide  ein

https://youtu.be/HwUJdM0aFXw

Hier zeige ich euch was ihr tun müsst, nachdem ihr das Image herruntergeladen habt, und es auf eine SD-karte mit hilfe von Raspberry Pi Imager, kopiert habt.
Dieses Image was von "re4son" zur verfügung gestellt wurde, ist komplett und bedarf KEIN "apt-get update/upgrade".. dieser vorgang würde dafür sorgen das eucher Pi-Tail nicht mehr funktioniert wie gewohnt

Hotspot name:
sepultura
Passwort:
R4t4m4h4tt4

in ConnectBot:
root@192.168.43.254

ssh/root passwort:
toor

mon0up
wifite
(crtl+c =beenden // mon0down beendet monitor mode)

Tipp: VNC kontrolle:
wenn ihr im "Pi-Tail" seid
gebt folgenden befehl ein:
vncserver

oben rechts auf die 3punkte klicken und auf "Port-weiterleitung" gehen
nickname:localhost
type: local
source port: 5901
destination: 127.0.0.1:5901

öffnet eine VNC app und fügt eine neue Verbindung hinzu:
name:PiTail0
adresse: 127.0.0.1:5901
user: root
passwort: toortoor


Es gibt eine Pi-Tail version von "kali.org"
dieses ist zwar aktueller, bedarf doch mehr konfigurationen..
anstatt bei ConnectBot root@192.168.43.254 müsstet ihr kali@192.168.43.254 eingeben und euer ssh passwort lautet kali statt toor
damit alles wie gewohnt funktioniert, geht wie folgt vor:

verbinden mit kali@192.168.43.254
passwort: kali
[jetzt seid ihr ein normaler user der immer sudo eingeben müsste.. um wieder root-user zu sein, tut folgendes..]
befehl:
- sudo passwd root
[da die neue kali version gar kein root passwort hat, fragt er euch direkt nach einem neuen]
- toor
- toor (bestätigung)
euer passwort ist nun wieder "toor"
beendet die jetzige verbindung und nutzt die root@192.168.43.254 mit dem standart passwort "toor"
(ist wichtig damit alle skripte wie gewohnt funktionieren)

https://github.com/trendy77/kaliPiBOOT
https://github.com/Re4son/
