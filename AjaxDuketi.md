Ajax je tehnika za ucitavanje podataka u dio stranice bez da se cjela stranica mora refresovati. Podatci se cesto salju u formatu JsoN(JavaScript Object Notation)

MOgucnost ucitavanje novog sadrzaja u dio stranice poboljsava 'user experience' jer korisnik ne treba da ceka da se cjela stranica ucita ako samo dio nje se treba ucitati.

Ovo je dovelo do popularizacije, tako zvanih "single page web aspps" web based tools koji se vise ponasaju kao software aplikacije, bez obzira sto se pokrecu u browseru.

Ovao Poglavlje pokriva:

* Sta je Ajax
    * Ajax dozvoljava da trazis podatke sa servera i ucitas ih bez da refresujes cjelu stranicu. 
    
* Formati Podataka
    * Serveri tipicno salju HTML, XML ili Json.
    
* JQUERY & AJAX
    * jQuery olaksava pravljenje ajax requesta i obradjuje podatke koje server posalje nazat.
    
    
### Zasto bi koristili Ajax?

Ajax koristi asynchronous procesing model.  To znaci da mozes raditi sto god hoces dok pas donese kolu :). 

U principu znaci da korisnik moze raditi druge stvari dok browser ceka da se podatci ucitaju, ubrzavajuci "user experience".


Sta je synchronous processing model?
*   Tipicno kad browser ucitava stranicu i naidje na `<script>` element, stane dok ne ucitai i procesuira podatke.
