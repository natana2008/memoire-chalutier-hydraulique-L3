# MÉMOIRE DE FIN D'ÉTUDES

## LICENCE 3 — GÉNIE MÉCANIQUE ET INDUSTRIEL

---

## **ÉTUDE ET DIMENSIONNEMENT DES SYSTÈMES HYDRAULIQUES ET PNEUMATIQUES D'UN CHALUTIER ARRIÈRE DE 18 MÈTRES**

---

**Présenté par :** ANDRIANIRINA Natana Julien

**Soutenu le :** ________________________

**Directeur de mémoire :** [Nom du Directeur]

**Examinateurs :**
- [Nom Examinateur 1]
- [Nom Examinateur 2]

**PROMOTION 2026**

---

## REMERCIEMENTS

Je tiens à exprimer ma sincère reconnaissance à l'ensemble du corps enseignant du département Génie Mécanique & Industriel pour la qualité de la formation dispensée tout au long de cette Licence 3, et pour les bases méthodologiques rigoureuses qui ont permis la réalisation de ce mémoire.

Mes remerciements vont également aux membres du jury pour le temps consacré à l'examen de ce travail, à mon directeur de mémoire pour son encadrement scientifique, aux ingénieurs des chantiers navals pour leur expertise technique, et à toute personne ayant contribué, de près ou de loin, à la relecture et à l'amélioration de ce manuscrit.

---

## RÉSUMÉ

Ce mémoire présente une **étude complète de dimensionnement des systèmes hydrauliques et pneumatiques d'un chalutier arrière de 18 mètres**, navire type de la flottille industrielle française. L'étude porte sur quatre systèmes critiques : le **treuil de pêche** (système de puissance principale), la **timonerie** (gouvernail assisté hydrauliquement), la **grue de pont** (manutention et sauvetage), et le **circuit d'air comprimé** (démarrage moteur et auxiliaires).

### **Démarche scientifique appliquée (IMRAD) :**

1. **Introduction** : Problématique industrielle et contexte réglementaire maritime
2. **Méthodologie** : Approche progressive (effort opérationnel → pression/débit → composants → vérifications)
3. **Résultats** : Dimensionnement détaillé de chaque système avec calculs numériques
4. **Discussion** : Analyse comparative des solutions techniques et conformité réglementaire
5. **Conclusion** : Synthèse et perspectives d'optimisation énergétique

### **Apports principaux :**

- **Formulations mathématiques complètes** basées sur les équations de continuité (Bernoulli, Darcy-Weisbach, Reynolds)
- **Calculs numériques détaillés** appliqués à un cas réel (chalutier 18 m, capacité de pêche 40 tonnes/jour)
- **Sélection de composants commerciaux réels** avec marges de sécurité conformes aux normes
- **Vérifications réglementaires** selon SOLAS (Convention Internationale pour la Sauvegarde de la Vie en Mer) et EN 13000 (grues de manutention)
- **Bilan énergétique global** permettant le dimensionnement du moteur principal (≈ 500-600 kW)
- **Sources académiques et normes ISO** intégrales pour chaque calcul

### **Spécificités du travail :**

Ce mémoire combine rigueur théorique et applicabilité industrielle : chaque formule est démontrée, chaque calcul est justifié, et chaque choix technique est traçable. L'étude montre comment les contraintes réelles d'exploitation (amplitude des marées, conditions météorologiques, sécurité de l'équipage) déterminent les caractéristiques des composants, inversant ainsi la logique naïve d'une simple « application de formule ».

**Mots-clés :** hydraulique navale | treuil de pêche | timonerie | grue marine | pneumatique | dimensionnement | puissance moteur | normes SOLAS | pertes de charge | chalutier arrière

---

## TABLE DES MATIÈRES

### **PARTIE I — ÉTATS DE L'ART**

1. **Chapitre I** — Principes fondamentaux de la transmission hydraulique et pneumatique
2. **Chapitre II** — Mécanique des fluides et équations des pertes de charge
3. **Chapitre III** — Équipements hydrauliques et pneumatiques des navires de pêche
4. **Chapitre IV** — Réglementation, normes et conformité maritime

### **PARTIE II — MÉTHODOLOGIE, RÉSULTATS ET DISCUSSIONS**

5. **Chapitre V** — Présentation du projet et spécifications du chalutier
6. **Chapitre VI** — Dimensionnement du système hydraulique du treuil de pêche
7. **Chapitre VII** — Dimensionnement de la timonerie et de la grue de pont
8. **Chapitre VIII** — Dimensionnement du circuit pneumatique
9. **Chapitre IX** — Bilan énergétique global et puissance moteur principal
10. **Chapitre X** — Discussions, comparaisons et perspectives

### **ÉLÉMENTS FINAUX**

- Conclusion générale
- Annexes (tableaux de données, fiches techniques, schémas)
- Bibliographie complète
- Webographie et normes

---

## LISTE DES ACRONYMES, ABRÉVIATIONS ET NOTATIONS

### **Grandeurs hydrauliques**

| Notation | Signification | Unité |
|----------|---------------|-------|
| **p** | Pression de service | bar |
| **Q** | Débit volumique | L/min |
| **P_utile** | Puissance hydraulique utile | kW |
| **P_absorbée** | Puissance absorbée par la pompe | kW |
| **V_g** | Cylindrée du moteur/pompe | cm³/tr |
| **C_moteur** | Couple en sortie de moteur hydraulique | N·m |
| **C_tambour** | Couple sur le tambour du treuil | N·m |
| **F_vérin** | Force en sortie de vérin | N |
| **D** | Alésage (vérin) / diamètre (conduite) | mm |
| **η_v** | Rendement volumétrique | — |
| **η_m** | Rendement mécanique | — |

### **Grandeurs pneumatiques**

| Notation | Signification | Unité |
|----------|---------------|-------|
| **p_air** | Pression d'air comprimé | bar |
| **Q_air** | Débit d'air | L/min |
| **V_air** | Volume d'air consommé | L (CNTP) |
| **V_cyl** | Cylindrée du compresseur | cm³/tr |

### **Mécanique des fluides**

| Notation | Signification | Unité |
|----------|---------------|-------|
| **ρ** | Masse volumique du fluide | kg/m³ |
| **μ** | Viscosité dynamique | Pa·s |
| **ν** | Viscosité cinématique | m²/s |
| **v** | Vitesse d'écoulement | m/s |
| **Re** | Nombre de Reynolds | — |
| **λ** | Coefficient de perte de charge linéaire | — |
| **Δp_lin** | Perte de charge linéaire | bar |
| **Δp_sing** | Perte de charge singulière | bar |
| **ξ** | Coefficient de perte singulière | — |

### **Efforts et géométrie du navire**

| Notation | Signification | Unité |
|----------|---------------|-------|
| **T** | Effort de traction du chalut | N (ou tonnes-force) |
| **C_r** | Couple résistant du safran | N·m |
| **L_bras** | Bras de levier du vérin | m |
| **M** | Moment de renversement (grue) | N·m |
| **α** | Angle d'inclinaison du vérin | ° |
| **LOA** | Longueur hors tout | m |
| **r_tambour** | Rayon du tambour du treuil | m |

### **Facteurs et ratios**

| Notation | Signification | Unité |
|----------|---------------|-------|
| **i** | Rapport de réduction (réducteur) | — |
| **k** | Facteur de charge ou marge de sécurité | — |
| **LMI** | Limiteur de moment (grue) | — |

### **Normes et standards**

| Acronyme | Signification |
|----------|---------------|
| **ISO** | International Organization for Standardization |
| **EN** | Norme européenne (European Norm) |
| **SOLAS** | Safety Of Life At Sea (Convention Internationale) |
| **IMO** | International Maritime Organization |
| **IACS** | International Association of Classification Societies |
| **DNV GL** | Det Norske Veritas — Germanischer Lloyd (Société de classification) |
| **ABS** | American Bureau of Shipping |
| **BV** | Bureau Veritas |
| **GL** | Germanischer Lloyd |
| **FRL** | Filtre-Régulateur-Lubrificateur (pneumatique) |

---

**Fin des pages préliminaires — Début de la Partie I**
