//tunti 3-control statements//
paras lukea code -tekstinä, jolloin koodin sisennykset näkyvät oikein. 

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

summa = 0  
laskin = 0   

arvosana = int(input('Anna arvosana, kun haluat lopettaa niin syötä -1: '))  
while arvosana != -1:  
    summa += arvosana  
    laskin += 1  
    arvosana = int(input('Anna arvosana, kun haluat lopettaa niin syötä -1: ')) //Kysyy arvosanaa uudelleen//

if laskin != 0:  //Jos laskimen arvo on enemmän kuin nolla//  
    keskiarvo = summa / laskin  
    print('Luokan keskiarvo on {keskiarvo:.2f}, arvosanoja on annettu {laskin} kappaletta') //keskiarvo kahdella desimaalilla//   
else:  
    print('Yhtään arvoa ei syötetty')  


## for ##
**for** merkki **in** 'ohjelmointi':  //**for**-komennolla erotetaan variaabeli **merkki** 'ohjelmointi'-sanasta jokainen merkki kahdella välilyönnillä  
    print(merkki, end='  ')  //end=' ' määrää välimerkiksi välilyönnin, sep='; ' määrää separator-merkiksi puolipisteen  
  **sep**: Mitä lisätään arvojen väliin saman print-kutsun sisällä. Lisää myös rivinvaihdon.  
  **end**: Mitä lisätään lopuksi tulostuksen jälkeen (oletuksena rivinvaihto). Ei vaihda riviä.    

for looppaa jokaisen merkin yhtälössä kunnes merkit loppuvat eli se käy jokaisen yhtlön läpi annetun ohjeen mukaisesti.  
Ensin se tarkastaa ensimmäisen kirjaimen tai merkin, tekee sille määrätyn tehtävän ja palaa sitten takaisin komentoon ja seuraavaan merkkiin 
sanassa ohjelmointi: tsekkaa ekan kirjaimen O, lisää väliin ohjeistuksen mukaisesti kaksi välilyöntiä ja menee vasta sitten tarkastamaan seuraavan kirjaimen H, lyö pari välilyöntiä ja niin edelleen...  

listojen käsittely for-komennolla:  

maara=0  
for number in [2, -3, 0, 17, 9]:    //[]squarebrackets define list  
    maara = maara + number  
    print(maara)  
tulostuu:  
2  eli 0+2  
-1 eli 2-3   
-1 eli -1+0   
16 eli -1+17  
25 eli 16+9     

esim. keskiarvo.py 
**kokonaispistemaara** = 0  #alussa kokonaispistemäärä asetetaan nollaksi, alkupiste  
**laskin** = 0  #alussa myös ns. kierrolaskin on nollassa, alkupiste  
**arvosanat** = [98, 76, 71, 87, 83, 90, 57, 79, 82, 94]  #arvosanat listataan arvosanat-nimen alle  

for **arvosana** in **arvosanat**:              #määritellään uusi muuttuja "arvosana"  
    **kokonaispistemaara** += **arvosana**      #jokaisen kierroksen arvosana lisätään kokonaispistemäärään   
    **laskin** += 1                             #jokaisen kierroksen jälkeen kierrolaskin lisää yhden yksikön laskimeen.    

**keskiarvo** = kokonaispistemaara/laskin      #uusi muuttuja keskiarvo eli kokonaispisteet/kierrokset  
print(f'Luokan keskiarvo on {keskiarvo}')      #f-string toiminnolla näyttää vastauksen "Luokan keskiarvo on _vastaus_" 

Jos ei tiedetä kuinka monta oppilasta kurssilla on niin käytetään toistokertojen vahtia eli looppia toistetaan kunnes tietty ehto tai arvo havaitaan. (sentinel-controlled iteration) 
**while -komento**


f-string  
numero1 = 7  
numero2 = 5  
print(f'{numero1} kertaa {numero2} on {numero1*numero2}')


## range ##
for laskin in range(10): //0-9 bittilaskentaa eli ensimmäinen numero on nolla  
    print(laskin, sep='/ ') 

0/  
1/  
2/  
ym. 

for laskin in range(0-10):  
    print(laskin, end='/ ')
    
0/  1/  2/  3/  4/  ym. 

for number in range(5, 121, 5):   
    print(number, end='*')  
antaa tulokseksi luvut 5-120, jotka ovat viidellä jaollisia ja laittaa lukujen väliin tähden.  (Githubissa muuttaa muodon erilaiseksi)  

5*10*15*20*25*30*35*40*45*50*55*60*65*70*75*80*85*90*95*100*105*110*115*120*

for number in range(120, 4, -5): 
    print(number, sep='*') //laskee 120 viidellä jaolliset numerot ja listaa ne allekkain//


Tehtävänä oli tehdä laskin joka laskee 0-100 sisältä joka toisen numeron yhteen. 
loppusumma=0  //aloitusarvo//
for number in range(0, 101, 2):     //100 tulee olla mukana, joten laskeminen loppuu 101-lukuun//  
    loppusumma += number    //loppusumma
    print(loppusumma)   

Desimaalilaskentaa raha-arvoilla, korkoa korolle -laskin ja Decimal-kirjaston käyttöönotto

amount = 100.53  
from decimal import Decimal  
principal = Decimal('1000.00')  
rate = Decimal('0.05')  
  
x = Decimal('100.5')  
y = Decimal('2')  
  
for year in range(1, 11):  
    amount = principal*(1+rate)**year  
    print(f'{year:>2}{amount:>10.2f}')  //tulostaa vuoden eli rivin kaksi ensimmäistä merkkiä (:>2) ja kerääntyneen summan eli riviltä osoitettuna 10 seuraavaa merkkiä (:>10), joista kaksi  merkkiä on varattuna desimaalille (.2f) eli desimaalipisteestä kaksi oikealle.  



## with ##
## boolean: and, or and not ##
## break ##
## continue ##

