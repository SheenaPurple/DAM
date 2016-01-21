#1.6 Fases del desenvolupament dels sistemes d’informació

Una aplicació informàtica necessitarà moltes petites accions (i no tan petites) per
ser creada. S’han desenvolupat moltes metodologies que ofereixen un acompanyament
al llarg d’aquest desenvolupament, proporcionant pautes, indicacions,
mètodes i documents per ajudar, sobretot, els caps de projecte més inexperts.
Dintre d’aquestes metodologies hi ha Mètrica v3.0. Ha estat desenvolupada pel
Ministeri d’Administracions Públiques. Es tracta d’una metodologia per a la
planificació, desenvolupament i manteniment dels sistemes d’informació d’una
organització. Per al desenvolupament de programari cal fixar-se en la part
que fa referència al desenvolupament dels sistemes d’informació (SI), dins la
metodologia Mètrica. Divideix el desenvolupament en 5 fases, que se segueixen
de forma seqüencial.

També és important tenir clarament identificats els rols dels components de l’equip
de projecte que participaran en el desenvolupament de l’aplicació informàtica. A
Mètrica aquests perfils són:
* Parts interessades (stakeholders)
* Cap de Projecte
* Consultors
* Analistes
* Programadors
A la figura 1.14 hi podeu observar les cinc fases principals de la metodologia
Mètrica v3.0.

1.6.1 Estudi de viabilitat del sistema

El propòsit d’aquest procés és analitzar un conjunt concret de necessitats, amb la
idea de proposar una solució a curt termini. Els criteris amb què es fa aquesta
proposta no seran estratègics sinó tàctics i relacionats amb aspectes econòmics,
tècnics, legals i operatius.
Entorns de desenvolupament 33 Desenvolupament de programari
Els resultats de l’estudi de viabilitat del sistema constituiran la base per
prendre la decisió de seguir endavant o abandonar el projecte.

1.6.2 Anàlisi del sistema d’informació
El propòsit d’aquest procés és aconseguir l’especificació detallada del
sistema d’informació, per mitjà d’un catàleg de requisits i d’una sèrie de
models que cobreixin les necessitats d’informació dels usuaris per als quals
es desenvoluparà el sistema d’informació i que seran l’entrada per al procés
de Disseny del sistema d’informació.
En primer lloc, es descriu el sistema d’informació, a partir de la informació
obtinguda en l’estudi de viabilitat. Es delimita el seu abast, es genera un catàleg
de requisits generals i es descriu el sistema mitjançant uns models inicials d’alt
nivell.
Es recullen de forma detallada els requisits funcionals que el sistema d’informació
ha de cobrir. A més, s’identifiquen els requisits no funcionals del sistema, és a
dir, les facilitats que ha de proporcionar el sistema, i les restriccions a què estarà
sotmès, quant a rendiment, freqüència de tractament, seguretat...
Normalment, per tal d’efectuar l’anàlisi se sol elaborar els models de casos d’ús
i de classes, en desenvolupaments orientats a objectes, i de dades i processos
en desenvolupaments estructurats. D’altra banda, s’aconsella dur a terme una
definició d’interfícies d’usuari, ja que facilitarà la comunicació amb els usuaris
clau.

1.6.3 Disseny del sistema d’informació
El propòsit del disseny és obtenir la definició de l’arquitectura del sistema
i de l’entorn tecnològic que li donarà suport, juntament amb l’especificació
detallada dels components del sistema d’informació. A partir d’aquesta
informació, es generen totes les especificacions de construcció relatives al
propi sistema, així com l’especificació tècnica del pla de proves, la definició
dels requisits d’implantació i el disseny dels procediments de migració i
càrrega inicial.
En el disseny es generen les especificacions necessàries per a la construcció del
sistema d’informació, com per exemple:
Entorns de desenvolupament 34 Desenvolupament de programari
* Els components del sistema (mòduls o classes, segons el cas) i de les
estructures de dades.
* Els procediments de migració i els seus components associats.
* La definició i revisió del pla de proves, i el disseny de les verificacions dels
nivells de prova establerts.
* El catàleg d’excepcions, que permet establir un conjunt de verificacions
relacionades amb el propi disseny o amb l’arquitectura del sistema.
* L’especificació dels requisits d’implantació.

1.6.4 Construcció del sistema d’informació
La construcció del sistema d’informació té com a objectiu final la
construcció i la prova dels diferents components del sistema d’informació,
a partir del seu conjunt d’especificacions lògiques i físiques, obtingut en la
fase de disseny. Es desenvolupen els procediments d’operació i de seguretat,
i s’elaboren els manuals d’usuari final i d’explotació, aquests últims quan
sigui procedent.
Per aconseguir aquest objectiu, es recull la informació elaborada durant la fase
de disseny, es prepara l’entorn de construcció, es genera el codi de cada un dels
components del sistema d’informació i es van duent a terme, a mesura que es vagi
finalitzant la construcció, les proves unitàries de cada un d’ells i les d’integració
entre subsistemes. Si fos necessari efectuar una migració de dades, és en aquest
procés on es porta a terme la construcció dels components de migració i dels
procediments de migració i càrrega inicial de dades.

1.6.5 Implantació i acceptació del sistema
Aquest procés té com a objectiu principal el lliurament i l’acceptació
del sistema en la seva totalitat, que pot comprendre diversos sistemes
d’informació desenvolupats de manera independent, i un segon objectiu, que
és dur a terme les activitats oportunes per al pas a producció del sistema.
Un cop revisada l’estratègia d’implantació, s’estableix el pla d’implantació i es
detalla l’equip que el portarà a terme.
Per a l’inici d’aquest procés es prenen com a punt de partida els components
del sistema provats de forma unitària i integrats en el procés de construcció,
així com la documentació associada. El sistema s’ha de sotmetre a les proves
Entorns de desenvolupament 35 Desenvolupament de programari
d’implantació amb la participació de l’usuari d’operació. La responsabilitat, entre
altres aspectes, és comprovar el comportament del sistema sota les condicions més
extremes. El sistema també serà sotmès a les proves d’acceptació, que seran dutes
a terme per l’usuari final.
En aquest procés s’elabora el pla de manteniment del sistema, de manera que
el responsable del manteniment conegui el sistema abans que aquest passi a
producció.
També s’estableix l’acord de nivell de servei requerit una vegada que s’iniciï
la producció.
