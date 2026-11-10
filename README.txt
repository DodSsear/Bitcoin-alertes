BITCOIN ALERTES — VERSION 1

CONTENU
- index.html : application complète
- manifest.webmanifest : configuration PWA
- sw.js : cache de base pour le mode application
- icon.svg : icône

LANCEMENT LOCAL
Pour tester rapidement sur ordinateur, ouvrez un terminal dans ce dossier et lancez :
  python -m http.server 8000
Puis ouvrez http://localhost:8000

IMPORTANT : pour installer une PWA sur iPhone ou Windows, le site doit être publié sur une adresse HTTPS. Le lancement local sur iPhone ne fonctionne pas en ouvrant simplement le fichier HTML.

INSTALLATION IPHONE
1. Publier le dossier sur un hébergement HTTPS.
2. Ouvrir l'adresse dans Safari.
3. Toucher Partager, puis Sur l'écran d'accueil.
4. Lancer l'app depuis son icône.
5. Autoriser les notifications si proposées.

INSTALLATION WINDOWS
1. Ouvrir l'adresse HTTPS dans Edge ou Chrome.
2. Choisir Installer cette application dans le menu du navigateur.

DONNÉES ET ALERTES
- Prix, historique et flux temps réel : API publique Binance BTCUSDT.
- RSI 14, EMA 9 et EMA 21 calculés dans le navigateur.
- Signal ACHAT : croisement haussier EMA9/EMA21 avec RSI de confirmation.
- Signal VENTE : croisement baissier EMA9/EMA21 avec RSI de confirmation.
- Les alertes sont déclenchées lorsqu'un nouveau signal apparaît sur les données reçues.
- Aucun ordre n'est envoyé et aucune clé API n'est requise.

LIMITES DE CETTE V1
- L'application doit rester ouverte pour recevoir le flux WebSocket et analyser les signaux.
- Les notifications en arrière-plan sur iPhone exigent une PWA publiée et les conditions iOS compatibles; cette V1 ne contient pas de serveur push.
- Le graphique utilise Lightweight Charts chargé depuis un CDN; une connexion Internet est requise.
- Les signaux sont expérimentaux et ne constituent pas des conseils financiers.
