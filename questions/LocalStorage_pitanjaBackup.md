### Questions
1. Sta je LocalStorage?
    * Interna baza podataka koju mozemo koristiti u browseru
2. Koliko je oubicajna velicina LocalStorage-a u Mb?
    * 5-10mb
3. Ko vidi podatke u localStorage?
    * samo domen koji je 'orgin\
4. Sta ce se desiti ako, dva puta koristimo metodu `.setItem(key,value)` sa istim kljucem(key)?
    * unisticemo prvu, samim tim owrridn.
5. Sta se desava ako ubacimo u array mnostvo kljuceva i sve to stringifiramo.
    * u glavnom nista, ali ako ih ima na hiljade problem zbog cpu-a
6. Da li ima neka konvencija za davanje imena kljucevima u localStorage?
    *   nema, ali treba mislisti na to da kad ih brisemo ima smisla
7. Kako izbjeci konflikt sa drugim aplikacija sa iste domene u localStorageu?(array)
    *   stavimo ih sve u jedan array i onda uvjek znamo koliko ima tih kljuceva od nase aplikacije
8. Sta je QUOTA_EXCEEDED_ERR 
    * greska koja se javi kad istrosis max kolicinu koju ti baza dozvoljava (5-10mb)
9. za razliku od localStorage ona je za kratke staze?
    * sessionstorage
10. Kljucna razlika izmedju localStorage i "seke".
    * kad se resetuj browser
11. Kako je organiziran webStorage(localstorage i ), ko moze pristupiti sta?
    * prema orginu, orgin je domen samo orgin moze pristupiti svome lokalnom storageu
12. Kako da dodas item u bazu?
    *   localStorage.setItem('key','shit to add');
13. Kako da uzmes item iz baze?
    *   .getItem(key)
14. Sta je assosiative array?
    *   objek koji ima sposobnosti ponasanja kao array, neke metode
15. Sta radi localStorage.length?
    * ukupan broj kljuceva iz baze sa orgina-a
16. Kako sve mozemo brisati iz localStorage?3
    *   clear,removeItem i treci neznam
17. Koja je razlika izmedju clar metode i removeItem?
    *   cler uradi drop svega
18. Da li kljucevim moraju biti unikatni?
    * ne nuzno ali prepises 
19. Sta se desava ako isti kljuc koristimo za 2 druga inputa.
    * prepise se preko
20. Koliko milisekundi ima od 1970 do danas?
    * mnogo, new Date() .getTime()
21. Jedan od nacina sastavljanja unikatnog key-a
    * sufix + .getTime()
22. Kako napraviti Naming scheme za tvoju app, sta je najvaznije? del?
    * tako da bude imuna na to ako se izbrise jedan key
23. Metoda za dobivanje broja i floata?
    * parseInt() parseFloat()
24. Sta je event Object? I kako ga dobiti?
    * argument koji dajemo event Handleru daje nam pristup eventObj koji ima razne, nama potrebne informacije o tome objk koji je podstaknuo event
    *
25. Kako se definise redosljed u localStorage? 
    *   browser odlucuje nije standardizirano.