# La Méthode BMad Code pour le Workflow Collaboratif Humain-Agent dans la Réalisation de Produits et le Développement Logiciel

**Breakthrough Method Agile-Ai Driven-Development (BMAD)**

Rejoignez-nous sur le [Forum de Discussion Communautaire](https://github.com/bmadcode/BMAD-METHOD/discussions), contribuez, faites évoluer et améliorez les idées présentées ici. Cette méthode est indépendante de l'IDE et fonctionne parfaitement avec Cursor, Cline, RooCode, Augment et Aider ! Si vous disposez d'un agent intelligent, cela vous aidera à le maîtriser et à maintenir une dynamique positive !

Consultez également [la Partie 1 sur la chaîne YouTube BMad Code](https://youtu.be/JbhiLUY_V2U) - n'hésitez pas à commenter, aimer et vous abonner pour recevoir les futures vidéos et mises à jour.

Remarque : Selon l'outil que vous utilisez, le dossier [[prompts]](./ai-pm/prompts/) devrait être configuré pour être ignoré par l'indexation de votre base de code LLM (par exemple, avec Cursor, ajoutez-les à .cursorindexingignore - cela peut différer pour Cline et Roo).

## Aperçu général

La Méthode BMad est une approche (pas si) révolutionnaire du développement logiciel qui exploite des processus basés sur l'IA pour accélérer et améliorer l'ensemble du cycle de vie du développement de produits, de l'idéation et de l'adéquation au marché jusqu'à l'implémentation du code par les agents.

Cette méthode se veut indépendante des outils et inclut un flux de travail intégré dans les prompts de rôle. Il s'agit d'un workflow quelque peu manuel qui peut être utilisé de plusieurs façons.

Elle peut facilement être adaptée aux spécificités de n'importe quel ensemble d'outils de codage basé sur des agents, IDE ou plateforme.

## Qu'est-ce que la Méthode BMad ?

La Méthode BMad est une approche complète et étape par étape qui transforme une idée de produit en une application entièrement implémentée via une chaîne de prompts agile en :

1. Structurant le processus de développement en phases distinctes basées sur des personas IA
2. Générant des artefacts détaillés à chaque phase
3. Utilisant un flux de travail séquentiel pour suivre la progression
4. Permettant à l'IA de coder l'application complète sur la base de spécifications générées qui sont granulaires et détaillées, vous préparant ainsi au succès maximal.

## Premiers pas

### Prérequis

- Un assistant IA capable d'utiliser ces prompts (Claude, GPT-4, Gemini, etc.)
- Optionnel - Recommandé : Accès à une IA de Recherche Approfondie
- Connaissance de base de Cursor / Cline / Roo / CoPilot Agent
- Une idée de produit ou de projet logiciel que vous souhaitez construire avec l'IA

### Flux de travail

La Méthode BMad suit un flux de travail structuré :

1. **De l'idée à la documentation** : Utilisez les prompts dans l'ordre pour générer toute la documentation nécessaire au projet
2. **Règles de l'agent** : Les résultats des prompts recommanderont un ensemble de règles de base si vous le souhaitez.
3. **Suivi de progression de type Kanban** : Déplacez les artefacts générés à travers les dossiers :
   - `1-ToDo` : Histoires ordonnées séquentiellement en attente d'implémentation
   - `2-InProgress` : Histoires en cours d'implémentation
   - `3-Done` : Histoires terminées

## Séquence de prompts

Le dossier `prompts` contient des prompts soigneusement élaborés pour chaque phase du développement.
Ceci est destiné au projet MVP le plus ambitieux

1. **Assistant de recherche : Analyse** (`0-research-assistant.md`) : Recherche approfondie optionnelle sur votre concept de produit
2. **Analyste d'affaires : Brief du projet** (`1-business-analyst.md`) : Définir votre idée de produit et la portée du MVP
3. **Chef de produit : PRD** (`2-PM.md`) : Créer des exigences détaillées pour le produit
4. **PM/UX/UI : Prompt de génération d'UI** (`3-PM-UX-Ui.md`) : Définir des spécifications complètes d'UI/UX
5. **Recherche architecturale approfondie : Mises à jour du PRD** (`4-Arch-Deep.md`) : Étape de recherche approfondie optionnelle pour générer des pratiques et règles à jour
6. **Architecte : Document d'architecture** (`5-Arch.md`) : Créer un plan architectural détaillé
7. **Propriétaire technique du produit : Liste d'épopées** (`6-PO.md`) : Décomposer les exigences en histoires implémentables
8. **Scrum Master technique : Fichiers d'histoires pour agents** (`7-SM.md`) : Transformer les histoires en histoires super détaillées prêtes pour les agents de développement (il n'est pas recommandé de générer toutes les histoires avec ceci dès le début - privilégiez plutôt l'utilisation de l'agent /role-prompts/dev.md avec un flux de travail intégré pour élaborer les histoires une par une selon les besoins d'implémentation.)

## Avantages clés

- **Économisez du temps et de l'argent** : Flux d'implémentation prévisible avec moins de retravail coûteux ou de consommation de crédits d'agent que produit le codage improvisé
- **Documentation cohérente** : Générez des artefacts complets et alignés
- **Flux de travail optimisé pour l'IA** : Histoires Kanban structurées spécifiquement conçues pour l'implémentation humaine ou par IA
- **Dette technique réduite** : Assurez la cohérence architecturale dès le départ
- **Collaboration simplifiée** : Artefacts clairs pour toutes les parties prenantes, humaines et IA

## Comment faire

Il est recommandé de consulter cette série de vidéos en commençant par [la Partie 1 sur la chaîne YouTube BMad Code](https://youtu.be/JbhiLUY_V2U) et également de consulter le [Forum de Discussion](https://github.com/bmadcode/BMAD-METHOD/discussions) dans les prochains jours où BMad et la communauté partageront et collaboreront, nous l'espérons, et fourniront d'autres ajustements, conseils et astuces !

Mais la **méthode rapide** est :

1. Clonez ce projet
2. Commencez par le premier prompt dans `prompts/0-research-assistant.md` (ou passez au 1 si la recherche n'est pas nécessaire) pour faire une étude de marché avec les capacités de recherche approfondie d'un LLM
3. Suivez chaque prompt dans l'ordre, en fournissant les résultats des étapes précédentes comme contexte au nouveau prompt lorsque cela est indiqué dans le prompt actuel
4. Une fois que le PO a généré la liste finale d'histoires, collez-la dans le PRD.
5. Générez chaque histoire utilisateur détaillée et implémentez-les une par une. Les histoires servent de système de mémoire et d'historique du développement agile incrémental.
6. Suivez la progression jusqu'à ce que toutes les histoires soient terminées pour réaliser le MVP.

Ma recommandation est de profiter des applications web Google Gemini ou ChatGPT pour la génération de brainstorming de recherche approfondie, du PRD, et de la recherche approfondie pour l'architecture si nécessaire. Au-delà de cela, il est assez facile de prendre les éléments d'artefacts nécessaires pour mettre le markdown dans le dossier ai du projet, puis d'utiliser des prompts depuis l'IDE pour générer l'architecture des fichiers, les mises à jour de la liste d'histoires dans le PRD par le PO, et éventuellement la génération d'histoires.

## Modifications

Ce n'est qu'une idée de ce qui fonctionne pour moi pour construire de façon incrémentale des applications complexes de l'idée à la création. Mais j'utilise des variantes de cette méthode pour travailler sur des bases de code existantes, où je vais mettre en place un PRD avec des listes de tâches et utiliser le document d'architecture pour mettre en place des garde-fous et des détails supplémentaires dont le LLM a besoin pour comprendre, s'ils ne sont pas déjà en place.

Le partage de tous ces prompts ne sont que des suggestions - je vous recommande FORTEMENT d'utiliser ces idées pour ajuster et affiner ce qui fonctionne pour vous ! Expérimentez avec différents modèles, et avec le temps, ils s'amélioreront.

Pour les petits projets, un PRD et les fichiers d'histoires peuvent être plus que suffisants. Et pour les projets plus ambitieux ou comportant des inconnues, utilisez l'étape de brainstorming et de recherche approfondie pour vous aider.

Les artefacts valides pour l'application tels que les arborescences sources, les règles, la documentation d'architecture peuvent fournir une valeur au-delà de l'implémentation initiale de la tâche en cours et peuvent vivre avec le projet, généralement déplacés dans le dossier docs, et les règles peuvent également être ajoutées à CONTRIBUTING.md. En mettant les règles dans ce fichier, il peut être utilisé par les humains et les outils d'IA.

Par exemple, dans Cursor, avec un bon fichier contributing, vous pouvez avoir une règle permanente pour toujours référencer le fichier contributing.md pour son ensemble de règles de base. Et ensuite, si vous utilisez Cline ou CoPilot, vous pouvez faire de même avec leurs systèmes de règles ou instructions personnalisées d'agent.

## Améliorations futures

1. Outil Méthode BMad
2. Gems améliorés
3. Version MCP si vous souhaitez tout faire au sein de l'IDE
4. Intégration Jira optionnelle
5. Intégration Trello optionnelle

## Contribution

Intéressé à améliorer la Méthode BMad ? Consultez nos [directives de contribution](CONTRIBUTING.md).

## Licence

[Inclure ici les informations de licence appropriées]
