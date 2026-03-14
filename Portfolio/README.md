
# 🎓 Portfolio Personnel — Salma Balmir

> **Mini Projet 1 — Technologies Web et Web Sémantique**  

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)](https://developer.mozilla.org/fr/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)](https://developer.mozilla.org/fr/docs/Web/CSS)
[![GitHub Pages](https://img.shields.io/badge/GitHub-Pages-black?style=flat&logo=github)](https://pages.github.com/)

---

## 📌 Présentation

Ce projet est un **portfolio web personnel** réalisé dans le cadre du Mini Projet 1 du module Technologies Web et Web Sémantique. Il présente mon parcours académique, mes compétences techniques et pédagogiques, ainsi que mes projets réalisés durant ma formation en **Licence Éducation en Informatique** et en **Master SDIA**.

---

## 🗂️ Structure du projet

```
portfolio/
├── portfolio.html     # Structure et contenu HTML du site
├── portfolio.css      # Mise en page, styles et effets visuels
├── photo.png          # Photo de profil
└── README.md          # Documentation du projet
```

---

## 📄 Sections du site

| Section | Identifiant | Description |
|---|---|---|
| **Accueil** | `#accueil` | Présentation rapide avec nom, statut et boutons |
| **À propos** | `#apropos` | Parcours académique et timeline |
| **Compétences** | `#competences` | Cartes de compétences + barres de progression |
| **Projets** | `#projets` | 4 projets avec technologies utilisées |
| **Contact** | `#contact` | Coordonnées et formulaire de contact |

---

## 🧱 Explication du code HTML

### 1. Structure de base

```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio Salma Balmir</title>
    <link rel="stylesheet" href="portfolio.css" />
</head>
```

| Balise / Attribut | Rôle |
|---|---|
| `<!DOCTYPE html>` | Déclare que le fichier est en HTML5 |
| `lang="fr"` | Indique la langue de la page (français) |
| `charset="UTF-8"` | Encode les caractères spéciaux (é, è, ç…) |
| `viewport` | Rend la page adaptable sur mobile |
| `<link rel="stylesheet">` | Relie le fichier CSS à la page HTML |

---

### 2. Navigation (`<nav>`)

```html
<nav id="navbar">
    <div class="nom-site">Mon Portfolio</div>
    <ul id="menu">
        <li><a href="#apropos">À propos</a></li>
        <li><a href="#competences">Compétences</a></li>
        <li><a href="#projets">Projets</a></li>
        <li><a href="#contact">Contact</a></li>
    </ul>
</nav>
```

- `<nav>` : balise sémantique pour la barre de navigation
- `href="#apropos"` : lien interne qui fait défiler vers la section `id="apropos"`
- `<ul>` + `<li>` : liste non ordonnée pour les liens du menu
- La classe `.actif` est ajoutée dynamiquement par JavaScript au lien de la section visible

---

### 3. Section Accueil

```html
<section id="accueil">
    <div class="texte-accueil">
        <p class="statut">Étudiante en 1er année Master SDIA</p>
        <h1>Salma <span class="mot-couleur">Balmir</span></h1>
        <p class="description">...</p>
        <div class="boutons">
            <a href="#projets" class="btn-principal">Voir mes projets</a>
            <a href="#contact" class="btn-secondaire">Me contacter</a>
        </div>
    </div>
    <div class="carte-profil">
        <img src="photo.png" alt="Salma Balmir" class="photo" />
        ...
    </div>
</section>
```

- `<section>` : balise sémantique pour regrouper un bloc thématique
- `<h1>` : titre principal de la page (un seul par page pour le SEO)
- `<span class="mot-couleur">` : applique une couleur violette uniquement sur "Balmir"
- `<img src="photo.png">` : affiche la photo de profil
- `alt="Salma Balmir"` : texte alternatif pour l'accessibilité

---

### 4. Section Projets — carte projet

```html
<div class="carte-projet">
    <div class="vignette v1">🤖</div>
    <div class="corps-projet">
        <h3>Smart Task Manager with AI Integration</h3>
        <p>Description du projet...</p>
        <div class="tags-projet">
            <span>JAVA</span>
            <span>JAVAFX</span>
        </div>
        <div class="liens-projet">
            <a href="..." class="lien-voir">Voir le projet</a>
            <a href="..." class="lien-git">GitHub</a>
        </div>
    </div>
</div>
```

- Chaque projet est une carte indépendante avec vignette, description, tags et liens
- `.vignette.v1 / v2 / v3 / v4` : couleur de fond différente selon le projet
- `.tags-projet span` : badges technologiques

---

### 5. Formulaire de contact

```html
<form id="formulaire" onsubmit="envoyerMessage(event)">
    <input type="text" id="fname" required />
    <input type="email" id="email" required />
    <textarea id="message" required></textarea>
    <button type="submit" id="btn-envoyer">Envoyer 🚀</button>
</form>
```

- `onsubmit="envoyerMessage(event)"` : appelle la fonction JavaScript à la soumission
- `required` : validation HTML5 native (champ obligatoire)
- `type="email"` : vérifie automatiquement le format de l'adresse email

---

## 🎨 Explication du code CSS

### 1. Variables CSS (`:root`)

```css
:root {
    --violet:  #7c3aed;
    --rose:    #ec4899;
    --bleu:    #0ea5e9;
    --jaune:   #f59e0b;
    --fond:    #f8f7ff;
}
```

Les **variables CSS** permettent de centraliser toutes les couleurs du site. Pour changer la couleur principale, il suffit de modifier `--violet` ici, et tout le site se met à jour automatiquement.

---

### 2. Flexbox — Navigation

```css
#navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
}
```

| Propriété | Effet |
|---|---|
| `display: flex` | Active le modèle Flexbox |
| `justify-content: space-between` | Logo à gauche, menu à droite |
| `align-items: center` | Aligne verticalement au centre |

---

### 3. CSS Grid — Grille de projets

```css
.grille-projets {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 22px;
}
```

| Propriété | Effet |
|---|---|
| `display: grid` | Active la grille CSS |
| `repeat(auto-fit, ...)` | Nombre de colonnes automatique selon la largeur |
| `minmax(260px, 1fr)` | Chaque carte fait minimum 260px, maximum 1 fraction |
| `gap: 22px` | Espace entre les cartes |

---

### 4. Pseudo-éléments `::before` / `::after`

```css
/* Barre colorée en haut de chaque carte compétence */
.carte-comp::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 4px;
    background: linear-gradient(90deg, var(--violet), var(--rose));
}

/* Cercle décoratif dans la section accueil */
#accueil::after {
    content: '';
    position: absolute;
    width: 240px; height: 240px;
    border-radius: 50%;
    background: rgba(236, 72, 153, 0.07);
}
```

Les pseudo-éléments créent des **éléments décoratifs sans HTML supplémentaire**. `content: ''` est obligatoire pour qu'ils s'affichent.

---

### 5. Effets hover (survol)

```css
.carte-projet:hover {
    transform: translateY(-6px);
    box-shadow: 0 18px 40px rgba(124, 58, 237, 0.12);
    border-color: var(--violet);
}
```

- `transform: translateY(-6px)` : fait monter la carte de 6px au survol
- `box-shadow` : ajoute une ombre portée colorée
- `transition: 0.25s` : rend l'animation fluide

---

### 6. Soulignement animé du menu

```css
#menu a::after {
    content: '';
    position: absolute;
    bottom: 0; left: 0;
    width: 0;
    height: 2px;
    background-color: var(--violet);
    transition: width 0.25s;
}

#menu a:hover::after {
    width: 100%;  /* le trait grandit au survol */
}
```

Le trait part de 0 et s'étend jusqu'à 100% de la largeur du lien quand on le survole.

---

### 7. Media Queries — Responsive Design

```css
/* Tablette */
@media (max-width: 900px) {
    #accueil {
        flex-direction: column; /* empile les blocs verticalement */
        text-align: center;
    }
}

/* Mobile */
@media (max-width: 768px) {
    .grille-projets {
        grid-template-columns: 1fr; /* une seule colonne */
    }
}

/* Petit mobile */
@media (max-width: 480px) {
    #menu { display: none; } /* masque le menu de navigation */
}
```

Les **media queries** adaptent la mise en page selon la taille de l'écran.

---

## ⚡ Explication du code JavaScript

### 1. Menu actif au scroll

```javascript
window.addEventListener('scroll', function () {
    let actuelle = '';
    toutesLesSections.forEach(function (sec) {
        if (window.scrollY >= sec.offsetTop - 100) {
            actuelle = sec.id;
        }
    });
    tousLesLiens.forEach(function (lien) {
        lien.classList.remove('actif');
        if (lien.getAttribute('href') === '#' + actuelle) {
            lien.classList.add('actif');
        }
    });
});
```

- `addEventListener('scroll')` : déclenche la fonction à chaque défilement
- `window.scrollY` : position verticale actuelle du scroll
- `sec.offsetTop` : distance de la section depuis le haut de la page
- `classList.add('actif')` : ajoute la classe CSS `.actif` sur le lien correspondant

---

### 2. Confirmation d'envoi du formulaire

```javascript
function envoyerMessage(e) {
    e.preventDefault(); // empêche le rechargement de la page
    var btn = document.getElementById('btn-envoyer');
    btn.textContent = '✅ Message envoyé !';
    btn.style.background = '#10b981'; // vert
    setTimeout(function () {
        btn.textContent = 'Envoyer le message 🚀';
        btn.style.background = ''; // remet la couleur originale
        document.getElementById('formulaire').reset(); // vide le formulaire
    }, 3000); // après 3 secondes
}
```

- `e.preventDefault()` : bloque le comportement par défaut du formulaire (rechargement)
- `setTimeout(..., 3000)` : exécute le reset après 3000 millisecondes (3 secondes)

---

## 🚀 Projets présentés

### 1. Smart Task Manager with AI Integration
Application intelligente de gestion des tâches avec priorisation automatique par IA.  
`Java` `JavaFX`

### 2. Planification Robuste sur Grille — Chaînes de Markov
Modélisation de l'incertitude dans un environnement grille pour calculer des politiques optimales.  
`Python` `Chaînes de Markov` `Optimisation`

### 3. Comparaison de Métaheuristiques — TSP
Implémentation et comparaison de 8 algorithmes d'optimisation sur le problème du voyageur de commerce.  
`Python` `NumPy` `HC Best` `Recuit Simulé` `Tabou` `GRASP` `VNS` `ILS`

### 4. Quiz Interactif Web
Application web de quiz adaptatif selon le niveau et les performances de l'élève.  
`HTML` `CSS` `PHP`

---

## 👩‍💻 Auteure

**Salma Balmir**  
Étudiante en 1ère année Master SDIA  
Titulaire d'une Licence Éducation en Informatique (2022–2025)

📧 salmabalmir55@gmail.com  
🐙 [github.com/BSalma55](https://github.com/BSalma55)  
💼 [linkedin.com/in/salma-balmir-723a68290](https://www.linkedin.com/in/salma-balmir-723a68290/)

---

## 📅 Informations du projet

| Champ | Détail |
|---|---|
| **Module** | Technologies Web et Web Sémantique — Mini Projet 1 |
| **Année universitaire** | 2025–2026 |
| **Technologies** | HTML5 · CSS3 |
| **Dépôt** | [github.com/BSalma55](https://github.com/BSalma55) |
