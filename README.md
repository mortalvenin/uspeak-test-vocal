# USpeak — prototype vocal local (version 0.1)

Prototype **indépendant** du projet Flutter d'origine. Aucun fichier du projet source n'est modifié.

## Essai sur iPhone
1. Héberger `index.html` et `app.js` ensemble sur un hébergement HTTPS statique (par exemple GitHub Pages ou Netlify). Ne pas ouvrir le HTML directement depuis l'application Fichiers.
2. Ouvrir l'URL dans Safari et autoriser le microphone.
3. Faire 30 cycles « Démarrer / Arrêter », avec lecture de la phrase entre les cycles. Exporter le diagnostic.
4. Tester « Charger Whisper Tiny EN », puis « Transcrire ». Cette étape requiert Internet au premier chargement et peut échouer sur iPhone par manque de mémoire ou incompatibilité de moteur. La capture audio seule peut fonctionner même si Whisper ne fonctionne pas.

## Limites
- Aucune garantie de fonctionnement hors ligne : la mise en cache des modèles dépend du navigateur, et aucun service worker n'est fourni dans ce premier test.
- Le chargement initial de Transformers.js et du modèle nécessite Internet.
- Les fichiers audio ne sont pas transmis à un serveur de transcription. Les ressources de la bibliothèque et du modèle sont téléchargées depuis des services externes.
- La transcription Whisper ne mesure pas directement la qualité phonétique et peut normaliser les erreurs.
- Tester sur un véritable iPhone ; le test sur PC ne valide pas Safari iOS.
- Si Safari refuse le décodage du format enregistré, le diagnostic permettra de le voir.

## Intégration
Ne pas intégrer dans Flutter avant validation des 30 cycles et de la transcription locale. La prochaine phase sera un pont JS ↔ Dart avec adaptation du service `speech_recognition_service.dart`.
