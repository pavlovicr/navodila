Reinstalacija :

Reinstalacija vsebine iz računalnika, ki že ima željeni commit file  v lastnemu Git Repo
::
	git reset --hard efgestujizlm098nhg

Reinstalacija vsebine iz githuba
::
	git fetch --install
	git reset --hard origin/stevilcenje

Reinstalacija psql baze. Bazo najprej zbrišemo
::
	psql bcs < arhiv010218

Migrate v django opravimo z migriranjem, ki kopira samo manjkajoče dele
::
	python manage.py migrate --fake-initial
