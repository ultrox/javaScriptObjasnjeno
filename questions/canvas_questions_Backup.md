#### Questions:

1.  Kako Pravimo canvas? Procedura?
    *Definisemo canvas tag u html-u skupa sa sirinom i visinom
    * uzemmo referencu na canvas el iz dom-a
    * definisemo kontekst 2d
    * i to je to
3.  Zasto ne Flash ili spec app umjesto canvasa?
    *   Skup
    *   security
2.  Kako pripremimo kanvas za crtanje?
    *   definisemo kontekst crtamo po 2d kontekstu
    *   
3.  Koja je standardna velicina (sirina i visina) canvasa
    *   300x150
4.  Zasto web developeri ne preferiraju CSS za definisanje velicine kanvasa?
    * razvuce rezoluciju
6.  Sta je canvas?
    *   html element po kojem crtamo pixele sa JS-om
7.  Da li je kanvas providan?
    * providan
7.  Kako 'pristupamo' kanvasu da pocenmo crtati:
    * referencu od canvasa, definisemo context pristupamo kontekstu i crtamo
8.  Koju metodu koristimo da obojimo kvadrat.
    *   context.fillRect(x,y,width,heigth);
9.  Kako kanvas zna da je kvadrat crn?
    *   defaultna boja je crna def u fill and stroke style
10. Kako da promjenimo boju za obojiti(fillovati) kvadrat/krug.
    * fillStyle = 'boja koja hoces'
11. Sta ako hocu da imam samo border oko kvadrata/kruga?
    * stroke(); ili strokeRect
12. Kako da promjenimo boju bordera oko kvdrata/kruga
    * styleStroke = 'whatever'
13. Zasto koristimo znake navoda kad koristimo css propertise.
    * zbog variabila u js-u
14. Sta je arc
    *  metoda za 2d kontekst, koristimo za crtanje lukova
15. Sta je path.
    *   nevidljivi kao grafitnom olovkom naznacimo put i onda preko njega prikazujemo oblik
16. Kako nacrtati krug?       
    *   beginPath(); context.arc(width,height,radious,startAngle,endAngle,direction), fill() ili stroke()
17. Kako nacrtati trougao?
    *   beginPath(); moveTo(x,y),lineTo(x,y),lineTo(x,y),closePath();fill()
18. Kako koristimo beginPath metodu.
    *   da naznacimo da otvaramo obiljezavanje nekog oblika, to je prvi step.Trougao ili luk
19. Kako izrazavamo stepene unutar kanvasa?  
    * radian
20. Koliko je 360 stepeni izrazeno u jedinici za kanvas? 
    *   2Pi 
21. Koja metoda za crtanje texta unutar `canvas`  
    *   drawText('text',x,y)
22. Kad crtas text u kanvasu koje jos properties moras definisati. 
    * .font, .textAlign, borderline
23. Sta se desava kad podesis context.property
    * nemaam pojma
24. Kako dodati sliku u kanvas?
    * new Image9) dodas src stavis je na kanvas sa drawImage(image,x,y)
25. Sta se desi kad stavis text ovako `<canvas>You see me? Do you?</canvas>`
    *
28. Zasto ne crtamo direktno na kanvasu, nego u kontextu?
    * zbog kurca
    
    