# Conventions de Commit

Nous suivons la spécification [Conventional Commits](https://www.conventionalcommits.org/) :

```
<type>[scope optionnel]: <description>

[corps optionnel]

[footer(s) optionnel(s)]
```

## Les types incluent :

- feat : Une nouvelle fonctionnalité
- fix : Une correction de bug
- docs : Changements de documentation
- style : Changements qui n'affectent pas la signification du code
- refactor : Changements de code qui ne corrigent pas un bug et n'ajoutent pas de fonctionnalité
- perf : Améliorations de performance
- test : Ajout ou correction de tests
- chore : Changements dans le processus de build ou les outils auxiliaires

## Exemples :

- `feat: ajouter un système d'authentification utilisateur`
- `fix: résoudre le problème de non-chargement des données`
- `docs: mettre à jour les instructions d'installation`

## Règles pour les Agents IA

<rules>
- Toujours exécuter `git add .` depuis la racine de l'espace de travail pour indexer les changements
- Vérifier les changements indexés avant de commiter pour s'assurer qu'aucun fichier non intentionnel n'est inclus
- Formater les titres de commit comme `type: brève description` où le type est l'un des suivants :
  - feat : nouvelle fonctionnalité
  - fix : correction de bug
  - docs : changements de documentation
  - style : formatage, points-virgules manquants, etc.
  - refactor : restructuration de code
  - test : ajout de tests
  - chore : tâches de maintenance
- Garder le titre de commit bref et descriptif (max 72 caractères)
- Ajouter deux sauts de ligne après le titre du commit
- Inclure un paragraphe détaillé expliquant :
  - Quels changements ont été effectués
  - Pourquoi les changements étaient nécessaires
  - Tous les détails d'implémentation importants
- Terminer le message de commit par " -Message de Commit Généré par Agent"
- Pousser les changements vers la branche distante actuelle
</rules>
