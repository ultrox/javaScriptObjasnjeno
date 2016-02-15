#### Questions:

1.  Kako Pravimo canvas? Procedura?
    * Tako sto definisemo kanvas tagu u html-u `<canvas id="stoka"></canvas>`
    * Zatim uzememo referencu na canvas u DOM-u `var c = document.getElementById('stoka')`
    * Definisemo kontekstu `var context = c.getContext('2d');` 
3.  Zasto ne Flash ili spec app umjesto canvasa?
    * Poznatao je da je flash sigurnosna rupa, komplikovan je i obicno treba neko ko poznaje Flash
    * Ovdje se drzimo poznatih tehnologija.
2.  Kako pripremimo kanvas za crtanje?
    * Tako sto definisemo kontekst i zovemo kontekstove metode i osobine.
3.  Koja je standardna velicina (sirina i visina) canvasa
    * Kad se ne definise exsplicitno, velicina je 300px x 150px;
4.  Zasto web developeri ne preferiraju CSS za definisanje velicine kanvasa?
    * Rastegne kanvas, ostane isti broj pixela, rezolucija.
6.  Sta je canvas?
    * Kanvas je novi html5 property po kojima mozemo crtati sa javascriptom.
7.  Da li je kanvas providan?
    *   Da
7.  Kako 'pristupamo' kanvasu da pocenmo crtati:
    *   Preko contexta, preko contextovih metoda i osobina.
8.  Koju metodu koristimo da potpuno obojimo oblik?
    *   fill() ili strokeFill zavisi sta bojimo.
9.  Kako kanvas zna da je kvadrat crn?
    *   Definisano ponasanje fillStyle osobina.
10. Kako da promjenimo boju za obojiti(fillovati) kvadrat/krug.
    *   promjenimo osobinu u fillStyle = '#fff'
11. Sta ako hocu da imam samo border oko kvadrata/kruga?
    * koristi metodu .stroke() ili za kvadrat strokeRect()
12. Kako da promjenimo boju bordera oko kvdrata/kruga
    *   strokeStyle = "red"
13. Zasto koristimo znake navoda kad koristimo css propertise.
    *   jer compiler se sjebe i ne bi razaznao js var od nekih propertisa.
14. Nacrtaj krug sa ?
    * arc()
16. Kako nacrtati krug? (receptici)      
    *   context.pathBegin();
    * context.arc(x,y,radious,startAngle,endAngle,direction);
    * context.fill() ili context.stroke()
17. Kako nacrtati kvadrat?
    *   Koristeci fillRect(x,y,width,height);
18. Kako koristimo beginPath metodu.
    *   Kad pocinjemo crtati novi oblik, beginPath sluzi za rec "hey novi oblik pocinje"
19. Mi mislimo u stepenima, a kanvas misli u ?  
    *   radian
20. Koliko je 360 stepeni izrazeno u jedinici na kojoj misli kanvas? 
    * 2 radiana ili ti 2xPI
21. Koju metodu koristis za dodavanje teksta na 'canvas'? 
    * strokeText("this is stupid text",x,y,width(option))
    * fillText('some text',x,y,w);
22. Kad crtas text u kanvasu koje jos properties mozes definisati. 
    * context.font(),textAlign(),textBaseline
24. Kako dodati sliku u kanvas?
    * stvoriti img object as `new Image()`
    *   Dodati src `img.src`
    *   na `img.onload = function() { context.drawImage(img,x,y);};`
25. Sve na kanvasu je ?
    * Pixels
26. Ova context metoda stvara kvadrat? 2
    * strokeRect()
27. Sta treba da znamo kad 'dilamo' sa slikama na kanvasu?(jedna ona stvar sto nas zezucka?)
    * na onload odraditi dodavanje, slika treba vremena da se ucita.
28.  Kako uciniti path oblik vidljivim?
    * context.stroke() ili context.fill();
29. Objekt sa metodama i osobinama(property) da mozes crtati na canvas-u?
    *   canvas.getContext('2d');
30. Sta se desi kad stavis text ovako `<canvas>You see me? Do you?</canvas>`
    *   Browser ako podrzava element nece pokazati tekst ili ako ne podrzava ce prikazati tekst.
31. Nevidljiva Linije koju stvars da nacrtas oblik?
    * Path
32. Mozes da znas da se nesto zavrsilo ucitavati koristeci  _ _ _ _ _ _ handler.
    * onload
    
    
    