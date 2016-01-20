#1.4 Paradigmes de programació

És difícil establir una classificació general dels llenguatges de programació, ja
que existeix un gran nombre de llenguatges i, de vegades, diferents versions d’un
mateix llenguatge. Això provocarà que en qualsevol classificació que es faci un
mateix llenguatge pertanyi a més d’un dels grups establerts. Una classificació
molt estesa, atenent a la forma de treballar dels programes i a la filosofia amb què
van ser concebuts, és la següent:
• Paradigma imperatiu/estructurat.
• Paradigma d’objectes.
• Paradigma funcional.
• Paradigma lògic.
El paradigma imperatiu/estructurat deu el seu nom al paper dominant
que exerceixen les sentències imperatives, és a dir aquelles que indiquen
dur a terme una determinada operació que modifica les dades guardades en
memòria.

Alguns dels llenguatges imperatius són C, Basic, Pascal, Cobol...
La tècnica seguida en la programació imperativa és la programació estructurada.
La idea és que qualsevol programa, per complex i gran que sigui, pot ser
representat mitjançant tres tipus d’estructures de control:
• Seqüència.
• Selecció.
• Iteració.

D’altra banda, també es proposa desenvolupar el programa amb la tècnica de
disseny descendent (top-down). És a dir, modular el programa creant porcions
més petites de programes amb tasques específiques, que se subdivideixen en altres
subprogrames, cada vegada més petits. La idea és que aquests subprogrames
típicament anomenats funcions o procediments han de resoldre un únic objectiu o
tasca.

Imaginem que hem de fer una aplicació que registri les dades bàsiques del personal
d’una escola, dades com poden ser el nom, el DNI, i que calculi el salari dels
professors així com el dels administratius, on el salari dels administratius és el
sou base (SOU_BASE) * 10 mentre que el salari dels professors és el sou base
(SOU_BASE) + nombre d’hores impartides (numhores) * 12.
Entorns de desenvolupament 22 Desenvolupament de programari
1 const float SOU_BASE = 1.000;
2
3 Struct Administratiu
4 {
5 string nom;
6 string DNI;
7 float Salari;
8 }
9
10 Struct Professor
11 {
12 string nom;
13 string DNI;
14 int numHores;
15 float salari;
16 }
17
18 void AssignarSalariAdministratiu (Administratiu administratiu1)
19 {
20 administratiu1. salari = SOU_BASE * 10;
21 }
22
23 void AssignarSalariProfessor (Professor professor1)
24 {
25 professor1. salari = SOU_BASE + (numHores * 12);
26 }

El paradigma d’objectes, típicament conegut com a Programació Orientada
a Objectes (POO, o OOP en anglès), és un paradigma de construcció de
programes basat en una abstracció del món real. En un programa orientat
a objectes, l’abstracció no són procediments ni funcions sinó els objectes.
Aquests objectes són una representació directa d’alguna cosa del món real,
com ara un llibre, una persona, una comanda, un empleat...
Alguns dels llenguatges de programació orientada a objectes són C++, Java, C#...
Un objecte és una combinació de dades (anomenades atributs) i mètodes (funcions
i procediments) que ens permeten interactuar amb ell. En aquest tipus de
programació, per tant, els programes són conjunts d’objectes que interactuen entre
ells a través de missatges (crides a mètodes).
La programació orientada a objectes es basa en la integració de 5 conceptes:
abstracció, encapsulació, modularitat, jerarquia i polimorfisme, que és necessari
comprendre i seguir de manera absolutament rigorosa. No seguir-los sistemàticament,
ometre’ls puntualment per pressa o altres raons fa perdre tot el valor i els
beneficis que ens aporta l’orientació a objectes.
1 class Treballador {
2 private:
3 string nom;
4 string DNI;
5 protected:
6 static const float SOU_BASE = 1.000;
7 public:
8 string GetNom() {return this.nom;}
9 void SetNom (string n) {this.nom = n;}
10 string GetDNI() {return this.DNI;}
11 void SetDNI (string dni) {this.DNI = dni;}
12 virtual float salari() = 0;
Entorns de desenvolupament 23 Desenvolupament de programari
13 }
14
15 class Administratiu: public Treballador {
16 public:
17 float Salari() {return SOU_BASE * 10};
18 }
19
20 class Professor: public Treballador {
21 private:
22 int numHores;
23 public:
24 float Salari() {return SOU_BASE + (numHores * 15);}
25 }

El paradigma funcional està basat en un model matemàtic. La idea és que
el resultat d’un càlcul és l’entrada del següent, i així successivament fins que
una composició produeixi el resultat desitjat.

Els creadors dels primers llenguatges funcionals pretenien convertir-los en llenguatges
d’ús universal per al processament de dades en tot tipus d’aplicacions,
però, amb el pas del temps, s’ha utilitzat principalment en àmbits d’investigació
científica i aplicacions matemàtiques.
Un dels llenguatges més típics del paradigma funcional és el Lisp. Vegeu un
exemple de programació del factorial amb aquest llenguatge:
1 > (defun factorial (n)
2 (if (= n 0)
3 1
4 (* n (factorial (− n 1)))))
5 FACTORIAL
6 > (factorial 3)
7 6

El paradigma lògic té com a característica principal l’aplicació de les regles
de la lògica per inferir conclusions a partir de dades.
Un programa lògic conté una base de coneixement sobre la que es duen a terme
consultes. La base de coneixement està formada per fets, que representen la
informació del sistema expressada com a relacions entre les dades i regles lògiques
que permeten deduir conseqüències a partir de combinacions entre els fets i, en
general, altres regles.
Un dels llenguatges més típics del paradigma lògic és el Prolog.
Exemple de desplegament pràctic del paradigma lògic
Determinarem si hem de prescriure al pacient estar a casa reposant al saber que es
compleixen els següents fets: malestar i 39º de temperatura corporal.
Regles de la base de coneixement:
* R1: Si febre, llavors estar a casa en repòs.
* R2: Si malestar, llavors posar-se termòmetre.
Entorns de desenvolupament 24 Desenvolupament de programari
* R3: Si termòmetre marca una temperatura > 37º, llavors febre.
* R4: Si diarrea, llavors dieta.

Si seguim un raonament d’encadenament cap endavant, el procediment seria:
1 Indicar el motor d'inferència, els fets: malestar i termòmetre
marca 39.
2
3 <code>Base de fets = { malestar, termòmetre marca º39 }
El sistema identifica les regles aplicables: R2 i R3. L’algorisme s’inicia aplicant la regla R2,
incorporant en la base de fets “posar-se el termòmetre”.
1 Base de fets = { malestar, termòmetre marca º39, posar−se termò
metre }
Com que no s’ha solucionat el problema, continua amb la següent regla R3, afegint a la
base de fets “febre”.
1 Base de fets = { malestar, termòmetre marca º39, posar−se termò
metre, febre }
Com que no s’ha solucionat el problema, torna a identificar un subconjunt de regles
aplicables, excepte les ja utilitzades. El sistema identifica les regles aplicables: R1, tot
incorporant a la base de fets “estar a casa en repòs”.
1 Base de fets = { malestar, termòmetre marca º39, posar−se termò
metre, febre, estar a casa en repòs}
Com que repòs està a la base de fets, s’ha arribat a una resposta positiva a la pregunta
formulada.
El paradigma és àmpliament utilitzat en les aplicacions que tenen a veure amb
la Intel·ligència Artificial, particularment en el camp de sistemes experts i processament
del llenguatge humà. Un sistema expert és un programa que imita el
comportament d’un expert humà. Per tant conté informació (és a dir una base de
coneixements) i una eina per comprendre les preguntes i trobar la resposta correcta
examinant la base de dades (un motor d’inferència).
També és útil en problemes combinatoris o que requereixin una gran quantitat o
amplitud de solucions alternatives, d’acord amb la naturalesa del mecanisme de
tornada enrere (backtracking).
