#1.2 Codi font, codi objecte i codi excutable: màquines virtuals

Per crear un programa el que es farà serà crear un arxiu i escriure a un fitxer el
seguit d’instruccions que es vol que l’ordinador executi. Aquestes instruccions
hauran de seguir unes pautes determinades en funció del llenguatge de programació
escollit. A més, haurien de seguir un ordre determinat que donarà sentit al
programa escrit. Per començar n’hi haurà prou amb un editor de text simple.
Un cop s’ha acabat d’escriure el programa, el conjunt de fitxers de text
resultants, on es troben les instruccions, es diu que contenen el codi font.
Aquest codi font pot ser des d’un nivell molt alt, molt a prop del llenguatge
humà, fins a un de nivell més baix, més proper al codi de les màquines, com
ara el codi assemblador.

La tendència actual és fer ús de llenguatges d’alt nivell, és a dir, propers al
llenguatge humà. Però això fa aparèixer un problema, i és que els fitxers de codi
font no contenen el llenguatge màquina que entendrà l’ordinador. Per tant, resulten
incomprensibles per al processador. Per poder generar codi màquina cal fer un
procés de traducció des dels mnemotècnics que conté cada fitxer a les seqüències
binàries que entén el processador.

El procés anomenat compilació és la traducció del codi font dels fitxers del
programa en fitxers en format binari que contenen les instruccions en un format

Executar un programa
Per “executar un programa”
s’entén fer que l’ordinador
segueixi totes les seves ordres,
des de la primera fins a la
darrera.
Editors de text simples
Un editor de text simple és
aquell que permet escriure-hi
només text sense format. En són
exemples el Bloc de Notes
(Windows), el Gedit o l’Emacs
(Unix).
En l’apartat “Tipus de
llenguatges de
programació” es
descriuen les
característiques dels
llenguatges màquina,
assemblador, d’alt nivell i
de propòsit específic.

El codi objecte de les
instruccions té aquest
aspecte:
10101001000001101100110
101001010111000011101111

Entorns de desenvolupament 12 Desenvolupament de programari
que el processador pot entendre. El contingut d’aquests fitxers s’anomena codi
objecte. El programa que fa aquest procés s’anomena compilador.
El codi objecte és el codi font traduït (pel compilador) a codi màquina, però
aquest codi encara no pot ser executat per l’ordinador.
El codi executable és la traducció completa a codi màquina, duta a terme per
l’enllaçador (en anglès, linker). El codi executable és interpretat directament
per l’ordinador.
L’ enllaçador és l’encarregat d’inserir al codi objecte les funcions de les llibreries
que són necessàries per al programa i de dur a terme el procés de muntatge
generant un arxiu executable.
Una llibreria és un col·lecció de codi predefinit que facilita la tasca del programador
a l’hora de codificar un programa.
A la figura 1.1 es mostra un resum ordenat de tots els conceptes definits. El codi
font desenvolupat pels programadors es convertirà en codi objecte amb l’ajuda del
compilador. Aquest ajudarà a localitzar els errors de sintaxi o de compilació que es
trobin al codi font. Amb l’enllaçador, que recollirà el codi objecte i les llibreries,
es generarà el codi executable.


Procés de transformació d’un codi font a un codi executable
1.2.1 Màquina virtual
El concepte de màquina virtual sorgeix amb l’objectiu de facilitar el desenvolupament
de compiladors que generen codi per a diferents processadors.
La compilació consta de dues fases:
* La primera parteix del codi font a un llenguatge intermedi obtenint un
programa equivalent amb un menor nivell d’abstracció que l’original i que
no pot ser directament executat.
* La segona fase tradueix el llenguatge intermedi a un llenguatge comprensible
per la màquina.
Entorns de desenvolupament 13 Desenvolupament de programari
Arribat aquest punt es podria plantejar la pregunta: per què dividir la compilació
en dues fases? L’objectiu és que el codi de la primera fase, el codi intermedi, sigui
comú per a qualsevol processador, i que el codi generat en la segona fase sigui
l’específic per a cada processador. De fet, la traducció del llenguatge intermedi
al llenguatge màquina no se sol fer mitjançant compilació sinó mitjançant un
intèrpret, tal com es mostra en la figura 1.2.

Màquina virtual
La màquina virtual Java
La màquina virtual Java (JVM) és l’entorn en què s’executen els programes Java.
És un programa natiu, és a dir, executable en una plataforma específica, que és
capaç d’interpretar i executar instruccions expressades en un codi de bytes o (el
bytecode de Java) que és generat pel compilador del llenguatge Java.
La màquina virtual Java és una peça fonamental de la tecnologia Java. Se situa
en un nivell superior al maquinari sobre el qual es vol executar l’aplicació i
actua com un pont entre el codi de bytes a executar i el sistema. Així, quan un
programador escriu una aplicació Java, ho fa pensant en la JVM encarregada
d’executar l’aplicació i no hi ha cap motiu per pensar en les característiques
de la plataforma física sobre la qual s’ha d’executar l’aplicació. La JVM serà
l’encarregada, en executar l’aplicació, de convertir el codi de bytes a codi natiu de
la plataforma física.

El gran avantatge de la JVM és que possibilita la portabilitat de l’aplicació a
diferents plataformes i, així, un programa Java escrit en un sistema operatiu
Windows es pot executar en altres sistemes operatius (Linux, Solaris i Apple OS
X) amb l’únic requeriment de disposar de la JVM per al sistema corresponent.
Codi de bytes
El codi de bytes no és un
llenguatge d’alt nivell, sinó un
veritable codi màquina de baix
nivell, viable fins i tot com a
llenguatge d’entrada per a un
microprocessador físic.
Entorns de desenvolupament 14 Desenvolupament de programari
Als materials web es pot
trobar una explicació, pas
a pas, de com
descarregar i instal·lar la
màquina virtual Java.

El concepte de màquina virtual Java s’usa en dos àmbits: d’una banda, per fer
referència al conjunt d’especificacions que ha de complir qualsevol implementació
de la JVM; d’altra banda, per fer referència a les diverses implementacions de la
màquina virtual Java existents i de les quals cal utilitzar-ne alguna per executar les
aplicacions Java.

L’empresa Sun Microsystems és la propietària de la marca registrada Java, i
aquesta s’utilitza per certificar les implementacions de la JVM que s’ajusten i són
totalment compatibles amb les especificacions de la JVM, en el prefaci de les quals
es diu: “Esperem que aquesta especificació documenti suficientment la màquina
virtual de Java per fer possibles implementacions des de zero. Sun proporciona
tests que verifiquen que les implementacions de la màquina virtual Java operen
correctament.”
