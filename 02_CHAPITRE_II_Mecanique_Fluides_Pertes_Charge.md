# CHAPITRE II — MÉCANIQUE DES FLUIDES ET ÉQUATIONS DES PERTES DE CHARGE

## II.1 Propriétés fondamentales du fluide hydraulique

Tout calcul de dimensionnement hydraulique repose sur la connaissance des propriétés physiques du fluide. Pour les circuits embarqués sur navires, on utilise des **huiles minérales hydrauliques** conformes à la norme ISO 11158 (HM 46).

### **II.1.1 Masse volumique ρ (kg/m³)**

La masse volumique détermine l'inertie du fluide et influence les phénomènes transitoires (coup de bélier).

$$\rho_{\text{huile hydraulique}} \approx 870 \text{ kg/m}^3 \quad \text{(à 15°C, pression atmosphérique)}$$

Variation avec la température :

$$\rho(T) = \rho_0 \times [1 - \alpha_T \times (T - T_0)]$$

où α_T ≈ 0.0007 K⁻¹ (coefficient d'expansion thermique).

Pour une augmentation de +50°C :

$$\rho(65°C) = 870 \times [1 - 0.0007 \times 50] = 840 \text{ kg/m}^3$$

**Impact sur le dimensionnement :**
- L'inertie du fluide diminue légèrement avec la température
- Les pertes de charge varient inversement (voir coefficient λ au II.2)

### **II.1.2 Viscosité dynamique μ (Pa·s) et cinématique ν (m²/s)**

La viscosité caractérise la résistance du fluide à l'écoulement par frottement interne.

**Relation entre viscosité dynamique et cinématique :**

$$\nu = \frac{\mu}{\rho}$$

**Grades de viscosité ISO (norme ISO 3448) :**

| Grade ISO | Viscosité nominale ν (mm²/s à 40°C) | Viscosité minimale | Viscosité maximale |
|---|---|---|---|
| ISO VG 32 | 32 | 28.8 | 35.2 |
| ISO VG 46 | 46 | 41.4 | 50.6 |
| ISO VG 68 | 68 | 61.2 | 74.8 |
| ISO VG 100 | 100 | 90 | 110 |

**Pour le chalutier 18 m :** ISO VG 46 (viscosité courante pour hydraulique marine)

$$\mu_{\text{HM46}} \approx 46 \text{ mm}^2/\text{s} = 46 \times 10^{-6} \text{ m}^2/\text{s} \quad \text{(à 40°C)}$$

$$\mu_{\text{(Pa·s)}} = \nu \times \rho = 46 \times 10^{-6} \times 870 = 0.040 \text{ Pa·s}$$

### **II.1.3 Variation de viscosité avec la température**

La viscosité est **très sensible à la température**. Elle suit une loi de type :

$$\log \log(\mu + 0.7) = A - B \times \log T$$

où T est en Kelvin. En pratique, on utilise l'**indice de viscosité (VI)** défini par ISO 2909 :

$$VI = \frac{L - U}{L - H} \times 100$$

Pour les huiles minérales standards : VI ≈ 95-105

Pour les huiles synthétiques : VI ≈ 130-150

**Exemple numérique :**

Huile ISO VG 46 à différentes températures :

| Température (°C) | Viscosité (mm²/s) | Viscosité (Pa·s) |
|---|---|---|
| 0 | 180-200 | 0.15-0.17 |
| 20 | 65-75 | 0.056-0.065 |
| 40 | 46 | 0.040 |
| 60 | 26-28 | 0.022-0.024 |
| 80 | 14-16 | 0.012-0.014 |

**Impact critique :** Une huile trop froide (0°C) augmente les pertes de charge d'un facteur 4-5, réduisant le débit et ralentissant les manœuvres. Une huile trop chaude (>70°C) réduit le film lubrifiant et accélère l'usure.

→ **Thermostat de circuit** indispensable, maintenant l'huile entre 45-55°C (optimum)

### **II.1.4 Compressibilité du fluide**

L'huile hydraulique est *quasi-incompressible* mais pas parfaitement incompressible. Son module de compressibilité est :

$$K = -\rho \frac{dp}{d\rho} \approx 1700 \text{ MPa} \quad \text{(à 25°C, 1 bar de pression absolue)}$$

Variation avec la pression :

$$K(p) = K_0 \times \left(1 + 0.0025 \times \frac{p}{p_0}\right)$$

Pour p = 280 bar (pression du treuil) :

$$K(280) = 1700 \times \left(1 + 0.0025 \times 280\right) = 2990 \text{ MPa}$$

**Conséquence pratique :** Bien que faible, cette compressibilité explique :
- Les phénomènes transitoires (coup de bélier) lors de fermetures rapides
- Les délais de réponse du circuit (quelques millisecondes)
- La nécessité d'amortisseurs et accumulateurs

---

## II.2 Régimes d'écoulement et nombre de Reynolds

### **II.2.1 Définition et formule du nombre de Reynolds**

Le nombre de Reynolds adimensionnel caractérise le régime d'écoulement — laminaire ou turbulent :

$$Re = \frac{\rho v D}{\mu} = \frac{v D}{\nu}$$

où :
- **ρ** = masse volumique (kg/m³)
- **v** = vitesse moyenne d'écoulement (m/s)
- **D** = diamètre hydraulique (m)
- **μ** = viscosité dynamique (Pa·s)
- **ν** = viscosité cinématique (m²/s)

**Pour une conduite de section circulaire :**

$$D = d_{\text{interne}}$$

**Pour une conduite de section rectangulaire (cas rare en hydraulique navale) :**

$$D_{\text{équivalent}} = \frac{4 \times A}{P}$$

où A = aire de section, P = périmètre mouillé.

### **II.2.2 Critères de transition : régimes d'écoulement**

| Régime | Domaine Re | Caractéristiques | Pertes de charge |
|---|---|---|---|
| **Laminaire** | Re < 2 300 | Filets fluides parallèles, ordre parfait, pas de mélange transversal | Proportionnelles à v (Poiseuille) |
| **Transitoire** | 2 300 < Re < 4 000 | Débuts de turbulence, instabilités | Transition progressive |
| **Turbulent** | Re > 4 000 | Mélange désordonné, tourbillons, eddies | Proportionnelles à v² (Darcy-Weisbach) |

### **II.2.3 Calcul de Re pour un circuit hydraulique type**

**Exemple : Treuil du chalutier (chapitre VI)**

Données :
- Débit Q = 60 L/min = 1 L/s = 0.001 m³/s
- Diamètre conduite refoulement D = 19 mm = 0.019 m
- Viscosité cinématique ν = 46 × 10⁻⁶ m²/s

**Vitesse d'écoulement :**

$$v = \frac{Q}{A} = \frac{4Q}{\pi D^2} = \frac{4 \times 0.001}{\pi \times (0.019)^2} = \frac{0.004}{0.001134} = 3.53 \text{ m/s}$$

**Nombre de Reynolds :**

$$Re = \frac{v D}{\nu} = \frac{3.53 \times 0.019}{46 \times 10^{-6}} = \frac{0.0671}{46 \times 10^{-6}} = 1,459$$

**Conclusion :** Re < 2 300 → **Régime laminaire**

### **II.2.4 Coefficient de perte de charge linéaire λ**

Le coefficient λ dépend du régime d'écoulement et, en régime turbulent, de la rugosité relative de la conduite.

**Régime laminaire (Re < 2 300) :**

$$\lambda = \frac{64}{Re}$$

Pour Re = 1 459 :

$$\lambda = \frac{64}{1459} = 0.0439$$

**Régime turbulent lisse (Re > 4 000, tubage lisse) :**

Formule de Blasius (pour 4 000 < Re < 100 000) :

$$\lambda = 0.316 \times Re^{-0.25}$$

**Régime turbulent rugueux :**

Formule implicite de Colebrook-White :

$$\frac{1}{\sqrt{\lambda}} = -2 \log_{10} \left( \frac{k/D}{3.7} + \frac{2.51}{Re\sqrt{\lambda}} \right)$$

où k = rugosité absolue de la conduite (en m).

Pour acier galvanisé : k ≈ 0.15 mm
Pour cuivre : k ≈ 0.0015 mm (lisse)

**En pratique**, le coefficient λ est lu sur le **diagramme de Moody** (graphique Re vs λ tenant compte de k/D).

---

## II.3 Équation de continuité et conservation du débit

### **II.3.1 Principe de continuité**

Pour un fluide incompressible circulant dans une conduite :

$$Q = \text{constant}$$

Le débit volumique en tout point est constant :

$$Q = v_1 A_1 = v_2 A_2 = v_3 A_3 = \ldots$$

**Conséquence immédiate :** Une réduction de la section augmente la vitesse proportionnellement.

### **II.3.2 Application au dimensionnement**

La vitesse d'écoulement en fonction du débit et du diamètre :

$$v (m/s) = \frac{Q (L/min) \times 1000}{60 \times A (mm^2)} \times 10^{-6}$$

$$v (m/s) = \frac{Q (L/min)}{0.06 \times A (mm^2)} \times 10^{-6} = \frac{Q (L/min)}{6 \times 10^4 \times d^2 (mm)}$$

Pour une conduite de diamètre d et débit Q :

$$v = \frac{4Q}{\pi d^2} \quad \text{(en unités SI : Q en m³/s, d en m)}$$

**Ordres de grandeur des vitesses recommandées :**

| Type de circuit | Vitesse recommandée (m/s) | Justification |
|---|---|---|
| Aspiration pompe | 0.6 - 1.2 | Éviter cavitation (p trop basse) |
| Refoulement pompe | 3 - 5 | Économie de puissance, Re modéré |
| Retour vers réservoir | 1 - 2 | Faible perte de charge, bruit réduit |
| Lignes de commande | 0.3 - 1 | Contrôle précis, bruit minimal |

**Exemple applicatif :**

Pour Q_treuil = 60 L/min avec v_refoulement = 4 m/s :

$$4 = \frac{60}{6 \times 10^4 \times d^2} \quad \Rightarrow \quad d^2 = \frac{60}{4 \times 6 \times 10^4} = 0.000250 \quad \Rightarrow \quad d = 15.8 \text{ mm}$$

**Choix commercial :** DN 16 (diamètre nominal 16 mm, diamètre interne ≈ 12.7 mm selon ISO 4401)

---

## II.4 Équation de Darcy-Weisbach et pertes linéiques

### **II.4.1 Formule générale**

La perte de charge linéique le long d'une conduite est donnée par l'équation de Darcy-Weisbach :

$$\Delta p_{\text{lin}} \text{ (Pa)} = \lambda \times \frac{L}{D} \times \frac{\rho v^2}{2}$$

**Conversion en bar :**

$$\Delta p_{\text{lin}} \text{ (bar)} = \lambda \times \frac{L \text{ (m)}}{D \text{ (m)}} \times \frac{\rho \text{ (kg/m}^3) \times v^2 \text{ (m}^2/\text{s}^2)}{2 \times 10^5}$$

ou, en utilisant la viscosité cinématique :

$$\Delta p_{\text{lin}} \text{ (bar)} = 0.005 \times \lambda \times \frac{L}{D} \times \frac{\rho v^2}{2}$$

### **II.4.2 Exemple numérique : Circuit du treuil**

**Données :**
- Débit Q = 60 L/min = 0.001 m³/s
- Diamètre conduite refoulement D = 16 mm = 0.016 m
- Longueur L = 40 m (longueur équivalente tuyauterie moteur treuil)
- Viscosité ν = 46 × 10⁻⁶ m²/s
- Masse volumique ρ = 870 kg/m³
- Coefficient λ (à calculer)

**Étape 1 : Vitesse d'écoulement**

$$v = \frac{4 \times Q}{\pi D^2} = \frac{4 \times 0.001}{\pi \times (0.016)^2} = \frac{0.004}{0.000804} = 4.97 \text{ m/s}$$

**Étape 2 : Nombre de Reynolds**

$$Re = \frac{v D}{\nu} = \frac{4.97 \times 0.016}{46 \times 10^{-6}} = 1,728$$

**Étape 3 : Coefficient λ (régime laminaire)**

$$\lambda = \frac{64}{Re} = \frac{64}{1,728} = 0.0370$$

**Étape 4 : Perte de charge linéique**

$$\Delta p_{\text{lin}} = 0.005 \times 0.0370 \times \frac{40}{0.016} \times \frac{870 \times (4.97)^2}{2}$$

$$= 0.005 \times 0.0370 \times 2,500 \times \frac{870 \times 24.7}{2}$$

$$= 0.005 \times 0.0370 \times 2,500 \times 10,743 = 49.7 \text{ bar}$$

**Observations :**
- Cette perte est très élevée → le diamètre de 16 mm n'est pas adapté
- Refaire le calcul avec DN 22 (d ≈ 20 mm) réduirait v et donc Δp

---

## II.5 Pertes de charge singulières

### **II.5.1 Définition et formule générale**

Aux pertes linéiques réparties s'ajoutent des **pertes localisées** (singulières) causées par des accidents géométriques du circuit : coudes, raccords, changements de section, vannes, clapets, filtres.

Chacune est modélisée par un coefficient adimensionnel **ξ** :

$$\Delta p_{\text{sing}} \text{ (Pa)} = \xi \times \frac{\rho v^2}{2}$$

**En bar :**

$$\Delta p_{\text{sing}} \text{ (bar)} = \xi \times \frac{\rho v^2}{2 \times 10^5}$$

### **II.5.2 Coefficients ξ typiques en hydraulique navale**

| Singularité | Coefficient ξ | Commentaires |
|---|---|---|
| **Coude 90° (rayon standard r = D)** | 0.3 - 0.5 | Dépend de la forme du raccord |
| **Coude 90° (rayon faible r < 0.5D)** | 0.8 - 1.2 | Très turbulent, bruit |
| **Coude 45°** | 0.15 - 0.25 | Moins agressif |
| **Té de jonction (passage direct)** | 0.3 - 0.5 | |
| **Té de jonction (sortie latérale)** | 1.0 - 2.0 | Réduction de section |
| **Vanne d'arrêt (grand ouverte)** | 0.2 - 0.3 | Très peu de restriction |
| **Vanne d'arrêt (moitié ouverte)** | 5 - 10 | Restriction significative |
| **Clapet anti-retour (bon état)** | 1.0 - 1.5 | Élément critique du circuit |
| **Clapet anti-retour (usé, encrassé)** | 3 - 5 | Nécessite maintenance |
| **Filtre (état propre, porosité 10 μm)** | 0.5 - 1.0 | |
| **Filtre (encrassé, colmatage)** | 3 - 8 | Signal pour maintenance/remplacement |
| **Raccord rapide (connecté)** | 0.3 - 0.8 | Source fréquente de fuites |
| **Sortie de conduite (débouché libre)** | 1.0 | Perte complète d'énergie cinétique |
| **Entrée de conduite (prise dans réservoir)** | 0.5 - 1.0 | Dépend de la forme de la prise |

### **II.5.3 Longueur équivalente et méthode de calcul simplifiée**

Une approche simplifiée consiste à convertir chaque singularité en **longueur équivalente** L_eq :

$$L_{\text{eq}} = \frac{\xi}{\lambda} \times D$$

Puis à ajouter cette longueur fictive à la longueur réelle pour le calcul Darcy-Weisbach.

**Exemple :** Coude 90° (ξ = 0.4) dans une conduite D = 16 mm avec λ = 0.037

$$L_{\text{eq}} = \frac{0.4}{0.037} \times 0.016 = 0.173 \text{ m}$$

Donc, un coude équivaut à 17 cm de conduite droite.

### **II.5.4 Inventaire des singularités — Circuit réel du treuil**

Pour un circuit hydraulique complet (chapitre VI), on recense :

**Refoulement pompe → moteur treuil :**
- 2 coudes 90° : ξ = 2 × 0.4 = 0.8
- 3 raccords rapides : ξ = 3 × 0.5 = 1.5
- 1 filtre : ξ = 0.8
- 1 clapet anti-retour : ξ = 1.2
- **Total ξ = 4.3**

**Retour moteur → réservoir :**
- 1 clapet anti-retour : ξ = 1.2
- 1 raccord rapide : ξ = 0.5
- 1 filtre retour : ξ = 1.0
- **Total ξ = 2.7**

**Perte singulière totale (refoulement, v = 4.97 m/s) :**

$$\Delta p_{\text{sing}} = 4.3 \times \frac{870 \times (4.97)^2}{2 \times 10^5} = 4.3 \times \frac{21,453}{200,000} = 0.46 \text{ bar}$$

---

## II.6 Perte de charge totale et vérification du circuit

### **II.6.1 Formule complète**

La perte de charge totale dans une ligne hydraulique est la somme des pertes linéiques et singulières :

$$\Delta p_{\text{total}} = \Delta p_{\text{linéique}} + \Delta p_{\text{singulière}}$$

$$\Delta p_{\text{total}} (bar) = 0.005 \times \lambda \times \frac{L}{D} \times \frac{\rho v^2}{2} + \xi \times \frac{\rho v^2}{2 \times 10^5}$$

### **II.6.2 Critères de conformité**

Pour un circuit hydraulique naval en régime permanent, les pressions de perte de charge doivent rester dans des limites acceptables :

**Ligne refoulement pompe :**
- Perte admissible : Δp < 5 bar (max 8 bar en cas de surcharge temporaire)
- Chute de pression à la pompe : doit rester < 3 bar pour ne pas dégrader les performances

**Ligne retour vers réservoir :**
- Perte admissible : Δp < 2 bar
- Retour trop restreint peut causer cavitation et surpression au réservoir

**Lignes de commande (pilotage) :**
- Perte admissible : Δp < 1 bar
- Essentiel pour la réactivité des distributeurs

### **II.6.3 Vérification de la pression d'aspiration**

La pompe ne doit jamais "aspirer le vide". La pression à l'entrée de la pompe doit rester > 0.5 bar absolu (minimum 0.3 bar relatif).

**Condition :**

$$p_{\text{réservoir}} + \rho g h - \Delta p_{\text{aspiration}} \geq 0.5 \text{ bar (absolu)}$$

où h = hauteur verticale pompe au-dessus du réservoir (généralement h = 0 sur navire).

Pour un réservoir à pression atmosphérique (1.013 bar) :

$$1.013 - \Delta p_{\text{aspiration}} \geq 0.5 \quad \Rightarrow \quad \Delta p_{\text{aspiration}} \leq 0.513 \text{ bar}$$

→ **Limitation de la perte d'aspiration à ~0.3 bar max** pour rester confortable.

---

## II.7 Phénomènes transitoires critiques

### **II.7.1 Cavitation**

La cavitation se produit lorsque la pression locale du fluide chute en dessous de sa **pression de vapeur saturante**.

**Pression de vapeur de l'huile hydraulique HM46 :**

$$p_{\text{vap}} \approx 0.05 \text{ bar (absolu à 40°C)}$$

**Conditions favorisant la cavitation :**
- Aspiration pompe mal alimentée (perte d'aspiration excessive)
- Filtre encrassé bloquant le flux
- Réservoir trop bas par rapport à la pompe
- Température élevée (p_vap augmente avec T)

**Conséquences :**
- Perte de puissance (bulles réduisent la compressibilité)
- Bruit caractéristique "mitrailleuse"
- Érosion des surfaces des pompes et distributeurs
- Oxydation accélérée de l'huile

**Prévention :**
- Prise d'aspiration large et immergée au réservoir
- Filtre aspiration < 100 μm pour éviter surpression locale
- Entretien préventif du filtre aspiration

### **II.7.2 Coup de bélier**

Le coup de bélier est une **surpression transitoire** résultant de la fermeture brutale d'une vanne ou de l'arrêt d'un actionneur.

**Mécanisme :**

Lorsqu'un moteur hydraulique tourne à vitesse N et que l'on ferme brutalement le distributeur, l'énergie cinétique du fluide en mouvement se transforme en énergie de pression :

$$\Delta p_{\text{transitoire}} \sim \rho c \Delta v$$

où :
- **c** = célérité de l'onde de pression dans le fluide (≈ 1 400 m/s pour huile minérale)
- **Δv** = variation de vitesse d'écoulement

**Exemple chiffré :**

Moteur treuil à v = 5 m/s, arrêt brutal :

$$\Delta p_{\text{transitoire}} \sim 870 \times 1400 \times 5 = 6.09 \times 10^6 \text{ Pa} = 61 \text{ bar}$$

**Conséquences :**

Si le pic transitoire s'ajoute à la pression nominale de service (280 bar) :

$$p_{\text{max}} = 280 + 61 = 341 \text{ bar}$$

Ce dépassement peut endommager les composants (joints, pompe, distributeur) non dimensionnés pour cette surcharge.

**Solutions d'amortissement :**

1. **Limiteur de pression** taré à p_max (290 bar pour marge) → dérive l'excédent
2. **Accumulateur hydropneumatique** → absorbe l'énergie transitoire
3. **Amortisseur (valve d'amortissement)** → ralentit la fermeture du distributeur

### **II.7.3 Coupure de charge (load shedding)**

Lorsqu'un actionneur tourne librement et que le distributeur est brutalement fermé (ou que l'actionneur s'arrête), il peut se produire une **dépression** :

$$p_{\text{min}} = p_{\text{nominal}} - \Delta p_{\text{transitoire}}$$

Cas limite : p_min devient négative → cavitation.

**Prévention :**

Clapets anti-cavitation (pilot-operated check valves) placés en sortie des actionneurs → garantissent une pression minimale (0.3-0.5 bar au-dessus du retour).

---

## II.8 Bilan énergétique et rendement hydraulique

### **II.8.1 Équation d'énergie — Forme générale**

Pour un fluide en mouvement dans un circuit hydraulique, l'équation de Bernoulli généralisée s'écrit :

$$\frac{p_1}{\rho g} + \frac{v_1^2}{2g} + z_1 + H_{\text{pompe}} = \frac{p_2}{\rho g} + \frac{v_2^2}{2g} + z_2 + \Delta H_{\text{total}}$$

où :
- **H_pompe** = charge apportée par la pompe (J/kg)
- **ΔH_total** = pertes de charge totales (J/kg)
- **z** = hauteur géométrique (m)

**Conversion en puissance :**

$$P = \rho g Q H = p Q \times 10^5 / (60 \times 10^5) = p Q / 600 \quad \text{(kW, p en bar, Q en L/min)}$$

### **II.8.2 Rendement global du circuit**

$$\eta_{\text{global}} = \frac{P_{\text{utile}}}{P_{\text{absorbée}}} = \frac{\text{Puissance restitue à l'actionneur}}{\text{Puissance prélevée sur moteur principal}}$$

**Décomposition en rendements élémentaires :**

$$\eta_{\text{global}} = \eta_{\text{pompe}} \times \eta_{\text{distributeur}} \times \eta_{\text{tuyauterie}} \times \eta_{\text{actionneur}}$$

**Valeurs typiques :**

- **η_pompe** (pistons axiaux) = 0.94 (rendement volumétrique + mécanique)
- **η_distributeur** (4/3 proportionnel) = 0.98
- **η_tuyauterie** (pertes linéiques/singulières) = 0.85-0.92
- **η_actionneur** (moteur/vérin) = 0.96-0.98

$$\eta_{\text{global}} \approx 0.94 \times 0.98 \times 0.88 \times 0.97 = 0.78 \text{ (78%)}$$

### **II.8.3 Puissance dissipée en chaleur**

La puissance perdue sous forme de chaleur est :

$$P_{\text{thermique}} = P_{\text{absorbée}} \times (1 - \eta_{\text{global}})$$

Pour P_absorbée = 300 kW et η_global = 0.78 :

$$P_{\text{thermique}} = 300 \times (1 - 0.78) = 66 \text{ kW}$$

Cette puissance thermique doit être dissipée par le **réservoir et l'échangeur thermique** pour maintenir la température stable.

---

## II.9 Critères de dimensionnement des conduites

### **II.9.1 Sélection du diamètre**

Le dimensionnement des conduites hydrauliques repose sur le **compromis** entre :
- **Petit diamètre** → perte de charge réduite, masse réduite, coût réduit
- **Grand diamètre** → perte de charge accrue, masse augmentée, coût augmenté

La pratique industrielle retient des **vitesses d'écoulement** comme critère :

| Type de ligne | Vitesse recommandée | Justification |
|---|---|---|
| Aspiration | 0.6 - 1.2 m/s | Minimiser cavitation |
| Refoulement haute pression | 3 - 5 m/s | Standard industriel |
| Retour | 1 - 2 m/s | Bruit réduit, économie |
| Pilotage | 0.3 - 1 m/s | Précision, sécurité |

### **II.9.2 Tableau de sélection rapide**

Pour un circuit de débit Q (L/min), le diamètre nominal DN (mm) peut être approché par :

| Débit Q (L/min) | Diamètre refoulement (DN, mm) | Diamètre retour (DN, mm) |
|---|---|---|
| 10 | 10 | 16 |
| 20 | 12 | 20 |
| 40 | 16 | 25 |
| 60 | 20 | 32 |
| 100 | 25 | 40 |
| 150 | 32 | 50 |

---

## SOURCES CHAPITRE II

**Normes ISO de référence :**
- ISO 4413:2010 — *Transmissions hydrauliques — Règles générales et sécurité*
- ISO 4414:2010 — *Transmissions pneumatiques — Règles générales et sécurité*
- ISO 11158:2012 — *Huiles hydrauliques — Catégorie ISO VG 32 à 100 — Spécifications*
- ISO 3448:1992 — *Huiles industrielles — Classification selon la viscosité*
- ISO 2909:2002 — *Huiles minérales — Détermination de l'indice de viscosité*

**Références académiques :**
- Darcy, H. & Weisbach, J. (1858) — *Researches Experimental Upon the Flow of Water*. Academy of Sciences, Paris.
- Colebrook, C.F. (1939) — "Turbulent flow in pipes, with particular reference to the transition region between smooth and rough pipe." Journal of the Institution of Civil Engineers, 11(4), 133-156.
- Idel'cik, I.E. (1986) — *Mémento des pertes de charge* (2e éd.). Eyrolles, Paris.

**Traités spécialisés en hydraulique :**
- Backé, W. & Murrenhoff, H. (2008) — *Fluid Power Engineering*. RWTH Aachen University.
- Esposito, A. (2003) — *Fluid Power with Applications* (5e éd.). Prentice Hall. ISBN: 0130615250
- Poulit-Huet, J. & Huet, J.-P. (1998) — *Hydraulique Industrielle*. Dunod, Paris.

**Manuels de conception (constructeurs) :**
- Rexroth Bosch — *Fluid Power Systems Design Handbook*. Brochure RE 50016
- Parker — *Hydraulic Fluid Power Systems Handbook*. Publication GMM-001
- Eaton — *Hydraulic Pump Design and Performance*. Manual EATON-7620-F

**Articles scientifiques :**
- Moody, L.F. (1944) — "Friction factors for pipe flow." Transactions ASME, 66(8), 671-684.

---

**Fin du Chapitre II**