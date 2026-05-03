# AXIOM — Landing Page

> *"veritas nihil nisi veritas"*

---

## Structure du projet

axiom/
├── index.html
├── style.css
├── FOND-AXIOME.jpeg          # Image de fond hero + form section
├── MacBook Air - 2.png       # Image plein écran (image-section)
└── Capture d'écran 2026-04-13 150748.png  # Logo Axiom

---

## Sections

| ID | Classe CSS | Description |
|----|-----------|-------------|
| `#accueil` | `.hero` | Section hero plein écran avec titre, citation et CTA |
| `#pourquoi-nous` | `.image-section` | Image plein écran MacBook |
| `#reassurance` | *(section texte 3 colonnes)* | Arguments de réassurance |
| `#inscription` | `.form-section` | Formulaire d'inscription (Nom, Prénom, Email) |

---

## Design System

### Typographies
- **Josefin Sans** (100 / 200 / 300) — titres, navbar, boutons
- **Cormorant Garamond** (italic 300) — citations

### Couleurs
| Variable | Valeur | Usage |
|----------|--------|-------|
| `--white` | `#ffffff` | Texte principal |
| `--off-white` | `rgba(255,255,255,0.85)` | Sous-titres |
| `--muted` | `rgba(255,255,255,0.55)` | Citations |
| `--gold` | `#b8976a` | Logo, accents dorés |
| Fond global | `#0a0a0a` | Background sombre |

---

## Navigation

La navbar est fixe (`position: fixed`) avec un effet de verre (`backdrop-filter: blur`).  
Les liens sont ancrés via les `id` des sections :

html
<a href="#accueil">ACCUEIL</a>
<a href="#pourquoi-nous">POURQUOI NOUS ?</a>
<a href="#reassurance">REASSURANCE</a>
<a href="#inscription">INSCRIPTION</a>
```

Le scroll fluide est géré par `scroll-behavior: smooth` sur `html, body`.

---

## Transitions & Fondus

Les fondus entre sections sont réalisés avec des pseudo-éléments CSS `::before` / `::after` en `linear-gradient` vers `#0a0a0a`.

| Section | Effet |
|---------|-------|
| `.hero::before` | Fondu bas (sortie vers le bas) |
| `.form-section::before` | Fondu haut (entrée par le haut) |
| `.image-section::before` | Fondu haut |
| `.image-section::after` | Fondu côtés + fondu bas |

---

## Lancer le projet

Ouvre simplement `index.html` dans un navigateur.  
Aucune dépendance, aucun build requis — HTML/CSS pur.

---

*© 2025 Axiom. Tous droits réservés.*
