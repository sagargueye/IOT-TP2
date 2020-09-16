# IOT-TP2
Ce TP a pour but deux objectifs : 1. Connecter différents dispositifs aux interfaces d’un micro-contrôleur pour obtenir ses données ou interagir avec l’environnement. 2. Ce TP va vous permettre d’aller plus loin dans l’exploration des micro-contrôleurs en découvrant l’accès par les voies numériques, analogiques et bus. Dans ce TP vous allez tester plusieurs capteurs/acteurs à partir de votre micro-contrôleur micro :bit, dans ce but vous allez continuer à explorer la documentation de ce module..

## Exercice 1
`from microbit import *
while True:
    #led rouge allumé
    pin0.write_digital(1)
    sleep(3000)
    pin0.write_digital(0) // on l'eteint apres 3 seconde
    #led vert allumé
    pin2.write_digital(1)
    sleep(3000)
    pin2.write_digital(0)// on l'eteint apres 3 seconde
    #led jaune allumé
    pin1.write_digital(1)
    sleep(3000)
    pin1.write_digital(0) // on l'eteint apres 3 seconde
`
## Exercice 2

`from microbit import *
import neopixel
from random import randint
 
#Neopixel with 2 LEDs
neo = neopixel.NeoPixel(pin0, 1)
while True:
    #Iterate over each LED in the strip
    for pixel_id in range(0, len(neo)):
        neo[pixel_id] = (0, 0, 255) #bleu
        neo.show()
        sleep(1000)
        neo[pixel_id] = (255, 255, 255) #blanc 
        neo.show()
        sleep(1000)
        neo[pixel_id] = (255, 0, 0) #rouge
        neo.show()
        sleep(1000)`

## Exercice 3
`print("mon angle" + str(accelerometer.get_x())) ` 
il affiche sur la console minicom le resultat de sortie

## Exercice 4
`
def on_forever():
 BME280.power_on()
 basic.show_number(BME280.temperature(BME280_T.T_C))
 basic.show_number(BME280.humidity())
basic.forever(on_forever)
`
On a utliser l'IDE makecode car on n'arrivait pas à importer la biblioteque BME280

## Exercice 5

