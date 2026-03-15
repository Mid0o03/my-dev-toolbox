# Accessibilité (A11y)

L'accessibilité web permet à tous d'utiliser vos interfaces, y compris les personnes utilisant des lecteurs d'écran ou naviguant uniquement au clavier.

## 🧱 Structure Sémantique
Privilégiez toujours le HTML sémantique aux `<div>` et `<span>`.
- `<header>`, `<nav>`, `<main>`, `<footer>`, `<section>`, `<article>`, `<aside>`.
- Un seul `<h1>` par page. Ordre logique des titres (`h2`, `h3`, ...).

## ⌨️ Navigation au Clavier
- Tous les éléments interactifs (boutons, liens) doivent être focalisables via `Tab`.
- Ne jamais supprimer l'outline de focus sans alternative visuelle :
```css
/* MAUVAIS */
*:focus { outline: none; }
/* BIEN (ou laisser par défaut) */
*:focus-visible { outline: 2px solid blue; }
```

## 🖼️ Images
- Utilisez l'attribut `alt` pour toutes les images.
- `alt=""` pour les images purement décoratives (elles seront ignorées par les lecteurs d'écran).

## 🏷️ Rôles et ARIA
Utilisez ARIA uniquement si le HTML sémantique ne suffit pas.
- `aria-label="Fermer le menu"` : Pour un bouton ne contenant qu'une icône.
- `aria-hidden="true"` : Pour cacher un élément aux lecteurs d'écran.
- `aria-expanded="false/true"` : Pour indiquer l'état d'un menu déroulant.
- `role="alert"` : Pour les messages d'erreur ou notifications dynamiques.

## 🎨 Contrastes et Couleurs
- Ratio de contraste minimum de **4.5:1** pour le texte normal.
- Ne jamais utiliser la couleur comme seule façon de transmettre une information (ajoutez des icônes ou du texte).

## 🛠️ Outils de vérification
- **Lighthouse** (dans Chrome DevTools).
- **axe DevTools** (extension navigateur).
- **WAVE** (Web Accessibility Evaluation Tool).
