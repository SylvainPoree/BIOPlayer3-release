# BIOPlayer 3.1.4-dev.3

- Version temporaire etude du pb avec kdrive, tentative d'amélioration à bas niveau (écritures fichiers)
  Ainsi si on constate que cela supprime le bug, on supprime d'autres bugs en d'autres circonstances d'écriture intense
- Amélioration des Logs : modification qui vont rester sauf pb
  Niveau de log appliqué immédiatement, sans redémarrage.
  Consoles centralisées, objets et piles d’appels conservés.
  Traces d’ouverture, sauvegarde et lecture audio ajoutées.
  Diagnostics de crash locaux et détection d’un arrêt anormal au lancement suivant.
  Conservation de cinq archives du journal.
- à venir ensuite amélioration de l'enregistrement quand déplacement des points et zoom
