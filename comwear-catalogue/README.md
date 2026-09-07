# Com’Wear — catalogue produit

Catalogue textile personnalisable, en une page HTML autonome (aucune dépendance, aucun build).
Ouvrir `index.html` dans un navigateur, ou publier `standalone.html` en fichier statique.

## Ce que fait la page

| Fonction | Détail |
| --- | --- |
| **31 références** | 7 familles, de l’entrée de gamme événementielle au softshell technique |
| **Filtres** | recherche plein texte, famille, technique de marquage compatible, tri prix / grammage |
| **Fiche produit** | coloris interactifs, tailles, composition, emplacements possibles, tarif dégressif |
| **Générateur de devis** | textile + marquage chiffrés par palier de quantité, frais de mise en route, TVA, total TTC |
| **Impression** | feuille de style dédiée : catalogue complet, ou devis seul |

Le devis est conservé dans le navigateur du visiteur (`localStorage`), rien n’est envoyé nulle part.

## Statut des contenus

| Élément | Statut |
| --- | --- |
| Familles, références, marques, compositions, grammages | Références réelles du marché du textile promotionnel — **à confronter au catalogue fournisseur de Com’Wear** |
| Prix textile (`base` + coefficients de palier) | **Ordres de grandeur** — à caler sur les tarifs d’achat et la marge |
| Prix marquage, frais de mise en route, minimums | **Ordres de grandeur** — à valider avec l’atelier |
| Délais (48 h à 8 j), étapes de commande | Hypothèses à confirmer |
| Coloris | Nuancier générique — les teintes réelles varient d’une marque à l’autre |
| Adresse, téléphone, courriel | Placeholders |
| Identité visuelle (couleurs, typographies) | Proposition — le site com-wear.fr n’a pas pu être consulté depuis l’environnement de production |

Les caractéristiques techniques citées (grammages, certifications GOTS / OEKO-TEX / EN ISO 20471,
tenue au lavage, minimums par technique) correspondent aux usages du métier, mais engagent
Com’Wear dès la mise en ligne : elles doivent être relues par l’atelier.

## Parti pris

- **Identité** : indigo de travail et ocre fil sur une toile chaude. L’interface reste presque
  monochrome pour une raison précise — ce sont les coloris des vêtements qui doivent porter la
  couleur de la page. L’ocre est réservé à un seul usage : tout ce qui touche au devis.
- **Typographie** : Familjen Grotesk (titres), Hanken Grotesk (textes), Spline Sans Mono
  (références, grammages, tailles, prix) — le monospace tient le rôle de l’étiquette de composition.
- **Le marquage n’est pas une option en fin de page.** C’est le cœur du métier, donc il est présent
  partout : filtre de premier niveau, technique affichée sur chaque fiche, emplacements par produit,
  et prix intégré au devis. Un catalogue qui ne chiffrerait que le textile ne servirait à rien.
- **Illustrations** : silhouettes SVG teintées en direct par le coloris choisi, plutôt que des
  photos. Aucune image à produire, aucun poids réseau, et les 31 références sont cohérentes
  entre elles dès le premier jour.
- **Pas de photo produit = pas de fausse promesse.** Le jour où les photos d’atelier existent,
  elles remplacent les silhouettes sans toucher au reste.

## Détails techniques

- HTML/CSS/JS natif, un seul fichier, ~1 400 lignes, aucune image externe.
- Responsive de 360 px à 1 920 px, thèmes clair et sombre (bascule + préférence système).
- `prefers-reduced-motion` respecté, focus clavier visible, fiches ouvrables au clavier,
  tiroirs fermables par `Échap`.
- `index.html` omet volontairement `<!doctype>` / `<html>` / `<body>` : utilisable tel quel comme
  artefact publié, et s’affiche correctement ouvert directement dans un navigateur.
  `standalone.html` est la version complète, avec `noindex`, pour publication sur serveur.

## Pistes pour la suite

- Brancher le devis sur un envoi réel (formulaire, e-mail ou CRM) — aujourd’hui il se copie ou s’imprime.
- Import du tarif fournisseur en CSV plutôt que des prix codés dans le fichier.
- Photos d’atelier et rendus de marquage réels, en remplacement des silhouettes.
- Balisage `Product` + `Offer` (Schema.org) si le catalogue devient indexable.
- Passerelle vers le configurateur existant : depuis une fiche, arriver pré-rempli sur com-wear.fr.
