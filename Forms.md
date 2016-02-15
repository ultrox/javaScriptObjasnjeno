### Forms - Dukett
 el['e' + event + callback] -> ovaj kurac je izmisljen od John Rissa ili kako god da mu je ime 
 
 ubacuje novu metodu u el obj
jQuery(http://ejohn.org/projects/flexible-javascript-events/).
### Forms Collection
To je specijalna kolekcija koja drzi sve reference na `<form>` elemente u array like node kolekciji.
* `document.forms[0]`
    * pristupa prvom form elementu
### Element Collection
Ovo je super dio form element kolekcije, svaki od form elemenata se moze pristupiti sa item number-om, ili id/name atribut imenom.

Primjer:

    var elements = document.forms[0];
    elements.name // will give you name id/name atribut;
    elements.password; // ako u form elementima/kontrolama ima password ili id password
    //mozes da mu pristupis i po index broju
    elements.elements[0] //to ce biti prvi element u prvom form elementu,ako je to 'name'
    elements.name;

### Form Controls
Vise na Dukett 580;
