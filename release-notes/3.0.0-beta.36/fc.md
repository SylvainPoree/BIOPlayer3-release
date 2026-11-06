# Changements principaux

- UI : ajout pis harmonisation du halo lumineux / clignotement sur les notes quand une musique joue.
- UI : affichage en gras quand une musique joue.
- UI : modification du texte d'aide de recherche, qui dépend maintenant des vraies limites maximales selon que la licence est activée ou pas.
- UI : gestion du zoom à l'initialisation.
- UI : zoom au survol des exercices, des icônes crayon pis des autres contrôles.
- DEBUG : correction du décalage du résultat de recherche en lecture lors d'appuis répétés sur Entrée.
- FONC : sans licence active, les interactions restent disponibles pis seule la limite du nombre de musiques par exercice change.
- UI : plus de BIOP / BIOPLayer / Bioplayer visible, seul BIOPlayer reste affiché.
- UI : plus d'émoticônes SMS dans les JSON UI.
- UI : suppression de la restriction de décalage droite-gauche dans la musique jouée.
- FONC : le mode sans licence active limite de nouveau les séances à 5 exercices.
- FONC : la limite du nombre de musiques par exercice dépend maintenant de la licence.
- FONC : les ajouts, duplications, imports pis drops d'exercices respectent maintenant la limite liée à la licence.
- FONC : les séances dépassant la limite autorisée ne peuvent plus être modifiées ni sauvegardées tant que la licence n'est pas active.
- FONC : nouvelle option : centrer la consigne en cours d'édition.
- FONC : un clic sur le nom de la musique jouée retrouve l'origine de cette musique : exercice ou recherche.
- TECH : journalisation de la procédure de mise à jour.
- TECH : modification du mail admin envoyé lors d'une création.
