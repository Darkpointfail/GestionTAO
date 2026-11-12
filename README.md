# Gestion TAO

Site vitrine de Gestion TAO (Martin Beauchamp, fondateur et animateur) : formations de produits, dégustations animées et photographie.

## Structure

- `index.html` : le site, une seule page sans dépendance (polices Google Fonts).
- `seq/` : l'intro en 477 images (48 i/s, interpolées), regroupées par 4 sur 120 planches (2 × 2), en trois versions chargées selon l'écran : `xl` 2560 × 1440 (écrans Retina et 4K), `hd` 1920 × 1080, `mob` 1080 × 1800 (téléphone en portrait, cadrage vertical). Les planches sont décodées à l'avance hors du fil principal (createImageBitmap) pour un scroll sans saccade.
- Intro en mouvement continu : la molette, le trackpad ou le doigt font avancer la vidéo avec de l'inertie et une vitesse plafonnée. Elle passe au ralenti sur chaque titre (constante `STOPS` dans `index.html`), glisse jusqu'au titre suivant quand on lâche, et l'image « respire » au repos. Un bouton « Passer l'intro » et des repères cliquables permettent d'aller plus vite.
- `img/` : les photos des sections (extraites de la vidéo).
- `video/intro-4k.mp4` : la vidéo d'intro agrandie en 4K (Real-ESRGAN, qualité maximale), `video/intro-source-480p.mp4` : l'originale.

## Voir le site en local

```
python3 -m http.server 8000
```

puis ouvrir http://localhost:8000.

## Contenu provisoire

Le texte souligné en pointillé (classe `ph` dans le HTML) est provisoire et doit être validé avec Martin. Le formulaire de demande n'est relié à rien pour l'instant.
