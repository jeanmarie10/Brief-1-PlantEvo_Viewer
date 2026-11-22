# PlantEvo Viewer

Site web **statique** (HTML et CSS, sans JavaScript ni framework) qui raconte l'évolution des végétaux,
« de l'eau à la terre », pour un stand d'exposition sur l'agriculture.
Projet 1 de la Digital Farming School.

## Pages

| Page | Fichier | Rôle |
|---|---|---|
| Accueil | `index.html` | Bannière et chiffres clés, frise des 6 étapes (Menu), « À propos » (Pourquoi ce projet ? Comment ça marche ?), pied de page avec les sources |
| Groupes | `pages/algues.html`, `pages/mousses.html`, `pages/fougeres.html`, `pages/coniferes.html`, `pages/graminees.html`, `pages/dicotyledones.html` | Une page par groupe, même gabarit |

Les liens « Menu », « À propos » et « Sources » de la barre de navigation pointent vers des ancres de `index.html`
(`#menu`, `#a_propos`, `#sources`).

Chaque page de groupe contient : un fil d'Ariane avec compteur d'étape (par exemple 1 / 6), une bannière,
le problème résolu (avec ses badges), l'appareil végétatif, la reproduction
et une section « Observé sur le terrain » (photo, espèce, coordonnées GPS, lieu, carte SIG).
Certaines pages ajoutent un encadré (par exemple « Focus pollinisateurs » sur Dicotylédones).
En bas de page : un bouton « Retour au menu » et un lien vers le groupe précédent ou suivant.

## Structure du projet

```
plantevo-viewer/
  index.html
  README.md
  css/
    style.css
  pages/
    algues.html  mousses.html  fougeres.html  conifere.html  graminees.html  dicotyledones.html
  image/
    accueil/  algues/  mousses/  fougeres/  coniferes/  graminees/  dicotyledones/
    reproduction/  terrain/
  sig/
    cartes/
```

## Choix techniques

- **HTML5 sémantique** : header, nav, main, section, footer.
- **Un seul fichier CSS** (`css/style.css`), commenté partie par partie (`/* Fil d'ariane */`, `/* Bannière */`, etc.)
  et organisé en 4 blocs : éléments communs, page d'accueil, pages de groupe, mobile.
- **Flexbox** (barre de navigation, boutons, badges, colonnes de texte) et **grid** (statistiques, frise des étapes,
  grilles des pages de groupe).
- **Pages de groupe en pourcentages** : largeurs, marges et tailles de texte en `%`, proportions des images avec `aspect-ratio`.
- **Adaptable au téléphone** : une media query (largeur maximale de 768 px) pour les pages de groupe.
- **Sans JavaScript** : survols et transitions en CSS, défilement doux avec `scroll-behavior: smooth`.
- **Police Akshar** chargée depuis Google Fonts (lien externe, connexion nécessaire), avec `sans-serif` en secours.
- **Accessibilité** : chaque image a un texte alternatif (`alt`) et une légende, lien actif repéré par `aria-current`.

## Utiliser le site

Ouvrir `index.html` dans un navigateur (double-clic), ou avec l'extension Live Server de VS Code.
Une connexion internet est nécessaire pour afficher la police.

## Auteur
Lien figma: https://www.figma.com/design/26NFQoCJAj7fGwrrmLPISW/PlantEvo-Viewer---Maquette?node-id=0-1&t=kvvX9uIVF0YnPvhJ-1
Dadié Ebey Jean-marie Michel, Agritech, 22/11/2026.