# Pourquoi le résultat du défi 1b change quand on redimensionne la fenêtre ?

- Les pseudo‑éléments (`::before`, `::after`) **font partie du rendu CSS**, donc :
  - ils dépendent de la **largeur disponible** ;
  - ils réagissent aux **media queries** ;
  - ils sont affectés par le **layout** (flex, grid, wrap, overflow, etc.) ;
- Quand la fenêtre change de taille :
  - le layout se réorganise ;
  - la place disponible change ;
  - le pseudo‑élément peut se déplacer, se réduire, s’étendre ou passer à la ligne.
- Conclusion :
  - **le pseudo‑élément n’est pas fixe** → il change avec le responsive.

---

# Un pseudo‑élément ::before est‑il lisible par un lecteur d’écran ?

- **Non.**
- Un pseudo‑élément :
  - n’existe pas dans le **DOM** ;
  - n’a pas de **rôle sémantique** ;
  - n’a pas de **texte accessible** ;
  - est purement **visuel**.

---

# Qu’est‑ce que ça implique pour ce qu’on y met ?

- On peut y mettre :
  - décorations ;
  - icônes décoratives ;
  - emojis décoratifs ;
  - éléments purement visuels.

- On ne doit **jamais** y mettre :
  - du texte important ;
  - des informations nécessaires à la compréhension ;
  - des labels ;
  - des messages d’erreur ;
  - des données dynamiques essentielles.

- Règle d’or :
  - **Information → HTML**
  - **Décoration → CSS**

