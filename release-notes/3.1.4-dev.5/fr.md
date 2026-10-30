# BIOPlayer 3.1.4-dev.5

- 1.
Corrigé des mises à jour du zoom physiologique
◦
Suppression des notifications renvoyées à la fenêtre qui vient de changer le zoom : elles pouvaient rétablir une ancienne valeur et provoquer un double affichage.
◦
Regroupement des changements arrivant dans une même image d’affichage.
◦
Le zoom reste enregistré dans config.json. Nous n’avons pas ajouté l’enregistrement uniquement au relâchement du slider.
2.
Ajouté un diagnostic temporaire
◦
Journalisation des écritures, fichiers temporaires, erreurs et nouvelles tentatives.
◦
Surveillance indépendante du .toro, qui continue pendant 15 secondes après l’arrêt de BIOPlayer.
◦
Activation automatique dans les versions dev et bêta, avec des traces conservées dans logs.
3.
Corrigé un risque de perte des préférences
◦
Une erreur de relecture de config.json pouvait conduire à réenregistrer les valeurs par défaut.
◦
Désormais, cette sauvegarde est refusée et les données existantes sont conservées. Une demande ultérieure peut réessayer normalement.
Le crash et la disparition du .toro ne sont toujours pas expliqués.
