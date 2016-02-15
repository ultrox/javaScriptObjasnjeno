#### Questions:

1.  Kako Pravimo canvas? Procedura?
    *   Da zaista postoji procedura za pravljenje canvasa.
    *   Pocinjemo tako sto u html-u definisemo `canvas` element
    *   Zatim uzememo referencu iz DOM-a
    *   Definisemo kontekst sa getContext(contextType) - Sada mozemo poceti.
3.  Zasto ne Flash ili spec app umjesto canvasa?
    *   Flash je star, jako sigurnosno problematican i ne moze se manipulisati sa njim sa JS.
    *   Applikacija je poprilicno skupa, pisanje specijalizirane aplikacije that is.
2.  Kako pripremimo kanvas za crtanje?
    *   U principu po kanvasu se ne moze crtati dok se ne definise kontekst, po kojem se crta.
    *   Kontekst definisemo 'zovuci' getContext(type) metodu na canvas referencu. 
3.  Koja je standardna velicina (sirina i visina) canvasa
    *   300 x 150 px relativno mala, kad ne definisemo velicinu.
4.  Zasto web developeri ne preferiraju CSS za definisanje velicine kanvasa?
    * Razlog jer css samo razvuce kanvas od 300 x150px bez stvaranja novih pixela, za razliku od html-atributa.
6.  Sta je canvas?
    *   Kanvas je kao platno, povrsina po kojoj crtamo pixele koristeci JavaScript api.
7.  Da li je kanvas providan?
    * Kanvas je providan,da!
7.  Kako 'pristupamo' kanvasu da pocenmo crtati:
    * Tako sto pristupimo contextu, crtamo po konetkstu.
8.  Koju metodu koristimo da obojimo kvadrat.
    * fillRect - Stvara i popuni bojom kvadrat
9.  Kako kanvas zna da je kvadrat crn?
    * to je defaultna vrijednost fillStyle property-a.
10. Kako da promjenimo boju za obojiti(fillovati) kvadrat/krug.
    *   Koristeci property(osobinu) fillStyle = 'color'
11. Sta ako hocu da imam samo border oko kvadrata/kruga?
    * druga 'sestrinska' metoda `strokeRect(x,y,width,height);`
12. Kako da promjenimo boju bordera oko kvdrata/kruga
    * Tako sto opet promjenimo fillStyle property, svaki put kad promjenimo taj Prop, to je nova boja koju koristimo za sve.
13. Zasto koristimo znake navoda kad koristimo css propertise.
    * Ovo je jako intuitivno, jer javascript ne bi znao razliku od svojih variabila i ostalih stvari iz JS-a.
14. Sta je arc
    * Arc je metoda koja se koristi path kruga, ili krivih linija radije receno. Ne crtamo sa njom krug doslovno, vec naznacujemo sa njom krive linije, koje mogu biti i krug.
15. Sta je path.
    * Path je kao nevidljivo konstruisanje oblika po kojem ce mo stvoriti odredjen oblik. Path ne stvara, vec konstruise.
16. Kako nacrtati krug?       
    * Puni krug je relativno jednostavno nacrtati koristeci arc metodu `context.arc(x,y,radius,startingAngle,endAngle,direction);` stim da moramo otpoceti sa metodom beginPath. i na kraju zavrsimo metodom koja u principu stvara krug context.fill(), ili context.stroke();
17. Kako nacrtati trougao?
    * trougao slicno kao krug u smislu da ga 'pathujemo' ali jednostavnije. Prvo naznacimo pocetak tako sto , kazemo "beginPath". zatim se pomjerimo na startnu poziciju sa `.moveTo(x,y)`, i onda krecemo crtati spajajuci tacke koristeci metodu  `.lineTo(x,y)` ta metoda zapravo definise NOVU TACKU, koja zatim spoji zadnju lokaciju(TACKU) sa novom. Zatvorimo trougao, sa `closePath()` koja spoji zadnju tacku sa prvom. Zavrsavamo sa `context.stroke();` ili `context.fill();`
18. Kako koristimo beginPath metodu.
    *   Ovo je metoda koja naglasava 'E sada crtamo path', bez nje nece da moze.
19. Kako izrazavamo stepene unutar kanvasa?  
    * Radiant Pi = 180stepeni = 1 Radian
20. Koliko je 360 stepeni izrazeno u jedinici za kanvas? 
    *   2Pi = 360stepeni.
21. Koja metoda za crtanje texta unutar `canvas`  
    *   `fillText('This is my text',x,y,maxWidth)` maxWidth je opcioni element.
22. Kad crtas text u kanvasu koje jos properties moras definisati. 
    *   Nekoliko, textAligh, font, baseline.
23. Sta se desava kad podesis context.property
    *   To je jedini nacin da pises po kanvasu, da kontrolises kanvas ili ono sto se pojavljuje.
24. Kako dodati sliku u kanvas?
    * Prvo stvoriti new img objekt `new Image()` zatim dodati src tome objektu. I onda imamo sliku. Nakon toga taj objekt slike staviti na kanvas sa .drawImage(img,x,y) and boom imas sliku na kanvasu.
25. Sta se desi kad stavis text ovako `<canvas>You see me? Do you?</canvas>`
    *   To je staro html ponasanje koje kaze, ako je element nepoznat, pokazi ono sto se nalazi izmedju, inace zanemari.
28. Zasto ne crtamo direktno na kanvasu, nego u kontextu?
    *   Razlog je taj jer se kanvas razvija i moze se reci da je u povojima, te se ocekuju i drugi konteksti sa svojim metodama, tako da se zapravo modulira api na nacin da se deleguju metode po kontekstima.
    
    