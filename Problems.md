# My Problems and Solutions

1. Unutar objekta ne mogu promjeniti stanje sa drugim stanjem.
        var obj = {name: 'Marko',age: 22, surname: this.name}

Frustracije frustracije, ovo ne moze jer samo **'behaviour'** moze mjenjati stanje, jer treba raditi assign operaciju, odnosno treba funkcija.

    function() { this.surname = this.name }
Problematikus je bio u tome jer sam ovo zaboravio, i trazim nacin kako i nikako naci, mislim se koji mi je.

2. text form keyboard event, ako hocu da mi uhvati "enter" i posalje "form" bez da resetuje stranicu, moram iskljuciti 'defaultno ponasanje.
	* .onkeypress path moram koristiti 
            return false.
	* AddEventListner i u handleru 
            event.preventDefault();

