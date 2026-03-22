# 🧪 TP N°4 — Introduction à JavaScript

> **Master SDIA** · Technologies du Web & Web Sémantique  
> École Normale Supérieure de l'Enseignement Technique de Mohammedia

---

## 📋 Description

Ce dépôt contient les solutions aux exercices du **TP n°4** portant sur les fondamentaux du langage **JavaScript** : types simples, déclarations de variables, instructions de contrôle et itérations.

---

## 🎯 Objectifs pédagogiques

- Maîtriser les types primitifs et la déclaration de variables en JavaScript
- Implémenter des fonctions avec logique conditionnelle (`if/else`)
- Utiliser les boucles `while` et `for`
- Manipuler des algorithmes mathématiques classiques

---

## 📁 Structure du projet

```
td1-javascript/
│
├── exercice1/
│   ├── conversion_temperatures.html 
│
├── exercice2/
│   ├── conversion_durees.html 
│
├── exercice2bis/
│   ├── conversion_durees_v2.html     
│
├── exercice3/
│   ├── trois_nombres.html
│ 
├── exercice4/
│   ├── triangle1.html                 # Triangle avec while
│   └── triangle2.html                  # Triangle avec FOR
│
├── exercice4bis/
│   ├── pyramide.html             
│
├── exercice5/
│   ├── nombre_premier.html          
│
├── exercice6/
│   ├── fibo1.html                      # nième terme de Fibonacci
│   └── fibo2.html                     # Premier terme > valeur donnée
│
├── exercice7/
│   └── racine_carree.js              # Valeur approchée de √A
│
└── README.md
```

---

## 📝 Détail des exercices

### Exercice 1 — Conversion de températures
**Fonction :** `degreC(tempF)`  
Convertit une température en **Fahrenheit** vers **Celsius** à l'aide de la formule :

$$tempC = \frac{5}{9} \times (tempF - 32)$$

```
Entrée : 60.0 °F  →  Sortie : 15.6 °C
Entrée :  0.0 °F  →  Sortie : -17.8 °C
```

---

### Exercice 2 — Conversion de durées
**Fonction :** `hjms(secondes)`  
Décompose un nombre de secondes en **jours / heures / minutes / secondes**.

```
Entrée : 235789 s  →  2 jours 17 heures 29 minutes 49 secondes
Entrée : 567231 s  →  6 jours 13 heures 33 minutes 51 secondes
```

---

### Exercice 2-bis — Conversion de durées (version améliorée)
Version améliorée de `hjms` avec :
- Omission des unités nulles
- Accord du singulier si la valeur est égale à `1`

```
Entrée : 3621 s  →  1 heure 21 secondes
```

---

### Exercice 3 — Classer 3 nombres
**Fonction :** `troisNombres(a, b, c)`  
Affiche 3 nombres saisis par l'utilisateur dans l'**ordre croissant**.

```
Entrée : 14, 10, 17  →  Sortie : 10 14 17
```

---

### Exercice 4 — Motifs triangulaires
Affiche un triangle de `*` de taille `n` :
- **`triangle1(n)`** — avec des boucles `while`
- **`triangle2(n)`** — avec des boucles `for`

```
Taille 6 :
*
**
***
****
*****
******
```

---

### Exercice 4-bis — Pyramide
**Fonction :** `pyramide(n)`  
Affiche une pyramide de `*` centrée de taille `n`.

```
Taille 7 :
      *
     ***
    *****
   *******
  *********
 ***********
*************
```

---

### Exercice 5 — Nombre premier
**Fonction :** `estPremier(n)`  
Teste si un entier positif est **premier** (divisible uniquement par 1 et lui-même).

```
Entrée : 7   →  7 est un nombre premier
Entrée : 25  →  25 n'est pas un nombre premier, il est divisible par 5
```

---

### Exercice 6 — Suite de Fibonacci
- **`Fibo1(n)`** — Calcule le `n`-ième terme de la suite de Fibonacci
- **`Fibo2(valeur)`** — Retourne le premier terme de Fibonacci supérieur à une valeur donnée

Formule de récurrence :  
$$u_0 = 0,\quad u_1 = 1,\quad u_{n+1} = u_n + u_{n-1}$$

---

### Exercice 7 — Racine carrée approchée
**Fonction :** `Raca1(A)`  
Calcule une valeur approchée de $\sqrt{A}$ par la suite de récurrence de **Héron** :

$$u_{n+1} = \frac{1}{2}\left(u_n + \frac{A}{u_n}\right)$$

Convergence atteinte lorsque $|u_n^2 - A| < 10^{-6}$.

```
Entrée : A = 19.23  →  Valeur approchée : 4.385202389856321
```

---

## 🚀 Exécution

### Prérequis
- Un navigateur web moderne (Chrome, Firefox, Edge…)

### Lancer un exercice
Ouvrir directement le fichier `.html` de l'exercice souhaité dans le navigateur :

```
exercice1/conversion_temperatures.html
exercice2/conversion_durees.html
...
```

Les résultats s'affichent dans la **console DevTools** (`F12` → onglet *Console*).

---

## 🛠️ Technologies utilisées

| Technologie | Usage |
|---|---|
| JavaScript (ES6+) | Langage principal |
| HTML5 | Intégration navigateur |

---

## 👤 Auteur

| Champ | Détail |
|---|---|
| **Nom** | *BALMIR Salma* |
| **Filière** | Master SDIA |
| **Établissement** | ENSET Mohammedia |
| **Année universitaire** | 2025 / 2026 |

---

## 📄 Licence

Ce projet est réalisé dans un cadre **académique** — ENSET Mohammedia.  
Reproduction à des fins pédagogiques autorisée avec mention de la source.
