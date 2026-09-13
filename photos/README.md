# Photos du site

Dépose les fichiers ici, **avec exactement ces noms**. Ils apparaissent automatiquement
sur le site. Un fichier manquant n'affiche jamais d'image cassée : le cadre stylé reste
à sa place avec son intitulé.

## Portfolio (section « Réalisations ») — carré, 1:1

| Fichier | Ce qu'on veut voir |
|---|---|
| `degrade-bas.jpg` | dégradé bas, de dos ou 3/4 |
| `skin-fade.jpg` | skin fade, profil net |
| `coupe-barbe.jpg` | combo coupe + barbe, face |
| `design-traits.jpg` | traits / motifs à la lame, gros plan |
| `avant-apres.jpg` | avant / après côte à côte |
| `mid-fade.jpg` | mid fade, 3/4 |
| `crop-texture.jpg` | crop texturé, face |
| `contours-lame.jpg` | contours à la lame, gros plan nuque ou tempe |

**Format :** carré, **1200 × 1200 px**, JPG qualité 80, moins de 250 Ko par fichier.

## Équipe — portrait, 4:5

| Fichier | Ce qu'on veut voir |
|---|---|
| `barbier-1.jpg` | portrait vertical, au salon |
| `barbier-2.jpg` | portrait vertical, au salon |
| `barbier-3.jpg` | portrait vertical, au salon |

**Format :** vertical, **800 × 1000 px**, JPG qualité 80, moins de 200 Ko par fichier.

## Conseils de prise de vue

Le site est noir mat avec du néon rouge. Les photos qui rendent le mieux :

- lumière latérale, fond sombre, pas de flash direct
- cadrer serré sur la coupe, pas sur toute la pièce
- éviter les photos jaunes de néon blanc — refroidir un peu à la retouche
- toujours le même angle pour les trois portraits d'équipe

## Compression

Sur un Mac, pour faire tenir une photo sous la limite :

```bash
# redimensionner et compresser les carrés du portfolio
sips -Z 1200 photo.jpg --out degrade-bas.jpg

# vérifier le poids
ls -lh *.jpg
```

## Si tu changes les noms

Les noms de fichiers sont écrits dans `index.html`, section `RÉALISATIONS`
(`<img src="./photos/...">`). Change-les aux deux endroits ou garde ceux du tableau.
