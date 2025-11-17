# Fansite Japon

Un site web moderne et innovant dédié à la culture japonaise, avec un design unique basé sur des bandes horizontales animées.

## Description

Ce projet présente quatre aspects emblématiques de la culture japonaise à travers une interface interactive et visuellement impressionnante :

- **L'Empereur du Japon** - Gardien de la tradition millénaire
- **Maître Sushis** - L'art culinaire japonais par excellence
- **Hideaki Anno** - Le créateur visionnaire d'Evangelion
- **Masashi Kishimoto** - Le génie derrière Naruto

## Caractéristiques Principales

### Structure HTML ([Index.html](Index.html))
- **Header fixe** avec navigation et logo en japonais (日本)
- **4 sections en bandes horizontales** :
  - Empereur du Japon - Gardien de la tradition millénaire
  - Maître Sushis - L'art culinaire japonais par excellence
  - Evangelion (Hideaki Anno) - Le créateur visionnaire
  - Naruto (Masashi Kishimoto) - Le génie du manga
- **Footer** avec navigation répétée

### Design CSS ([styles.css](styles.css))

#### Effet de bandes qui grossissent au survol
- Les bandes passent de `flex: 1` à `flex: 2.5` au survol
- Les autres bandes se rétrécissent à `flex: 0.5`
- Transitions fluides avec `cubic-bezier` pour un mouvement naturel

#### Styles visuels
- **4 gradients colorés distincts** pour chaque section
- **Effets d'apparition progressifs** :
  - Titre qui grossit
  - Sous-titre qui monte
  - Icône qui tourne
- **Header et footer** avec effet de transparence (`backdrop-filter`)
- **Design responsive** pour mobile

### Animations au Survol

Lorsque vous passez la souris sur une bande :
1. La bande s'agrandit considérablement
2. Le titre grossit et l'espacement des lettres augmente
3. Le sous-titre apparaît en montant
4. Une icône apparaît avec rotation
5. L'overlay sombre s'éclaircit

## Structure du Projet

```
fansite-project/
├── Index.html      # Page d'accueil principale
├── styles.css      # Styles et animations
└── README.md       # Documentation
```

## Technologies Utilisées

- **HTML5** : Structure sémantique
- **CSS3** : Animations, transitions, flexbox, gradients
- **Google Fonts** : Typographie moderne

## Comprendre le Cubic-Bezier

### Qu'est-ce que le Cubic-Bezier ?

Le `cubic-bezier` est une fonction mathématique qui définit **comment une animation accélère et ralentit** au fil du temps. C'est une courbe de Bézier cubique utilisée pour créer des transitions plus naturelles et personnalisées.

### Comment ça fonctionne ?

```css
transition: all 0.6s cubic-bezier(0.4, 0, 0.2, 1);
```

**Syntaxe** : `cubic-bezier(x1, y1, x2, y2)`
- **4 valeurs** entre 0 et 1 qui définissent 2 points de contrôle
- Ces points contrôlent la forme de la courbe d'animation

### Visualisation

Imaginez un graphique où :
- **Axe horizontal (X)** = le temps (de 0% à 100% de l'animation)
- **Axe vertical (Y)** = la progression (de l'état initial à l'état final)

```
Y (progression)
│     ╱
│   ╱
│  ╱   (point de contrôle 2)
│ ╱
│╱ (point de contrôle 1)
└─────────────────── X (temps)
```

### Dans ce projet

`cubic-bezier(0.4, 0, 0.2, 1)` crée un mouvement qui :
1. Démarre doucement (accélération progressive)
2. Accélère au milieu
3. Ralentit en fin pour un arrêt en douceur

C'est plus naturel qu'un simple `ease` ou `linear`.

### Comparaison avec les valeurs prédéfinies

```css
/* Valeurs standards */
ease:        cubic-bezier(0.25, 0.1, 0.25, 1)    /* Par défaut */
linear:      cubic-bezier(0, 0, 1, 1)             /* Vitesse constante */
ease-in:     cubic-bezier(0.42, 0, 1, 1)          /* Démarre lent */
ease-out:    cubic-bezier(0, 0, 0.58, 1)          /* Finit lent */
ease-in-out: cubic-bezier(0.42, 0, 0.58, 1)       /* Lent au début et fin */
```

### Pourquoi l'utiliser ?

Pour l'effet de **bandes qui grossissent**, `cubic-bezier(0.4, 0, 0.2, 1)` donne un mouvement fluide et professionnel, similaire au Material Design de Google. L'animation n'est pas robotique mais organique.

**Outil pratique** : Créez vos propres courbes sur [cubic-bezier.com](https://cubic-bezier.com) pour visualiser et tester différentes valeurs en temps réel !

## Techniques d'Animation CSS Utilisées

Le projet utilise plusieurs techniques d'animation avancées :

- **Flexbox dynamique** : Les bandes changent de taille proportionnellement
- **Cubic-bezier** : Courbes d'animation personnalisées pour un mouvement naturel
- **Transform & Opacity** : Transitions fluides des éléments
- **Backdrop-filter** : Effet de flou pour le header et footer

## Installation

1. Clonez ou téléchargez le projet
2. Ouvrez `Index.html` dans votre navigateur web
3. Aucune dépendance ou installation requise

## Utilisation

Passez simplement votre souris sur les différentes bandes pour voir les animations et explorer les différentes sections du site.

## Personnalisation

### Modifier les couleurs
Dans `styles.css`, modifiez les gradients de chaque bande :

```css
.strip-1 {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}
```

### Ajuster la vitesse d'animation
Modifiez la durée dans les propriétés `transition` :

```css
transition: all 0.6s cubic-bezier(0.4, 0, 0.2, 1);
```

### Changer l'effet de grossissement
Ajustez les valeurs `flex` dans le CSS :

```css
.strip:hover {
    flex: 2.5;  /* Taille au survol */
}
```

## Améliorations Futures

- Ajouter des pages détaillées pour chaque section
- Intégrer des images de fond pour chaque bande
- Ajouter des effets sonores au survol
- Créer une version avec scroll parallax
- Ajouter un mode sombre/clair

## Auteur

Projet créé en 2024

## Licence

Projet personnel - Libre d'utilisation
