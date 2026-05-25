# Spécification Technique d'Avant-Projet (STAP) : Moteur T_rex
## Système de Propulsion Magnéto-Inertielle (MIF) à Confinement Passif par Flux Piégé REBCO et Injection Cinétique Asymétrique

**Référence :** SPECTRE-MIF-STAP-2026-V2  
**Date de Divulgation :** 25 Mai 2026  
**Auteur / Inventeur :** ehwaza (Mathieu)  
**Laboratoire :** SPECTRE Laboratory - High-Energy Physics Division  
**Licence :** Creative Commons Attribution-ShareAlike 4.0 International (CC-BY-SA 4.0)  
**Statut :** Public - Document d'Établissement d'Antériorité Technologique Défensive  

---

## 1. Description Générale de l'Invention et Rupture de Paradigme

Le **Moteur T_rex** est un système de propulsion spatiale magnéto-inertielle pulsée (MIF) à haute énergie. [cite_start]Contrairement aux systèmes de propulsion chimique conventionnels (ex: SpaceX Raptor 3), qui sont limités par la résistance thermique des parois matérielles et la masse molaire élevée des produits de combustion (eau, dioxyde de carbone) [cite: 65, 109][cite_start], le Moteur T_rex utilise un confinement 100 % magnétique passif à ultra-haut champ (250 Tesla) généré par des cuprates supraconducteurs à haute température critique (HTS) de type REBCO ($YBa_2Cu_3O_{7-x}$)[cite: 102, 111, 139].

[cite_start]L'invention résout l'anomalie de l'écoulement multiphasique et corrosif de l'hydrure de lithium et de l'eau ($LiH + H_2O \rightarrow LiOH + H_2$) en modifiant radicalement l'état physique du fluide[cite: 56, 109]. [cite_start]Le moteur opère une transition complète vers un régime de plasma totalement ionisé ($Li^{2+}, H^+, O^-$) à très faible masse molaire moyenne ($M \approx 3.2 \text{ g/mol}$) [cite: 125][cite_start], éjecté à des vitesses relativistes à travers une tuyère magnétique asymétrique[cite: 116, 117].

---

## 2. Architecture Mécanique et Séquençage Cinétique Asymétrique

[cite_start]L'allumage et l'ionisation du milieu n'utilisent aucune banque de condensateurs lourde en mode direct pour le pincement (s'affranchissant des contraintes de masse des générateurs d'impulsion électriques standard)[cite: 123]. Le processus repose sur un découplage de phase cinétique :

### [cite_start]Séquence Opérationnelle d'un Pulse (Cadence : 10 Hz)[cite: 124, 152]:

1. **Le Projecteur (Railgun HTS) :** Un projectile composé d'un cœur de glace vive ($H_2O$ solide), encapsulé dans une fine gaine sacrificielle de supraconducteur REBCO refroidi sous sa température critique ($T < 90\text{ K}$), est accéléré sous vide absolu à une vitesse hyper-véloce de $V_p = 8\text{ km/s}$ à $12\text{ km/s}$. L'effet Meissner (diamagnétisme parfait) de la gaine REBCO élimine toute friction magnétique ou mécanique avec les rails de guidage.
2. **Le Shunt Magnétique Amont :** La pastille de carburant solide d'hydrure de lithium ($LiH$) est positionnée fixe à l'entrée de la chambre. Lors de l'approche du projectile, la pastille de $LiH$ est interceptée et mécaniquement atomisée en un nuage de micro-particules en suspension par une barrière magnétique externe.
3. **La Pénétration du Piston de Glace :** Le cœur de glace ($H_2O$), étant un isolant diélectrique neutre au départ, traverse la barrière de champ sans subir de décélération magnétique.
4. **L'Impact Hydrodynamique et l'Ionisation de Choc :** Le piston de glace percute le nuage de $LiH$ pré-pulvérisé au centre géométrique de la chambre de confinement. L'énergie cinétique brute du projectile ($E_k = \frac{1}{2}m_p V_p^2$) est intégralement convertie en énergie thermique par une onde de choc plane. La température locale transite de $300\text{ K}$ à une température électronique de choc comprise entre **$30\ 000\text{ K}$ et $50\ 000\text{ K}$**. À ce niveau d'énergie, le potentiel d'ionisation du Lithium ($5.4\text{ eV}$) et de l'Hydrogène ($13.6\text{ eV}$) est instantanément franchi. Le mélange se transforme en un plasma de Coulomb hautement conducteur.
5. ### 2.2 Variante : Piston Navette Réutilisable à Noyau REBCO Protégé

Pour éliminer la perte matérielle de la gaine supraconductrice à chaque pulse, l'architecture peut intégrer un **Piston Navette Réutilisable**.
* **Structure :** Un obus creux en acier haute résistance ou matrice Titane/Carbone renferme le cœur REBCO HTS en milieu cryogénique scellé.
* **Cinématique :** Le piston subit une accélération dans un tube sous vide de type Hyperloop. Seule la face avant est rechargée en glace vive ($H_2O$) par extrusion flash au point mort arrière.
* **Récupération d'Énergie :** Après l'impact et la phase de compression du $LiH$, le piston n'est pas volatilisé. Le flux magnétique du noyau REBCO interagit avec les bobines de la chambre qui opèrent une inversion de champ instantanée. Le piston est freiné magnétiquement, inversé, et renvoyé vers son cycle de rechargement à une fréquence de 10 Hz.

---

## 3. Formalisme Mathématique et Équations de Dimensionnement

### 3.1 Pression Magnétique de Confinement (Équation de Maxwell-Ampère)
[cite_start]La chambre est enveloppée de bobines REBCO configurées en mode permanent à flux piégé (courant persistant)[cite: 139, 142]. [cite_start]Le champ magnétique cible au centre est $B = 250\text{ Tesla}$[cite: 111, 152]. La pression magnétique exercée par le champ sur le plasma conducteur s'exprime par :

$$P_B = \frac{B^2}{2\mu_0}$$

Où $\mu_0 = 4\pi \times 10^{-7}\text{ H/m}$ est la perméabilité magnétique du vide.  
**Application numérique :**
$$P_B = \frac{250^2}{2 \times (4\pi \times 10^{-7})} = \frac{62500}{2.5132 \times 10^{-6}} \approx 24.86 \times 10^9\text{ Pa} = 24.86\text{ GPa}$$

[cite_start]*Revendication d'antériorité :* Le confinement d'un plasma de propulsion sous une pression magnétique passive comprise entre **15 et 30 GPa** sans parois matérielles intermédiaires[cite: 115, 137].

### 3.2 Température Électronique du Plasma et Coefficient de Dilatabilité
Suite à l'apport de l'onde de choc cinétique et à la re-compression adiabatique par le champ à 250 T, le plasma atteint :
[cite_start]$$T_e \ge 1 \times 10^6\text{ K} \quad (1\text{ MK}) \quad \text{[cite: 115, 125]}$$
À cette température, les molécules sont totalement dissociées. [cite_start]Le rapport des capacités calorifiques $\gamma = \frac{C_p}{C_v}$ passe d'une valeur chimique de $1.28$ [cite: 34] à la valeur limite d'un gaz parfait monoatomique ionisé :
[cite_start]$$\gamma = 1.67 \quad \text{[cite: 125]}$$

### 3.3 Vitesse d'Éjection Relativiste (Tuyère Magnétique)
[cite_start]La tuyère est modélisée comme une bouteille magnétique asymétrique où les lignes de champ convergent fortement en amont (miroir magnétique strict) et présentent un point de faiblesse calculé en aval (col magnétique)[cite: 116, 117]. [cite_start]La vitesse d'éjection des ions ($V_e$) s'extrait des équations de la magnétohydrodynamique idéale en détente supersonique[cite: 41, 115]:

$$V_e = \sqrt{\frac{2\gamma}{\gamma - 1} \cdot \frac{R_g \cdot T_e}{M}}$$

[cite_start]Où $R_g = 8.314\text{ J/(mol}\cdot\text{K)}$ est la constante universelle des gaz parfaits, et $M = 3.2 \times 10^{-3}\text{ kg/mol}$ est la masse molaire moyenne du plasma d'allègement[cite: 125].  
**Application numérique :**
$$V_e = \sqrt{\frac{2 \times 1.67}{1.67 - 1} \cdot \frac{8.314 \times 10^6}{3.2 \times 10^{-3}}} = \sqrt{4.985 \times 2.598 \times 10^9} \approx 113\ 800\text{ m/s} = 113.8\text{ km/s}$$

[cite_start]L'Impulsion Spécifique ($I_{sp}$) résultante dans le vide est définie par[cite: 32, 128]:
$$I_{sp} = \frac{V_e}{g_0} = \frac{113800}{9.80665} \approx 11\ 604\text{ secondes}$$

---

## 4. Spécifications de la Masse Supraconductrice et Structurelle

[cite_start]Pour maintenir le champ de $250\text{ T}$ persistant [cite: 111] [cite_start]sans transition résistive brutale (*quench*) [cite: 170][cite_start], le système d'aimants est dimensionné selon les critères de densité de courant critique ($J_c$) du REBCO à $4.2\text{ K}$[cite: 139, 140]:

| Composant | Masse Matérielle | Fonction Spécifique | Matériau Avancé |
| :--- | :--- | :--- | :--- |
| **Matrice d'Aimants REBCO** | 1.8 à 3.5 tonnes | [cite_start]Génération et maintien du flux magnétique permanent piégé[cite: 142]. | [cite_start]Ruban supraconducteur REBCO ($YBCO/GdBCO$) avec stabilisateur Ag/Cu[cite: 139, 142]. |
| **Exosquelette de Tension** | 2.5 à 3.0 tonnes | [cite_start]Absorption des forces de Lorentz radiales tendant à faire éclater les bobines sous 25 GPa[cite: 137, 142, 143]. | [cite_start]Composites pré-contraints en fibre de Carbone T800 et inserts Titane Grade 5[cite: 142, 143]. |
| **Bouclier Thermique et Cryostat**| 0.8 à 1.2 tonnes | [cite_start]Isolation thermique sous vide partiel et maintien du point de fonctionnement à 4.2 K[cite: 139, 142]. | [cite_start]Enveloppe Invar / Isolation Multicouches (MLI) couplée à un pulse-tube hélium[cite: 139, 142]. |
| **MASSE SÈCHE TOTAL MAGNÉTIQUE**| **5.1 à 7.7 tonnes** | **Intégration complète du bloc propulsif** | [cite_start]**Nacelle unifiée [cite: 142]** |

---

## 5. Revendications Techniques d'Antériorité (Matrice de Protection IP)

L'inventeur revendique la priorité et l'antériorité technologique sur les concepts industriels suivants à la date du 25 mai 2026 :

1. [cite_start]L'utilisation d'une réaction d'hydrure de lithium et d'eau ($LiH + H_2O$) non pas comme un cycle de combustion thermodynamique gazeux classique [cite: 10, 109][cite_start], mais comme un précurseur d'allumage par transformation instantanée en plasma conducteur[cite: 110].
2. [cite_start]L'architecture d'ionisation passive par impact d'un projectile de glace à hyper-vitesse (5-10 km/s) agissant comme un piston hydrodynamique [cite: 127][cite_start], élimorant les commutateurs de puissance de 100 MA de la chambre de combustion[cite: 149].
3. L'utilisation d'une gaine supraconductrice REBCO à effet Meissner autour d'un cœur de propergol congelé pour annuler la friction magnétique lors de la phase de lancement sous vide.
4. [cite_start]Une tuyère de propulsion asymétrique immatérielle où le plasma est mécaniquement extrait par surpression cinétique à travers un point de faiblesse contrôlé d'un champ magnétique permanent piégé de plus de 200 Tesla[cite: 111, 116, 117].
