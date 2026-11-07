# Changements principaux

- UI : Amélioration du repérage de la musique en cours de lecture (note de musique) dans la séance et dans les résultats de recherche.
- UI : Amélioration de l'aspect visuel de la manette.
- UI : Suppression du reste de code de boule de chargement oscillante dans l'écran Fusion.
- DEBUG : Correction de zones invisibles qui pouvaient intercepter des clics sur l'écran d'accueil : il est maintenant possible de cliquer sur les drapeaux et les boutons même quand Kiki ou -BIOPlayer- sont dessus.
- FONC : Amélioration de la récupération d'identifiant : une clé de licence manquante est générée automatiquement si le compte utilisait encore la valeur temporaire `000-000-000`.
- TECH : Amélioration de la publication des notes de mise à jour GitHub Pages, sans dépendance à `rsync`.
- TECH : Séparation des installateurs Windows par canal : `BIOPlayer`, `BIOPlayer Beta` et `BIOPlayer Dev` peuvent maintenant cohabiter sur le même poste.
- UI : Correction du champ éditeur Windows : il reste `BIOPlayer` pour tous les canaux.
