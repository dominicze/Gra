# Gra
#Gra polegająca na odgadnieciu w 5 probach wylosowanej przez komputer liczby
#Zadanie moduly
'''oznaczenia:
li-wylosowana liczba
lu-liczba uzytkownika'''

from random import randint
li=randint(0,100)
print(li)
print('Gra polega na odgadnieciu wylosowanej przez komputer liczby z zakresu '
      '0-100 w 5 probach. Powodzenia')
for i in range(5):
    
    lu=float(input('Podaj liczbe: '))
    
    if i<4:
        if li<lu:
            odp='Wylosowana liczba jest mniejsza.'
        elif li>lu:
            odp='Wylosowana liczba jest wieksza.'
        elif li==lu:
            odp='Zgadles. Wylosowana liczba to %d.' % (li)
            print(odp)
            break
        print(odp)
        
    elif i==4:
        if li<lu:
            odp='Wylosowana liczba jest mniejsza. Nie zgadles. Koniec prob. Graj dalej.'
        elif li>lu:
            odp='Wylosowana liczba jest wieksza. Nie zgadles. Koniec prob. Graj dalej.'
        elif li==lu:
            odp='Zgadles. Wylosowana liczba to %d.' % (li)
            print(odp)
            break
        print(odp)
        
pytanie=input('Czy chcesz wejsc na wyzszy poziom? t/n ')
    
if pytanie=='t':
    print('Gra polega na odgadnieciu wylosowanej przez komputer liczby z zakresu '
    '1-1000 w 5 probach. Powodzenia')

czy_grac=True
while czy_grac:
      
    from random import randint
    li2=randint(1,1000)
    print(li2)

    for i in range(5):
    
        lu2=float(input('Podaj liczbe: '))
            
        if i<4:
            if li2<lu2:
                odp2='Wylosowana liczba jest mniejsza.'
            elif li2>lu2:
                odp2='Wylosowana liczba jest wieksza.'
            elif li2==lu2:
                odp2='Zgadles. Wylosowana liczba to %d.' % (li2)
                print(odp2)
                break
            print(odp2)
                
        elif i==4:
            if li2<lu2:
                odp2='Wylosowana liczba jest mniejsza. Nie zgadles. Koniec prob. Graj dalej.'
            elif li2>lu2:
                odp2='Wylosowana liczba jest wieksza. Nie zgadles. Koniec prob. Graj dalej.'
            elif li2==lu2:
                odp2='Zgadles. Wylosowana liczba to %d.' % (li)
                print(odp2)
                break
            print(odp2)

    pytanie2=input('Czy chcesz grac dalej? t/n ')
    if pytanie2=='n':
        czy_grac=False
