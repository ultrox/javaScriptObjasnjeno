1. Sta je 'container' u video formatu?     
    * Kontejner je kao omotnica za pismo u koju stavljamo dva pisma na cijem listu je napisan
    * video koji je enkodiran i audio koji je enkodiran
    * Znaci video container sluzi da drzi dva fajla koja su enkodirana svaki u svome formatu.
2. Uobicajni conteineri na webu
    * WebM - backed by Google
    * ogg - Open G
    * mp4 - safari but mostly every other major browser
3. Sta je codec?
    * codec je kao brava iza koje je zakljucan pravi sadrzaj.
    * sluzi da bi se video/audio smanjio size i osigurao pustanje 
    * koristi se kad se stvara fajl i kad se pusta
4. Popularni codecs?
    * h.264
    * VP8
    * Theora
5. Kako radi `<source>` element   
    * tako sto u njegovom src atributu mozes podesiti vise razliciting fajl izvora
    * koje onda browser moze iskorisiti na osnovu metadata
6. Sta radi canPlayType:
    * Ispituje metadata od videa i odlucuje da li ga moze pustiti
7.  Sta tacno dobijes od canPlayType?
    * 3 vrijednosti '', 'maybe' probably
7. Sta je bitrate
    * Broj bitova koje browser mora obraditi u vremenskoj jedinici da bi ispravno prikazao video.
8. What is MIME?
    * fajl/container vrijednost
9. 3 Vrijednosti koje nam canPlayType metoda pruza?
    * odgovorio
10. Kad mozemo dobiti 'probably' koristeci canPlayType?
    * samo kad u type ubacimo i codecs, odnosno vise metainformacija
6. Kako podesiti zvuk?
    * property volume = 0.0 i max 1.0
7. Kako da uhvatis pixele koji se nalaze u jednom frejmu?
    * sa kanvas metodom drawImage pustajuci mu video objekt kao argument,
    * zato sto video i canvas objekt imaju specijalnu vezu te je ovo moguce
8. Sta je video frejm?
    * je kvadrat piksela u vremenskoj jedinici :)
8.  Sta je frame rate?
    * kolicina tih kvadrata u 1sekundi
9. Scratch Buffer wtf is that?
    * metoda sa kojom mozemo da obradimo video frejm koristeci video obj i 2 canvas elementa
10. Koliko 1px ima boja? 
    * 4 RGB/A
11. Kako postaviti svoju sliku umjesto prvog frejma na videu  
    * koristeci video.load() i video.poster = 'img
13. Kako da podesimo alternativna videa
    * sa source elementom
14. Kako pomoci browseru da bolje ustanovi da li moze pustiti video
    * type = 'video/mp4; codecs="h.264,aac"';
15. Kako pustiti flash
    * koristeci objekt element
16. Za sta je dobro koristiti setTimout sa video obradom?
   * kad pucamo na svaki frejm u videu da ga obradimo sa tacno onom funkcijom koju zelimo
17. Kako obradjujemo greske sa videom?
     * postojei listner za error koji postavimo na video obj kad se klikne play
18. Error codes
    4 koja nemam pojma
    
