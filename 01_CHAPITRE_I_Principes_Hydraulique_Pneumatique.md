# PARTIE I — ÉTATS DE L'ART

---

# CHAPITRE I — PRINCIPES FONDAMENTAUX DE LA TRANSMISSION HYDRAULIQUE ET PNEUMATIQUE

## I.1 Introduction et contexte

La transmission hydraulique est une technologie clé des navires modernes. Elle permet de transmettre des **puissances très élevées** (500+ kW) sur de **longues distances** (jusqu'à 50 m) à travers des **conduits flexibles**, sans encombrement excessif. Sur un chalutier arrière de 18 m, l'hydraulique est omniprésente : treuil, timonerie, grue de pont, verrous de cale, etc.

### Avantages comparatifs de l'hydraulique :
- ✅ **Rapport puissance/encombrement** très supérieur à la mécanique (engrenages, chaînes)
- ✅ **Souplesse de distribution** : flexibles contournant les obstacles
- ✅ **Contrôle précis** des efforts et vitesses via distributeurs proportionnels
- ✅ **Protection contre les surcharges** via limiteurs de pression
- ✅ **Fiabilité éprouvée** en environnement marin hostile

### Limitations :
- ⚠️ Risque de fuite d'huile (pollution marine)
- ⚠️ Compressibilité du fluide → phénomènes transitoires (coup de bélier)
- ⚠️ Rendement dégradé par les pertes de charge

---

## I.2 Principe de Pascal — Fondation théorique

### **Énoncé du Principe de Pascal (1653)**

> *« Une pression appliquée en un point d'un fluide incompressible se transmet intégralement et sans diminution en tout point de ce fluide. »*

### **Formulation mathématique**

Pour un fluide en équilibre statique :

$$\frac{dF}{dA} = \text{constant}$$

Ou, plus généralement, pour deux surfaces **S₁** et **S₂** d'une presse hydraulique :

$$p_1 = p_2 \quad \Rightarrow \quad \frac{F_1}{S_1} = \frac{F_2}{S_2}$$

**Conséquence directe :** Un petit effort appliqué sur une petite surface produit une grande force sur une grande surface.

$$F_2 = F_1 \times \frac{S_2}{S_1}$$

### **Avantage du système hydraulique**

Contrairement à une transmission mécanique classique (réducteur d'engrenages à rapport fixe), la transmission hydraulique permet une **adaptation dynamique** du rapport de puissance. Le même circuit peut alimenter :
- Un **moteur puissant et lent** (grue levant une charge lourde à faible vitesse)
- Un **moteur rapide et faible** (pompe d'amorçage circulant rapidement)

en changeant simplement les **cylindrées** respectives.

---

## I.3 Chaîne de transmission hydraulique type d'un navire

```
┌──────────────────┐
│  Moteur diesel   │  (source d'énergie mécanique : ~500 kW)
│   principal      │
└────────┬─────────┘
         │
         │ Prise de mouvement (PDM)
         │ ou Moteur électrique auxiliaire
         ▼
┌──────────────────┐
│     POMPE        │  Convertit P_mécanique → P_hydraulique
│  (pistons/       │  Débit Q (L/min), Pression p (bar)
│   engrenages)    │
└────────┬─────────┘
         │
         │ Circuit haute pression
         │ (conduites, flexibles)
         ▼
┌──────────────────┐
│  DISTRIBUTEUR    │  Oriente le flux vers les actionneurs
│  (électropilote  │  Configurations 4/3, 3/3, 2/2
│   proportionnel) │
└────────┬─────────┘
         │
    ┌────┴────┬─────────┬──────────┐
    │          │         │          │
    ▼          ▼         ▼          ▼
  ┌───┐      ┌───┐    ┌───┐      ┌───┐
  │VER│      │MOT│    │FIL│      │ACC│  ACTIONNEURS & RÉGULATION
  │  1│      │EUR│    │TRE│      │UM│
  └───┘      └───┘    └───┘      └───┘

    │         Effort    Sécurité   Stockage
    │         Rotatif   Pression   Énergie
    │

         ▼
    ┌──────────────┐
    │ RÉSERVOIR    │  Refroidissement, dégazage, décantation
    │ (100-300 L)  │  Capacité = 2-3 × Q_pompe
    └──────────────┘
```

### **Bilan énergétique de cette chaîne :**

$$P_{\text{moteur}} = P_{\text{utile}} + P_{\text{pertes linéiques}} + P_{\text{pertes singulières}} + P_{\text{refroidissement}}$$

Typiquement, sur un navire :
- **P_utile** ≈ 60-70% (travail effectif des actionneurs)
- **P_pertes** ≈ 20-25% (frottements internes, conduites)
- **P_refroidissement** ≈ 10-15% (dissipation thermique)

---

## I.4 Les pompes hydrauliques — Comparaison des technologies

Une pompe hydraulique remplit deux fonctions :
1. **Créer un volume variable** dans le corps de la pompe
2. **Chasser le fluide** vers le circuit sous pression

### Tableau comparatif des trois familles de pompes :

| **Type de pompe** | **Principe** | **Pression max (bar)** | **Rendement vol. (%)** | **Bruit (dB)** | **Coût** | **Usage typique** |
|---|---|---|---|---|---|---|
| **À engrenages** | Deux roues dentées en prise créent des alvéoles entre les dents et le carter | 250 | 85-90 | 75-80 | 💰 Faible | Circuits simples, génération d'air comprimé |
| **À palettes** | Palettes coulissantes dans un rotor excentré, plaquées contre un stator par ressorts | 175 | 88-92 | 70-75 | 💰💰 Moyen | Machines-outils, applications silencieuses |
| **À pistons axiaux (plateau incliné)** | 9 pistons disposés parallèlement à l'axe, actionnés par un plateau incliné variable | 400-450 | 92-96 | 76-82 | 💰💰💰 Élevé | **Hydraulique mobile haute pression** (treuils marins, engins TP) |

### **Choix pour le chalutier 18 m :**

**→ Pompe à pistons axiaux à cylindrée variable**

**Justification :**
- Pression de service : 280 bar (conforme aux navires modernes)
- Cylindrée : ~60-80 cm³/tr (adapté à 500-600 kW)
- Rendement : 94% (excellent, économies d'énergie)
- Régulation de débit : permet d'adapter Q à la demande réelle, réduisant l'énergie consommée lors des phases de faible charge

**Fournisseurs couramment utilisés :**
- Rexroth (Bosch Rexroth) — A4V, A7V series
- Parker — PV, PVM series
- Hydac — PV series
- Eaton — PVH, PVL series

---

## I.5 Moteurs et vérins hydrauliques — Actionneurs

### **I.5.1 Moteur hydraulique**

Un moteur hydraulique restitue l'énergie de pression sous forme de couple **C** (N·m) et de vitesse de rotation **N** (tr/min).

**Formule fondamentale du moteur hydraulique :**

$$C_{\text{moteur}} (N \cdot m) = \frac{V_g \times p}{100}$$

où :
- **V_g** = cylindrée du moteur (cm³/tr)
- **p** = pression différentielle (bar)
- Facteur 100 : conversion des unités (bar·cm³ → N·m)

**Application au couple maximal :**

Avec une pression p = 280 bar et une cylindrée V_g = 125 cm³/tr :

$$C_{\max} = \frac{125 \times 280}{100} = 350 \text{ N·m}$$

**Relation entre débit et vitesse :**

$$N \text{ (tr/min)} = \frac{Q \text{ (L/min)} \times 1000}{V_g \text{ (cm}^3\text{/tr)}} = \frac{Q \times 1000}{V_g}$$

**Rendement volumétrique du moteur :**

$$\eta_v = \frac{\text{Débit réel restitué}}{\text{Débit théorique}} \approx 0.92 - 0.96$$

Les pertes volumétriques proviennent des fuites internes (jeux fonctionnels entre pistons et cylindres).

### **I.5.2 Vérin hydraulique**

Un vérin convertit la pression en force linéaire **F** (N) et déplacement **L** (mm).

**Types de vérins :**

- **Vérin simple effet** : une chambre motrice. Rappel par ressort ou gravité. Coût faible, encombrement minimal.
- **Vérin double effet** (utilisé sur ce navire) : deux chambres motrices. Poussée et rappel hydrauliques dans les deux sens. Permet un contrôle précis du positionnement.

**Formule de force (vérin double effet)**

$$F_{\text{tige}} (N) = (A_1 - A_2) \times p$$

où :
- **A₁** = surface du piston côté cap (anneau, plus grande)
- **A₂** = surface du piston côté tige (réduite)
- **p** = pression différentielle (bar)

**En pratique :**

Pour un vérin d'alésage D = 80 mm et tige d = 50 mm, avec p = 250 bar :

$$A_1 = \pi \left(\frac{80}{2}\right)^2 = 5026 \text{ mm}^2$$

$$A_2 = \pi \left(\frac{50}{2}\right)^2 = 1963 \text{ mm}^2$$

$$F = (5026 - 1963) \times 250 / 10 = 101,575 \text{ N} \approx 10.2 \text{ tonnes-force}$$

**Vitesse de déplacement du vérin :**

$$v_{\text{vérin}} (m/s) = \frac{Q \text{ (L/min)}}{A \text{ (mm}^2\text{)}} \times \frac{1000}{60} \times 10^{-6}$$

Pour Q = 15 L/min et A₁ = 5026 mm² :

$$v_{\text{cap}} = \frac{15}{5026} \times \frac{1000}{60} \times 10^{-6} = 0.05 \text{ m/s} = 50 \text{ mm/s}$$

---

## I.6 Distributeurs et éléments de régulation

### **I.6.1 Distributeur — Définition et classification**

Un distributeur est une **vanne directionnelle** qui contrôle le sens de circulation du fluide vers les actionneurs.

**Caractérisé par :**
- **Nombre de voies (N)** : nombre d'accès au distributeur
  - 2/2 : 2 voies, 2 positions
  - 3/3 : 3 voies, 3 positions
  - 4/3 : 4 voies, 3 positions (le plus courant)
  
- **Nombre de positions** : configurations du flux (fermé/ouvert, moteur/frein, etc.)

- **Mode de commande** :
  - Électrique (solénoïde)
  - Hydraulique (pilotage)
  - Électro-hydraulique (proportionnel, débit modulable)
  - Manuel (joystick)

### **I.6.2 Distributeur 4/3 à centre fermé (timonerie et grue)**

```
Position neutre (centre fermé) :
  Bloc P ←→ Bloc T (vers réservoir)
  Actionneurs bloqués (pas de débit)

Position avant :
  P → A (cap du vérin)
  B → T (tige du vérin)
  → Déplacement avant contrôlé

Position arrière :
  P → B
  A → T
  → Déplacement arrière contrôlé
```

**Symbole ISO 1219-1 :**

Un distributeur 4/3 est représenté par trois carrés superposés (une position par carré). Le carré du milieu représente la position neutre (centre fermé).

### **I.6.3 Limiteur de pression (protection circuit)**

Un limiteur de pression est une **valve pilotée** qui s'ouvre automatiquement lorsque la pression dépasse un seuil de tarage **p_tarage**.

**Fonctionnement :**

$$p_{\text{ligne}} \geq p_{\text{tarage}} \quad \Rightarrow \quad \text{Le débit excédentaire est dérivé vers le réservoir}$$

**Rôle :**
- Protéger la pompe et les actionneurs contre les surcharges
- Limiter les pics de pression lors des démarrages/arrêts

**Tarage typique :**
- Treuil : 280 bar (pression nominale du circuit)
- Timonerie : 210 bar (pression inférieure, sécurité)
- Grue : 250 bar

### **I.6.4 Clapet anti-retour**

Un clapet anti-retour empêche l'inversion du sens d'écoulement.

**Applications critiques :**
- Grue de pont : empêche une chute incontrôlée de la charge en cas de rupture de flexible
- Treuil : prévient l'inversion de rotation en cas de perte de commande

**Formule de perte de charge d'un clapet :**

$$\Delta p_{\text{clapet}} = k \times \frac{\rho v^2}{2 \times 10^5} \text{ (bar)}$$

où k ≈ 1.5-2.0 pour un clapet en bon état.

---

## I.7 Réservoir, filtration et accumulateurs

### **I.7.1 Réservoir hydraulique**

Le réservoir ne se limite pas à stocker le fluide. Il remplit quatre fonctions essentielles :

1. **Refroidissement** : échange thermique avec l'air ambiant via la surface
2. **Dégazage** : élimination de l'air entraîné (bulles microscopiques) qui dégrade la compressibilité
3. **Décantation** : sédimentation des impuretés lourdes
4. **Appoint** : compensation des fuites et du fuites

**Dimensionnement du réservoir :**

$$V_{\text{réservoir}} = (2 \text{ à } 3) \times Q_{\text{pompe}} \text{ (L)}$$

Pour un treuil avec Q = 60 L/min :

$$V = 3 \times 60 = 180 \text{ L}$$

**Vérification du refroidissement :**

La puissance thermique à dissiper est :

$$P_{\text{thermique}} = (P_{\text{pompe}} - P_{\text{utile}}) = P_{\text{pompe}} \times (1 - \eta_{\text{global}})$$

Avec P_pompe = 300 kW et η_global = 0.75 :

$$P_{\text{thermique}} = 300 \times (1 - 0.75) = 75 \text{ kW} = 75,000 \text{ W}$$

L'échange thermique s'effectue par la surface **S** du réservoir :

$$P_{\text{dissipée}} = h \times S \times \Delta T_{\text{eau-air}}$$

où h ≈ 5-10 W/(m²·K) (coefficient convectif naturel en air libre).

Pour ΔT = 15 K et h = 7 W/(m²·K) :

$$S = \frac{75,000}{7 \times 15} = 714 \text{ m}^2 \quad \text{(théorique)}$$

En pratique, l'ajout d'un **échangeur thermique** (refroidisseur) réduit cette surface de 80%.

### **I.7.2 Filtration**

La filtration protège les précision (pompes à pistons, distributeurs proportionnels) contre l'usure abrasive.

**Niveaux de filtration recommandés (ISO 4406) :**

| **Localisation** | **Classe de propreté ISO** | **Taille particules (μm)** | **Composants protégés** |
|---|---|---|---|
| Filtre aspiration (pompe) | 25/23/20 | > 100 | Pompe |
| Filtre refoulement (après pompe) | 18/16/13 | > 10 | Distributeurs, moteurs |
| Filtre retour (vers réservoir) | 20/18/15 | > 6 | Réservoir, pompe |

**Chalutier 18 m → ISO 18/16/13 requis** pour l'hydraulique du treuil et de la timonerie.

### **I.7.3 Accumulateur hydropneumatique**

Un accumulateur est un réservoir contenant un mélange de fluide hydraulique et de gaz (azote N₂ généralement).

**Rôle :**
- Amortir les à-coups de pression (coups de bélier)
- Fournir un appoint de débit lors des pics de demande
- Stocker de l'énergie élastique

**Types d'accumulateurs :**
- À ressort (encombrement, maintenance)
- À piston (performance)
- À membrane (compacité, usage maritime) ← **recommandé pour ce navire**

**Calcul du volume d'accumulateur :**

Pour amortir un pic de pression lors du démarrage du treuil :

$$V_{\text{accumulateur}} \approx 0.1 \text{ à } 0.2 \times V_{\text{réservoir}}$$

Soit 18-36 L pour un réservoir de 180 L.

---

## I.8 Transmission pneumatique — Complément hydraulique

### **I.8.1 Principe et applications maritimes**

Un circuit pneumatique fonctionne sur le même principe que l'hydraulique, **mais avec un fluide compressible : l'air**.

**Compressibilité de l'air :**

$$p_1 V_1 = p_2 V_2 \quad \text{(Loi de Boyle-Mariotte à T constante)}$$

Cette compressibilité change fondamentalement le comportement :
- **Avantage** : absorption naturelle des à-coups
- **Inconvénient** : précision de positionnement réduite

### **I.8.2 Chaîne pneumatique type d'un navire**

```
┌──────────────────┐
│  Compresseur     │  Génère l'air comprimé
│  (électrique ou  │  Pression typique : 7 bar (démarrage), 6 bar (auxiliaires)
│  direct moteur)  │  Débit : 300-500 L/min
└────────┬─────────┘
         │
    ┌────▼────┐
    │ Réservoir │  Volume tampon : 300-500 L
    │  air 7bar │  Lisse les pics, limite arrêt/redémarrage
    └────┬─────┘
         │
    ┌────▼──────────────────────┐
    │  Ensemble FRL             │  Conditionnement de l'air
    │ (Filtre-Régul-Lubrifiant) │
    │                           │
    │ Filtre : 5 μm             │  Élimine humidité et impuretés
    │ Régulateur : 6 bar        │  Abaisse la pression
    │ Lubrificateur : huile     │  Protège actionneurs pneumatiques
    └────┬──────────────────────┘
         │
    ┌────┴────┬──────────┐
    │          │          │
    ▼          ▼          ▼
  ┌────┐    ┌────┐    ┌──────┐
  │VER │    │VAL │    │MOTEUR│  ACTIONNEURS PNEUMATIQUES
  │PNE│    │VER │    │PNEU. │
  └────┘    └────┘    └──────┘
   
  Démarrage  Arrêt    Outils auxiliaires
  moteur     vannes   (découpe filets, etc.)
```

### **I.8.3 Différences hydraulique vs pneumatique**

| **Critère** | **Hydraulique** | **Pneumatique** |
|---|---|---|
| **Pression service** | 100-450 bar | 4-10 bar (auxiliaires), 20-30 bar (démarrage moteur) |
| **Puissance transmissible** | Très élevée (kW) | Modérée (< 5 kW typiquement) |
| **Précision positionnement** | Élevée (fluide incompressible) | Modérée-basse (air compressible) |
| **Risque de fuite** | Pollution par huile | Aucun (air gratuit) |
| **Coût fluide** | 500-1000 €/an (traitement huile) | Négligeable (air atmosphérique) |
| **Temps de réponse** | Rapide (< 100 ms) | Très rapide (< 50 ms) |
| **Sécurité marins** | Risque de projection d'huile sous pression | Aucun risque d'injection |

### **I.8.4 Débit et puissance pneumatiques**

La puissance pneumatique utile est :

$$P_{\text{pneu}} (W) = p (Pa) \times Q (m^3/s) = p (bar) \times Q (L/min) / 600$$

Pour p = 6 bar et Q = 100 L/min :

$$P_{\text{pneu}} = 6 \times 100 / 600 = 1 \text{ kW}$$

Cette puissance réduite justifie l'usage pneumatique pour les **auxiliaires** (démarrage moteur, outils manuels) et non pour les efforts majeurs.

---

## I.9 Grandeurs caractéristiques et relation fondamentale de puissance

### **I.9.1 Relation puissance-pression-débit**

La puissance hydraulique utile transmise par un circuit est :

$$P_{\text{utile}} (kW) = \frac{p \text{ (bar)} \times Q \text{ (L/min)}}{600}$$

Cette relation unit les trois grandeurs fondamentales du circuit :
- **p** : pression (bar) — intensité de l'effort
- **Q** : débit (L/min) — vitesse du mouvement
- **P** : puissance (kW) — énergie par unité de temps

### **I.9.2 Puissance absorbée vs puissance utile**

La pompe doit absorber une puissance supérieure à la puissance utile pour compenser les pertes :

$$P_{\text{absorbée}} = \frac{P_{\text{utile}}}{\eta_{\text{global}}}$$

où η_global est le rendement global du circuit :

$$\eta_{\text{global}} = \eta_{\text{volumétrique}} \times \eta_{\text{mécanique}} \times \eta_{\text{hidráulique}}$$

Avec :
- η_volumétrique ≈ 0.94 (pertes internes de la pompe)
- η_mécanique ≈ 0.96 (frottements aux paliers)
- η_hydraulique ≈ 0.85 (pertes de charge en conduites)

$$\eta_{\text{global}} \approx 0.94 \times 0.96 \times 0.85 \approx 0.77 \text{ (77%)}$$

Donc, pour une puissance utile de 100 kW :

$$P_{\text{absorbée}} = \frac{100}{0.77} = 130 \text{ kW}$$

### **I.9.3 Application au calcul de puissance moteur principal**

C'est cette relation qui structure l'ensemble des calculs de la **Partie II** :

1. On définit l'effort mécanique requis (traction du chalut, couple du safran, masse à lever)
2. On en déduit la pression et le débit nécessaires
3. On calcule la puissance hydraulique utile
4. On remonte jusqu'à la puissance absorbée par chaque système
5. On somme sur tous les systèmes (treuil, timonerie, grue) pour obtenir la **puissance totale** à installer sur le moteur principal

$$P_{\text{moteur}} \geq P_{\text{treuil}} + P_{\text{timonerie}} + P_{\text{grue}} + P_{\text{auxiliaires}}$$

avec marge de sécurité de 10-15%.

---

## I.10 Synthèse et transition vers la mécanique des fluides

Ce chapitre a établi les **fondations théoriques** de la transmission hydraulique et pneumatique. Le Chapitre II approfondira le comportement des fluides en mouvement (équations de Bernoulli, Darcy-Weisbach), élément clé pour vérifier que les **pertes de charge** restent acceptables et que le **dimensionnement des conduites** est approprié.

### **Points clés à retenir :**

✅ **Principe de Pascal** : pression transmise intégralement dans fluide incompressible

✅ **Pompe à pistons axiaux** : meilleur choix pour hydraulique marine haute pression

✅ **Moteur/Vérin** : convertissent pression en effort/mouvement via formules C = (V_g × p)/100 et F = A × p

✅ **Distributeur 4/3 centre fermé** : orchestre le flux dans les deux sens, bloque en neutre

✅ **Réservoir** : 2-3 × débit pompe, refroidissement et filtration essentiels

✅ **Relation P = (p × Q)/600** : lie pression, débit et puissance — clé du dimensionnement

✅ **Rendement global ~77%** : différence significative entre puissance utile et puissance absorbée

---

## SOURCES CHAPITRE I

**Normes ISO :**
- ISO 4413:2010 — *Transmissions hydrauliques — Règles générales et sécurité*
- ISO 1219-1:2012 — *Symboles graphiques et schémas des systèmes et installations hydrauliques*
- ISO 6162:2015 — *Interfaçage hydraulique — Tailles et caractéristiques des raccords*

**Références académiques :**
- Esposito, A. (2003) — *Fluid Power with Applications*. Pearson Education. ISBN: 978-0130615251
- Backé, W. & Murrenhoff, H. (2008) — *Fluid Power Engineering*. RWTH Aachen University
- Poulit-Huet, J. (1998) — *Hydraulique Industrielle* (2e éd.). Dunod, Paris. ISBN: 2-10-002755-4

**Traités spécialisés :**
- Nenni, M.E. & Nicholas, J.D. (2013) — *Encyclopedia of Marine Technology*. Society of Naval Architects and Marine Engineers (SNAME)
- Det Norske Veritas (DNV-GL) — *Rules for Classification of Ships*. Part 3, Chapter 9 (Hydraulic and Pneumatic Systems). [www.dnvgl.com](https://www.dnvgl.com)

**Manuels constructeurs (Rexroth Bosch) :**
- Rexroth Bosch — *A4V Bent Axis Pump — Technical Data*. Publication RE 92104
- Rexroth Bosch — *4WRPEH — Proportional Directional Valve*. Publication RE 13154

---

**Fin du Chapitre I**