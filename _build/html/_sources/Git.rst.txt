GIT
======

instalacija
::
	sudo apt-get install git
posodobi zadnjo verzijo
::
	git clone git://git.kernel.org/pub/scm/git/git.git
nastavitve uporabnika
::
	git config --global user.name "pavlovicr"
	git config --global user.email pavlovicrados@gmail.com

prelistajmo nastavitve in spremenimo nastavitve 
::
	git config --list
	vim ~/.gitconfig 

osnovne komande
^^^^^^^^^^^^^^^
inicializacija direktorija v katerem bomo izvajali git ukaze
::
	git init
dodamo spremembe
::
	git add .
pospremimo spremembe
::
	git commit -m "spremljajoci tekst" -a  
dve muhi na en mah
::
	git commit -a -m "spremni tekst"
ustvari nov repository na GitHub in remot povezavo
::
	git remote add origin https://github.com/pavlovicr/udpp.git

ko origin že obstaja, ga izbrišemo z  	
::
	git remote rm origin  
ko nas sprašuje za uporabniško ime
::
	git remote set-url origin git@github.com:pavlovicr/udpp.git

priprava kljuca
^^^^^^^^^^^^^^^
v linux terminalu ustvarimo ssh ključ
na vprašanja odgovorimo z enter
gremo v fail ~/.ssh/id_rsa.pub in skopiramo ključ
v GitHub v settings generiramo nov ključ s kopiranjem kode iz id_rsa.pub  
::
	ssh-keygen -t rsa -C "pavlovicrados@gmail.com"
	vim  ~/.ssh/id_rsa.pub


ostale komande
^^^^^^^^^^^^^^
kakšne so razlike, ki še niso ažurirane v gitu
::
	git diff
	git diff --staged
kje smo z gitiranjem
::
    git status
unstage file
::
	git reset mojfile
poglej naslov remota
::
	git remote -v
kloniraj vsebino iz remota
::
	git clone git@github.com:pavlovicr/udpp.git
	git clone https://github.com/pavlovicr/udpp.git






