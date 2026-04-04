
# 📘 TP5 — Introduction à JavaScript : Évènements

> **Master SDIA — Technologies du Web & Web Sémantique**  
> L'École Normale Supérieure de l'Enseignement Technique de Mohammedia  
> 👤 SALMA BALMIR

---

## 📋 Description

Ce TP introduit la **gestion des évènements en JavaScript** à travers quatre exercices progressifs : de la permutation de champs texte jusqu'à une calculatrice scientifique complète avec CSS Grid.

---

## 🗂️ Structure du projet

```
TP5/
│
├── exercice1.html       # Permutation de deux champs texte
├── exercice2.html       # Calculatrice simple (4 opérations)
├── exercice3.html       # Calculateur IMC
├── exercice4.html       # Calculatrice scientifique avancée
└── README.md
```

---

## 🧪 Exercices

### Exercice 1 — Permutation [`exercice1.html`](./exercice1.html)

**Objectif :** Un formulaire avec deux zones de texte et un bouton **Permuter**. Au clic, le contenu des deux champs s'échange.

**Concepts clés :**
- Manipulation du DOM (`.value`)
- Variable temporaire pour la permutation
- Gestion de l'évènement `onclick`


---

### Exercice 2 — Calculatrice Simple [`exercice2.html`](./exercice2.html)

**Objectif :** Une calculatrice effectuant les **4 opérations arithmétiques** de base.

**Concepts clés :**
- `parseFloat()` pour la conversion des entrées
- Gestion de plusieurs boutons avec `onclick`
- Affichage dynamique du résultat
- Gestion de la division par zéro


---

### Exercice 3 — Calculateur IMC [`exercice3.html`](./exercice3.html)

**Objectif :** Calculer et interpréter l'**Indice de Masse Corporelle** selon les normes OMS.

**Formule :**

$$IMC = \frac{Poids\ (kg)}{Taille^2\ (m)}$$

**Interprétation OMS :**

| IMC | Interprétation |
|-----|----------------|
| < 18,5 | Insuffisance pondérale (maigreur) |
| 18,5 – 25 | Corpulence normale |
| 25 – 30 | Surpoids |
| 30 – 35 | Obésité modérée |
| 35 – 40 | Obésité sévère |
| > 40 | Obésité morbide ou massive |

**Concepts clés :**
- Calcul mathématique (`Math.pow`)
- Structures conditionnelles `if / else if`
- Retour d'un message contextuel dynamique

---

### Exercice 4 — Calculatrice Scientifique [`exercice4.html`](./exercice4.html)

**Objectif :** Une calculatrice scientifique complète en **JavaScript pur** avec mise en page **CSS Grid**.

**Fonctions disponibles :**

| Touche | Fonction |
|--------|----------|
| `sin` `cos` `tan` | Fonctions trigonométriques |
| `Inv` | Fonctions inverses (asin, acos, atan) |
| `ln` `log` | Logarithmes naturel et décimal |
| `π` `e` | Constantes mathématiques |
| `x²` `x^` | Puissances |
| `EXP` | Notation scientifique |
| `√` | Racine carrée |
| `%` | Modulo / pourcentage |
| `CE` | Effacer l'écran |
| `( )` | Parenthèses |

**Concepts clés :**
- CSS Grid pour la grille de boutons
- Objet `Math` de JavaScript (`Math.sin`, `Math.log`, `Math.PI`…)
- Évaluation d'expressions mathématiques
- Gestion de l'affichage en temps réel

---

## 🛠️ Technologies utilisées

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)

- **HTML5** — Structure et formulaires
- **CSS3 / Grid** — Mise en page (notamment Exercice 4)
- **JavaScript** — Logique, évènements, calculs

---

## 🚀 Utilisation

Aucune installation requise. Cloner le dépôt et ouvrir directement les fichiers dans un navigateur :

```bash
git clone https://github.com/Salmabalmir55/Technologies-Web-et-Web-S-mantique.git
cd Technologies-Web-et-Web-S-mantique/TP5

# Ouvrir un exercice (exemple)
open exercice1.html        # macOS
xdg-open exercice1.html    # Linux
# ou double-cliquer sur le fichier sous Windows
```

---

## 📚 Notions JavaScript abordées

- Sélection d'éléments DOM — `getElementById`, `querySelector`
- Évènements — `onclick`, `addEventListener`
- Manipulation des valeurs — `.value`, `parseFloat`, `parseInt`
- Conditions — `if / else if / else`
- Objet `Math` — `Math.pow`, `Math.sqrt`, `Math.sin`, `Math.PI`…
- CSS Grid Layout

---

## 👩‍🎓 Informations académiques

| Champ | Détail |
|-------|--------|
| **Établissement** | ENSET Mohammedia |
| **Formation** | Master SDIA |
| **Module** | Technologies du Web & Web Sémantique |
| **TP** | TP5 — Évènements JavaScript |
| **Étudiante** | Salma Balmir |

---

*Réalisé dans le cadre du Master SDIA — ENSET Mohammedia* 🎓
