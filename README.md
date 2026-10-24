# Zone Rouge

Jeu en monde ouvert style GTA, en 3D dans le navigateur (Three.js). Il tourne sur ordinateur, téléphone et iPad.

## Jouer

- **En ligne** : active GitHub Pages sur ce dépôt (voir plus bas) et ouvre le lien.
- **En local** : ouvre `index.html` dans un navigateur récent (Chrome, Safari, Edge, Firefox). Une connexion internet est nécessaire au premier lancement, car les bibliothèques 3D sont chargées depuis un CDN.

## Contrôles

| Action | Clavier | Tactile |
|---|---|---|
| Se déplacer / conduire | Z Q S D ou W A S D | Joystick / volant |
| Action, monter en voiture | F ou E | ACTION |
| Sauter, frein à main | Espace | SAUTER / FREIN À MAIN |
| Courir | Shift | COURIR |
| S'accroupir | Ctrl gauche ou X | ACCROUPI |
| Esquiver | Q ou Alt | ESQUIVE |
| Nitro | N | NITRO |
| Zoom caméra | C | — |
| Carte | M | — |
| Carabine de chasse / appeau | K / L | — |
| Zoom lunette / retenir son souffle | molette ou + et − / Shift | ZOOM / SOUFFLE |
| Menu | P ou Échap | — |

## Contenu

- Grande ville avec quartiers, plage, îles, montagnes, rocade et autoroutes
- Campagne autour de la ville : village des Granges, hameau, deux fermes (vaches, champs, silo), station-service du Col
- Chasse dans les montagnes : cerfs, biches, sangliers, renards et ours avec vue, ouïe et odorat (vent), carabine à lunette ×4 à ×12, balistique, appeau, pavillon de chasse et tableau de chasse
- Missions d'histoire, braquages (approche furtive ou bourrin), guerres de gangs
- Voitures, motos, bateaux, hélicoptères, avions et parachute
- Drift avec score et combos, courses de rue, Neon Karting (kart ou moto), démolition derby
- Infiltration : champ de vision des gardes, éliminations silencieuses, caméras de surveillance
- Casino, bowling, stand de tir, salle de sport, bourse, appartement, garage et tuning
- Météo, saisons, cycle jour/nuit, radio
- 5 emplacements de sauvegarde (stockés dans le navigateur)

## Mettre le jeu en ligne avec GitHub Pages

1. Dépose `index.html` et `README.md` à la racine du dépôt.
2. Va dans **Settings → Pages**.
3. Dans **Source**, choisis **Deploy from a branch**, puis la branche `main` et le dossier `/ (root)`.
4. Enregistre. Au bout d'une minute ou deux, le jeu est disponible à l'adresse `https://<ton-pseudo>.github.io/<nom-du-depot>/`.

## Notes techniques

- Tout le jeu tient dans un seul fichier `index.html` (code, textures et modèles intégrés).
- Bibliothèques chargées depuis un CDN : Three.js r128 (avec post-traitement et GLTFLoader) et Cannon.js 0.6.2 pour la physique.
- Les sauvegardes utilisent le `localStorage` du navigateur. Elles restent sur l'appareil et ne sont pas partagées entre deux navigateurs.
- Multijoueur (jusqu'à 4 joueurs) : l'hôte crée une partie et reçoit un code de 5 caractères, ses potes le tapent pour rejoindre. La mise en relation passe par le service gratuit PeerJS, puis les appareils se parlent directement (WebRTC). Si ce service est inaccessible, le jeu propose un mode « codes longs » qui marche sans aucun service.
