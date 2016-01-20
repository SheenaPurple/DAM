#1.1 Concepte de programa informàtic

Un primer pas per poder començar a analitzar com cal fer un programa informàtic
és tenir clar què és un programa i què significa aquest concepte. En contrast amb
altres termes usats en informàtica, és possible referir-se a un “programa” en el
llenguatge col·loquial sense haver d’estar parlant necessàriament d’ordinadors. Es
podria estar referint al programa d’un cicle de conferències o de cinema. Però, tot
i que no es tracta d’un context informàtic, aquest ús ja aporta una idea general del
seu significat.

Entorns de desenvolupament 10 Desenvolupament de programari
Un programa infomàtic és un conjunt d’esdeveniments ordenats de manera
que se succeeixen de forma seqüencial en el temps, un darrere l’altre.
Un altre ús habitual, ara sí vinculat al context de les màquines i els autòmats,
podria ser referir-se al programa d’una rentadora o d’un robot de cuina. En aquest
cas, però, el que se succeeix són un conjunt, no tant d’esdeveniments, sinó d’ordres
que l’electrodomèstic segueix ordenadament. Un cop seleccionat el programa que
volem, l’electrodomèstic fa totes les tasques corresponents de manera autònoma.
Per exemple, el programa d’un robot de cuina per fer una crema de pastanaga seria:

1. Espera que introduïu les pastanagues ben netejades, una patata i espècies al
gust.
2. Gira durant 1 minut, avançant progressivament fins a la velocitat 5.
3. Espera que introduïu llet i sal.
4. Gira durant 30 segons a velocitat 7.
5. Gira durant 10 minuts a velocitat 3 mentre cou a una temperatura de 90
graus.
6. S’atura. La crema de pastanaga està llesta!

Aquest conjunt d’ordres no és arbitrari, sinó que serveix per dur a terme una tasca
de certa complexitat que no es pot fer d’un sol cop. S’ha de fer pas per pas. Totes
les ordres estan vinculades entre si per arribar a assolir aquest objectiu i, sobretot,
és molt important la disposició en què es duen a terme.
Entrant ja, ara sí, en el món dels ordinadors, la manera com s’estructuren les
tasques que han de ser executades és similar als programes d’electrodomèstics
anteriorment citats. En aquest cas, però, en lloc de transformar ingredients (o
rentar roba bruta, si es tractés d’una rentadora), el que l’ordinador transforma és
informació o dades.

Un programa informàtic no és més que un seguit d’ordres que es porten a
terme seqüencialment, aplicades sobre un conjunt de dades.
Quines dades processa un programa informàtic? Bé, això dependrà del tipus de
programa:
* Un editor processa les dades d’un document de text.
* Un full de càlcul processa dades numèriques ubicades en un fitxer.
* Un videojoc processa les dades que fan referència a la forma i ubicació
d’enemics i jugadors, les interfícies gràfiques on es trobarà el jugador, els
punts aconseguits...
Entorns de desenvolupament 11 Desenvolupament de programari
* Un navegador web processa les ordres de l’usuari i les dades que rep des
d’un servidor ubicat a internet.
* Un reproductor de vídeo processa els fotogrames emmagatzemats en un
arxiu i l’àudio relacionat.

Per tant, la tasca d’un programador informàtic és escollir quines ordres constituiran
un programa d’ordinador, en quin ordre s’han de dur a terme i sobre quines
dades cal aplicar-les perquè el programa porti a terme la tasca que ha de resoldre.
La dificultat de tot plegat serà més o menys gran depenent de la complexitat
mateixa d’allò que cal que el programa faci. No és el mateix establir què ha de
fer l’ordinador per resoldre una multiplicació de tres nombres que per processar
textos o visualitzar pàgines a Internet.
D’altra banda, un cop fet el programa, cada cop que s’executi, l’ordinador complirà
totes les ordres del programa.

De fet, un ordinador és incapaç de fer absolutament res per si mateix, sempre
cal dir-li què ha de fer. I això se li diu mitjançant l’execució de programes. Tot
i que des del punt de vista de l’usuari pot semblar que quan es posa en marxa
un ordinador aquest funciona sense executar cap programa concret, cal tenir en
compte que el seu sistema operatiu és un programa que està sempre en execució.
