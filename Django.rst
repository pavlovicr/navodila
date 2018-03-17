DJANGO
======

Sortiranje : Poglej django dictsort
::
	class meta :
		ordering = ['stevilka']
		ordering = ['polje__stevilka'], če se sklicujemo na polje iz drugega classa. pazi 2x __

	druga možnost : v templates
			popisnapostavka.podrobnost.all|dictsort:"stevilka"

Grupiranje :
::
	<!-- v podrobnosti grupiramo object_list po po polju predmet_merila -->
	{% regroup objects_list by merilo.podlaga_merila.predmet_merila as ratata %}
	<!-- in zlistamo objekte "podrobnosti " po predmet_merila -->
	{% for podrobnosti in ratata %} {% podrobnosti.tekst %}{% endfor%}

		
**class Specifikacija**
	predmet = Foreignkey(PredmetSpecifikacije)

**class PredmetSpecifikacije**





Query s strani **"Specifikacija"**


a=Specifikacija.objects.all() .... print(a)..izpis vseh specifikacij

b=Specifikacija.objects.get(pk=1)..print(b)..izpis specifikacije s pk=1

c=b.predmet........................print(c)..izpis predmeta, ki pripada specifikaciji "b"

a[1].predmet.......................print(a[1].predmet) ..iz list(a) izpiše predmet specifikacije"c"


Query s strani **"PredmetSpecifikacije"**

a= PredmetSpecifikacije.get(pk=1)..print(a)...izpis "predmeta specifikacije" s pk=1

b= specifikacija_set.all().........print(b)...izpis vseh specifikacij predmeta specifikacije s pk=1





::
DJANGO
	pip3 install Django==1.11
	django-admin startproject kalk
	django-admin startproject . # s piko ne ustvari nepomembnega direktorija
