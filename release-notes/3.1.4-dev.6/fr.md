# BIOPlayer 3.1.4-dev.6

- Ajout de copier coller dans exercices et musiques
- Révision des menus contextuels
- Mise en paramètre la notion d'ouvrir dans une deuxième fenêtre
- Diverses améliorations de l'affichage
# Journal simplifié des modifications

Date : 29 octobre 2026.

Ce journal résume les modifications réalisées dans cette conversation. Il ne couvre pas les autres changements déjà présents dans le projet.

## 1. Analyse des avertissements npm

Identification des bibliothèques responsables des avertissements et distinction entre les outils de fabrication et les fonctions utilisées dans BioPlayer.

Les dépendances indirectes n'ont pas été remplacées de force pour masquer les avertissements.

## 2. Mise à jour de l'import PDF

- Une protection contre l'utilisation d'`eval` a d'abord été ajoutée à l'ancienne version de PDF.js.
- PDF.js a ensuite été mis à jour de **3.11.174 à 6.4.299**. Cette version supprime le mécanisme concerné ; l'ancien paramètre de protection a donc été retiré lors de la migration.
- Adaptation des imports JavaScript, du chargement du worker et de la libération des ressources après conversion.
- Mise à jour des workflows de fabrication Mac et Linux vers **Node.js 22**, et indication du minimum Node.js 22.13 dans le README.
- Vérification de l'import de texte et du JSON intégré aux PDF BioPlayer, y compris sans moteur graphique natif disponible.

## 3. Correction de l'import PDF vers TORO

Le test avec le PDF fourni et un PDF généré par BioPlayer a révélé un défaut : l'import ajoutait `.toro` au nom interne de la séance. À l'ouverture, ce nom était ensuite ajouté à la description.

- Correction du nom interne pour éviter cette modification de la description.
- Vérification des quatre exercices du PDF fourni.
- Ajout d'un test de non-régression : export d'une séance en PDF, import par le menu, puis comparaison du fichier TORO restauré avec l'original.
- Résultat : fichiers identiques octet pour octet pour le cas testé avec le même nom de fichier, y compris musiques, réglages et champs supplémentaires.

## 4. Suppression de fluent-ffmpeg

- Suppression de **fluent-ffmpeg 2.1.3** et de ses dépendances exclusives.
- Remplacement de la conversion active vers FLAC par un appel direct au FFmpeg déjà fourni avec BioPlayer.
- Suppression d'une ancienne conversion qui était commentée.
- Conservation des options de transfert des métadonnées et des chapitres.
- Correction de la réutilisation des conversions en cours et du calcul du chemin de sortie.
- Tests des erreurs, des réessais, des chemins particuliers et de plusieurs formats audio. Les échantillons audio décodés sont identiques avant et après les conversions sans perte testées.

## 5. Suppression d'electron-rebuild

Suppression d'**electron-rebuild 3.2.9**, après vérification qu'aucun script du projet ne l'appelait.

Cette suppression a éliminé plusieurs anciennes dépendances et leurs avertissements. La compilation et la préparation de l'application ont été vérifiées.

## 6. Mise à jour des outils de fabrication

- Passage d'**electron-builder 24.13.3 à 26.18.0**.
- Verrouillage explicite d'**Electron à 37.10.3**, également dans la configuration de fabrication.
- Adaptation des options de signature Windows pour BioPlayer et Admin DB.
- Passage de `tar` à **7.5.22** ; ce paquet n'est plus signalé par l'audit réalisé après migration.
- Génération des deux installateurs Windows de test, sans signature ni publication.
- Vérification du véritable exécutable BioPlayer emballé et des métadonnées de mise à jour.

La cible minimale Mac reste **macOS 11 Big Sur**.

## 7. Mise à jour de la génération PDF

- Passage de **pdfmake 0.2.23 à 0.3.13**, avec PDFKit 0.20.2.
- Suppression de `jpeg-exif`, `crypto-js` et des anciens forks PDFKit associés.
- Adaptation de la génération PDF à l'API utilisant des promesses.
- Mise à jour des bibliothèques chargées par l'interface et des polices intégrées.
- Traitement des erreurs de génération et prévention d'une écriture tardive après expiration du délai.
- Vérification du texte, des accents, du gras, de l'italique, des courbes, des durées et du JSON intégré.
- Contrôle visuel d'un PDF d'exemple et tests dans l'application Windows emballée.

## Situation à la fin de cette conversation

**Electron reste en version 37.10.3. Aucune publication n'a été effectuée.**

Cinq avertissements de dépréciation restent présents dans le verrou :

- `boolean@3.2.0`
- `glob@7.2.3`
- `inflight@1.0.6`
- `lodash.isequal@4.5.0`
- `rimraf@2.6.3`

D'autres alertes de sécurité subsistent dans l'audit ; les modifications ne constituent pas un traitement complet de toutes les dépendances.

Les tests réalisés ici sont principalement sous Windows. Restent à vérifier avant livraison : installation et mise à jour sur une machine Windows de test, fabrication du paquet Mac universel et fonctionnement sur un véritable Mac Big Sur.

Des essais isolés de démarrage Electron ont provoqué des plantages natifs pendant la conversation. Leur cause interne précise n'a pas été établie. Les validations suivantes avec le lancement habituel et le véritable exécutable emballé ont réussi sans reproduire ces plantages.

## Rapports détaillés

- [Validation electron-builder 26](validation-electron-builder-26.md)
- [Validation pdfmake 0.3](validation-pdfmake-0.3.md)

- Pendant la modification directe d'un nom d'exercice, les caractères comme `<`, `>` et `&` restent affichés tels qu'ils ont été saisis.
- Les informations affichées au survol d'une musique restent du texte, même si les tags du fichier contiennent des balises.
- Après plusieurs demandes de lecture rapprochées, seule la dernière est prise en compte. Une réponse tardive ne relance plus une musique après un arrêt ou une pause.
- Le remplacement d'une musique introuvable reste associé au bon exercice, même s'il est déplacé pendant la recherche. Les réglages de découpage, de volume et de fondu modifiés entre-temps sont conservés.
- Si les préférences ne peuvent pas être enregistrées, un message visible permet de réessayer sans quitter BIOPlayer.
- Toutes les archives conservées sont proposées pour la restauration, y compris au-delà des 30 plus récentes.
- Une archive dont le contenu n'est pas une séance valide est refusée avant de remplacer le fichier courant. Les anciens formats restent acceptés.
- Si une fenêtre Session plante alors que BIOPlayer fonctionne encore, les dernières modifications déjà reçues sont sauvegardées avant de fermer cette fenêtre.
- Dans l'administration mobile, supprimer un utilisateur ne retire plus un autre utilisateur de la liste si la sélection change pendant l'attente. Les actions incompatibles sont bloquées pendant cette suppression.
- Un double clic rapide sur la suppression d'une musique ne supprime plus deux morceaux.
- Une erreur de relecture des préférences conserve les réglages en cours, notamment le choix de créer automatiquement un PDF, et permet de réessayer.
- Les fichiers de séance conservent leurs majuscules et minuscules à l'ouverture. Deux fichiers réellement différents ne sont plus confondus sur les disques qui distinguent ces caractères ; un même fichier reste protégé contre les doubles ouvertures.
- Les archives créées avec l'ancien chemin en minuscules restent accessibles lorsqu'elles concernent la même séance. Les copies de récupération restent séparées pour les fichiers distincts.
- La mise à jour d'une grande bibliothèque limite le nombre de vérifications de fichiers simultanées pour éviter de surcharger l'ordinateur ou le disque.
- Les sauvegardes évitent de relire inutilement la copie originale de récupération. Les copies de sécurité et la vérification de la séance enregistrée sont conservées.
- À l'ouverture d'une séance, les demandes rapprochées partagent le chargement de la bibliothèque. Une mise à jour de l'index depuis les options reste bien prise en compte, même pendant ce chargement.
- Les recherches successives dans une grande bibliothèque sont plus rapides grâce à la réutilisation du texte déjà préparé. Les accents, les expressions entre guillemets, les exclusions et les bibliothèques sélectionnées gardent le même fonctionnement. Les changements de critères et les mises à jour de l'index restent pris en compte.
- Les niveaux de journalisation sont pris en compte avant de préparer et transférer les messages de diagnostic, ce qui évite du travail inutile lorsque seules les erreurs sont demandées.
- Un changement du niveau de journalisation s'applique aussi aux fenêtres déjà ouvertes, sans redémarrage. Les erreurs utiles et les diagnostics de démarrage sont conservés.
- Si une musique ne peut pas être chargée ou lue, un message près du lecteur indique le nom et l'emplacement du fichier, avec un bouton « Réessayer ». Le lecteur revient à l'arrêt et l'indicateur de préparation disparaît.
- La nouvelle tentative relit le fichier concerné. Choisir une autre musique ou arrêter la lecture empêche une ancienne erreur de relancer le mauvais morceau. Le bouton de lecture permet aussi de réessayer la musique en échec.
- Essai : pendant les calculs de raccords, un seul message « Préparation des raccords… » reste affiché avec un indicateur d'activité, sans pourcentage ni changement de texte. Il est possible d'annuler cette préparation.
- Le spectre se dessine sans message ni commande de progression supplémentaires. Les traitements courts n'affichent pas de nouveau message.

