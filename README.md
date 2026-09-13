# The Line Up — site du salon

Barber shop, 265 rue des Pyrénées, Paris 20e.
Site d'une seule page, sans dépendance ni étape de build.

## Mise en ligne

Hébergé par GitHub Pages sur la branche `main`, à la racine.
Toute modification poussée est en ligne une à deux minutes plus tard.

## Structure

| Fichier | Rôle |
|---|---|
| `index.html` | tout le site : HTML, CSS et JS dans un seul fichier |
| `photos/` | photos du salon — voir `photos/README.md` pour les noms et formats attendus |
| `og.png` | image affichée quand le lien est partagé (WhatsApp, Instagram, SMS) |
| `favicon.svg` | icône de l'onglet |
| `apple-touch-icon.png` | icône si le site est ajouté à l'écran d'accueil d'un iPhone |
| `robots.txt` | autorise l'indexation, indique le sitemap |
| `sitemap.xml` | liste les pages pour Google Search Console |
| `site.webmanifest` | nom et couleurs quand le site est ajouté à l'écran d'accueil |

## Brancher l'agenda Planity

Une seule ligne à modifier, dans `index.html`, au-dessus du bloc de
configuration de la réservation :

```js
const PLANITY_URL = '';
```

Vide, le tunnel se termine sur un récapitulatif avec la mention « démo ».
Renseigné, un bouton « Voir sur Planity » apparaît et la mention disparaît.

## Changer de nom de domaine

Trois endroits à mettre à jour, tous avec la même URL :

1. `index.html` — balise `<link rel="canonical">`, `og:url`, `twitter:image`,
   `og:image`, et les champs `url` / `image` / `@id` du bloc JSON-LD
2. `robots.txt` — ligne `Sitemap:`
3. `sitemap.xml` — balise `<loc>`

Puis ajouter un fichier `CNAME` à la racine contenant le domaine, et cocher
« Enforce HTTPS » dans Settings → Pages.

## Équipe

Les trois barbiers sont des emplacements vides tant que le salon n'a pas
donné les prénoms. Deux endroits à mettre à jour par personne, et ils
doivent concorder :

1. le tableau `BARBERS` dans `index.html` (`name`, `initial`, `specialty`)
2. la section « L'équipe » du HTML — cherche `Prénom à compléter` : titre,
   spécialité, phrase de présentation et texte alternatif de la photo

Les portraits vont dans `photos/` sous les noms `barbier-1.jpg`,
`barbier-2.jpg`, `barbier-3.jpg`.

## Horaires et prestations

Tout se règle en haut du bloc de configuration dans `index.html` :
`SERVICES`, `BARBERS`, `TIMES`, `CLOSED_DAYS`, `DAYS_AHEAD`.
Les horaires affichés dans la section Infos et dans le JSON-LD sont à
tenir cohérents avec ces valeurs.
