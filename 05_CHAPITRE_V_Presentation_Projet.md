# PARTIE II — MÉTHODOLOGIE, RÉSULTATS ET DISCUSSIONS

---

# CHAPITRE V — PRÉSENTATION DU PROJET ET SPÉCIFICATIONS TECHNIQUES DU CHALUTIER

## V.1 Définition du chalutier 18 m — Cas d'étude

### **V.1.1 Caractéristiques générales**

Le chalutier arrière étudié dans ce mémoire est un **navire de pêche commercial type**, représentatif de la flottille française opérant sur le plateau continental atlantique.

| **Caractéristique** | **Valeur** | **Remarques** |
|---|---|---|
| **Longueur hors tout (LOA)** | 18.0 m | Entre bâbord et tribord, mesure réglementaire |
| **Largeur (Bau)** | 5.8 m | Dimension transversale maximale |
| **Creux (tirant d'eau)** | 3.2 m | De la quille au pont supérieur |
| **Tonnage brut (GT)** | 95 GT | Calculé selon Convention IMO 1969 |
| **Tonnage de jauge net (NT)** | 28 NT | Volume des espaces marchands |
| **Déplacement (Δ)** | 110 tonnes | Poids total du navire en flotaison |
| **Puissance moteur principal** | 600 kW (≈ 815 CV) | Moteur diesel Baudouin ou MAN 6 cyl. |
| **Capacité de cale** | 45 tonnes | Poisson frais maintenu à 0°C |
| **Autonomie** | 12-15 jours | Avec ravitaillement en carburant |
| **Équipage** | 5-6 marins | 1 capitaine, 1 mécanicien, 3-4 marins pêcheurs |
| **Coût construction** | €800 k - €1.2 M | Selon chantier et spécifications (2024) |

### **V.1.2 Type de pêche — Chalutage arrière au chalut de fond**

Le **chalutage arrière** est la technique dominante pour ce type de navire :

**Processus opérationnel :**

1. **Phase de transit** (30-60 min)
   - Navire se rend sur zone de pêche (20-50 milles nautiques)
   - Moteur diesel : régime constant 2 500-2 700 tr/min
   - Consommation : ~80-120 L diesel/heure

2. **Phase de mise à l'eau** (5 min)
   - Chalut lancé par la rampe arrière (environ 40 kg de matériel)
   - Grue de pont aide à la manipulation si nécessaire
   - Funes (câbles tracteurs) déroulées progressivement

3. **Phase de traînage** (30-120 min)
   - Navire tracte le chalut par 40-50 tonnes d'effort (traction)
   - Vitesse de traînage : 3-4 nœuds (1.5-2.0 m/s)
   - Treuil en charge permanente, moteur diesel à mi-régime

4. **Phase de remontée** (8-15 min)
   - Signal radio du maître pêche : "commencer la remontée"
   - Moteur diesel accélère à plein régime (2 800 tr/min)
   - Treuil ramène le chalut à bord via la rampe

5. **Phase de virage et tri** (20-40 min)
   - Navire tourne pour nouvelle traîne (manœuvre timonerie complète)
   - Équipage trie la capture : conservation du poisson commercial, rejet des poissons non viables
   - Nettoyage du filet

**Cycle complet :** 2-3 traînes par jour = 8-10 heures de pêche/jour, 6 jours/semaine

### **V.1.3 Spécifications de pêche — Données d'entrée**

Ces données constituent le **point de départ du dimensionnement** de tous les systèmes hydrauliques.

| **Paramètre de pêche** | **Valeur** | **Source** |
|---|---|---|
| **Poids du chalut vide** | 2 tonnes | Masse du filet + structure métallique |
| **Poids du chalut plein (capture + eau)** | 45 tonnes | Charge maximale en remontée |
| **Traction du chalut en traînage** | 50 tonnes-force | Mesure par dynamomètre nautique |
| **Vitesse de traînage** | 1.5 m/s (3 nœuds) | Standard commercial chalutage |
| **Vitesse de remontée du chalut** | 0.75 m/s | Vitesse de rotation du tambour treuil |
| **Profondeur de pêche** | 200 m | Plateau continental atlantique |
| **Longueur funes (câbles treuil)** | 40 m par tambour | 2 × 40 m = 80 m total (déroulement contrôlé) |
| **Diamètre funes acier galv.** | 24 mm | Standard maritime classe 8×19 |
| **Charge de rupture des funes** | 480 kN ≈ 48 tonnes-force | Spécification fournisseur (Bridon) |
| **Marge de sécurité funes** | 2.5 | 48 / 20 = 2.4 (acceptable) |

---

## V.2 Méthodologie générale de dimensionnement (approche IMRAD)

### **V.2.1 Vue d'ensemble — Les 5 étapes**

Le dimensionnement de chaque système hydraulique suit une **démarche itérative** identique :

```
┌─────────────────────────────────────────────────────────────┐
│ ÉTAPE 1 : DÉFINIR L'EFFORT OPÉRATIONNEL REQUIS             │
│ (Traction, couple, force, charge)                           │
│ Source : données de pêche, capacité navire, sécurité        │
└────────────────────┬────────────────────────────────────────┘
                     │
┌────────────────────▼────────────────────────────────────────┐
│ ÉTAPE 2 : CALCULER PRESSION ET DÉBIT THÉORIQUES            │
│ (Via formules Pascal, continuité, puissance)                │
│ Hypothèse : rendements de 90-95%                            │
└────────────────────┬────────────────────────────────────────┘
                     │
┌────────────────────▼────────────────────────────────────────┐
│ ÉTAPE 3 : SÉLECTIONNER COMPOSANTS COMMERCIAUX              │
│ (Pompe, moteur, vérin, réservoir, accumulateur)            │
│ Source : catalogues Rexroth, Parker, Hydac, Eaton          │
│ Avec marge de sécurité k = 1.1-1.3 selon composant         │
└────────────────────┬────────────────────────────────────────┘
                     │
┌────────────────────▼────────────────────────────────────────┐
│ ÉTAPE 4 : VÉRIFIER PERTES DE CHARGE ET TUYAUTERIE          │
│ (Darcy-Weisbach, Reynolds, singularités)                    │
│ Condition : Δp_total < p_nominale / 10                      │
│ Sinon : augmenter diamètre conduite et recalculer           │
└────────────────────┬────────────────────────────────────────┘
                     │
┌────────────────────▼────────────────────────────────────────┐
│ ÉTAPE 5 : VÉRIFIER CONFORMITÉ RÉGLEMENTAIRE                │
│ (SOLAS, EN 13000, DNV GL, ISO 4413)                         │
│ → Certification par classe et mise en service              │
└─────────────────────────────────────────────────────────────┘
```

### **V.2.2 Hypothèses générales de calcul**

Pour tous les circuits du chalutier 18 m, on adopte les **hypothèses standardisées** suivantes :

| **Hypothèse** | **Valeur** | **Justification** |
|---|---|---|
| **Fluide hydraulique** | ISO VG 46 (HM minérale) | Standard naval, viscosité stable 40-60°C |
| **Masse volumique fluide** | ρ = 870 kg/m³ | À 40°C, ISO 11158 |
| **Viscosité cinématique** | ν = 46 × 10⁻⁶ m²/s | À 40°C, ISO VG 46 |
| **Pression service treuil** | p = 280 bar | Pompe pistons axiaux standard |
| **Pression service timonerie** | p = 210 bar | Sécurité, vérin plus compact |
| **Pression service grue** | p = 250 bar | Compromis puissance-volume |
| **Température circuit** | T = 45-55°C | Régulation thermostat |
| **Rendement volumétrique pompe** | η_v = 0.94 | Pistons axiaux Rexroth/Parker |
| **Rendement mécanique pompe** | η_m = 0.96 | Standard industrie |
| **Rendement tuyauterie** | η_tuy = 0.88 | Pertes linéiques + singularités |
| **Rendement actionneur** | η_act = 0.97 | Moteur/vérin basse vitesse |
| **Rendement global système** | η_glob = 0.77 | Produit des rendements élémentaires |
| **Facteur charge simultanée** | k_sim = 0.85-1.0 | Variant selon scénario opérationnel |
| **Marge de sécurité pompe** | k_pompe = 1.15 | Norme ISO 4413 § 5.3 |
| **Marge de sécurité moteur** | k_moteur = 1.1 | Garantit couple réserve |
| **Marge de sécurité vérin** | k_vérin = 1.2 | Absorbe pics transitoires |
| **Marge de sécurité tuyauterie** | k_tuy = 1.3 | Tolérances fabrication + usure |

---

## V.3 Scénarios opérationnels et critères de charge

### **V.3.1 Scénario 1 — Remontée du chalat plein (CRITIQUE)**

**Conditions :**
- Chalut chargé de 45 tonnes remontant à la rampe
- Treuil fonctionnant à vitesse nominale
- Timonerie passive (navire stabilisé en ligne)
- Grue inactive

**Efforts appliqués :**

| **Système** | **Charge** | **Débit requis** | **Puissance utile** |
|---|---|---|---|
| **Treuil** | 45 tonnes × 0.75 m/s | 250 L/min | 330 kW |
| **Timonerie** | Couple de direction | 20 L/min | 5 kW |
| **Grue** | Arrêtée | 0 L/min | 0 kW |
| **TOTAL** | — | 270 L/min | 335 kW |

**Puissance absorbée par moteur principal :**

$$P_{\text{moteur}} = \frac{335}{0.77} + 15\% \text{ marge} = 435 + 65 = 500 \text{ kW} \quad \text{(acceptable pour 600 kW)}$$

### **V.3.2 Scénario 2 — Manœuvre navire + maintien chalat**

**Conditions :**
- Navire en virage serré (évasion chalutier concurrent, manœuvre d'urgence)
- Timonerie en charge maximale (angle 35°)
- Treuil maintient charge en suspens (faible débit, pression élevée)
- Grue inactive

**Efforts appliqués :**

| **Système** | **Charge** | **Débit requis** | **Puissance utile** |
|---|---|---|---|
| **Treuil** | 45 tonnes bloqué | 5 L/min (circulation freinage) | 20 kW |
| **Timonerie** | Couple max 120 kN·m | 100 L/min (débit max) | 35 kW |
| **Grue** | Arrêtée | 0 L/min | 0 kW |
| **TOTAL** | — | 105 L/min | 55 kW |

**Remarque :** Bien que la puissance soit inférieure au scénario 1, les **débits individuels sont très différents**. Ceci justifie des pompes **indépendantes** plutôt qu'une pompe centralisée (architecture split).

### **V.3.3 Scénario 3 — Sauvetage à la grue**

**Conditions :**
- Grue levant une embarcation de 5 tonnes
- Timonerie assurant le positionnement fin
- Treuil potentiellement en retenue (cas d'urgence)

**Efforts appliqués :**

| **Système** | **Charge** | **Débit requis** | **Puissance utile** |
|---|---|---|---|
| **Treuil** | 15 tonnes retenue | 10 L/min | 30 kW |
| **Timonerie** | Positionnement fin | 50 L/min | 18 kW |
| **Grue** | 5 tonnes levage | 120 L/min (vitesse rapide sauvetage) | 50 kW |
| **TOTAL** | — | 180 L/min | 98 kW |

**Puissance absorbée :**

$$P_{\text{moteur}} = \frac{98}{0.77} + 15\% = 128 + 19 = 147 \text{ kW}$$

Facilement absorbée par 600 kW disponibles.

### **V.3.4 Synthèse — Charge de dimensionnement**

Le **scénario critique** est la **remontée du chalut plein** (Scénario 1) :

$$P_{\text{dimensionnement}} = 500 \text{ kW (absorbée)}$$

Cette puissance détermine :
- Cylindrée totale des pompes
- Débit nominal du circuit
- Capacité du réservoir
- Puissance à pélever sur PDM moteur

---

## V.4 Données géométriques du treuil

### **V.4.1 Tambour du treuil**

```
Vue de profil du tambour :

        Rayon r = 0.6 m
        Diamètre D_tambour = 1.2 m
        
        
        ├─────────────────────┤
        
        Axe de rotation
        (pivot central)
              │
    ┌─────────┼─────────┐
    │         │         │
    │   ┌─────────────┐ │
    │   │  Câble en   │ │  Pas axial : 50 mm
    │   │ spirale sur │ │  (espacement entre spires)
    │   │  le tambour │ │
    │   └─────────────┘ │
    │         │         │
    └─────────┼─────────┘
              │
        
    Largeur du tambour : 800 mm (pour 2 funes côte à côte)
    Capacité totale : 80 m de câble 24 mm (40 m par fune)
    Poids du tambour à vide : 800 kg
    Poids du tambour chargé (80 m câble) : 800 + 2 × (80 × 5 kg/m) = 1 600 kg
```

### **V.4.2 Rapport de réduction du réducteur treuil**

Le réducteur (boîte de vitesses mécanique) réduit la **vitesse** du moteur hydraulique et **augmente le couple** en sortie.

**Données d'entrée :**
- Vitesse moteur hydraulique : N_moteur = 240 tr/min (vitesse nominale moteur pistons 250 cm³ @ 280 bar)
- Vitesse de remontée chalut : v_chalut = 0.75 m/s
- Rayon tambour : r = 0.6 m

**Vitesse du tambour requise :**

$$N_{\text{tambour}} = \frac{v_{\text{chalut}}}{\text{circonférence}} \times 60$$

$$N_{\text{tambour}} = \frac{0.75}{2 \pi \times 0.6} \times 60 = \frac{0.75}{3.77} \times 60 = 11.9 \text{ tr/min}$$

**Rapport de réduction :**

$$i = \frac{N_{\text{moteur}}}{N_{\text{tambour}}} = \frac{240}{11.9} = 20.2 \approx 1:20$$

**Couple en sortie du réducteur :**

Couple moteur @ 280 bar :

$$C_{\text{moteur}} = \frac{V_g \times p}{100} = \frac{250 \times 280}{100} = 700 \text{ N·m}$$

Couple tambour (avec rendement réducteur η_r = 0.95) :

$$C_{\text{tambour}} = C_{\text{moteur}} \times i \times \eta_r = 700 \times 20 \times 0.95 = 13,300 \text{ N·m}$$

**Traction théorique maximale :**

$$T_{\max} = \frac{C_{\text{tambour}}}{r} = \frac{13,300}{0.6} = 22,167 \text{ N} \approx 22.2 \text{ tonnes-force}$$

**Vérification :** T_max = 22 tonnes << 45 tonnes requises

→ **Problème : un seul moteur ne suffit pas !**

**Solution :** **Deux moteurs parallèles** (un par tambour) :

$$T_{\max,\text{total}} = 2 \times 22 = 44 \text{ tonnes-force} \approx 45 \text{ tonnes} \quad ✓$$

---

## V.5 Bilan énergétique global du navire

### **V.5.1 Consommation énergétique par système**

Pour 8 heures d'opération navale type (1 traîne = 2.5 heures) :

| **Système** | **Puissance moyenne** | **Durée** | **Énergie** |
|---|---|---|---|
| **Treuil** | 250 kW | 15 min remontée × 3 traînes | 12.5 kWh |
| **Timonerie** | 10 kW | 8 h (continu) | 80 kWh |
| **Grue** | 30 kW | 20 min total | 10 kWh |
| **Compresseur air** | 2.2 kW | 1 h démarrage + 1 h usage | 2.2 kWh |
| **Pompe circulation réfrigération** | 5 kW | 8 h continu | 40 kWh |
| **TOTAL HYD. + PNEU.** | — | — | **144.7 kWh** |

**Consommation diesel pour 8 h opération :**

À 2 500 tr/min moyen :

$$\text{Consommation moteur} = 80-100 \text{ L diesel/h} \times 8 \text{ h} = 640-800 \text{ L}$$

**Efficacité énergétique globale :**

Rendement diesel moteur : η_diesel ≈ 0.35 (efficacité thermique standard)

$$E_{\text{combustible}} = 700 \text{ L} \times 8.6 \text{ kWh/L} \times 0.35 = 2 107 \text{ kWh}$$

**Hydraulique reçoit :**

$$E_{\text{hydraulique}} = 600 \text{ kW} \times 8 \text{ h} \times 0.77 = 3696 \text{ kWh}$$

(Rendement global système hydraulique 77%)

**Coût opérationnel (2024, diesel 1.40 €/L) :**

$$\text{Coût diesel} = 700 \text{ L} \times 1.40 €/L = 980 € \text{ pour 8h} = 122.5 €/\text{heure}$$

---

## V.6 Données d'environnement et contraintes

### **V.6.1 Conditions marines extrêmes**

Le chalutier doit opérer dans les conditions suivantes :

| **Paramètre** | **Limite nominale** | **Limite extrême** | **Impact hydraulique** |
|---|---|---|---|
| **Température air extérieur** | 5-25°C | -5°C à +40°C | Viscosité huile varie ; thermostat indispensable |
| **Température eau mer** | 5-18°C (Atlantique N) | 3-20°C | Refroidissement échangeur thermique |
| **Agitation (houle)** | Mer 2-4 (modérée) | Mer 7-8 (tempête) | Pics de charge imprévisibles ; accumulateur absorbe |
| **Vibrations moteur diesel** | 50-100 Hz | Selon régime | Flexibles anti-vibrations essentiels |
| **Humidité relative** | 60-85% | 95% en tempête | Corrosion des circuits ouverts ; entretien renforcé |
| **Inclinaison navire (gîte)** | 0-5° | 0-15° en tempête | Pompe peut caviter si navire trop gîté ; capteur inclinaison |

### **V.6.2 Considérations de sécurité pour l'équipage**

La présence d'humains dans un environnement confiné accentue les exigences de sécurité :

- **Confinement du circuit hydraulique** : aucun risque d'injection sous pression (>280 bar)
- **Signalisation des tuyauteries** : marquage clair du débit, pression, fluide
- **Accessibilité pour maintenance** : tous composants accessibles sans démontage majeur
- **Procédures d'urgence** : coupure rapide du circuit, saignement de pression avant intervention
- **Équipement de protection** : gants, lunettes pour manipuler huile chaud

---

## SOURCES CHAPITRE V

**Données opérationnelles chalutiers :**
- Ifremer — *Profils technico-économiques des navires de pêche français* (Rapport annuel 2023)
- FAO — *Code of Conduct for Responsible Fisheries* (1995, révisé 2020)
- Defrance, J. & Laroche, J. (2012) — "Fishing fleet dynamics in the Bay of Biscay: a modelling approach." ICES Journal of Marine Science, 69(7), 1226-1237.

**Spécifications techniques :**
- Bridon — *Wire Rope Specification for Marine Applications* (catalogue 2024)
- Rexroth Bosch — *Mobile Hydraulic Components — Application Manual* (RE 92100)
- Baudouin Engines — *6M33TC Diesel Engine Technical Specifications* (datasheet 2023)

**Normes d'exploitation :**
- ISO 4413:2010 — *Transmissions hydrauliques — Règles générales et sécurité*
- DNV GL — *Rules for Classification of Ships — Part 3, Chapter 9* (édition 2024-01)
- IMO Res. A.749(18) — *Code of Safety for Fishermen and Fishing Vessels*

---

**Fin du Chapitre V**

Continuons maintenant vers le **Chapitre VI : Dimensionnement du système hydraulique du treuil de pêche...**