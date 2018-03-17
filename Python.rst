PYTHON
======

instalacija Pythona
-------------------

download iz https://www.python.org/downloads/python3.6.3
iz download direktorija Python-3.6.3 izvršimo ukaze
::
    ./configure
    sudo make
    sudo make install

delo z moduli
-------------

informacije o modulu datetime dirktno iz linux terminala
::
	pydoc datetime

kodo, ki je vpisana pod tem izrazom zažene samo takrat, ko poženemo izvirni fajl
in ne z >>> import mojmodul.
Koristno pri delu s testi, ki so sestavni del kode na istem fajlu
::
	if __name__ == '__main__':

instalacija lastnih modulov v site-packages, ki se nahaja v 
home/pavlovicr/virtualno_test/lib/python3.5/site-packages
::
	>>> import sys
	>>> sys.path.append('~/vaja')
	>>> import vaja 
	>>> import primer

izpis imena modula , ki je bil importan 
primer za ime modula 'time'
::
	>>> import time
	>>> time.__name__	 
delo s časom 
::
	>>> import datetime
primer tekoče ure
	>>>a=datetime.datetime.now().hour
lahko tudi
	>>> import datetime
	>>> from datetime import datetime
	>>> a=datetime.now()
	>>> a.hour
	>>> a.minute
	>>> a.day
primer 12 sekund do izklopa
::
	>>>import time	
	>>>time.sleep(12)
primer današnji dan
::
	>>>time.localtime().tm_mday
primer danes
::
	>>>time.asctime()

razno
-----

pip
--- 

::
	sudo apt-get install python3-pip pip3 install –upgrade pip
	sudo apt-get install python3-pip
	pip3 install --upgrade pip


seznam instaliranih programov
::
	pip freeze

testiranje
izpis izvajanja testa kode, ko je test sestavni del kode
::
	python vaja.py -v


VIRTUALNO OKOLJE
----------------
VIRTUALNO OKOLJE
^^^^^^^^^^^^^^^^

sudo pip3 install https://github.com/pypa/virtualenv/tarball/master je opcija z zadnjo verzijo
LOCAL je ime novega virtualnega okolja, ki ga bomo rabili za development
::

    sudo pip3 install virtualenv 
    sudo pip3 install https://github.com/pypa/virtualenv/tarball/master    
    virtualenv local(moje virtualno okolje) 

    virtualenv -p python3 local
    pip install --upgrade virtualenv

OKOLJE ZA DEVELOPMENT(local)
^^^^^^^^^^^^^^^^^^^^^

mogoče je treba s sudo pip3
v requirements/local.txt so naloženi programi za development
::
	source LOCAL/bin/activate
	pip install -r requirements/local.txt


