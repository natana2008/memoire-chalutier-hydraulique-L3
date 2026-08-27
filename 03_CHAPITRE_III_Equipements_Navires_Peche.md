# CHAPITRE III — ÉQUIPEMENTS HYDRAULIQUES ET PNEUMATIQUES DES NAVIRES DE PÊCHE

## III.1 Le chalutier arrière — Architecture générale et historique

### **III.1.1 Définition et contexte**

Un **chalutier arrière** est un navire de pêche commercial dont la caractéristique essentielle est le **traînage et la remontée du chalut par l'arrière** du navire, via une **rampe inclinée** ou **passerelle de pêche**.

**Dimensions typiques du chalutier 18 m :**

| Caractéristique | Valeur |
|---|---|
| Longueur hors tout (LOA) | 18.0 m |
| Largeur (Bau) | 5.8 m |
| Creux (tirant d'eau) | 3.2 m |
| Tonnage brut (GT) | ≈ 80-100 |
| Puissance moteur | 500-600 kW (diesel) |
| Capacité de cale | 40-50 tonnes de poisson frais |
| Autonomie | 10-15 jours de mer |
| Équipage | 5-7 marins |

### **III.1.2 Évolution du chalutier arrière**

Avant les années 1970, les navires de pêche pratiquaient le **chalutage latéral** : le chalut était lancé et remonté par le **côté du navire** (tribord ou bâbord). Cette pratique exposait l'équipage à des risques très élevés :
- Risque de chute à la mer lors des manœuvres
- Risque de compression par les câbles sous tension
- Efficacité réduite des manœuvres

L'adoption progressive du **chalutage arrière** à partir des années 1970 a révolutionné la sécurité et l'efficacité :
- **Rampe inclinée** à l'arrière : le chalut monte naturellement par glissement
- **Treuil positionné sur le pont arrière** : opérateur à l'abri
- **Grue de pont** intégrée pour la manutention
- **Timonerie hydraulique** permettant les manœuvres de positionnement précis

Cette architecture est devenue **standard international** pour la flottille de pêche commerciale (FAO, ILO, IMO).

---

## III.2 Le système hydraulique du treuil de pêche

### **III.2.1 Fonction générale**

Le treuil remonte le chalut chargé de poisson. C'est le système hydraulique **le plus puissant** du bord.

**Efforts à maîtriser :**
- Traction du chalut plein : T = 40-50 tonnes-force (400-500 kN)
- Vitesse de remontée : v_chalut = 0.5-1.0 m/s
- Durée d'une remontée : 8-12 minutes

**Puissance requise :**

$$P_{\text{treuil}} = T \times v = 450,000 \text{ N} \times 0.75 \text{ m/s} = 337.5 \text{ kW}$$

### **III.2.2 Architecture du treuil — Types**

**A) Treuil simple tambour (économique)**

```
        Arbre moteur
             │
        ┌────▼────┐
        │ Réducteur │  i = 1:10 à 1:15
        │ (engrenages)
        └────┬────┘
             │
        ┌────▼────────────┐
        │   TAMBOUR        │  Diamètre ≈ 1 m
        │  (simple)        │  Câble 24 mm acier
        └──────────────────┘
```

**Avantages :** coût, encombrement réduit
**Inconvénients :** manœuvres limitées, assiette du filet non contrôlable

**B) Treuil double tambour (industrie standard)**

```
        Arbre moteur
             │
        ┌────▼────┐
        │ Réducteur │  i = 1:12
        │  double  │
        └────┬────┘
             │
        ┌────┴────────┬────────────┐
        │             │            │
    ┌───▼───┐    ┌────▼────┐   Boîte de vitesses
    │TAMBOUR│    │TAMBOUR   │   (couplage)
    │  Droit│    │ Gauche   │
    └───────┘    └──────────┘
    
    Câble droit (40m, 24mm)     Câble gauche (40m, 24mm)
```

**Avantages :** contrôle indépendant des deux câbles, ajustement de l'assiette du filet
**Inconvénients :** plus onéreux, plus complexe

**C) Treuil "split" fractionné (haute performance) — Chalutier 18 m étudié**

```
    Moteur diesel 600 kW
    Prise de mouvement (PDM)
             │
        ┌────┴─────────┬────────────┐
        │              │            │
    ┌───▼───┐      ┌───▼───┐   ┌───▼───┐
    │POMPE 1 │      │POMPE 2 │   │POMPE 3 │  Trois circuits indépendants
    │(treuil)│      │(timon.)│   │(grue)  │
    │120cm³ │      │45cm³   │   │60cm³   │
    └───┬───┘      └───┬───┘   └───┬───┘
        │              │            │
    ┌───▼─────────────┬────────────┬────┐
    │   DISTRIBUTEUR 1 │ DIST. 2    │ DIST. 3 │
    └───┬─────────────┼────────────┼────┘
        │             │            │
    ┌───▼────┐    ┌──▼──┐    ┌────▼───┐
    │ MOTEUR  │    │VÉRINS│    │MOTEUR   │
    │TREUIL   │    │SAFRAN│    │GRUE     │
    │250 cm³  │    │85mm  │    │125 cm³  │
    └─────────┘    └──────┘    └─────────┘
    
    Tambour Droit    Barre      Palan
    Tambour Gauche   à vent
```

### **III.2.3 Composition du circuit treuil — Cas du chalutier 18 m**

```
┌──────────────────────────────────────────────────────────┐
│ CIRCUIT TREUIL — ARCHITECTURE COMPLÈTE                   │
└──────────────────────────────────────────────────────────┘

GÉNÉRATION D'ÉNERGIE :
  Moteur diesel 600 kW (2 500-2 800 tr/min)
         │
    Prise de mouvement (PDM)
    Arbre de sortie : 150-200 kW @ 2 500 tr/min
         │
    ┌────▼────────────────────────┐
    │   POMPE HYDRAULIQUE          │
    │   Type : Pistons axiaux      │
    │   Cylindrée : 120 cm³/tr     │
    │   Pression : 280 bar         │
    │   Débit théorique : 300 L/min│ (120 × 2500 / 1000)
    │   Rendement : 94%            │
    │   Débit réel : 282 L/min     │
    └────┬───────────────────────┘
         │
DISTRIBUTION ET RÉGULATION :
         │
    ┌────▼──────────────────────┐
    │ LIMITEUR DE PRESSION       │
    │ Tarage : 280 bar           │
    │ Rôle : Protection circuit   │
    └────┬──────────────────────┘
         │
    ┌────▼────────────────────────────┐
    │ DISTRIBUTEUR 4/3 CENTRE FERMÉ    │
    │ Type : Électrohydraulique        │
    │ Voies : 4 (P, T, A, B)          │
    │ Positions : 3 (Avant/Neutre/Ar) │
    │ Commande : Électrique + Pilotage│
    │ Débit nominal : 250 L/min       │
    └────┬─────────────────────────┘
         │
    ┌────┴──────────────────────┐
    │                           │
    ▼                           ▼
┌─────────────────┐      ┌──────────────────┐
│ MOTEUR TREUIL 1 │      │ MOTEUR TREUIL 2  │
│ (Tambour droit) │      │ (Tambour gauche) │
│ Type : Pistons  │      │ Type : Pistons   │
│ Cylindrée : 250 │      │ Cylindrée : 250  │
│ cm³/tr          │      │ cm³/tr           │
│ P_max : 280 bar │      │ P_max : 280 bar  │
│ Couple : 700 N·m│      │ Couple : 700 N·m │
│ Vitesse : 240   │      │ Vitesse : 240    │
│ tr/min          │      │ tr/min           │
│ Rendement : 96% │      │ Rendement : 96%  │
└────────┬────────┘      └────────┬─────────┘
         │ Sortie                 │ Sortie
         │ Arbre @ 240 tr/min     │ Arbre @ 240 tr/min
         │ Couple : 700 N·m       │ Couple : 700 N·m
         │                       │
    ┌────▼──────────────┐   ┌────▼──────────────┐
    │ RÉDUCTEUR 1       │   │ RÉDUCTEUR 2       │
    │ Rapport : 1:10    │   │ Rapport : 1:10    │
    │ Entrée : 240/min  │   │ Entrée : 240/min  │
    │ Sortie : 24 tr/min│   │ Sortie : 24 tr/min│
    │ Couple sortie :   │   │ Couple sortie :   │
    │ 7 000 N·m         │   │ 7 000 N·m         │
    └────┬──────────────┘   └────┬──────────────┘
         │                       │
    ┌────▼───────────────────────▼────┐
    │   EMBRAYAGE / FREIN              │
    │   Système de sécurité            │
    │   Prévient la rotation libre     │
    └────┬───────────────────────────┘
         │
    ┌────▼──────────────────────────┐
    │   TAMBOUR TREUIL              │
    │   Diamètre extérieur : 1.2 m  │
    │   Rayon : 0.6 m               │
    │   Câble : 24 mm acier galv.   │
    │   Longueur par tambour : 40 m │
    │   Charge : 40 tonnes @ 0.75 m/s
    └───────────────────────────────┘

RETOUR :
    │
    ┌▼─────────────────────────────────┐
    │ CLAPET ANTI-RETOUR (sécurité)    │
    │ Craquement : 280 bar             │
    │ Empêche chute libre du chalat    │
    └─┬──────────────────────────────┘
     │
    ┌▼──────────────────────────────┐
    │ RÉSERVOIR                       │
    │ Volume : 200 L                  │
    │ Capacité de refroidissement     │
    │ Décantation des impuretés       │
    └─────────────────────────────────┘
```

---

## III.3 La timonerie hydraulique (gouvernail)

### **III.3.1 Fonction et contraintes**

La timonerie contrôle la direction du navire via le **gouvernail** (ou **safran**).

**Efforts à maîtriser :**
- Couple résistant du safran : C_r = 8-12 tonnes-force·m (80-120 kN·m)
- Angle de barre : 0° à 35° (chaque bord)
- Vitesse de basculement : 2-4 sec pour passer de -35° à +35° (manœuvre)

### **III.3.2 Architecture — Vérin de barre**

La timonerie moderne utilise un **système de vérins hydrauliques double effet** :

```
    Tête de barre
    (pivot supérieur)
         │
    ┌────▼────────────────────┐
    │  PIVOT SUPÉRIEUR         │
    │  Permet la rotation      │
    └────┬───────────────────┘
         │
    ┌────▼────────────────────────────┐
    │   CHAPPE DE BARRE               │
    │   (liaison safran-vérins)       │
    └────────────────────────────────┘
         │
    ┌────┴────────────────────┬────────────────────┐
    │                         │                    │
    ▼                         ▼                    ▼
┌─────────────┐         ┌─────────────┐      ┌──────────────┐
│ VÉRIN 1     │         │ VÉRIN 2     │      │ VÉRIN 3      │
│ (Poussée)   │         │ (Poussée)   │      │ (Secours)    │
│ D = 80 mm   │         │ D = 80 mm   │      │ D = 80 mm    │
│ Course : 400│         │ Course : 400│      │ Course : 400 │
│ mm          │         │ mm          │      │ mm           │
│ 2 actifs +  │         │ 2 actifs +  │      │ 1 en secours │
│ 1 secours   │         │ 1 en secours│      │              │
└──────┬──────┘         └──────┬──────┘      └──────┬───────┘
       │                       │                    │
       │ (Tige-Poussée)        │ (Tige-Poussée)    │ (Tige)
       │                       │                    │
    ┌──┴──────────────────────┴────────────────────┴───┐
    │           SAFRAN (Gouvernail)                    │
    │           Profil hydrodynamique                  │
    │           Surface : 6-8 m²                       │
    │           Masse : 2-3 tonnes                     │
    └────────────────────────────────────────────────┘
```

### **III.3.3 Système de distribution hydraulique (timonerie)**

```
POMPE TIMONERIE
(45 cm³, 210 bar, 112 L/min)
       │
    ┌──▼────────────────────────┐
    │ DISTRIBUTEUR 4/3           │
    │ Commande : JOYSTICK        │
    │ Centre : Fermé (sécurité)  │
    │ Si lâche → blocage safran  │
    └──┬──────────────────────┘
       │
    ┌──┴──────────────┬──────────────┐
    │                 │              │
    ▼                 ▼              ▼
┌──────────────┐ ┌────────────┐ ┌─────────────┐
│ VERS VÉRINS 1│ │ VERS VÉRINS│ │LIGNE RETOUR │
│ & 2 (P→A)   │ │ 3 (P→A)    │ │ VERS RÉSER. │
└──────┬───────┘ └────┬───────┘ └──────┬──────┘
       │              │                │
    ┌──▼──────────────▼────┐          │
    │  ACCUMULATEUR        │          │
    │  Lisse les pics      │          │
    │  V = 20-30 L         │          │
    │  p_tarage = 210 bar  │          │
    └──┬──────────────────┘          │
       │                             │
    ┌──┴─────────────────────────────▼──────┐
    │      VÉRINS (Parallèle ou Tandem)     │
    │                                        │
    │ Vérins 1 & 2 : Débrayable pour test  │
    │ Vérin 3 : Secours (de sécurité)      │
    │ Commande manuelle possible            │
    └─────────────────────────────────────┘
```

### **III.3.4 Calcul de force du vérin**

**Effort résistant du safran à 10 nœuds (5 m/s) :**

$$F_{\text{résistant}} = \frac{1}{2} \rho_{\text{eau}} V^2 S C_d$$

où :
- ρ_eau = 1 025 kg/m³
- V = 5 m/s
- S = 6 m² (surface du safran)
- C_d ≈ 2.0 (coefficient de traînée)

$$F = \frac{1}{2} \times 1025 \times 25 \times 6 \times 2 = 153,750 \text{ N} \approx 15.4 \text{ tonnes-force}$$

**Couple résistant :**

$$C_r = F \times L_{\text{bras}} = 153,750 \times 0.5 = 76,875 \text{ N·m}$$

(où L_bras = 0.5 m est la distance du centre de pression à l'axe de safran)

**Force requise par vérin (2 vérins en parallèle) :**

$$F_{\text{vérin}} = \frac{C_r}{L_{\text{moment}}} \div n_{\text{vérins}}$$

où L_moment ≈ 0.4 m (distance vérins à l'axe pivot).

$$F_{\text{vérin}} = \frac{76,875}{0.4} \div 2 = 96,094 \text{ N par vérin}$$

**Pression requise (vérin D = 80 mm) :**

$$A_{\text{piston}} = \pi (40)^2 = 5,027 \text{ mm}^2$$

$$p = \frac{F}{A} = \frac{96,094 \times 10}{5,027} = 191 \text{ bar}$$

→ **Tarage pompe timonerie : 210 bar** (avec marge 10%)

---

## III.4 La grue de pont

### **III.4.1 Fonction**

La grue de pont permet la **manutention et le sauvetage** :
- Chargement/déchargement du navire
- Enlèvement des captures du chalut
- Opérations de sauvetage maritime (SOLAS)
- Manœuvres de dépannage

**Capacité typique :** 5-10 tonnes de charge
**Portée :** 8-12 m (depuis navire vers quai ou embarcation)

### **III.4.2 Architecture — Moteur hydraulique rotatif**

```
POMPE GRUE (60 cm³, 250 bar, 150 L/min)
     │
  ┌──▼────────────────────────────┐
  │ DISTRIBUTEUR 4/3 PROPORTIONNEL │
  │ Commande : Pendentif           │
  │ Débit modulable (0-100%)       │
  └──┬─────────────────────────────┘
     │
  ┌──▼─────────────────────────────────┐
  │ LIMITEUR DE MOMENT (LMI)            │
  │ Système de sécurité : calcul continu│
  │ du moment de renversement           │
  │ Coupe flux si M > M_max             │
  └──┬────────────────────────────────┘
     │
  ┌──▼──────────────────┐
  │ MOTEUR GRUE (125    │
  │ cm³/tr, 250 bar)    │
  │ Couple : 312 N·m    │
  │ Vitesse : 240 tr/min│
  └──┬──────────────────┘
     │
  ┌──▼───────────────────┐
  │ RÉDUCTEUR (1:6)      │
  │ Sortie : 40 tr/min  │
  │ Couple sortie :      │
  │ 1 872 N·m            │
  └──┬──────────────────┘
     │
  ┌──▼──────────────────────────┐
  │ TAMBOUR GRUE                 │
  │ Diamètre : 0.4 m             │
  │ Câble : 16 mm acier          │
  │ Capacité : 10 tonnes         │
  │ Vitesse de levage : 0.6 m/s  │
  └──────────────────────────────┘
```

### **III.4.3 Système de limitation du moment (LMI)**

**Problématique :** La grue ne doit jamais renverser le navire. Le moment du poids levé (pris à distance du navire) doit rester < moment d'assiette du navire.

**Formule du moment de renversement :**

$$M = P \times d$$

où :
- P = poids de la charge (kN)
- d = distance horizontale du centre de masse au-dessus du centre de gravité du navire (m)

**Limite de sécurité (réglementation EN 13000) :**

$$M_{\text{max}} \leq 0.85 \times M_{\text{stabilité du navire}}$$

**Système LMI :** Capteurs mesurent en continu :
1. La charge (via capteur de pression du moteur grue)
2. La portée (via capteur de position du bras ou du câble)
3. L'assiette du navire (via inclinomètre)

Si M > M_max → **électrovanne coupe le flux hydraulique vers le moteur grue** (sécurité passive).

---

## III.5 Circuit pneumatique d'air comprimé

### **III.5.1 Applications**

Le circuit pneumatique du navire fournit l'air comprimé pour :
1. **Démarrage du moteur diesel** (4-6 bouteilles à 30 bar, cylindrée totale 60-100 L)
2. **Accessoires de pont** (outils pneumatiques, vannes pilotées, manomètres)
3. **Signalisation** (sirène de brume, klaxons)

### **III.5.2 Architecture complète**

```
COMPRESSEUR (électrique, 2.2 kW)
Débit : 200 L/min @ 7 bar
Pression de décharge : 7.5 bar
Détente automatique à 7 bar
     │
  ┌──▼─────────────────┐
  │ RÉSERVOIR           │
  │ PRINCIPAL           │
  │ Volume : 400 L      │
  │ Pression : 7 bar    │
  │ Capacité : ~2 800 L │
  │ d'air @ 1 bar       │
  └──┬────────────────┘
     │
  ┌──▼──────────────────────┐
  │ FRL PRINCIPAL            │
  │ (Filtre-Régul.-Lubrif.)  │
  │ Filtre : 5 μm            │
  │ Régulateur : 6 bar       │
  │ Lubrification : 1 goutte/min
  └──┬─────────────────────┘
     │
  ┌──┴────────────┬────────────┬──────────────┐
  │               │            │              │
  ▼               ▼            ▼              ▼
┌────────┐  ┌─────────┐  ┌──────────┐  ┌──────────┐
│BOUTEILL│  │ACCESSOI│  │ MANOMÈTR│  │SIGNALISA│
│E DÉMAR.│  │RES PONT│  │E + SOUPAPE  │TION     │
│30 bar  │  │(outils)│  │DE SÉCU.   │ (Sirène) │
│ × 4    │  │        │  │           │          │
│        │  │        │  │           │          │
│Secteur A│  │Secteur │  │Secteur A  │ Secteur C│
└────────┘  └─────────┘  └──────────┘  └──────────┘
```

---

## SOURCES CHAPITRE III

**Normes et standards maritimes :**
- IMO Resolution A.481(12) — *Code of Safe Practice for Ships with Low Freeboard*
- SOLAS (1974) — *International Convention for the Safety of Life at Sea* — Convention Internationale pour la Sauvegarde de la Vie en Mer (mise à jour 2024)
- EN 13000:2015+A1:2018 — *Grues de manutention — Grues mobiles de chantier — Règles de sécurité*
- ISO 4414:2010 — *Transmissions pneumatiques — Règles générales et sécurité*

**Directives et classifications :**
- DNV GL — *Rules for Classification of Ships — Part 3, Chapter 9 (Hydraulic and Pneumatic Systems)*. [www.dnvgl.com](https://www.dnvgl.com)
- ABS — *Rules for Building and Classing Steel Vessels — Part 4, Chapter 7 (Mechanical Systems)*
- Bureau Veritas — *Rules for the Classification of Steel Ships*

**Traités spécialisés en navires de pêche :**
- Nenni, M.E. & Nicholas, J.D. (2013) — *Encyclopedia of Marine Technology*. SNAME (Society of Naval Architects and Marine Engineers). ISBN: 978-0939773794
- Eyres, D.J. (2012) — *Ship Construction* (7e éd.). Butterworth-Heinemann. ISBN: 978-0080966304

**Manuels techniques constructeurs :**
- Rexroth Bosch — *Mobile Machinery — Technical Data and Engineering Handbook*. Publication RE 92100
- Parker — *Hydraulic Components & Systems — Marine Applications*. Manual GMM-002
- Hydac — *Hydraulic System Design — Marine and Offshore*. Brochure SY-PB-001

---

**Fin du Chapitre III**