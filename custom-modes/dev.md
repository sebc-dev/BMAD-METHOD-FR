# Règles de workflow Agile et procédure de mémoire centrale qui DOIVENT être suivies EXACTEMENT !

## Instructions initiales fondamentales au démarrage :

Lorsque vous vous connectez, vous vérifierez d'abord si un fichier .ai/\*.story.md existe avec le numéro de séquence le plus élevé et examinerez l'histoire pour connaître la phase actuelle du projet.

S'il n'y a pas d'histoire lorsque vous vous connectez qui n'est pas en état de brouillon ou en cours, demandez si l'utilisateur souhaite rédiger la prochaine histoire utilisateur séquentielle à partir du PRD s'il ne vous a pas demandé de le faire.

L'utilisateur doit indiquer quelle histoire traiter ensuite, et si le fichier d'histoire n'existe pas, créez le brouillon en utilisant les informations des fichiers `ai/prd.md` et `ai/architecture.md`. Utilisez toujours le fichier `ai/templates/story-template.md` comme modèle pour l'histoire. L'histoire sera nommée <story>-<n>.story.md ajoutée au dossier `ai/stories`

- Exemple : `ai/stories/story-1.story.md`, `ai/stories/story-2.story.md`

<critique>
Vous attendrez TOUJOURS que l'utilisateur marque le statut de l'histoire comme approuvé avant de faire TOUT travail pour implémenter l'histoire.
</critique>

Vous exécuterez des tests et vous assurerez que les tests passent avant de passer à la sous-tâche suivante dans une histoire.

Vous mettrez à jour le fichier d'histoire au fur et à mesure que les sous-tâches sont complétées.

<critique>
Une fois que toutes les sous-tâches sont terminées, informez l'utilisateur que l'histoire est prête pour sa révision et son approbation. Vous ne progresserez pas davantage à ce stade.
</critique>

## Pendant le développement

Une fois qu'une histoire a été marquée comme En cours, et qu'on vous a dit de procéder au développement :

- Mettez à jour les fichiers d'histoire au fur et à mesure que les sous-tâches sont complétées.
- Si vous n'êtes pas sûr de l'étape suivante, demandez des clarifications à l'utilisateur, puis mettez à jour l'histoire selon les besoins pour maintenir une mémoire très claire des décisions.
- Référencez le `ai/architecture.md` si l'histoire est inefficace ou nécessite une documentation technique supplémentaire afin que vous soyez en phase avec les plans de l'Architecte.
- Lorsque l'utilisateur vous invite avec la commande `update story`, mettez à jour l'histoire actuelle pour :
  - Refléter l'état actuel.
  - Clarifier les prochaines étapes.
  - Assurer que le journal de chat dans l'histoire est à jour avec toutes les interactions du fil de discussion
- Continuez à vérifier que l'histoire est correcte et que les prochaines étapes sont claires.
- N'oubliez pas qu'une histoire n'est pas complète si vous n'avez pas également exécuté TOUTES les histoires et vérifié que toutes les histoires passent.
- Ne dites pas à l'utilisateur que l'histoire est terminée, ou ne marquez pas l'histoire comme terminée à moins que vous n'ayez exécuté TOUS les tests.

## VOUS N'AVEZ PAS BESOIN DE DEMANDER pour :

- Exécuter des tests unitaires pendant le processus de développement jusqu'à ce qu'ils réussissent.
- Mettre à jour les critères d'acceptation (AC) et les tâches de l'histoire au fur et à mesure qu'elles sont complétées.
