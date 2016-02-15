Chalange 1:
## Init:
loaduj video iz arraya, provjeri ekstenziju sa helper funkcijom

####Dodaj EventHandlere na njihove evente:
* handleControl
* setEffect
* setVideo

####Dodaj ovo na kraju init funkcije:
* pushUnpushButtons('video1',[])
* pushUnpushButtons('normal',[])

## getFormatExtention
Ne zaboravi dodati lokalnu varijabilu za video.

`var video = document.getElementById('video');`

## Creating HandleControle

#### Play blok
Ako user klikne na play, zovi play, imaj na umu ako je videio zavrsio play, mora se opet load(provjeri ovo).

#### Pause blok
pauziraj video sa pause metodom

#### Loop blok
Dodaj loop properti koje je boolian, kad user klikne loop i obrni kad iskljuci.

#### Mute blok
 Mute radi slicno kao i loop, obrni kad se opet stiste.
### BANG:
Find out what is video scrubber.

## Pisanje ended event funkcije
Unpush playbutton
i dodaj ovaj event handler na video objekt.

## Switching test videos *setVideo handler

definisi globalni obj videos sa dva videa. gdje ce biti imena videa bez ekstenzije.
videa moraju imati property ime kao i ID u html-u.

zavisno koje se dugme stisne if/else taj video load sa pushunpush-om.

### Helper play - ovo je moja ideja ali ne sjecam se zasto
Napisi funkciju helperplay koja ce u sebi imati load,play i pushunpush za play.

## Push Unpush
Premisa je da klasu selected postavis na aktivno dugme(koje se stisne) i na svim ostalim da ih skines sa toga sektora(controls,effect,video), to je array loop kroz array i skini sve.

Pazi na to da se dugme stisne 2x.

**Starting:**
Ova funkcija ima dva parametra, 
    * idToPush -> to je id od dugmeta na koji ce staviti 'selected' + sliku u css da je stisnut
    * idArrayToUnpush - to su svi ostali array-i u sektoru koji trebaju biti unpushed
    
Na pritisnuto dugme u klasu ubaci select, da oznacis dugme koje je stisnuto.
koristi **indexOf** da nadjes da li je 'select' prisutan

Probaj nekoliko stvari ovdje, jer vec je oznaceno samim tim sto je slika drugacija, klasa nije bitna toliko mnogo. Pokusaj traziti razliku u slici.


Zbunjuju me malo dvije stvari tu, ! i indexOf. Vise o ovoj funkciji na 379.



## Effects
Ovo je najkompliciraniji dio programa, sta cinimo sa takvim djelovima??? Jebeno ih rasclanimo do momenta da ne budu kompleksni, kompleksnost vodi do izbjegavanja :).

prvo definisi globalnu vari **effectFunction** koja ce poceti da drzi **null**

### setEffect - handler
Ok ovo je funkcija koja ce podesiti vrijednost u **effectFunction** na osnovu koje je dugme stisnuto.
Ovo je abstraktni nivo gdje funkciju koristimo kao mjenjac, ne moramo znati kako mjenjac radi ali kad pomjerimo rucicu, brzina se promjeni.

dvije funkcije, pushUnpush i setovanje vrijednosti u **effectFunction**

### Implementiraj scratch buffer

u html-u dodaj w720 h480
    * video #video
    * canvas 1 #buffer
    * canvas 2 #display

Pozicioniraj ih da 'leze' jedan na drugome, canvas je svakako providan tako da...

videoDiv relative

top:180;

left:190;

canvas absolute top i left 0;
395 str.

## Processing video

Na event 'play' dodaj listner **processFrame** tako da cim stisnes play odma krece i obrada videa.

### procesing frame funkcija

provjeri da li je video pauziran ili zavrsio ako da onda se samo vrati.

grab references za video, buffer i display(2d).


### Stvaranje Buffer-a
koristi `buffer.drawImage` da uzmes frejm od videa i stavis ga u buffer,

u var frejm sejvuj taj buffer frejm sa `getImageData`

Nakon toga mozes manipuliati frejm pixelima koji se nalazu u `frejm.data` da dodjes do njih moras loopovati kroz frame.data zapravo znati velicinu da mozes loopovati.

`frame.data.length /4` broj 4 je tu jer svaki pixel ima jos i 4 vrijednosti RGBA
podesi lokalne varijabile r,g,b (frejm data 0 1 2), takodjer dodaj ako je effect function drugaciji nego null; onda pozovi effect function, i passuj mu argumente:
* pozicija pixela (i)
* r,g,b i frame.data referencu na obj

I to je to jedan frejm procesuiran. 

Da nastavis procesuirati sledeci i sledeci, korisit `setTimeout(processFrame,0)`
Ovo se nece desiti u 0 milisekundi ali cim bude slobodan slot onda ce se desiti, sto je dovoljno dobro.



* Nadji id od ankora(elementa) koje je stisnuto i update interface accordingly.
