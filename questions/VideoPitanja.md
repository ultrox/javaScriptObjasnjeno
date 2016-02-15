0. Uncaught RangeError: Maximum call stack size exceeded

1. Sta je 'container' u video formatu?     
    * Conteiner je dio koji drzi u sebi video i audio enkodirane podatke.
2. Uobicajni conteineri na webu
    * mp4, WebM, ogg i flash Video(umire govno polako)
3. Sta je codec?
    * codec je software koji se koristi za coding i encoding video i audio fajlova.
4. Popularni codecs?
    * Video: H.264, VP8, Theora(open source)
    * Audio: AAC, Vorbis
5. Kako radi `<source>` element
    * Na nacin da dopusta browseru izbor na osnovu metadata da izabere koji format ce pustiti(top-bottom aproach)
    
6. Sta radi canPlayType:
    * provjerava i da li moze pustiti odredjeni video tako sto mu kao argument
    * obezbjedimo meta info kao sto je MIME i/ili type(codec)
7.  Sta tacno dobijes od canPlayType?
    * '' ako ne moze
    * 'maybe' vjerovatno moze
    * 'probably' -> jako siguran da moze
7. Sta je bitrate
    * Vrlo jednostavna analogija, ako si ikad bio negdje na autoputu i sjedis u guzvi i trebas platiti
    * putarinu ti si u tom momentu 1bit, auto ispred tebe je drugi bit, auto iza treci i tako sve redom
    * Browser je ciko koji stoji u kucici i ti mu dades karticu, on ti kaze koliko trebas platiti
    * ti mu das lovu a on tebi kusur i pusti te da prodjes. Ti si obradjen isto kao sto je obradjen 
    * i bit od strane browsera.
    
    * Broj auta koje ciko u kucici procesuira u nekoj vr jedinici(1s/1m) je carrate.
    * Broj bitova browser treba procesuirati u vremenskoj jedinici da dekodira video i ispravno ga prikaze

8. What is MIME?
    * Specificira container type 'video/mp4' ili video/ogg


9. 3 Vrijednosti koje nam canPlayType metoda pruza?
    * '','maybe', probably
10. Kad mozemo dobiti 'probably' koristeci canPlayType?
    * Samo kad obezbjedimo vise metainformacija o vide-u, npr: codec za a/v
    
        `type='video/ogg; codecs="theora,vorbis"'`

6. Kako podesiti zvuk?
    * uzeti referencu na video obj i podesiti properti volume = 0.0 - 1.0
7. Kako da uhvatis pixele koji se nalaze u jednom frejmu?
    * prvo definisemo uzmemo ref na frejm, zatim ustanovimo duzinu `frame.data.length` i podjelimo na 4(rbg/a)
    * i radimo iteraciju kroz 
8. Sta je video frejm?
    * Je kvadrat piksela(slika koja se ne mrda) u tacno odredjenoj vremenskoj jedinici.

8.  Sta je frame rate?
    * broj tih slika u sekundi, sto je broj veci to je i osjecaj za pokret kvalitetniji.

9. Scratch Buffer wtf is that?
    * Tehnika koja koristi 3 elementa, video objekt i 2 canvas elementa, jedan od njih se koristi kao buffer(mjesto za obradu) frejma, i treci za display toga obradjenog frejma.

10. Koliko 1px ima boja? 
    * Svaki pixel ima samo 3 boje + Alfa, kao i css boje.RGB (alfa je opacity)
11. Kako postaviti svoju sliku umjesto prvog frejma na videu
    * koristiti `video.poster` property
    
13. Kako da podesimo alternativna videa
    * koristeci `<source>`
14. Kako pomoci browseru da bolje ustanovi da li moze pustiti video
    * definiraj type sa vise metainformacija kao sto je MIME i codecs
15. Kako pustiti flash
    * sa object elementom
16. Za sta je dobro koristiti setTimout sa video obradom?
    * za obradu frejmova, pozivajuci funkciju koja obradjuje pixele ponaosob
    * i mjenja frejm. Ova metoda nije direktno povezana sa svakim frejmom, 
    * ali je najbolji metod za sada.
17. Kako obradjujemo greske sa videom?
    * imamo poseban event 'error' koji mozemo zvati na video objekt tako da mozemo 
    * koristiti handler funkciju da obavjestimo korisnika o gresci, i/ili reagujemo na vreme
18. Error codes
    * 4 vrste gresaka mozemo obratiti u error metodi
