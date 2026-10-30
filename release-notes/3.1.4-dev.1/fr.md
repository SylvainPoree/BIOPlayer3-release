# BIOPlayer 3.1.4-dev.1

- croisement possible des poignées de découpage
DEBUG
- La présentation de séance et les consignes sont maintenant sauvegardées pendant la saisie, même sans changer de champ. Une frappe continue n'empêche plus l'écriture régulière sur disque.
- Le déplacement d'un exercice conserve sa dernière consigne. Il ne réintroduit plus une ancienne copie du texte au début du glisser-déposer.
- Les consignes restent associées au bon exercice pendant une suppression ou un changement de position, y compris lorsqu'on continue à écrire pendant l'opération.
- Les rechargements de Session, notamment avec R, Ctrl/Cmd+R ou F5, attendent la sauvegarde des dernières consignes.
- La fermeture d'une séance bloque la saisie pendant sa sauvegarde finale. Si la sauvegarde échoue, la fenêtre reste ouverte et redevient modifiable.
- Les réglages de volume et de fondu prennent aussi en compte une consigne en cours de saisie, même après avoir replié un exercice.
- Sauvegarde plus fiable lors de modifications rapides : la dernière modification est conservée, même si une sauvegarde précédente est encore en cours.
- La restauration d'une archive fonctionne aussi quand une seule archive est conservée. L'archive choisie reste utilisable pendant la création de la copie de sécurité.
- Restaurer une séance déjà ouverte recharge maintenant cette séance. Les consignes en cours de saisie sont sauvegardées avant la restauration ; l'ancienne séance ne peut plus écraser la version restaurée. La lecture et l'historique Annuler/Recommencer repartent avec la séance rechargée.
- La copie d'une séance vers un fichier existant fonctionne correctement.
- L'import PDF reconnaît mieux les exercices présentés avec des titres en majuscules.
- Lorsqu'on choisit rapidement plusieurs musiques, la dernière musique demandée reste celle qui se charge, même si une précédente met plus de temps à répondre.
- Certains fichiers M4A au format Apple Lossless sont désormais correctement reconnus pour la lecture.
- Les noms d'exercices contenant des caractères comme `<` ou `>` s'affichent comme du texte, sans modifier la présentation de la séance.
- Une bibliothèque valide n'est plus signalée comme inutilisable simplement parce que ses titres ne contiennent aucun chiffre « 1 ».
- Après une erreur pendant l'indexation ou le choix du dossier de musiques, il est possible de relancer l'opération sans redémarrer BIOPlayer.
- L'ajout de nombreux fichiers à la bibliothèque demande moins de travail à l'ordinateur, tout en conservant les vérifications des conversions FLAC avant suppression des originaux.
- La vérification des musiques introuvables évite les demandes répétées pour un même fichier et ne modifie plus une ancienne liste déjà remplacée à l'écran. Les chemins locaux sont vérifiés directement sur le disque.
- Les outils de création PDF sont chargés au premier export, ce qui allège l'ouverture d'une séance. Le premier PDF peut donc prendre un peu plus de temps ; la création automatique à la fermeture attend aussi la fin du chargement et de l'écriture.
- La recherche de la durée des musiques utilise moins de mémoire, notamment pour les longs fichiers WAV et FLAC. Les fichiers avec une extension incorrecte ou une pochette incorporée restent pris en charge. Certains formats peuvent toujours demander une lecture complète pour déterminer leur durée.
- Lors de l'analyse de nombreux fichiers musicaux, les délais d'attente sont libérés dès que chaque analyse est terminée, ce qui évite de conserver des tâches inutiles.
- BIOAdmin Les demandes de création de compte, de clé oubliée et les opérations de l'outil Admin DB cessent d'attendre après 30 secondes si le service ne répond pas. Une demande expirée n'est pas relancée automatiquement.
- La vérification de connexion referme correctement les requêtes qui expirent et termine la lecture des réponses reçues.

