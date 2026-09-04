# LibertiWatt-Énergie — maquette de présentation

Maquette de page d'accueil (une seule page HTML autonome, sans dépendance ni build).
Ouvrir `index.html` dans un navigateur, ou consulter la version publiée transmise avec ce dossier.

## Statut des contenus

| Élément | Statut |
| --- | --- |
| Positionnement, structure, parcours | Proposition à valider |
| Chiffres de la section « Réalisations » | **Fictifs** — à remplacer par les chiffres réels |
| Fiche chantier, témoignages | **Exemples** — à remplacer par un chantier et des avis réels |
| Montants et barèmes des aides | Volontairement non chiffrés (hors TVA 5,5 %) — à figer au moment de la mise en ligne |
| Téléphone, e-mail, zone d'intervention | Placeholders |
| Formulaire | Non fonctionnel (aucun envoi) |
| Hypothèses du simulateur | 0,21 €/kWh, rachat surplus 0,04 €/kWh, 1 100 kWh/an/kWc, prime 80 €/kWc — à confirmer |

L'activité retenue (installateur photovoltaïque en autoconsommation, stockage, IRVE,
pompe à chaleur) est une hypothèse : le site actuel n'a pas pu être consulté depuis
l'environnement de production de la maquette. À corriger si le périmètre réel diffère.

## Parti pris

- **Identité** : bleu pétrole profond + ambre solaire, plutôt que le bleu/vert générique
  du secteur. Une seule couleur d'accent, utilisée avec parcimonie.
- **Typographie** : Archivo (titres, chasse élargie), Instrument Sans (textes),
  IBM Plex Mono (données, unités, libellés) — le monospace rappelle l'univers de la
  mesure et de la supervision.
- **Hero** : un panneau de supervision animé (production, batterie, maison, réseau)
  plutôt qu'une photo de toiture. Il montre le produit réellement vécu par le client.
- **Simulateur** : dimensionnement et économies calculés en direct, hypothèses affichées.
  C'est le principal outil de captation de contact de la page.
- **Parcours** : cinq étapes datées (J0 → J60) avec durées — la transparence sur les
  délais administratifs est un argument commercial rarement exploité par la concurrence.
- **Preuve** : chiffres d'exploitation + une fiche technique de chantier complète
  (puissance, modules, orientation, production mesurée, autoconsommation).

## Détails techniques

- HTML/CSS/JS natif, un seul fichier, ~1 000 lignes, aucune image externe
  (illustrations en SVG inline) — se charge instantanément.
- Responsive de 360 px à 1 920 px, menu mobile, `prefers-reduced-motion` respecté,
  focus clavier visible, contenu lisible sans JavaScript.
- Le fichier omet volontairement les balises `<!doctype>`/`<html>`/`<body>` : il est
  utilisable tel quel comme artefact publié, et s'affiche correctement ouvert
  directement dans un navigateur.

## Pistes pour la suite

- Pages secondaires : chaque solution, réalisations filtrables par commune, blog aides.
- Balisage `LocalBusiness` + `FAQPage` (Schema.org) pour le référencement local.
- Connexion du formulaire à un CRM et suivi des conversions du simulateur.
- Photos de chantiers réels, portraits d'équipe, logos des certifications.
