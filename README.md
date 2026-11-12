# Gestion TAO

Site vitrine de Gestion TAO (Martin Beauchamp, fondateur et animateur) : formations de produits, dégustations animées et photographie.

## Structure

- `index.html` : le site, une seule page sans dépendance (polices Google Fonts).
- `seq/hd/` et `seq/sd/` : l'intro en 477 images (48 i/s, interpolées), regroupées par 8 sur 60 planches (2 × 4). `hd` = 1440 × 810 par image pour les grands écrans, `sd` = 960 × 540 pour les mobiles. Les planches sont décodées à l'avance hors du fil principal (createImageBitmap) pour un scroll sans saccade.
- `img/` : les photos des sections (extraites de la vidéo).
- `video/intro-4k.mp4` : la vidéo d'intro agrandie en 4K (Real-ESRGAN), `video/intro-source-480p.mp4` : l'originale.

## Voir le site en local

```
python3 -m http.server 8000
```

puis ouvrir http://localhost:8000.

## Contenu provisoire

Le texte souligné en pointillé (classe `ph` dans le HTML) est provisoire et doit être validé avec Martin. Le formulaire de demande n'est relié à rien pour l'instant.
