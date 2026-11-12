# Gestion TAO

Site vitrine de Gestion TAO (Martin Beauchamp, fondateur et animateur) : formations de produits, dégustations animées et photographie.

## Structure

- `index.html` : le site, une seule page sans dépendance (polices Google Fonts).
- `frames-hd/` : 240 images 1920 × 1080 de l'intro, lues au scroll sur les grands écrans.
- `frames/` : 240 images 1024 × 576 pour les mobiles.
- `video/intro-4k.mp4` : la vidéo d'intro agrandie en 4K (Real-ESRGAN), `video/intro-source-480p.mp4` : l'originale.

## Voir le site en local

```
python3 -m http.server 8000
```

puis ouvrir http://localhost:8000.

## Contenu provisoire

Le texte souligné en pointillé (classe `ph` dans le HTML) est provisoire et doit être validé avec Martin. Le formulaire de demande n'est relié à rien pour l'instant.
