# Gestion TAO

Site vitrine de Gestion TAO (Martin Beauchamp, fondateur et animateur) : formations de produits, dégustations animées et photographie.

## Structure

- `index.html` : le site, une seule page sans dépendance (polices Google Fonts).
- `video/intro-1920.mp4` (1920 × 1080) et `video/intro-mobile.mp4` (1080 × 1800, cadrage vertical pour téléphone) : la vidéo de l'intro, 24 i/s, une image clé par image (`-g 1`) pour un scroll sans saccade. La page télécharge la vidéo en entier, puis la « seeke » selon la position du scroll, avec lissage et une seule demande de seek à la fois.
  Réencodage : `ffmpeg -i source.mp4 -an -vf "scale=1920:-2,fps=24" -c:v libx264 -g 1 -crf 23 -pix_fmt yuv420p -movflags +faststart intro-1920.mp4`
- Réglages de l'intro : hauteur de `#intro` dans le CSS (720vh = longueur du scroll), `VIDEO_END` dans le script (fin de la vidéo dans le scroll, ensuite zoom dans l'allée de vignes et passage au site).
- `img/` : les photos des sections (extraites de la vidéo).
- `video/intro-4k.mp4` : la vidéo d'intro agrandie en 4K (Real-ESRGAN, qualité maximale), `video/intro-source-480p.mp4` : l'originale.

## Voir le site en local

```
python3 -m http.server 8000
```

puis ouvrir http://localhost:8000.

## Contenu provisoire

Le texte souligné en pointillé (classe `ph` dans le HTML) est provisoire et doit être validé avec Martin. Le formulaire de demande n'est relié à rien pour l'instant.
