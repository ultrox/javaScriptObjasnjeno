### Questions
1. Sta je LocalStorage?
    *lokalna baza u browseru
2. Koliko je oubicajna velicina LocalStorage-a u Mb?
    * 5-10mb
3. Ko vidi podatke u localStorage?
    * samo domen, organizirane su po domenima, facebook ne moze vidjeti podatke od twiter
4. Sta ce se desiti ako, dva puta koristimo metodu `.setItem(key,value)` sa istim kljucem(key)?
    * override, value ce se izbrisati
5. Sta se desava ako ubacimo u array mnostvo kljuceva i sve to stringifiramo.
    *nista posebno ali moze biti problematikus na cpu tolika obrada, to ne znaci mnogo ako nema na *hiljade i hiljade kljuceva u array
6. Da li ima neka konvencija za davanje imena kljucevima u localStorage?
    * nema ali treba biti unikatna
7. Kako izbjeci konflikt sa drugim aplikacija sa iste domene u localStorageu?(array)
    * treba iznaci nacin da kljuc bude unikatan za tu aplikaciju, i sve kljuceve staviti u array i taj array pun kljuceva spasiti u bazu
8. Sta je QUOTA_EXCEEDED_ERR 
    * greska koja nam govorid da nam nedostaje prostora, 5-10mb ode bye
9. za razliku od localStorage ona je za kratke staze?
    * SessionStorage
10. Kljucna razlika izmedju localStorage i "seke".
    * sessionstorage se obrise nakon svakog browser restarta
11. Kako je organiziran webStorage(localstorage i ), ko moze pristupiti sta?
    * po domenu
12. Kako da dodas item u bazu?
    *setItem(key,value)
13. Kako da uzmes item iz baze?
    *getItem(key)
14. Sta je assosiative array?
    * objekt koji ima neke array elemente kao enumerible
15. Sta radi localStorage.length?
    * ukupnu kolicinu kljuceva u bazi
16. Kako sve mozemo brisati iz localStorage?3
    * clear(), removeItem, 
17. Koja je razlika izmedju clar metode i removeItem?
    * clear odradi drop cjele baze
18. Da li kljucevim moraju biti unikatni?
    * ne nuzno ali
19. Sta se desava ako isti kljuc koristimo za 2 druga inputa.
    * override
20. Koliko milisekundi ima od 1970 do danas?
    * sta je new Date() getTime
21. Jedan od nacina sastavljanja unikatnog key-a
    * var date = new Date();
    * date.getTime + Math.floor(Math.rand());
22. Kako napraviti Naming scheme za tvoju app, sta je najvaznije? del?
    * najvazinje je moci indentificirati koliko kljuceva ima, i pouzdan nacin da se odrzi integritet podataka nakon brisanja iz baze.
23. Metoda za dobivanje broja i floata?
    * parseInt, parseFloat
24. Sta je event Object? I kako ga dobiti?
    * Objekt koji dobijemo pristup kad specificiramo parametar u eventHandleru
25. Kako se definise redosljed u localStorage? 
    * browser odredjuje