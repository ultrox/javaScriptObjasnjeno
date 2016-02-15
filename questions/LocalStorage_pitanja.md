### Questions
1. Sta je LocalStorage?
    * je interna baza od browsera koju mozemo koristi da sacuvamo razne podatke lokalno, te poboljsamo user expirience.
2. Koliko je oubicajna velicina LocalStorage-a u Mb?
    * Uobicajna je oko 5 - 10 mb zavisno od browsera do browsera.
3. Ko vidi podatke u localStorage?
    * Podatci se cuvaju prema orginu-, odnosno domeni, i samo taj domene moze vidjeti i manipulisati svoje podatke.
4. Sta ce se desiti ako, dva puta koristimo metodu `.setItem(key,value)` sa istim kljucem(key)?
    * Value ce biti oweriden effektivno unistimo prijasnji item novim
5. Sta se desava ako ubacimo u array mnostvo kljuceva i sve to stringifiramo.
    * U principu to moze u koliko taj array nije ogroman, u hiljadama. Koristenje JSON metoda, moze bitit CPU and Battery heavy.
6. Da li ima neka konvencija za davanje imena kljucevima u localStorage?
    * Nema osim nas samih, trebamo iznaci rijesenje kako da generisemo kljuceve koji nece biti u konflikutu kad ih izbrisemo ili ako djele bazu sa ostalim aplikacijama.
7. Kako izbjeci konflikt sa drugim aplikacija sa iste domene u localStorageu?(array)
    * Dodamo sve kljuceve za tu domenu u array recimo 'facebookMsg' i to da bude kljuc
8. Sta je QUOTA_EXCEEDED_ERR 
    * TO je greska kojom nas browser obavjesti da je kolicina memorije istrosena.
9. za razliku od localStorage ona je za kratke staze?
    *   sessionStorage
10. Kljucna razlika izmedju localStorage i "seke".
    * sessonStorage izbrise vrijednosti nakon sto se browser izbrise.
11. Kako je organiziran webStorage(localstorage i ), ko moze pristupiti sta?
    * Organiziran prema 'orgin-u' gdje je orgin domen.
12. Kako da dodas item u bazu?
    * 2 metode localStorage.setItem(key,value) localStorage['mykey'] = 'true life'
13. Kako da uzmes item iz baze?
    * 2 metode localStorage.getItem(key), localStorage[key]
14. Sta je assosiative array?
    * array like behaviour u objektu, gdje imamo neke array sposobnosti uglavnom iteracije
15. Sta radi localStorage.length?
    * vrati nam ukupnu velicinu localStorage-a 
16. Kako sve mozemo brisati iz localStorage?3
    * removeItem() - single, clear() treci ocito ne znam
17. Koja je razlika izmedju clar metode i removeItem?
    * clear ocisti cjelu bazu, remove brise samo taj zadani kljuc.
18. Da li kljucevim moraju biti unikatni?
    * ne nuzno ali onaj koji nije ce da se prekopira effektivno ga unistavajuci.
19. Sta se desava ako isti kljuc koristimo za 2 druga inputa.
    * unistavanje starok, owerwriten
20. Koliko milisekundi ima od 1970 do danas?
    * Bili mi je zanimljivo saznati da var date = new Date(); var time = date.getTime(); vrati ne sadasnje vreme u milisekundama, nego vrijeme od 1970e sve do ovog momenta u milisekundama, samim tim praveci unikatan broj svake milisekunde
21. Jedan od nacina sastavljanja unikatnog key-a
    * sufix +(nesto unikatno kao vrijeme u milisekundama)
22. Kako napraviti Naming scheme za tvoju app, sta je najvaznije? del?
    * bitno je napraviti stvaranje kljuceva da ne zavise jedni od drugih, kad se izbrise jedan da ne dolazi do potencijalnih konflikata, recimo ako se ekskluzivno koristi .length metoda. vrlo jednostavno se moze doci do konflikta.
23. Metoda za dobivanje broja i floata?
    *parseInt i *parseFloat
24. Sta je event Object? I kako ga dobiti?
    * Event obj je defaultni obj kome dobijemo pristup kad nasem event handleru dodamo argument,
    * on nam daje razne informacije o tome eventu/elementu sa kojim radimo interakciju. Na taj nacin mozemo radimo interakciju sa razlicitim elementima kao sto su, dugmici, polja, onfocus itd.
25. Kako se definise redosljed u localStorage? 
    * I meni je ovo bilo cudno, ali nema konvencije za ovo, browseri implementiraju redosljed kako hoce, mi trebamo samo imati u vidu da se ne oslanjamo da localStorage redosljed.