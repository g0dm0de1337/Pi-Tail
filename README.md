# Pi-Tail (German / Deutsch)
***
re4son Kernel und Kali Image funktionieren auf den Raspberry Pi Zero! Hier eine Anleitung...

Hardware:

- Rasperry Pi Zero
- SD Card mit mindestens 8GB Speicherplatz
- Internetverbindung
- Zeit und ein bisschen Gedult :)

***
Führt kein Upgrade oder Update des Systems durch! Oder es kann zu ungewöhlichen Verhalten oder sogar Abstürze führen wenn nicht sogar das komplette System unbrauchbar machen..! 

re4son's Kernel erlaubt es dem Raspberry Pi, vom Managed Mode in den Wi-Fi Monitor Mode
zu wechseln, ohne das ein zusätzlicher Wi-Fi Dongle benötigt wird.

## Installation
Lade hierfür folgende Dateien herunter und speichere sie an einem Ort wo du sie einfach findest.


Image: Pi-Tail.img
Entwickler: re4son
Letztes Update:
2018
> wget https://docs.google.com/u/0/uc?id=1ZJc6p9e1fGLhuM-0hVn177i_VXL99aW4&export=download#Pi-Tail-180925.img.xz

Raspberry Pi Imager
> https://downloads.raspberrypi.org/imager/imager_latest.exe
***

Wenn alle benötigten Dateien heruntergeladen wurde, öffne das heruntergeladene Programm Rasperry Imager.
Nun solltest du die Möglichkeit haben, die SD Card auszuwählen sowie das heruntergeladene Image.
Vergewissere dich, das du bei der Auswahl der SD Card den gleichen Buchstaben erwischst, wie im Windows Explorer angezeigt. Wenn alles passt, dann starte Imager mit dem schreiben des Images auf die SD Card.
***
***

# Android Setup
Visualisierte Installations Guide:
> https://youtu.be/HwUJdM0aFXw

ConnectBot im Play Store herunterladen:
> https://play.google.com/store/apps/details?id=org.connectbot&hl=de_CH&gl=US

Hotspot: Um überhaupt mit dem Rasperry Pi Zero kommunizieren zu können, werden ein paar Einstellungen vorgenommen in den Hotspot Einstellungen von Android

Hotspot Name:
- sepultura

Passwort:
- R4t4m4h4tt4


Für ConnectBot sind diese Einstellungen ZWINGEND vorrausgesetzt
ConnectBot:
- root@192.168.43.254

root Passwort:
- toor
***

** Tipps & Tricks

- mon0up
- wifite
> (crtl+c = beenden // mon0down beendet Monitor Mode)

***
___________________________
***

VNC:
Wenn ihr im Pi-Tail eingeloggt seid
gebt folgenden Befehl ein um VNCServer zu starten
- vncserver

Danach erscheint ein Fenster. Oben rechts auf die drei Punkte klicken und auf "Port-weiterleitung" auswählen. Hier da dazu benötigten Einstellungen:

- nickname: localhost
- type: local
- source port: 5901
- destination: 127.0.0.1:5901
***

Für VNC App:
- name: PiTail0
- adresse: 127.0.0.1:5901
- user: root
- passwort: toortoor
***
***

### FAQ & Misc

# Es gibt eine Pi-Tail version von "kali.org"

> (momentan kali-linux-2021.3-rpi0w-pitail-armel.img.xz)

Dieses Image ist zwar neuer als das verwendet Image von hier, jedoch bedarf es noch mehr an Konfiguration.

Damit alle Skripte wie gewohnt funktionieren, muss du als root angemeldet sein. Seit Kali 2020 muss das Password von root erst vergeben werden. Dies ist schnell und unkompliziert erledigt:
***
Ersetzt bei ConnectBot / Anderes VNC/SSH App

> root@192.168.43.254

gegen
> kali@192.168.43.254 

Das neue Userlogin/SSH Passwort lautet:
> kali (statt toor)

damit alles wie gewohnt funktioniert, geht wie folgt vor:
verbinden mit 
> kali@192.168.43.254
> kali
- Root password fehlt... Also ergänzen wir diesen:
> sudo passwd root


Da die Neue Kali Version kein root password verlangt, wird ihr direkt nach einem neuen Password gefragt
Hier verwenden wir "toor" als Password (Pre Kali 2020 Images)
> toor
> toor     

(..als Bstätigung)
- [Passwort ist nun wieder "toor"]

Das Password wurde nun root erfolgreich zugewiesen. Nun können wir uns als root anmelden und alle Skripte funktioneren wieder gemäss Kali 2019 (Als Referenz)
> su
> toor

***
# [Trick]
Falls ihr euch bei diesem Image mit der ConnectBot App mit root einloggen wollt, folgende Schritte:
verbinden mit: 
> kali@192.168.43.254
- passwort: 
> kali
- passwd
Kali wird euch nach einem neuen Password fragen. Dies ist bestehend als "kali" definiert und sollte in diesem Fall angepasst werden:

> kali
> toortoor 
- [Neues Kali Passwort]
> toortoor 
- [Zur Verifizierung]
***
> Trennt die aktive Verbindung, ändert das neue Password in den bestehenden Passwordfelder in der ConnectApp / SSH App / VNC App

## Referenzen:
Raspberry Pi Kernel Dev:
- https://github.com/Re4son/
(Anleitung auf Englisch:
- https://whitedome.com.au/re4son/pi-tail/)
