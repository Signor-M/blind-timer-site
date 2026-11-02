# Blind Timer – Site « Comment jouer »

Page web statique qui explique, en images, comment jouer à **Blind Timer**, un jeu de timing à chrono caché pour 2 à 4 joueurs sur un seul appareil (créé avec GDevelop).

Le jeu ouvre cette page depuis le bouton « Comment jouer ? » du menu.

## Aperçu

- 7 étapes illustrées avec les captures d’écran du jeu
- Calcul des points et conseils
- Français et anglais (boutons FR / EN)
- Thème clair ou sombre selon l’appareil
- Aucune dépendance, aucun outil de build : du HTML, du CSS et un peu de JavaScript

## Structure

```text
.
├── index.html            # la page (HTML, CSS et JS dans un seul fichier)
├── assets/
│   ├── icon.png          # icône du jeu (512 × 512)
│   └── screens/          # captures d’écran utilisées dans les étapes
├── vercel.json           # réglages Vercel (cache et en-têtes)
├── .gitignore
└── README.md
```

## Lancer en local

Ouvre `index.html` dans un navigateur, ou lance un petit serveur :

```bash
python3 -m http.server 8000
```

Puis va sur <http://localhost:8000>.

## Langue de la page

La page détecte la langue de l’appareil. Pour forcer une langue, ajoute-la à la fin du lien :

- `https://TON-SITE.vercel.app/#fr` : français
- `https://TON-SITE.vercel.app/#en` : anglais

Dans GDevelop, le bouton du menu ouvre le lien avec `#en` ou `#fr` selon la langue du jeu.

## Modifier le contenu

- Le texte français est directement dans `index.html`.
- Le texte anglais est dans l’objet `EN`, dans la balise `<script>` en bas du fichier. Chaque texte porte un attribut `data-k` qui correspond à une clé de cet objet.
- Pour changer une capture, remplace le fichier dans `assets/screens/` en gardant le même nom.

## Déploiement

Le site est hébergé sur [Vercel](https://vercel.com), relié à ce dépôt GitHub. Chaque `git push` sur la branche `main` redéploie automatiquement le site.

Réglages Vercel : framework **Other**, aucune commande de build, aucun dossier de sortie à renseigner.

## Crédits

© 2026 MStudioGame. Tous droits réservés.
Police : [Space Grotesk](https://fonts.google.com/specimen/Space+Grotesk) (SIL Open Font License).
