# ANNEXES TECHNIQUES

---

## ANNEXE A — TABLES DE CONVERSION ET CONSTANTES

### A.1 Unités hydrauliques et conversions

| **Grandeur** | **Unité SI** | **Unité courante** | **Facteur conversion** |
|---|---|---|---|
| **Pression** | Pascal (Pa) | bar | 1 bar = 10⁵ Pa |
| **Pression** | Pa | psi (livres/po²) | 1 psi = 6 895 Pa |
| **Débit** | m³/s | L/min | 1 L/min = 1.667 × 10⁻⁵ m³/s |
| **Puissance** | Watt (W) | kW | 1 kW = 1 000 W |
| **Puissance** | W | CV (ch vapeur) | 1 CV = 735.5 W |
| **Couple** | N·m | kN·m | 1 kN·m = 1 000 N·m |
| **Force** | Newton (N) | kN | 1 kN = 1 000 N |
| **Force** | N | daN (déca-Newton) | 1 daN = 10 N |
| **Viscosité** | m²/s | cSt (centistoke) | 1 cSt = 10⁻⁶ m²/s |
| **Masse volumique** | kg/m³ | kg/L | 1 kg/L = 1 000 kg/m³ |

### A.2 Formules principales hydrauliques

**Puissance hydraulique :**
$$P [\text{kW}] = \frac{p [\text{bar}] \times Q [\text{L/min}]}{600}$$

**Débit volumique (pompe) :**
$$Q [\text{L/min}] = \frac{V_g [\text{cm}^3/\text{tr}] \times N [\text{tr/min}] \times \eta_v}{1000}$$

**Couple moteur hydraulique :**
$$C [\text{N·m}] = \frac{V_g [\text{cm}^3/\text{tr}] \times p [\text{bar}]}{100}$$

**Vitesse vérin :**
$$v [\text{m/s}] = \frac{Q [\text{L/min}]}{600 \times A [\text{cm}^2]}$$

**Force vérin :**
$$F [\text{N}] = p [\text{bar}] \times A [\text{cm}^2] \times 10$$

**Nombre de Reynolds :**
$$Re = \frac{v D}{\nu}$$

---

## ANNEXE B — TABLES DE PERTES DE CHARGE

### B.1 Coefficient de frottement λ (Moody diagram interpolé)

| **Re** | **Régime** | **λ (tube lisse)** |
|---|---|---|
| 1 000 | Laminaire | 64 / Re = 0.064 |
| 2 300 | Transitoire | ~0.042 |
| 4 000 | Transitoire-Turbulent | ~0.038 |
| 10 000 | Turbulent | ~0.032 |
| 100 000 | Turbulent développé | ~0.012 |

### B.2 Coefficients de perte singulière ξ (rugosité faible)

| **Singularité** | **ξ** | **Remarques** |
|---|---|---|
| Entrée réservoir (arrondie) | 0.08 | Bien profilée |
| Sortie réservoir (vive) | 1.0 | Sans arrondi |
| Coude 90° long rayon (r/D=1) | 0.4 | Rayon/diamètre = 1 |
| Coude 90° court rayon (r/D=0.5) | 0.9 | Rayon/diamètre = 0.5 |
| Coude 45° | 0.2 | Modéré |
| Raccord T (passage droit) | 0.6 | Écoulement axial |
| Raccord T (dérivation) | 1.0 | Écoulement latéral |
| Clapet anti-retour (ouvert) | 2.0 | Ouvert en charge |
| Filtre propre | 0.5 | Situation nominale |
| Filtre encrassé (limite) | 5.0 | En fin de vie |
| Distributeur 4/3 | 0.8-1.2 | Type proportionnel |

---

## ANNEXE C — SÉLECTION TUYAUTERIE (SAE, ISO, EN)

### C.1 Diamètres nominaux tuyaux hydrauliques

| **DN** | **Ø interne (mm)** | **Ø externe (mm)** | **P. max bar** | **Série** |
|---|---|---|---|---|
| **16** | 10 | 16 | 350 | SAE 100R13 |
| **20** | 12 | 20 | 350 | SAE 100R13 |
| **25** | 16 | 25 | 350 | SAE 100R13 |
| **32** | 20 | 32 | 350 | SAE 100R13 |
| **40** | 25 | 40 | 280 | SAE 100R1 |
| **50** | 32 | 50 | 280 | SAE 100R1 |
| **63** | 40 | 63 | 280 | SAE 100R1 |
| **80** | 50 | 80 | 210 | SAE 100R1 |
| **100** | 63 | 100 | 210 | SAE 100R1 |

**Légende :**
- **SAE 100R13** : Tube haute pression (tressé acier, 350 bar nominal)
- **SAE 100R1** : Tube basse/moyenne pression (moyen pression, 280 bar)
- **SAE 100R2** : Tube très basse pression (retour, < 50 bar)

---

## ANNEXE D — CARACTÉRISTIQUES HUILE HYDRAULIQUE HM ISO 46

### D.1 Propriétés physiques et chimiques

| **Propriété** | **Norme** | **Valeur typique** | **Unité** |
|---|---|---|---|
| **Viscosité cinématique @ 40°C** | ISO 3448 | 46 ± 4.14 | cSt |
| **Viscosité cinématique @ 100°C** | ISO 3448 | 6.9 ± 0.6 | cSt |
| **Indice de viscosité** | ISO 2909 | > 95 | — |
| **Masse volumique @ 15°C** | ISO 3104 | 870 ± 15 | kg/m³ |
| **Point éclair** | ISO 2592 | > 180 | °C |
| **Point d'écoulement** | ISO 3015 | < −15 | °C |
| **Indice d'acide** | ISO 6619 | < 0.5 | mgKOH/g |
| **Teneur eau** | ISO 6304 | < 500 | ppm |
| **Demande biochimique** | — | < 2 | ppm |

### D.2 Compatibilité joints

| **Matériau joint** | **HM 46** | **Remarques** |
|---|---|---|
| **NBR (Nitrile)** | ✓ Standard | Recommandé |
| **PTFE (Téflon)** | ✓ Acceptable | Pour pistons |
| **Cuir traité** | ✗ Proscrire | Gonflement |
| **Acrylique** | ✓ Bon | Haute température |

### D.3 Intervalle vidange

- **Service léger** : 2 000-2 500 heures
- **Service normal** : 1 500-2 000 heures
- **Service intensif** (treuil) : 1 000-1 500 heures
- **Remplacement filtre** : tous les 300-400 heures

---

## ANNEXE E — SCHÉMA P&ID SIMPLIFIÉ (DESCRIPTION TEXTUELLE)

### E.1 Circuit treuil (schéma ASCII)

```
MOTEUR DIESEL (600 kW @ 2500 tr/min)
            ↓
        PDM (Prise De Mouvement)
            ↓
    ┌─────────────────────────┐
    │  POMPE REXROTH A4V290   │
    │  350 bar, 680 L/min     │
    │  Cylindrée var.         │
    └────────┬────────────────┘
             │
             │ Refoulement DN63
             ↓
    ┌────────────────────┐
    │ LIMITEUR PRESSION  │
    │ Tarage 385 bar     │
    └────┬───────────────┘
         │
    ┌────┴──────────────────────────────┐
    │                                   │
    ↓                                   ↓
┌─────────────┐              ┌──────────────────┐
│  MOTEUR 1   │              │   MOTEUR 2       │
│ A6VM 500    │              │  A6VM 500        │
│ 500 cm³/tr  │              │  500 cm³/tr      │
│ 350 bar     │              │  350 bar         │
└──┬──────────┘              └────────┬─────────┘
   │                                  │
   │ Réducteur 1:8 (Brevini)         │ Réducteur 1:8
   │ Couple @ tambour                │ Couple @ tambour
   └──────┬──────────────────────────┘
          ↓
    ╔══════════════╗
    ║   TAMBOUR    ║
    ║   r = 0.6 m  ║
    ║   Chalut ↑   ║
    ╚══════════════╝

RETOUR (DN100) → RÉSERVOIR 2000L → FILTRE 10μm → ÉCHANGEUR 100kW
```

---

## ANNEXE F — ABAQUES DE SÉLECTION POMPES/MOTEURS

### F.1 Abaque puissance pompe (p vs Q)

```
Puissance (kW)
    ↑
 600 │     •••
    │    •   •
 500 │   •     •
    │  •   p=350bar •
 400 │ •           •
    │•             •
 300 │ ━━━━━━━━━━━━━━━━ p=280bar
    │
 200 │
    │
 100 │ ━━━━━━━━━━━━━━━━ p=210bar
    │
   0 └──────────────────────→ Débit (L/min)
      0   200   400   600   800
```

**Lecture :** À 680 L/min et 350 bar → P = 397 kW (pompe)

---

## ANNEXE G — CHECKLIST INSPECTION HYDRAULIQUE PRÉ-DÉMARRAGE

### G.1 Points de contrôle avant mise en service

- [ ] **Réservoir** : Niveau huile atteint (85% capacité), pas de fuite
- [ ] **Huile** : Couleur claire (pas de noircissement), pas d'odeur de brûlé
- [ ] **Conduites** : Aucune fuite visible, raccords serrés
- [ ] **Filtres** : Débit libre, pas d'indicateur rouge
- [ ] **Vérins** : Aucun suintement, course libre
- [ ] **Moteurs** : Pas de fuite d'huile, accouplement libre
- [ ] **Distributeurs** : Passage libre 4/3, commande fluide
- [ ] **Limiteur** : Tarage vérifié à 385 bar
- [ ] **Manomètres** : Étalonnage à jour (≤ 1 an)
- [ ] **Clapets anti-retour** : Craquement @ 350 bar vérifié
- [ ] **Compresseur pneumatique** : Débit d'air correct
- [ ] **Échangeur thermique** : Circulation eau de mer active

---

## ANNEXE H — FORMULAIRE MAINTENANCE PRÉVENTIVE

### H.1 Calendrier maintenance 12 mois

| **Intervalle** | **Tâche** | **Responsable** | **Coût est.** |
|---|---|---|---|
| **Démarrage** | Checklist pré-démarrage | Mécanicien | — |
| **Hebdo** | Contrôle niveau réservoir | Marin | — |
| **500 h** | Contrôle fuites conduites | Mécanicien | €200 |
| **1 000 h** | Changement filtre refoulement | Mécanicien | €400 |
| **1 500 h** | Vidange huile complète | Mécanicien | €1 200 |
| **2 000 h** | Inspection pompes/moteurs | Ingénieur | €1 500 |
| **Annuel** | Certificat classe DNV GL | Bureau Veritas | €800 |
| **Annuel** | Étalonnage manomètres | Labo certifié | €300 |
| **Tous les 2 ans** | Inspection grue EN 13000 | Organisme agréé | €1 500 |

**Budget annuel estimé : 5 500-6 000 €**

---

## ANNEXE I — SYMBOLES P&ID ESSENTIELS (ISO 1219-1)

```
SYMBOLES PRINCIPAUX :

Pompe centrifuge        →  [cercle avec flèche]
Pompe cylindrée var.    →  [carré avec triangle]
Moteur cylindrée const. →  [carré rempli]
Moteur cylindrée var.   →  [carré avec triangle double]

Vérin simple effet      →  [rectangle avec tige unilatérale]
Vérin double effet      →  [rectangle avec tiges bilatérales]

Distributeur 4/3        →  [carré divisé en 4 carrés]
Limiteur pression       →  [triangle pointé vers bas + ressort]
Clapet anti-retour      →  [boule + ressort]

Filtre                  →  [entonnoir stylisé]
Échangeur thermique     →  [grille pointillée]
Accumulateur            →  [cercle divisé moitié/moitié]
Réservoir               →  [rectangle large ouvert]

Manomètre               →  [cercle + M]
Débitmètre              →  [cercle + Q]
Thermomètre             →  [cercle + T]
```

---

## ANNEXE J — EXEMPLES CALCULS NUMÉRIQUES DÉTAILLÉS

### J.1 Exemple : Calcul perte de charge conduite refoulement

**Données :**
- Q = 680 L/min = 0.0113 m³/s
- D_int = 50 mm = 0.050 m
- L = 35 m
- Fluide HM46 @ 40°C : ν = 46 × 10⁻⁶ m²/s, ρ = 870 kg/m³

**Étape 1 : Vitesse d'écoulement**
$$v = \frac{4Q}{\pi D^2} = \frac{4 \times 0.0113}{\pi \times 0.050^2} = 5.76 \text{ m/s}$$

**Étape 2 : Nombre de Reynolds**
$$Re = \frac{vD}{\nu} = \frac{5.76 \times 0.050}{46 \times 10^{-6}} = 6,261$$

**Régime :** Turbulent (Re > 4 000) ✓

**Étape 3 : Coefficient de frottement (Colebrook)**
$$\frac{1}{\sqrt{\lambda}} = -2 \log_{10}\left(\frac{k/D}{3.7} + \frac{2.51}{Re\sqrt{\lambda}}\right)$$

Avec k/D ≈ 0 (tube lisse hydraulique), itération donne **λ ≈ 0.032**

**Étape 4 : Perte linéique**
$$\Delta p_{lin} = 0.005 \times \lambda \times \frac{L}{D} \times \frac{\rho v^2}{2}$$
$$= 0.005 \times 0.032 \times \frac{35}{0.050} \times \frac{870 \times 5.76^2}{2}$$
$$= 0.005 \times 0.032 \times 700 \times 14,480 = 16.2 \text{ bar}$$

**Étape 5 : Perte singulière**
$$\Delta p_{sing} = \xi \times \frac{\rho v^2}{2 \times 10^5} = 3.0 \times \frac{14,480}{2 \times 10^5} = 0.217 \text{ bar}$$

**Résultat total :** Δp = 16.2 + 0.217 ≈ **16.4 bar**

(Comparaison avec Chapitre VI : valeur révisée montrant l'importance diamètre tuyau)

---

**FIN ANNEXES**