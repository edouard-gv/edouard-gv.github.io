## ÉPREUVE SPÉCIFIQUE - FILIÈRE PC

## PHYSIQUE

## Durée : 4 heures

N.B. : le candidat attachera la plus grande importance à la clarté, à la précision et à la concision de la rédaction. Si un candidat est amené à repérer ce qui peut lui sembler être une erreur d'énoncé, il le signalera sur sa copie et devra poursuivre sa composition en expliquant les raisons des initiatives qu'il a été amené à prendre.

## RAPPEL DES CONSIGNES

- Utiliser uniquement un stylo noir ou bleu foncé non effaçable pour la rédaction de votre composition ; d'autres couleurs, excepté le vert, peuvent être utilisées, mais exclusivement pour les schémas et la mise en évidence des résultats.
- Ne pas utiliser de correcteur.
- Écrire le mot FIN à la fin de votre composition.


## Les calculatrices sont autorisées.

## Le problème est composé de trois parties indépendantes.

Les points sont répartis approximativement de la façon suivante :

| Partie I | $25 \%$ |
| :--- | :--- |
| Partie II | $30 \%$ |
| Partie III | $45 \%$ |

## La qualité de l'air dans l'habitat

La notion de confort dans l'habitat caractérise, pour un individu donné, son état de satisfaction avec les conditions d'environnement. Indépendamment des conditions propres à l'individu que sont son métabolisme, son activité, son habillement et sa santé, il est reconnu que quatre paramètres influencent le confort : l'environnement thermique, l'éclairage, la protection acoustique et, enfin, la qualité de l'air dont on propose l'étude dans ce sujet.
On étudiera ainsi dans la partie I un système de ventilation mécanique visant à renouveler l'air dans l'habitat. On réalisera dans la sous-partie $\mathbf{I} . \mathbf{1}$ un bilan général d'énergie pour un fluide en écoulement stationnaire, avant d'analyser le principe d'une ventilation mécanique contrôlée à double flux en sous-partie I.2. Dans la partie II, on s'intéressera à l'humidité de l'air dans l'habitat avec quelques généralités sur l'air humide en sous-partie II.1, puis la description du fonctionnement d'un hygromètre capacitif en sous-partie II.2. Enfin, on abordera la problématique de la nuisance sonore liée aux systèmes de renouvellement d'air dans la partie III. On détaillera à cet effet le principe de la correction acoustique d'une pièce d'habitation en sous-partie III.1, puis celui d'un silencieux à résonateur de Helmholtz en sous-partie III.2.

## Données

- Masse molaire de l'air sec : $M_{a s}=29 \mathrm{~g} \cdot \mathrm{~mol}^{-1}$
- Masse molaire de l'eau : $M_{e}=18 \mathrm{~g} \cdot \mathrm{~mol}^{-1}$
- Constante des gaz parfaits : $R=8,3 \mathrm{~J} \cdot \mathrm{~K}^{-1} \cdot \mathrm{~mol}^{-1}$
- Rapport entre les capacités thermiques à pression et volume constants d'un gaz parfait diatomique pour les températures considérées : $\gamma=1,4$
- Pression atmosphérique : $p_{0}=1,0 \cdot 10^{5} \mathrm{~Pa}$
- Masse volumique de l'eau liquide pour les températures considérées : $\rho_{e}=1,0 \cdot 10^{3} \mathrm{~kg} \cdot \mathrm{~m}^{-3}$
- Permittivité du vide : $\varepsilon_{0}=8,9 \cdot 10^{-12} \mathrm{~F} \cdot \mathrm{~m}^{-1}$
- $\log (x)=\frac{\ln (x)}{\ln (10)}$
- Opérateurs en coordonnées cylindriques $(r, \theta, z)$ pour un champ scalaire $U$ et un champ vectoriel $\vec{a}=a_{r} \vec{u}_{r}+a_{\theta} \vec{u}_{\theta}+a_{z} \vec{u}_{z}$ :
$\overrightarrow{\operatorname{grad}}(U)=\frac{\partial U}{\partial r} \vec{u}_{r}+\frac{1}{r} \frac{\partial U}{\partial \theta} \vec{u}_{\theta}+\frac{\partial U}{\partial z} \vec{u}_{z}$
$\operatorname{div}(\vec{a})=\frac{1}{r} \frac{\partial\left(r a_{r}\right)}{\partial r}+\frac{1}{r} \frac{\partial a_{\theta}}{\partial \theta}+\frac{\partial a_{z}}{\partial z}$
$\overrightarrow{\operatorname{rot}}(\vec{a})=\left[\frac{1}{r} \frac{\partial a_{z}}{\partial \theta}-\frac{\partial a_{\theta}}{\partial z}\right] \vec{u}_{r}+\left[\frac{\partial a_{r}}{\partial z}-\frac{\partial a_{z}}{\partial r}\right] \vec{u}_{\theta}+\frac{1}{r}\left[\frac{\partial\left(r a_{\theta}\right)}{\partial r}-\frac{\partial a_{r}}{\partial \theta}\right] \vec{u}_{z}$


## Partie I- Le renouvellement de l'air dans l'habitat

La ventilation des principales pièces de l'habitat est indispensable pour assurer un niveau minimal de salubrité de l'air, par exemple par un simple apport d'air neuf de l'extérieur grâce à l'aération naturelle par les ouvrants de ces pièces (portes, fenêtres). Cette solution n'est toutefois pas sans inconvénients sur le confort thermique des occupants et l'efficacité énergétique de l'habitat, l'air extérieur étant plus froid que l'air intérieur en hiver et plus chaud en été. L'utilisation d'une ventilation mécanique contrôlée à double flux est aujourd'hui la solution la plus commune retenue pour éviter ces inconvénients.

## I. 1 - Bilan énergétique pour un fluide en écoulement stationnaire

On considère l'écoulement parfait et stationnaire d'un fluide à travers un système ouvert ( $\mathcal{S}$ ), définissant un volume de contrôle indéformable et fixe dans le référentiel d'étude $\mathcal{R}$ et présentant une entrée et une sortie (figure 1).
On définit comme système d'étude le système fermé, noté ( $\mathcal{S}^{*}$ ), constitué du fluide contenu à l'instant $t$ dans le volume de contrôle et du fluide de masse $\delta m_{1}$ qui y rentre entre les instants $t$ et $t+\mathrm{d} t$, situé entre les sections droites ( $\Sigma_{1}^{\prime}$ ) et ( $\Sigma_{1}$ ), et définissant un sous-système ( $\mathcal{S}_{1}$ ). À l'instant $t+\mathrm{d} t$, il est constitué du fluide contenu dans le volume de contrôle et du fluide de masse $\delta m_{2}$ qui en sort entre les instants $t$ et $t+\mathrm{d} t$, situé entre les sections droites $\left(\Sigma_{2}\right)$ et $\left(\Sigma^{\prime}{ }_{2}\right)$, et définissant un sous-système ( $\mathcal{S}_{2}$ ).
On note $T_{i}, p_{i}, \rho_{i}, e_{c, i}, e_{p, i}, u_{i}$ et $h_{i}$ respectivement la température, la pression, la masse volumique, l'énergie cinétique massique, l'énergie potentielle de pesanteur massique, l'énergie interne massique et l'enthalpie massique du fluide contenu dans chaque sous-système ( $\mathcal{S}_{i}$ ) où $i=1,2$.

![](https://cdn.mathpix.com/cropped/4bc0bb47-e03f-4b68-b88f-13e567a25830-03.jpg?height=575&width=1337&top_left_y=1571&top_left_x=370)
Figure 1 - Fluide en écoulement stationnaire : système fermé étudié

Q1. En traduisant la conservation de la masse du fluide contenu dans le système ( $\mathcal{S}^{*}$ ), justifier que le débit massique du fluide en entrée est égal à celui en sortie : $\frac{\delta m_{1}}{\mathrm{~d} t}=\frac{\delta m_{2}}{\mathrm{~d} t}=D_{m}$.

Q2. Montrer que le travail massique des forces pressantes reçu par le fluide contenu dans le système $\left(\mathcal{S}^{*}\right)$ pendant la durée d $t$ s'écrit : $w_{p}=\frac{p_{1}}{\rho_{1}}-\frac{p_{2}}{\rho_{2}}$.

Q3. Montrer que la variation d'énergie interne du fluide contenu dans le système ( $\mathcal{S}^{*}$ ) pendant la durée $\mathrm{d} t$ s'écrit : $\mathrm{d} U=D_{m}\left(u_{2}-u_{1}\right) \mathrm{d} t$.
Donner, sans calculs supplémentaires, les expressions des variations d'énergie cinétique macroscopique $\mathrm{d} E_{c}$ et d'énergie potentielle de pesanteur $\mathrm{d} E_{p}$ du fluide.

Q4. À partir d'un bilan énergétique pour le fluide contenu dans le système ( $\mathcal{S}^{*}$ ) pendant la durée $\mathrm{d} t$, établir l'expression du premier principe pour un écoulement stationnaire :

$$
D_{m}\left[\left(h_{2}+e_{c, 2}+e_{p, 2}\right)-\left(h_{1}+e_{c, 1}+e_{p, 1}\right)\right]=\mathcal{P}_{u}+\mathcal{P}_{t h}
$$

où $\mathcal{P}_{u}$ et $\mathcal{P}_{t h}$ sont respectivement la puissance mécanique des forces extérieures non conservatives autre que celle des forces pressantes (puissance dite utile) et le flux thermique reçus par le fluide contenu dans le volume de contrôle.

## 1.2 - Étude d'une ventilation mécanique contrôlée à double flux

On modélise une habitation par une pièce unique, de température intérieure supposée uniforme $T_{\text {int }}=20,0^{\circ} \mathrm{C}$ et maintenue constante grâce à un chauffage. L'air à l'extérieur de l'habitation est à la température constante $T_{\text {ext }}=0,0^{\circ} \mathrm{C}$.

Q5. En l'absence de toute ventilation, le flux thermique lié aux pertes à travers l'ensemble des parois (fenêtres, toit, murs) séparant l'habitation de l'extérieur est $\mathcal{P}_{t h, p}=5,0 \mathrm{~kW}$ en régime stationnaire. Estimer la résistance thermique $R_{t h}$ de l'ensemble de ces parois.

L'habitation est désormais munie d'une ventilation mécanique contrôlée (VMC) à double flux. Elle se distingue d'une VMC simple flux qui insuffle dans l'habitation de l'air froid neuf à la température $T_{\text {ext }}$ et extrait de l'air chaud vicié (c'est-à-dire ayant "servi") à la température $T_{\text {int }}$. Une VMC double flux comporte en effet un échangeur thermique tel que l'air chaud vicié sortant préchauffe l'air froid neuf entrant (figure 2).

![](https://cdn.mathpix.com/cropped/4bc0bb47-e03f-4b68-b88f-13e567a25830-04.jpg?height=639&width=1575&top_left_y=1726&top_left_x=228)
Figure 2 - Schéma de principe d'une VMC double flux

En régime stationnaire, l'air neuf entrant dans le système à la température $T_{\text {ext }}=0,0{ }^{\circ} \mathrm{C}$ traverse l'échangeur avec un débit massique $D_{m}=150 \mathrm{~kg} \cdot \mathrm{~h}^{-1}$ avant d'être insufflé dans l'habitation à la température $T^{\prime}{ }_{\text {ext }}=15,0^{\circ} \mathrm{C}$. Quant à l'air vicié aspiré dans l'habitation à la température $T_{\text {int }}=20,0^{\circ} \mathrm{C}$, il sort du système à la température $T^{\prime}{ }_{\text {int }}$ après traversée de l'échangeur avec le même débit $D_{m}$. Au sein de l'échangeur parfaitement isolé du reste du système, l'air neuf circule dans une conduite plane en contact avec une autre conduite plane dans laquelle circule l'air vicié de façon à assurer les échanges thermiques (figure 3). On néglige toute variation de l'énergie cinétique et de l'énergie potentielle de pesanteur de l'air circulant dans chacune des deux conduites.

![](https://cdn.mathpix.com/cropped/4bc0bb47-e03f-4b68-b88f-13e567a25830-05.jpg?height=334&width=906&top_left_y=742&top_left_x=317)
Figure 3 - Échangeur thermique

Q6. On assimile l'air supposé sec, donc sans vapeur d'eau, à un gaz parfait. Dans ces conditions, les capacités thermiques à pression et volume constants d'une quantité de matière $n$ d'air, notées respectivement $C_{P}$ et $C_{V}$, sont reliées par la relation de Mayer: $C_{P}-C_{V}=n R$. Établir l'expression de la capacité thermique massique à pression constante $c_{P}$ de l'air en fonction notamment du rapport $\gamma$ entre les capacités thermiques à pression et volume constants. Calculer $c_{P}$.

Q7. Montrer à l'aide de l'expression établie à la Q4 et en précisant les systèmes ouverts choisis que $T_{\text {int }}-T_{\text {int }}^{\prime}=T_{\text {ext }}^{\prime}-T_{\text {ext }}$. Calculer $T_{\text {int }}^{\prime}$.

Q8. Donner l'expression littérale du flux thermique $\mathcal{P}_{t h, a}$ reçu par l'air insufflé à la température $T^{\prime}{ }_{\text {ext }}$ pour le réchauffer à la température $T_{\text {int }}$ de la pièce. Calculer $\mathcal{P}_{t h, a}$.

Q9. Déduire des résultats précédents la puissance $\mathcal{P}_{c}$ fournie par le chauffage pour maintenir une température intérieure $T_{\text {int }}$ constante. Calculer $\mathcal{P}_{c}$.

Q10. Dans le cas d'une VMC simple flux, calculer le flux thermique $\mathcal{P}_{t h, a}^{\prime}$ reçu par l'air insufflé pour le réchauffer à la température de la pièce, puis la puissance $\mathcal{P}^{\prime}{ }_{c}$ fournie par le chauffage pour maintenir cette température constante. En déduire le pourcentage d'énergie économisée en passant d'une VMC simple flux à une VMC double flux : $\frac{\mathcal{P}^{\prime}{ }_{c}-\mathcal{P}_{c}}{\mathcal{P}^{\prime}{ }_{c}}$.
Quel serait le pourcentage d'énergie économisée si l'échange thermique entre l'air neuf et l'air vicié était parfait, c'est-à-dire si l'air vicié sortait de l'échangeur à la température $T_{\text {ext }}$ ?

## Partie II - L'humidité de l'air dans l'habitat

L'humidité de l'air d'une pièce doit être contrôlée. Trop grande, elle peut en effet favoriser le développement de moisissures, bactéries, acariens, mais aussi provoquer la dégradation de certains matériaux.

## II. 1 - L'air humide

L'air sec ne contient pas de vapeur d'eau. C'est un mélange de gaz, de proportions connues et invariables, principalement du diazote et du dioxygène. Un mélange d'air sec, de masse molaire $M_{a s}$ et de pression partielle $p_{a s}$, et de vapeur d'eau, de masse molaire $M_{e}$ et de pression partielle $p_{e}$, est qualifié d'air humide. Ce mélange sera considéré par la suite comme un mélange idéal de gaz parfaits.

L'air humide est caractérisé à la température $T$ par son degré hygrométrique $\varphi$ ou humidité relative: $\varphi=\frac{p_{e}}{p_{e, s a t}(T)}$ où $p_{e, s a t}(T)$ est la pression de vapeur saturante (pression d'équilibre liquide-vapeur) de l'eau pure à la température considérée.

Q11. Représenter l'allure du diagramme des phases pression-température du corps pur "eau". Y indiquer le domaine de chaque phase en présence. Définir avec précision les deux points caractéristiques qui y figurent.

L'air d'une cuisine hermétiquement close, de volume $V=50 \mathrm{~m}^{3}$, est à la pression atmosphérique $p_{0}$ et à la température $T=293 \mathrm{~K}$. À cette température, la pression de vapeur saturante de l'eau est égale à $2,3 \cdot 10^{3} \mathrm{~Pa}$. Le degré hygrométrique de l'air dans cette pièce est de $55 \%$.

Q12. Rappeler la relation entre $p_{0}$ et les pressions partielles $p_{e}$ et $p_{\text {as }}$.
Calculer les masses $m_{e}$ de vapeur d'eau et $m_{a s}$ d'air sec dans la pièce. En déduire la valeur de l'humidité spécifique $\phi$ de l'air de la pièce, exprimée en kg d'eau par kg d'air sec et définie par : $\phi=\frac{m_{e}}{m_{a s}}$.

Q13. On porte à ébullition un récipient rempli d'eau. Calculer le volume $V_{e}$ d'eau à évaporer pour saturer en humidité l'air de la cuisine, c'est-à-dire atteindre un degré hygrométrique de $100 \%$. On négligera l'augmentation de la température de l'air de la cuisine.

On considère maintenant que la cuisine de volume $V$ est dotée d'un système de renouvellement d'air. L'air est supposé homogène dans la pièce, avec à l'instant $t$ une concentration massique en vapeur d'eau $C(t)$ uniforme (exprimée en kg d'eau par $\mathrm{m}^{3}$ d'air). De l'air extérieur neuf, de concentration massique en vapeur d'eau $C_{\text {ext }}$ constante, entre dans la cuisine avec un débit volumique $D_{v}$, tandis que de l'air vicié de concentration massique $C(t)$ sort de la cuisine avec le même débit. Les personnes présentes dans la cuisine et leurs activités sont une source de vapeur d'eau. On note $S$ le taux de création de vapeur d'eau dans la pièce, c'est-à-dire la masse de vapeur d'eau créée par unité de temps.

Q14. Établir une équation différentielle vérifiée par $C(t)$ à partir d'un bilan de masse entre les instants $t$ et $t+\mathrm{d} t$ pour la vapeur d'eau dans l'air de la cuisine.
En déduire que le débit volumique minimal nécessaire pour maintenir une concentration en vapeur d'eau sous une valeur limite $C_{\text {lim }}$ s'écrit en régime stationnaire : $D_{v, m}=\frac{S}{C_{\text {lim }}-C_{\text {ext }}}$.

Q15. L'air extérieur, de température égale à $5^{\circ} \mathrm{C}$, a un degré hygrométrique de $100 \%$, soit une concentration massique en vapeur d'eau $C_{\text {ext }}=7,0 \cdot 10^{-3} \mathrm{~kg} \cdot \mathrm{~m}^{-3}$. Le taux de création de vapeur d'eau dans la cuisine est $S=0,30 \mathrm{~kg} \cdot \mathrm{~h}^{-1}$. Pour l'air dans la cuisine, de température égale à $20^{\circ} \mathrm{C}$, on souhaite ne pas dépasser un degré hygrométrique de $60 \%$, soit une concentration massique en vapeur d'eau $C_{\text {lim }}=1,0 \cdot 10^{-2} \mathrm{~kg} \cdot \mathrm{~m}^{-3}$. Calculer le débit volumique minimal nécessaire $D_{v, m}$. Commenter le choix d'un débit massique de renouvellement d'air $D_{m}=150 \mathrm{~kg} \cdot \mathrm{~h}^{-1}$ comme celui de la VMC double flux étudiée dans la partie $\mathbf{I}$.

## II. 2 - Principe d'un capteur d'humidité capacitif

Deux disques conducteurs, de rayon $a$, de même axe ( $O, \vec{u}_{z}$ ), distants de $d \ll a$, constituent les armatures d'un condensateur à vide (figure 4). La charge portée par chaque armature varie de façon sinusoïdale avec le temps, à la fréquence $f$. On note $q(t)=q_{0} \cos (2 \pi f t)$ la charge portée par l'armature supérieure à l'instant $t$. On suppose que le courant qui apporte ces charges arrive par des fils infinis confondus avec l'axe de révolution ( $O, \vec{u}_{z}$ ) du condensateur.
On s'intéresse au champ électromagnétique ( $\vec{E}(M, t) ; \vec{B}(M, t)$ ) en tout point $M$ à l'intérieur du condensateur et repéré par ses coordonnées cylindriques ( $r, \theta, z$ ) dans le repère ( $O, \vec{u}_{r}, \vec{u}_{\theta}, \vec{u}_{z}$ ).

![](https://cdn.mathpix.com/cropped/4bc0bb47-e03f-4b68-b88f-13e567a25830-07.jpg?height=442&width=524&top_left_y=1528&top_left_x=769)
Figure 4 - Condensateur à symétrie cylindrique
Les échelles ne sont pas respectées

Q16. Justifier par des considérations de symétries et d'invariances que le champ électrique $\vec{E}(M, t)$ est a priori de la forme : $\vec{E}(M, t)=E_{r}(r, z, t) \vec{u}_{r}+E_{z}(r, z, t) \vec{u}_{z}$.

Q17. On suppose en première approximation que $\overrightarrow{\operatorname{rot}}(\vec{E}) \simeq \overrightarrow{0}$. En déduire l'ordre de grandeur du rapport $\left|\frac{E_{r}}{E_{z}}\right|$. Conclure sachant que les effets de bords sont négligeables ( $d \ll a$ ).
Déduire d'une autre équation de Maxwell que le champ $\vec{E}(M, t)$ est finalement de la forme : $\vec{E}(M, t)=E_{z}(r, t) \vec{u}_{z}$.

Q18. On cherche en première approximation un champ uniforme à l'intérieur du condensateur : $\vec{E}(M, t)=\vec{E}_{0}(t)=E_{0, z}(t) \vec{u}_{z}$.
Déduire du théorème de Gauss appliqué à une surface à définir clairement, notamment à l'aide d'un schéma, l'expression du champ électrique $\vec{E}_{0}(t)$. On donnera le résultat en fonction de $q(t)$, $a$ et de la permittivité du vide $\varepsilon_{0}$. On admettra que le champ électrique est nul à l'extérieur du condensateur et on supposera que la densité surfacique de charges portée par chaque armature est uniforme.

Du fait de sa dépendance par rapport au temps, le champ $\vec{E}_{0}(t)$ crée un champ magnétique induit $\vec{B}_{1}(M, t)$. Le champ magnétique $\vec{B}_{1}(M, t)$ crée à son tour un champ induit $\vec{E}_{2}(M, t)$, terme correctif pour le champ électrique qui s'écrit : $\vec{E}(M, t)=\vec{E}_{0}(t)+\vec{E}_{2}(M, t)$.

Q19. À quelle condition portant sur $\left\|\vec{E}_{2}\right\|$ et $\left\|\vec{E}_{0}\right\|$ peut-on considérer que $\overrightarrow{\operatorname{rot}}(\vec{E}) \simeq \overrightarrow{0}$ comme supposé à la Q17 ?
On admet que cette condition est vérifiée si $a \ll c / f$ où $c$ est la célérité des ondes électromagnétiques dans le vide. Proposer une interprétation physique.

La condition précédente étant vérifiée, le champ électrique à l'intérieur du condensateur dérive donc d'un potentiel scalaire $V_{0}(M, t)$ tel que $\vec{E}_{0}=-\overrightarrow{\operatorname{grad}}\left(V_{0}\right)$.

Q20. Donner l'expression du potentiel scalaire $V_{0}(M, t)$ à une constante additive près.
Exprimer la différence de potentiel $V_{0}(z=d)-V_{0}(z=0)$ entre les deux armatures et en déduire que la capacité $C$ du condensateur s'écrit : $C=\frac{\varepsilon_{0} \pi a^{2}}{d}$.

On munit désormais le condensateur d'une armature poreuse et on le remplit d'un polymère hygroscopique pouvant adsorber l'eau de l'air et dont la permittivité diélectrique $\varepsilon$ est fonction du degré hygrométrique de l'air. On admet que la capacité $C$ de ce condensateur a la même expression que celle du condensateur à vide établie à la Q20 à condition de remplacer la permittivité $\varepsilon_{0}$ du vide par la permittivité $\varepsilon$ du polymère. Le condensateur possède en outre une résistance de fuite $R$, principalement due au polymère qui en adsorbant l'eau ne se comporte pas comme un isolant parfait. Le modèle électrique équivalent de ce condensateur est constitué de la capacité $C$ en parallèle avec la résistance $R$.
Le condensateur est inséré dans le circuit suivant (figure 5), appelé pont de Sauty, alimenté sous une tension sinusoïdale $e(t)$ de pulsation $\omega$, où la résistance $R_{0}$ et la capacité $C_{0}$ sont variables. On note $u(t)$ la tension entre les points $A$ et $B, \underline{e}$ et $\underline{u}$ les représentations complexes des tensions respectives $e(t)$ et $u(t)$. On note $\underline{Z}_{0}$ l'impédance de l'association parallèle de la capacité $C_{0}$ et de la résistance $R_{0}$ entre les points $M$ et $B$, et $\underline{Z}$ l'impédance de l'association parallèle de la capacité $C$ et de la résistance $R$ entre les points $B$ et $N$.

![](https://cdn.mathpix.com/cropped/4bc0bb47-e03f-4b68-b88f-13e567a25830-09.jpg?height=597&width=752&top_left_y=203&top_left_x=653)
Figure 5 - Pont de Sauty

Q21. Exprimer en fonction de $\underline{e}$ et des différentes impédances les tensions $\underline{u}_{A N}$ et $\underline{u}_{B N}$.
En déduire que $\underline{u}=\frac{R_{2} \underline{Z}_{0}-R_{1} \underline{Z}}{\left(R_{1}+R_{2}\right)\left(\underline{Z}_{0}+\underline{Z}\right)} \underline{e}$.
Q22. Le pont de Sauty est dit équilibré lorsque $\underline{u}=0$, quelle que soit la tension $\underline{e}$. Montrer que l'équilibre du pont permet de déterminer $R$ et $C$, dont on donnera l'expression en fonction de $R_{0}, R_{1}, R_{2}$ et $C_{0}$.

Q23. On utilise le condensateur en tant que capteur d'humidité dont on donne ci-dessous la courbe d'étalonnage (figure 6). Déterminer le degré hygrométrique de la pièce dans laquelle il est plongé sachant que le pont de Sauty est équilibré pour $C_{0}=1,44 \mathrm{nF}$ avec $R_{1} / R_{2}=0,1$.

![](https://cdn.mathpix.com/cropped/4bc0bb47-e03f-4b68-b88f-13e567a25830-09.jpg?height=819&width=1308&top_left_y=1507&top_left_x=372)
Figure 6 - Courbe d'étalonnage du capteur
Source : data sheet capacitive humidity sensor P14 rapid-W, Innovative Sensor Technology

## Partie III - Nuisances sonores

Dans un système de renouvellement d'air, de l'air vicié est aspiré et de l'air neuf insufflé dans la pièce à traiter. Entre l'aspiration et le soufflage, l'air a traversé des éléments générateurs de bruits (ventilateur, gaines…) qui peuvent parfois s'avérer gênants.

## III. 1 - Correction acoustique et théorie de la réverbération de Sabine

Afin d'assurer le confort acoustique des occupants d'une pièce d'habitation vis-à-vis des bruits qui lui sont propres, une solution consiste à recouvrir les parois de la pièce avec des matériaux absorbants appropriés. Cette méthode, appelée correction acoustique, permet d'optimiser selon l'usage de la pièce sa durée de réverbération liée à la multiplicité des échos sonores renvoyés par les parois.

On considère un fluide, caractérisé à l'équilibre par un champ des vitesses uniformément nul et des champs de pression et de masse volumique uniformes et stationnaires, notés respectivement $p_{0}$ et $\rho_{0}$. Lorsque l'équilibre est rompu au passage d'une onde sonore se propageant selon l'axe ( $O, \vec{u}_{x}$ ), le fluide est alors caractérisé à l'instant $t$ en tout point $M$ d'abscisse $x$ de l'écoulement supposé parfait par :

- un champ de pression $p(x, t)=p_{0}+p_{1}(x, t)$ où la quantité $p_{1}$ est appelée surpression ou pression acoustique ;
- un champ de masse volumique $\rho(x, t)=\rho_{0}+\rho_{1}(x, t)$;
- un champ des vitesses $\vec{v}(x, t)=\overrightarrow{0}+\vec{v}_{1}(x, t)=v_{1}(x, t) \vec{u}_{x}$.

Q24. La propagation de la perturbation dans le fluide est traitée dans l'approximation acoustique. Préciser le cadre de cette approximation.

Q25. Rappeler l'équation d'Euler, limitée aux seules forces pressantes (effets de la pesanteur négligés en particulier). En déduire après linéarisation l'équation de couplage :

$$
\rho_{0} \frac{\partial v_{1}}{\partial t}+\frac{\partial p_{1}}{\partial x}=0
$$

Établir de la même façon une seconde équation de couplage linéarisée à partir de l'équation locale de conservation de la masse.

Q26. Le fluide évolue de façon isentropique sous l'effet des ondes sonores. Montrer que $\rho_{1}=\rho_{0} \chi_{S, 0} p_{1}$ où $\chi_{S, 0}$ est le coefficient de compressibilité isentropique du fluide à l'équilibre.
On rappelle que $\chi_{S}=\frac{1}{\rho}\left(\frac{\partial \rho}{\partial p}\right)_{S}$.
Q27. Déduire de l'ensemble des résultats précédents que la pression acoustique $p_{1}(x, t)$ obéit à une équation de d'Alembert. Donner l'expression de la célérité $c$ des ondes sonores en fonction de $\chi_{S, 0}$ et $\rho_{0}$.

Q28. On suppose que le fluide évoluant de façon isentropique se comporte en outre comme un gaz parfait. Justifier que $p \rho^{-\gamma}=C^{\text {ste }}$ où $\gamma$ est le rapport entre les capacités thermiques à pression et volume constants du fluide. En déduire que la célérité des ondes sonores s'écrit :

$$
c=\sqrt{\frac{\gamma p_{0}}{\rho_{0}}}
$$

L'onde est plane, progressive, sinusoïdale de pulsation $\omega$, de la forme $p_{1}(x, t)=p_{1, m} \cos (\omega t-k x)$ pour la pression acoustique, avec $k=\frac{\omega}{c}$.

Q29. Déduire de l'une des équations de couplage établies à la Q25 l'expression du rapport $Z_{c}=\frac{p_{1}}{v_{1}}$, appelé impédance caractéristique du milieu, en fonction de $\rho_{0}$ et $c$. Que devient la relation entre $p_{1}$ et $v_{1}$ dans le cas d'une onde se propageant dans le sens inverse?

Q30. La densité volumique d'énergie sonore $\langle e\rangle_{T}$ associée à l'onde s'écrit en moyenne sur une période $T=\frac{2 \pi}{\omega}:\langle e\rangle_{T}=\frac{1}{2} \rho_{0}\left\langle v_{1}^{2}\right\rangle_{T}+\frac{1}{2} \chi_{S, 0}\left\langle p_{1}^{2}\right\rangle_{T}$.
Quelle est la signification physique de chacun des termes composant cette expression ? Exprimer $\langle e\rangle_{T}$ pour l'onde considérée en fonction de $p_{1, m}, \rho_{0}$ et $c$.

Q31. On appelle intensité sonore $I$ la grandeur définie par: $I=\left|\left\langle p_{1} v_{1}\right\rangle_{T}\right|$. Vérifier que cette grandeur est homogène à une puissance surfacique. Montrer que l'intensité sonore est proportionnelle à la densité volumique d'énergie sonore $\langle e\rangle_{T}$ pour l'onde considérée.

Le fluide est l'air d'une pièce d'habitation, au centre de laquelle se trouve une source sonore ponctuelle et isotrope, émettant de façon continue un son harmonique. En un point donné de la pièce, on distingue le champ direct dû à l'onde divergente émise par la source qui n'a pas encore rencontré d'obstacles, du champ réverbéré dû à l'ensemble des ondes ayant eu une ou plusieurs réflexion(s) sur les parois et les objets de la pièce. Dans la théorie de l'acousticien américain Sabine, la densité volumique d'énergie sonore du champ réverbéré $\left\langle e_{r}\right\rangle_{T}$ est supposée uniformément répartie dans toute la pièce à un instant donné. Dans ces conditions, on montre que l'intensité sonore correspondante s'écrit: $I_{r}=\frac{c\left\langle e_{r}\right\rangle_{T}}{4}$. On notera que $I_{r}$ et $\left\langle e_{r}\right\rangle_{T}$ sont des quantités moyennées sur une période $T$ de la source, mais sont susceptibles de varier sur une échelle de temps caractéristique $\tau$ beaucoup plus grande.

On néglige dans la suite l'absorption due à l'air, mais pas celle due aux parois et objets de la pièce. On note $V$ le volume de la pièce, $S$ la surface totale des parois et des objets de la pièce, $\alpha_{m}$ leur coefficient d'absorption moyen, défini comme le rapport entre la puissance sonore absorbée au niveau des parois et des objets et la puissance sonore incidente.
À l'instant $t=0$, on coupe la source sonore. On se propose d'établir la loi de décroissance $I_{r}(t)$ de l'intensité sonore du champ réverbéré au cours du temps.

Q32. Exprimer la puissance sonore moyenne $\mathcal{P}_{a}$ absorbée par les parois et les objets de la pièce en fonction de $I_{r}, \alpha_{m}$ et $S$.
Exprimer de même l'énergie sonore moyenne $\mathcal{E}(t)$ dans la pièce à l'instant $t$ en fonction de son volume $V, I_{r}$ et $c$

Q33. À l'aide d'un bilan d'énergie, montrer que l'intensité réverbérée $I_{r}(t)$ obéit à l'équation différentielle du premier ordre : $\frac{\mathrm{d} I_{r}}{\mathrm{~d} t}+\frac{\alpha_{m} S c}{4 V} I_{r}=0$.
Donner la loi d'évolution $I_{r}(t)$. On introduira un temps caractéristique $\tau$ et on notera $I_{r}(t=0)=I_{r, 0}$.

On définit le temps de réverbération $T_{r}$ comme la durée nécessaire pour que le niveau d'intensité sonore $L_{I}$ dans la pièce décroisse de 60 dB par rapport à son niveau initial, soit: $\Delta L_{I}=L_{I}\left(t=T_{r}\right)-L_{I}(t=0)=-60 \mathrm{~dB}$. On rappelle que le niveau d'intensité sonore est défini par: $L_{I}=10 \log \frac{I}{I_{0}}$ où $I_{0}=10^{-12} \mathrm{~W} \cdot \mathrm{~m}^{-2}$ est l'intensité sonore au seuil d'audibilité à 1000 Hz .

Q34. Exprimer le temps de réverbération $T_{r}$ en fonction de $\tau$. Vérifier qu'on retrouve la formule semi-numérique de Sabine : $T_{r}=0,16 \frac{V}{\alpha_{m} S}$, où le rapport $V / S$ est exprimé en m et $T_{r}$ en s. On prendra $c=3,4 \cdot 10^{2} \mathrm{~m} \cdot \mathrm{~s}^{-1}$ (air à la température $T_{0}=293 \mathrm{~K}$ à l'équilibre).

On considère une salle vide, de longueur $L=25 \mathrm{~m}$, de largeur $\ell=20 \mathrm{~m}$, de hauteur $h=10 \mathrm{~m}$, destinée à un concert de musique symphonique. Une mesure au sonomètre indique un temps de réverbération $T_{r}$ à 1000 Hz de $5,0 \mathrm{~s}$, plus élevé que le temps de réverbération optimal $T_{r, o p}$ (figure 7).

![](https://cdn.mathpix.com/cropped/4bc0bb47-e03f-4b68-b88f-13e567a25830-12.jpg?height=711&width=1374&top_left_y=1706&top_left_x=342)
Figure 7 - Temps de réverbération optimal à 1000 Hz en fonction du volume de la pièce

1. Orgue, audition directe. 2. Musique symphonique, audition directe. 3. Orgue, enregistrement. 4. Opéra, audition directe. 5. Jazz, audition directe. 6. Parole, audition directe. 7. Parole, enregistrement. 8. Variétés, enregistrement.

Source : L. Lamoral. Acoustique et architecture

Q35. Sachant que le coefficient d'absorption moyen $\alpha_{m, p}$ du public est égal à 0,90 , justifier si la présence d'un public permet oui ou non une qualité d'écoute du concert satisfaisante.

Cette question fait appel à une démarche de résolution de problème. Il est notamment attendu de préciser chaque notation introduite, de présenter de façon claire les hypothèses retenues, de mener des calculs littéraux avant toute application numérique.

## III. 2 - Principe d'un silencieux à résonateur de Helmholtz

Si un traitement acoustique de la pièce ne peut être envisagé, d'autres solutions sont possibles pour réduire l'impact du bruit généré par un système de renouvellement d'air. L'une d'elles consiste à insérer des silencieux le long des réseaux de gaines, munis entre autres de résonateurs de Helmholtz. On modélise un résonateur de Helmholtz par une cavité de grand volume $V_{c}$, reliée à l'air libre par l'intermédiaire d'un col cylindrique horizontal d'axe ( $O, \vec{u}_{x}$ ), de très faible section $s$ et de longueur $\ell$ (figure 8). Sous l'effet d'une perturbation, on considère que l'air situé dans le col oscille en bloc, à l'image d'un bouchon qui coulisserait. On note $x(t)$ le déplacement du centre d'inertie de cette tranche d'air à l'instant $t$ par rapport à sa position à l'équilibre, $p_{c}(t)$ la pression supposée uniforme dans la cavité, $\rho_{0}$ la masse volumique de l'air dans le col, supposée égale à tout instant à celle de l'air libre à la pression atmosphérique $p_{0}$. On néglige tout phénomène dissipatif et on considère que l'air dans la cavité, de comportement supposé parfait, évolue de façon isentropique.

![](https://cdn.mathpix.com/cropped/4bc0bb47-e03f-4b68-b88f-13e567a25830-13.jpg?height=266&width=835&top_left_y=1363&top_left_x=621)
Figure 8 - Modélisation d'un résonateur de Helmholtz. La zone grisée représente la tranche d'air qui oscille

Q36. Exprimer la résultante $\vec{F}_{p}$ des forces pressantes sur la tranche d'air en fonction de $p_{0}$, $p_{c}(t)$ et $s$.
En supposant que le volume de la tranche d'air est très petit devant le volume de la cavité, soit $\ell s \ll V_{c}$, montrer que $p_{c}(t) \simeq p_{0}\left(1+\frac{\gamma s x}{V_{c}}\right)$ au premier ordre, où $\gamma$ est le rapport entre les capacités thermiques à pression et volume constants de l'air.
En déduire que la résultante des forces pressantes sur la tranche d'air est équivalente à une force de rappel élastique de raideur $k: \vec{F}_{p}=-k x \vec{u}_{x}$. Exprimer $k$ en fonction de $V_{c}, s, \rho_{0}$ et de la célérité $c$ des ondes sonores dans l'air. On utilisera l'expression de $c$ établie à la Q28.

Q37. Montrer que la tranche d'air dans le col oscille de façon harmonique. Vérifier que la fréquence propre $f_{0}$ de ce système oscillant s'écrit : $f_{0}=\frac{1}{2 \pi} \sqrt{\frac{c^{2} s}{\ell V_{c}}}$.

Un résonateur expérimental est constitué d'un cylindre en PVC de volume $V_{c}=791 \mathrm{~cm}^{3}$, fermé à ses deux extrémités. L'une de ces extrémités est percée de façon à insérer un col cylindrique de section $s=1,89 \mathrm{~cm}^{2}$ et de longueur $\ell=5,0 \mathrm{~cm}$. Un microphone de petite taille, relié à un oscilloscope à mémoire, est inséré dans le grand volume. En engageant légèrement l'index dans le col et en le retirant brusquement, on enregistre le signal suivant (figure 9). Les conditions de l'expérience sont telles que $c=343 \mathrm{~m} \cdot \mathrm{~s}^{-1}$.

![](https://cdn.mathpix.com/cropped/4bc0bb47-e03f-4b68-b88f-13e567a25830-14.jpg?height=671&width=1171&top_left_y=568&top_left_x=429)
Figure 9 - Oscillations libres d'un résonateur de Helmholtz

Source : Bulletin de I'Union des Physiciens, volume 96, Juin 2002
Q38. Quelle serait la nature du signal attendu dans le cadre du modèle considéré dans les questions précédentes ? Comment expliquer la différence avec le signal enregistré ? Estimer le facteur de qualité $Q$ du résonateur.

Q39. Le facteur de qualité est suffisamment grand pour considérer que le système oscille à sa fréquence propre $f_{0}$. Comparer la valeur mesurée de cette fréquence à celle déduite du modèle utilisé.
En fait, les couches d'air situées de part et d'autre du col sont aussi entraînées dans le mouvement. Expliquer en quoi leur prise en compte permet d'affiner la modélisation.

Un haut-parleur, relié à un générateur basse fréquence, impose désormais à l'entrée du col une surpression variant de façon sinusoïdale à la pulsation $\omega$, de la forme $p(t)=p_{m} \cos (\omega t)$. La pression à l'entrée du col est donc égale à $p_{0}+p(t)$. On associe à cette pression acoustique la grandeur complexe $\underline{p}(t)=p_{m} \mathrm{e}^{\mathrm{j} \omega t}$ où $\mathrm{j}^{2}=-1$. On cherche une réponse de la tranche d'air de la forme $\underline{x}(t)=\underline{x}_{m} \mathrm{e}^{\mathrm{j} \omega t}$ en régime forcé en restant dans le cadre du modèle développé dans Q36 et Q37.

Q40. Établir l'expression de $\underline{x}(t)$. En déduire que la vitesse de la tranche d'air dans le col s'écrit en représentation complexe : $\underline{v}(t)=\underline{v}_{m} \mathrm{e}^{\mathrm{j} \omega t}$ où $\underline{v}_{m}=\frac{\mathrm{j} \omega p_{m}}{\rho_{0} \ell\left(\omega_{0}^{2}-\omega^{2}\right)}$.
Que dire de $\left|\underline{v}_{m}\right|$ dans le cas où $\omega=\omega_{0}$ ? En pratique, $\left|\underline{v}_{m}\right|$ reste borné. Expliquer pourquoi.

Un résonateur de Helmholtz est maintenant connecté en $z=0$ à une longue conduite cylindrique d'axe ( $O, \vec{u}_{z}$ ) et de section $S \gg S$ (figure 10). La masse volumique de l'air au repos dans la conduite est $\rho_{0}$.
Une onde acoustique incidente plane progressive sinusoïdale, de pulsation $\omega$, se propage dans la conduite dans le sens des $z$ croissants à la célérité $c$. Elle est caractérisée par sa pression acoustique $\underline{p}_{i}(z, t)=\underline{p}_{i, m} \mathrm{e}^{\mathrm{j}(\omega t-k z)}$. Du fait de la présence du résonateur en $z=0$, elle donne naissance à une onde réfléchie et une onde transmise, caractérisées par leurs pressions acoustiques respectives $\underline{p}_{r}(x, t)=\underline{p}_{r, m} \mathrm{e}^{\mathrm{j}(\omega t+k z)}$ et $\underline{p}_{t}(x, t) \underline{p}_{t, m} \mathrm{e}^{\mathrm{j}(\omega t-k z)}$.

![](https://cdn.mathpix.com/cropped/4bc0bb47-e03f-4b68-b88f-13e567a25830-15.jpg?height=722&width=1415&top_left_y=699&top_left_x=335)
Figure 10 - Résonateur de Helmholtz connecté à une conduite

Q41. Exprimer les champs des vitesses caractérisant les ondes acoustiques incidente, réfléchie et transmise, notées respectivement $\underline{v}_{i}(z, t), \underline{v}_{r}(z, t)$ et $\underline{v}_{t}(z, t)$, en fonction notamment de l'impédance caractéristique $Z_{c}$ de la conduite définie à la $\mathbf{Q 2 9}$.

Q42. On note $\underline{p}(t)=p_{m} \mathrm{e}^{\mathrm{j} \omega t}$ la pression acoustique et $\underline{v}(t)=\underline{v}_{m} \mathrm{e}^{\mathrm{j} \omega t}$ le champ des vitesses correspondant en $z=0$ à l'entrée du col du résonateur.
Exprimer $p_{m}$ en fonction de $\underline{p}_{i, m}$ et $\underline{p}_{r, m}$, puis en fonction de $\underline{p}_{t, m}$.
En supposant la conservation du débit volumique à travers la surface qui délimite la portion de la conduite en contact avec le résonateur en $z=0$ (figure 10), établir une relation entre $\underline{p}_{i, m}, \underline{p}_{r, m}, \underline{p}_{t, m}, \underline{v}_{m}, S, S$ et $Z_{c}$.

Un calcul non demandé permet de déduire de l'ensemble des résultats établis précédemment que :

$$
\underline{p}_{t, m}=\frac{\underline{p}_{i, m}}{1-\frac{\mathrm{j}}{2 \beta\left(\frac{\omega}{\omega_{0}}-\frac{\omega_{0}}{\omega}\right)}} \text { avec } \beta=\frac{\ell S \omega_{0}}{s c}
$$

Q43. Exprimer en fonction de $\omega, \omega_{0}$ et $\beta$ l'indice de perte de transmission $L_{T L}$ défini par

$$
L_{T L}=10 \log \left(\frac{\left|\underline{p}_{i, m}\right|^{2}}{\left|\underline{p}_{t, m}\right|^{2}}\right) \text { et exprimé en décibels. }
$$

Il y a en fait toujours des phénomènes dissipatifs dus à la viscosité dans le col, phénomènes pouvant être renforcés par l'adjonction dans le col de matériaux poreux. Dans ces conditions, l'indice de perte de transmission est également fonction d'un coefficient d'amortissement adimensionné $\alpha$ (figure 11).

![](https://cdn.mathpix.com/cropped/4bc0bb47-e03f-4b68-b88f-13e567a25830-16.jpg?height=693&width=1643&top_left_y=703&top_left_x=212)
Figure 11 - Indice de perte de transmission autour de la fréquence de résonance $f_{0}$ pour différentes valeurs des coefficients $\alpha$ et $\beta$

## Source : T.F.W. Embleton. Mufflers, in Noise and Vibration Control.

Q44. Identifier à l'aide des courbes de la figure 11 la nature du filtre acoustique que constitue le résonateur de Helmholtz relié à la conduite.
Pour une valeur du coefficient $\beta$ donnée, expliquer à l'aide des courbes l'intérêt d'avoir un coefficient d'amortissement $\alpha$ important.

## FIN

