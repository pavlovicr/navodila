READTHEDOCS
===========


`Getting Started`_.

.. _Getting Started: https://docs.readthedocs.io/en/latest/getting_started.html


Splošno : 

* aplikacija za oblikovanje teksta in objavo na internetu
* sphinx oblikovanje teksta lokalno v html formatu
* vaja je direktorij s katerga bomo pošiljali v vaja na github
* spletna stran ReadTheDocs za javno objavo 
* aplikacija deluje v pythonu 3 , priporočljivo jo je inštalirati v virtualnem okolju
* za django si poglej poglavje Read the Docs features 


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
   
   > pip install virtualenv
   > virtualenv virtualno
   > cd /virtualno/Scripts
   > activate
   > pip install sphinx sphinx-autobuild
   > mkdir vaja
   > cd vaja
   > mkdir docs
   > cd docs
   > sphinx-quickstart 


   

Oblikovanje :
^^^^^^^^^^^^^^

text = """
.. _top:

Hello word
----------



(1) zamiki

* zamik "*"
  
  - zamik še enkrat "-"

    + in še enkrat
