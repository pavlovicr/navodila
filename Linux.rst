LINUX
========================

Ustvarjanje fajlov in vsebin
----------------------------

ustvari nov fajl
::
	touch vaja1.txt
insert tekst "miha kovacev" v vaja1.txt in zbriši predhodni tekst
::
	echo “miha kovacev” > vaja1.txt
insert nov tekst k predhodnemu
::
	echo "županova micka2 >> vaja1.txt
poglej vsebino fajla vaja1.txt
::
	cat vaja1.txt
ustvari nov fajl in kopiraj vsebino iz fajla vaja1.txt
::
	cat ”vaja1.txt” > vaja2.txt 

Omrežje
-------

nastavitev static IP na RPi
::
	vim /etc/network/interfaces
	auto eth0
	iface eth0 inet static
	address 89.212.90.184
	netmask 255.255.255.0
	gateway 89.212.0.1	