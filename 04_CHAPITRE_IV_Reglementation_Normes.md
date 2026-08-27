# CHAPITRE IV — RÉGLEMENTATION, NORMES ET CONFORMITÉ MARITIME

## IV.1 Cadre réglementaire international

### **IV.1.1 Convention SOLAS — Safety Of Life At Sea**

La **Convention Internationale pour la Sauvegarde de la Vie en Mer (SOLAS)** est le traité maritime le plus important en matière de sécurité. Elle s'applique à tous les navires commerciaux de plus de 500 GT (tonnes brutes).

**Historique :**
- SOLAS 1974 (entrée en vigueur 1980)
- Amendements réguliers tous les 2-3 ans
- Version actuelle : SOLAS 2024 (au 1er janvier 2026)
- Adoptée par 167 États, dont la France (via l'Union Européenne)

**Pertinence pour le chalutier 18 m :**

Le chalutier 18 m ≈ 80-100 GT → **Navire de pêche commercial → SOLAS s'applique partiellement**.

En particulier :
- **Chapitre V (Sécurité de la navigation)** : équipement de navigation
- **Chapitre II-1 (Construction - Protections contre l'incendie)** : systèmes de sécurité
- **Chapitre II-2 (Système de sécurité, incendie et détection)** : équipements d'extinction
- **Chapitre VI (Opérations de chargement-déchargement)** : stabilité et charge
- **Chapitre VIII (Délivrance des certificats)** : inspections périodiques

### **IV.1.2 Organisation Maritime Internationale (IMO)**

L'IMO est l'agence spécialisée des Nations Unies pour la réglementation du transport maritime.

**Principaux résolutions applicables aux navires de pêche :**

| Résolution | Titre | Pertinence |
|---|---|---|
| IMO A.481(12) | Code of Safe Practice for Ships with Low Freeboard | Petits navires, stabilité |
| IMO A.749(18) | Code of Safety for Fishermen and Fishing Vessels | **Chalutiers directement visés** |
| IMO Resolution MSC.97(73) | Performance Standards for Ship-borne Data Recorders | Systèmes numériques |
| IMO MEPC.201(62) | 2012 Guidelines for the Implementation of MARPOL Annex I | Protection environnementale |

### **IV.1.3 Conventions ILO — International Labour Organization**

L'ILO s'intéresse aux conditions de travail à bord des chalutiers.

**Convention C188 (2007) — Work in Fishing Convention :**
- Conditions de travail et de sécurité des pêcheurs
- Stabilité et intégrité du navire
- Équipement de sécurité obligatoire
- Maintenance régulière des systèmes hydrauliques

---

## IV.2 Normes ISO applicables

### **IV.2.1 Normes de transmission hydraulique**

| Norme ISO | Titre | Domaine |
|---|---|---|
| **ISO 4413:2010** | *Transmissions hydrauliques — Règles générales et sécurité* | **Fondamentale pour tous les calculs** |
| **ISO 4414:2010** | *Transmissions pneumatiques — Règles générales et sécurité* | Circuits air comprimé |
| **ISO 1219-1:2012** | *Symboles graphiques et schémas — Éléments hydrauliques* | Schémas et documentation |
| **ISO 1219-2:2012** | *Symboles graphiques — Systèmes hydrauliques complexes* | Schémas avancés |
| **ISO 6162:2015** | *Interfaçage hydraulique — Tailles et caractéristiques des raccords* | Compatibilité mécanique |
| **ISO 11158:2012** | *Huiles hydrauliques — Catégories ISO VG 32 à 100* | Spécifications du fluide |
| **ISO 3448:1992** | *Huiles industrielles — Classification selon la viscosité* | Grades de viscosité |
| **ISO 2909:2002** | *Huiles minérales — Détermination de l'indice de viscosité* | Propriétés thermiques |

### **IV.2.2 Normes de sécurité des systèmes**

| Norme | Titre | Application |
|---|---|---|
| **ISO 13849-1:2015** | *Sécurité des machines — Parties système de commande relatives à la sécurité — Conception* | Systèmes de contrôle |
| **ISO 12922:2019** | *Lubrifiants pour moteurs de véhicules routiers — Spécifications de classification* | Compatibilité fluides |

---

## IV.3 Normes européennes (EN) — Directives CE

### **IV.3.1 EN 13000:2018 — Grues de manutention**

Cette norme s'applique à la **grue de pont** du chalutier.

**Titre complet :**
> *EN 13000:2018 — Grues de manutention — Grues mobiles de chantier — Règles de sécurité*

**Champs d'application :**
1. Grues à charger depuis le sol ou depuis un navire
2. Capacité nominale : 1 à 300 tonnes
3. Stabilité et contrôle des charges

**Exigences clés pour la grue navale :**

#### **A. Calcul du moment de renversement (stabilité)**

Le moment résistant du navire doit être ≥ 1.25 × moment d'application de la charge :

$$M_{\text{résistant}} \geq 1.25 \times P \times d$$

où :
- P = charge maximale (tonnes)
- d = distance horizontale du centre de gravité de la charge à l'axe vertical du navire (m)

#### **B. Système de limitation du moment (LMI)**

Obligatoire pour les grues navales de capacité > 5 tonnes.

**Fonctionnement :**
- Mesure continue du moment appliqué
- Coupure automatique du flux hydraulique si M > M_max
- Redondance de sécurité (deux capteurs indépendants)

**Formule de sécurité (EN 13000 § 7.7.2) :**

$$M_{\text{limité}} = 0.85 \times M_{\text{stabilité du navire}}$$

#### **C. Inspections et maintenances**

Fréquence **minimale** :
- Inspection visuelle : tous les **3 mois** ou 100 heures de fonctionnement
- Inspection approfondie : **annuellement**
- Certification : renouvellement tous les **2 ans** (DNV GL, ABS, BV)

### **IV.3.2 EN 1127-1:2019 — Atmosphères explosives**

Bien que le chalutier ne soit pas une zone ATEX, cette norme s'applique aux compresseurs et réservoirs pneumatiques si risque d'accumulation de poussière.

---

## IV.4 Normes de classification navale

### **IV.4.1 Sociétés de classification (Classification Societies)**

Pour opérer légalement, un navire commercial doit être **classé** par une société de classification reconnue par l'IMO. Les trois principales sont :

| Société | Acronyme | Spécialités |
|---|---|---|
| Det Norske Veritas — Germanischer Lloyd | **DNV GL** | Navires de pêche, off-shore |
| Bureau Veritas | **BV** | Navires commerciaux, yachts |
| American Bureau of Shipping | **ABS** | Pavillon US, standard international |

### **IV.4.2 Règles DNV GL pour navires de pêche**

**Publication de référence :**
> *DNV GL — Rules for Classification of Ships — Part 3, Chapter 9 (Hydraulic and Pneumatic Systems)*

**Exigences essentielles pour le chalutier :**

#### **A. Classification des circuits hydrauliques**

| Classification | Pression (bar) | Usage | Conformité |
|---|---|---|---|
| **Class A (Protection)** | < 35 | Circuits auxiliaires | Inspection annuelle |
| **Class B (Puissance)** | 35-210 | Timonerie, grue | Inspection tous les 2 ans |
| **Class C (Haute pression)** | > 210 | Treuil, moteurs principaux | Certificat tous les 5 ans |

→ **Le treuil du chalutier (280 bar) est Class C**

#### **B. Exigences de certification**

**Certificat de classe initial (ICS) :**
- Inspection d'un vérificateur DNV GL en cale sèche
- Tests de pression sur tous les circuits
- Vérification des calculs de dimensionnement
- Documentation complète du système

**Certificat périodique (ACS) :**
- Renouvellement tous les **5 ans**
- Inspection partielle en cale sèche : tous les **5 ans**
- Inspection intermédiaire : tous les **2.5 ans** en flot

#### **C. Documentation requise par DNV GL**

Pour chaque circuit hydraulique, le navire doit posséder :

1. **Plan général du circuit** (schéma P&ID — ISO 1219)
2. **Tableau de données techniques** :
   - Pression de service (bar)
   - Débit nominal (L/min)
   - Puissance (kW)
   - Cylindrées des pompes/moteurs (cm³/tr)
   - Matériaux des tuyauteries

3. **Manuels d'exploitation** :
   - Procédures de démarrage/arrêt
   - Limites opérationnelles
   - Procédures d'urgence (perte hydraulique)
   - Maintenance préventive

4. **Fiches d'entretien** :
   - Log book (journal de bord hydraulique)
   - Changement d'huile (tous les **2 000-3 000 heures** d'opération)
   - Remplacement des filtres (tous les **500-1 000 heures**)
   - Vérification des joints (trimestriellement)

---

## IV.5 Réglementations nationales — France

### **IV.5.1 Ministère des Affaires Maritimes**

En France, les navires de pêche sont sous la juridiction du **Ministère des Affaires Maritimes** (anciennement Ministère de la Mer).

**Textes applicables :**

| Texte | Domaine |
|---|---|
| **Décret n° 2017-1307** | Conditions d'armement des navires de pêche |
| **Décret n° 2020-1089** | Sécurité à bord des navires de pêche |
| **Arrêté du 23 novembre 1987** | Conditions de sécurité à bord des navires de pêche |

### **IV.5.2 Bureau Veritas — Organisme agréé**

En France, **Bureau Veritas (BV)** est l'organisme agréé pour certifier les navires de pêche.

**Processus de certification :**

1. **Demande d'inscription** : le propriétaire demande le classement auprès de BV
2. **Inspection initiale** : en cale sèche ou quai
3. **Certificat de classe** : valide 5 ans
4. **Inspections périodiques** :
   - Visite intermédiaire (2.5 ans)
   - Visite de renouvellement (5 ans)

### **IV.5.3 Contrôle des ports français**

Tous les ports français (Lorient, Boulogne, Concarneau, etc.) disposent d'un **Capitainerie du port** chargée du contrôle :
- Certificat de classe valide
- Équipements de sécurité en bon état
- Maintenance conforme aux normes
- Log books à jour

**Pénalités en cas de non-conformité :**
- Amende : 1 500 € à 150 000 € selon la gravité
- Interdiction de navigation
- Immobilisation du navire (jusqu'à conformité)

---

## IV.6 Critères de dimensionnement basés sur la réglementation

### **IV.6.1 Synthèse des contraintes**

Le dimensionnement des systèmes hydrauliques du chalutier 18 m doit respecter **simultanément** :

| Source | Contrainte | Traduction technique |
|---|---|---|
| **SOLAS** | Sécurité en cas de perte hydraulique | Doublage des circuits critiques, clapets anti-retour |
| **IMO A.749** | Stabilité et timonerie fiable | Timonerie redondante (vérins secours), réactivité < 5 sec |
| **EN 13000** | Grue sûre (LMI actif) | Limiteur de moment obligatoire, test annuel |
| **DNV GL** | Documentation et traçabilité | Logs détaillés, certificats d'inspection |
| **ISO 4413** | Conception hydraulique sûre | Choix composants, calculs pertes de charge |
| **ISO 11158** | Qualité du fluide | Classe ISO 18/16/13, changement tous les 2 000 h |

### **IV.6.2 Marge de sécurité — Coefficients k**

Les normes imposent des **marges de sécurité** sur les composants :

| Composant | Coefficient k | Application |
|---|---|---|
| **Pompe** | 1.15 | P_pompe = 1.15 × P_utile |
| **Moteur hydraulique** | 1.1 | C_moteur ≥ 1.1 × C_requis |
| **Vérin** | 1.2 | F_vérin ≥ 1.2 × F_requise |
| **Tuyauterie** | 1.3 | Δp_total_réelle ≤ Δp_calculée / 1.3 |
| **Limiteur de pression** | 1.1 | Tarage = 1.1 × p_nominale |
| **Accumulateur** | 1.25 | V_accum ≥ 1.25 × V_théorique |

**Justification :** Ces marges compensent :
- Les tolérances de fabrication des composants
- L'usure progressive en service
- Les pics transitoires non modélisés
- L'évolution des conditions opérationnelles (température, altitude)

### **IV.6.3 Facteur de charge simultanée**

Rarement tous les circuits ne fonctionnent simultanément à pleine charge. La réglementation définit des **facteurs de charge simultanée** :

| Scénario | Facteur |
|---|---|
| Treuil seul | 100% |
| Treuil + Timonerie (manœuvre) | 90% |
| Timonerie seule | 50% |
| Grue seule | 60% |
| Auxiliaires (lubrification, refroidissement) | 10% |

**Puissance moteur principal :**

$$P_{\text{moteur}} = \max\left(\sum P_i \times k_i\right) + 15\% \text{ (marge global)}$$

---

## IV.7 Vérifications réglementaires — Checklist pour le chalutier 18 m

### **IV.7.1 Vérifications avant mise en service**

```
□ SOLAS & IMO :
  ✓ Navire de pêche < 500 GT → SOLAS s'applique partiellement
  ✓ Timonerie hydraulique : temps de réaction < 5 sec (SOLAS Ch. V)
  ✓ Système de sauvetage intact (grue + moyens)
  ✓ Documentation complète à bord

□ EN 13000 (Grue) :
  ✓ Limiteur de moment (LMI) opérationnel
  ✓ Certification de stabilité (moment résistant mesuré)
  ✓ Inspection approfondie grue réalisée
  ✓ Manuel d'opération fourni aux marins

□ DNV GL (Classification) :
  ✓ Certificat de classe initial (ICS) obtenu
  ✓ Tous circuits classe C (280 bar treuil) testés à 1.5 × p_nominale
  ✓ Calculs de dimensionnement vérifiés par inspecteur
  ✓ Log books et fiches d'entretien prêts

□ ISO 4413 (Hydraulique) :
  ✓ Schémas P&ID conformes ISO 1219
  ✓ Pressions de service affichées sur chaque circuit
  ✓ Filtration conforme ISO 18/16/13
  ✓ Fluide HM46 (ISO 11158) chargé au réservoir

□ Maintenance :
  ✓ Plan de maintenance préventive établi
  ✓ Traçabilité des heures moteur mise en place
  ✓ Responsable de maintenance désigné
  ✓ Pièces de rechange critiques en stock
```

### **IV.7.2 Inspections périodiques (année 1, 2, 3, ...)**

**Trimestres 1 & 3 :**
- Vérification visuelle des fuites (jointures, flexibles)
- Test de pression résiduelle (s'il n'y a pas de fuite, les accumulateurs maintiennent la pression)
- Log book mis à jour

**Semestriel (tous les 6 mois) :**
- Remplacement des filtres refoulement et retour
- Analyse de l'huile (laboratoire) : viscosité, TAN (acidité), teneur en eau
- Nettoyage du réservoir (si nécessaire)

**Annuel (tous les 12 mois) :**
- Inspection approfondie par mécanicien qualifié
- Test en charge de tous les circuits
- Certification par DNV GL (visite annuelle)
- Remplacement partiel de l'huile (si TAN > 2.0 mg KOH/g)

**Tous les 2 ans :**
- Remplacement total de l'huile (2 000-3 000 heures opération)
- Inspection des joints internes des moteurs hydrauliques
- Certification de classe (BV ou DNV GL)

---

## SOURCES CHAPITRE IV

**Instruments internationaux :**
- SOLAS 1974 (consolidated edition 2024) — International Convention for the Safety of Life at Sea
- IMO Resolution A.749(18) — Code of Safety for Fishermen and Fishing Vessels (1991)
- ILO Convention C188 — Work in Fishing Convention (2007, entrée en vigueur 2017)

**Normes ISO :**
- ISO 4413:2010 — *Transmissions hydrauliques — Sécurité*
- ISO 11158:2012 — *Huiles hydrauliques — Spécifications*
- ISO 13849-1:2015 — *Sécurité des machines — Parties système de commande*

**Normes européennes :**
- EN 13000:2018 — *Grues de manutention — Grues mobiles de chantier — Sécurité*
- EN 1127-1:2019 — *Atmosphères explosives — Prévention et protection*

**Règles de classification navale :**
- DNV GL — *Rules for Classification of Ships — Part 3, Chapter 9 (Hydraulic and Pneumatic Systems)* (édition 2024-01)
- ABS — *Rules for Building and Classing Steel Vessels* (édition 2023)
- Bureau Veritas — *Rules for the Classification of Steel Ships* (édition 2024)

**Réglementation française :**
- Décret n° 2017-1307 du 29 septembre 2017 — Conditions d'armement des navires de pêche
- Décret n° 2020-1089 du 25 août 2020 — Sécurité à bord des navires de pêche
- Arrêté du 23 novembre 1987 — Conditions de sécurité à bord des navires de pêche
- Ministère de la Mer — Guide de conformité SOLAS pour navires < 500 GT

**Documentation opérationnelle :**
- IMO Res. A.900(21) — Guidelines for the Training and Certification of Officers Responsible for Cargo Operations on Ship and Tankers (certification des officiers d'exploitation)

---

**Fin du Chapitre IV — Fin de la Partie I (États de l'art)**
