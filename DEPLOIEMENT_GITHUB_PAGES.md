# Mettre le prototype USpeak en ligne gratuitement (GitHub Pages)

1. Connectez-vous à https://github.com et créez un dépôt **public** nommé `uspeak-test-vocal` (sans modèle).
2. Ouvrez le dépôt, choisissez **Add file > Upload files** et importez **les fichiers décompressés** `index.html`, `app.js`, `.nojekyll`, `README.md` (ne téléversez pas le ZIP comme site). Cliquez sur **Commit changes**.
3. Ouvrez **Settings > Pages**. Sous **Build and deployment**, sélectionnez **Deploy from a branch**, branche `main`, dossier `/(root)` puis **Save**.
4. Attendez le déploiement (parfois quelques minutes). L'adresse devrait ressembler à `https://VOTRE-PSEUDO.github.io/uspeak-test-vocal/`. Copiez l'URL exacte affichée dans **Settings > Pages**.
5. Sur iPhone, ouvrez l'URL dans Safari, autorisez le micro, testez 30 cycles de capture. Exportez le diagnostic. Testez ensuite le chargement Whisper, puis la transcription.

## Important
- Dépôt public : **n'y mettez pas le projet USpeak complet**, de clés Firebase, de secrets, ni de données privées. Ce paquet contient uniquement le prototype autonome.
- HTTPS est obligatoire pour le micro sur iPhone.
- GitHub Pages ne fait qu'héberger les fichiers statiques. Le modèle est téléchargé depuis un service externe au premier lancement.
- Ce prototype n'est pas encore une PWA hors ligne.
- Si le modèle échoue à charger, envoyez le fichier de diagnostic exporté et la version d'iOS.
