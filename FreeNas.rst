FreeNas
===========

Splošno :


OPERACIJSKI SISTEM :
* na dveh enakih USB ključih s priporočenimi 32 GiB , ki sta oba priključena med instalacijo
* boljše rezultate dosežemo s SSD diski vendar pobirajo prostor HDD diskom.


RAM :

*Jals niso ravno požrešni, kak -Giga je dobrodošel
*Dedupliciranje je požrešno in zahteva 5 Giga na Tera diska
*VM 1Giga na mašino
*izklopiti video kartico v biosu


SINHRONIZACIJA Z MEGA :

* nastavitev Cloud credential v System
* in opravila v Cloud Sync Tasks v Tasks






SNAPSHOTS :

* se hranijo na datasetu na katerem so narejeni ,  v skritemu direktoriju .zfs
*PAZI, samo če označimo recursiv se ustvarijo snapshoti na vseh podrejenih datasetih.
V nasprotnem bodo podatki v podrejenih datasetih izgubljeni
* v tasks je mogoče nastaviti ya vsak dataset avtomatsko izvajanje snapshotov.Pazi,
 da je vključen "Enabled" sicer ne bo nič s snemanjem.
*tudi prek putty lahko izvajamo snapshote v shellu


Wake on LAN (WOL) support depends on the FreeBSD driver for the interface. If the driver supports WOL, it can be enabled using ifconfig(8). To determine if WOL is supported on a particular interface, use the interface name with the following command. In this example, the capabilities line indicates that WOL is supported for the re0 interface:




















instalacija linux
^^^^^^^^^^^^^^^^^

Zahteve :

* python3
* virtualno okolje
* direktorij docs znotraj vaja
* iz direktorija docs zaženemo sphinx-quickstart


Instalacija :

::

   $ pip install sphinx sphinx-autobuild
   $ mkdir vaja
   $ cd vaja
   $ mkdir doc
   $ sphinx-quickstart


Pretvorba v html lokalno (znotraj docs) :
::

   $ make html

Test :
::

  $ sphinx-autobuild . _build/html






instalacija v windows
^^^^^^^^^^^^^^^^^^^^^

Zahteve :

* instalacija pythona3 za windows
* git za windows


* pravzaprav popolnoma enako kot v linuxu, le malo drugače aktiviramo virtualno
* gremo v CMD terminal , kjer je instaliran python
* instaliramo aplikacijo za virtualno okolje in ustvarimo naše virtualno okolje "virtualno"
* aktiviramo naše virtualno okolje
* instaliramo sphinx ali sphinx autobuild
* kjerkoli (virtualno) ustvarimo dirktorij našega projekta vaja in znotraj vaje docs
* znotrj docs poženemo sphinx-quickstart
* v failu indeks.rst imenujemo rst fajle, ki jih bomo videli
::
