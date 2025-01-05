//tunti 3-control statements//
## if 


## if...else 
pisteet = 80  
if pisteet >= 50:  
    print("hyväksytty")  
else:  
    print("Hylätty")  
    
## if...elif...else 
pisteet=**int(input**("Anna kurssisi yhteenlasketut pisteet /100 "))  
**if** pisteet <=50:  
    print("Tällä kertaa suoritus ei onnistunut, ota yhteys opettajaan yrittääksesi uudelleen")  
**elif** pisteet <=59:  
    print("Sait suoritettua kurssin hyväksytysti, arvosanasi on 1")  
**elif** pisteet <=69:  
    print("Sait suoritettua kurssin hyväkystysti, arvosanasi on 2")  
**elif** pisteet <=79:  
    print("Läpi meni helposti, onnittelut, arvosanasi on 3")  
**elif** pisteet <=89:  
    print("Onnittelut hienosta suorituksesta, arvosanasi on 4")  
**elif** pisteet <=100:  
    print("Huima suoritus, arvosanasi on 5!")  
**elif** pisteet >=101:   
    print("pisteitä pystyy kirjaamaan vaan väliltä 1-100, yritä uudelleen")  
    
## while ##

tuote =7  
**while** tuote <= 1000:    //tekee loopin niin pitkään kun tuotteen arvo on yli 1000//  
    tuote = tuote*7  
**print**(tuote)  

## for ##
**for** merkki **in** 'ohjelmointi':  //**for**-komennolla erotetaan variaabeli **merkki** 'ohjelmointi'-sanasta jokainen merkki kahdella välilyönnillä  
    print(merkki, end='  ')  //end=' ' määrää välimerkiksi välilyönnin, sep='; ' määrää separator-merkiksi puolipisteen  

for looppaa jokaisen merkin yhtälössä kunnes merkit loppuvat eli se käy jokaisen yhtlön läpi annetun ohjeen mukaisesti.  
Ensin se tarkastaa ensimmäisen kirjaimen tai merkin, tekee sille määrätyn tehtävän ja palaa sitten takaisin komentoon ja seuraavaan merkkiin 
sanassa ohjelmointi: tsekkaa ekan kirjaimen O, lisää väliin ohjeistuksen mukaisesti kaksi välilyöntiä ja menee vasta sitten tarkastamaan seuraavan kirjaimen H, lyö pari välilyöntiä ja niin edelleen...  

listojen käsittely for-komennolla:  

maara=0
for number in [2, -3, 0, 17, 9]:  //[]squarebrackets define list  
    maara = maara + number  
    print(maara)  

2  
-1  
-1  
16  
25    




## range ##
## with ##
## boolean: and, or and not ##
## break ##
## continue ##

