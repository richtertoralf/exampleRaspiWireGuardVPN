# exampleRaspiWireGuardVPN
Aufbau eines einfachen VPN mittels WireGuard unter Nutzung von mehreren Raspberry Pi und LTE-Routern.
(Setting up a simple VPN with WireGuard using multiple Raspberry Pi and LTE routers.)  
Achtung: Das ist keine Drag-and-Drop Anleitung.  
WireGuard ist ein schnelles, einfaches und modernes VPN-Protokoll. Hier kannst du lesen, wie du ein eigenes VPN-System selbst einrichten kannst. 
**Hintergrundinfos zu WireGuard findest du hier [https://www.wireguard.com/](https://www.wireguard.com/)** 
## die Idee ##
![Netzwerk](WireGuard_Gartenlaube.png)
**Steuerung der Raspbery Pi und der angeschlossenen Geräte von unterwegs und von zu Hause, mit der Besonderheit, das die Raspberry Pi nur über das Mobilfunknetz erreichbar sind.**
## Ausgangssituation ##
Es gibt nicht überall Internet per Glasfaser. In vielen Regionen komme ich nur über das Mobilfunknetz (per LTE) ins Internet. Die [IPV4-Adressen sind knapp](https://de.wikipedia.org/wiki/IPv4#Adressknappheit) und viele Mobilfunkanbieter stellen deshalb keine öffentlichen IP-Adressen zur Verfügung. Deshalb funktionieren die traditionellen Lösungen mit [DynDNS](https://de.wikipedia.org/wiki/Dynamisches_DNS) nicht mehr.  
Jeder Mobilfunkrouter ist anders und hat mehr oder weniger gute Konfigurationsmöglichkeiten. Hier kommt jetzt WireGuard und die Cloud ins Spiel. Wir können ein VPN aufbauen ohne Router konfigurieren zu müssen. Wir benötigen keine [Portweiterleitungen](https://de.wikipedia.org/wiki/Portweiterleitung) und kein DynDNS.
