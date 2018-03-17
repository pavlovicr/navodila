COOKIECUTTER
============

Project templates ali po domače, aplikacija s katero izdelamo predloge za instalacijo in nastavitve aplikacij.

`Getting Started`_.

.. _Getting Started: http://cookiecutter.readthedocs.io/en/latest/first_steps.html

Splošno :

* Za Windows in Linux

Zahteve :

* Python 2.7, 3.3, 3.4 ,3.5, 3.6 

Instalacija :
::
     
    pip install --upgrade cookiecutter

Izdelajmo enostaven primer predloge.
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
::

$ mkdir predloga
$ cd predloga
$ mkdir {{cookiecutter.ime_direktorija}}
$ cd {{cookiecutter.ime_direktorija}}
$ touch {{cookiecutter.file_ime}}.py

v file {{cookiecutter.file_ime}}.py vpišemo 
::

   print("Zdravo, {{cookiecutter.prejemnik_pozdrava}}!")

v direktoriju predloga ustvarimo še file cookiecutter.json 
::

$ touch cookiecutter.json

in vanj vpišemo
::

   {
    "ime_direktorija": "Zdravo",
    "file_ime": "pozdravi",
    "prejemnik_pozdrava": "Miha"
   }


    git clone git@github.com:audreyr/cookiecutter-pypackage.git


