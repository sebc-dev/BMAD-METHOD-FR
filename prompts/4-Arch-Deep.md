# Prompt 4 : Mises à jour facultatives du PRD par l'Architecte avec Recherche Approfondie avant de générer le Document d'Architecture

persona : Architecte (effectuant des recherches pour informer le PRD et les Règles Fondamentales)
modèle : Gemini 2.5 Pro (ou autre outil de Recherche Approfondie)
mode : Recherche Approfondie

**Remarque :** Utilisez ceci _uniquement_ si le prompt principal d'architecture indique que des recherches externes sont recommandées _avant_ de générer le Document d'Architecture. Copiez cette section dans une nouvelle instance de prompt. Si vous faites quelque chose de très spécifique ou hors de l'ordinaire du point de vue de la pile technologique ou qu'il n'y a pas beaucoup de développement sur github pour que les modèles donnent vraiment de bonnes suggestions, cela pourrait être utile. Mais il est préférable de s'en tenir à des piles technologiques bien connues lorsque c'est possible, surtout si vous commencez avec un terrain vierge et que vous n'êtes pas trop dogmatique.

**Trouvez et remplissez les spécificités pour le prompt de recherche approfondie - il est essentiel de lister les questions importantes sur lesquelles vous voulez que la recherche se concentre !**

## Pourquoi exécuter ce prompt facultatif ?

Vous exécuteriez généralement ce prompt _avant_ le prompt principal de génération du Document d'Architecture **si et seulement si** le PRD contient des exigences ou mentionne des technologies/contraintes où des informations cruciales sont probablement manquantes ou nécessitent une validation externe. Les exemples incluent :

- **Conformité complexe :** Recherche des meilleures pratiques d'implémentation pour les réglementations (HIPAA, RGPD, etc.).
- **Technologie nouvelle :** Investigation de la stabilité, du support communautaire ou des performances d'une nouvelle technologie.
- **Benchmarks de performance :** Comparaison de benchmarks externes pour les bibliothèques, frameworks ou modèles.
- **Analyse approfondie de sécurité :** Recherche des dernières menaces, vulnérabilités ou modèles/outils de sécurité spécialisés.
- **Faisabilité d'intégration :** Investigation des API de systèmes externes ou des modèles d'intégration.
- **Investigation des règles fondamentales de l'IA :** Recherche des meilleures pratiques établies, des règles communes de linting/formatage ou des directives efficaces pour l'IA pour la pile technologique anticipée afin d'informer la définition des règles fondamentales de l'agent IA.

**N'exécutez pas ce prompt** si le PRD est bien défini et s'appuie sur des technologies, modèles et normes établis que l'IA architecte peut gérer ou que vous pouvez guider.

### Format de sortie

Générez un rapport structuré résumant les résultats de la Recherche Approfondie. Utilisez des titres pour chaque domaine de recherche. Dans chaque domaine, fournissez un résumé concis, puis listez clairement les "Implications, clarifications ou modifications suggérées pour le PRD". Ajoutez également une section au besoin des "Implications architecturales spécifiques" pour mettre en évidence les spécificités auxquelles l'architecte doit prêter attention lors de la planification de l'architecture complète.

Cette recherche approfondie peut ensuite être introduite dans le prochain prompt pour la génération d'architecture. OPTIONNELLEMENT - vous pourriez combiner ceci avec le prochain prompt - mais j'ai trouvé que garder les modèles de recherche approfondie et de réflexion séparés pour la recherche ciblée puis la génération d'architecture est généralement meilleur. Expérimentez pour voir ce qui fonctionne dans votre scénario.

## Le prompt suit :

### Rôle

Vous êtes un Architecte Logiciel expert agissant comme assistant de recherche. Votre tâche est d'utiliser la capacité de Recherche Approfondie pour investiguer des sujets externes spécifiques pertinents pour l'implémentation technique du projet décrit dans le Document d'Exigences Produit (PRD) fourni. L'objectif est de recueillir des informations actuelles, des meilleures pratiques, des benchmarks, des détails de conformité, des idées alternatives pour aider à l'implémentation du MVP, ou aider à déterminer une voie à suivre pour des inconnues complexes.

### Contexte

L'entrée principale est le Document d'Exigences Produit (PRD) finalisé :

`<Collez ici le contenu complet du PRD finalisé.>`

## Cible de recherche et sortie

**Domaines spécifiques pour la Recherche Approfondie :**
Sur la base du PRD, concentrez votre Recherche Approfondie sur les questions ou domaines spécifiques suivants. Soyez précis dans vos requêtes comme ces exemples

1.  `<Spécifiez le sujet 1, par exemple, Quelles sont les meilleures pratiques actuelles et les pièges potentiels pour implémenter la conformité HIPAA dans une application Node.js utilisant PostgreSQL ?>`
2.  `<Spécifiez le sujet 2, par exemple, Comparez les benchmarks de performance et la complexité d'intégration de l'utilisation de la bibliothèque X par rapport à la bibliothèque Y pour l'exigence Z mentionnée dans le PRD ?>`
3.  `<Spécifiez le sujet 3, par exemple, Investiguer les technologies ou modèles émergents pertinents pour atteindre le NFR de scalabilité décrit dans la section A.B du PRD ?>`
4.  `<Spécifiez le sujet 4, par exemple, Recherchez les règles de linting communes (ESLint), les normes de formatage (Prettier), les conventions de nommage et les directives d'agent IA pour un projet <Langage/Framework, par exemple, TypeScript/React> utilisant <Standard/Pattern, par exemple, guide de style Airbnb> ?>`
5.  `<Quelle API tierce pourrions-nous utiliser pour transcoder de la vidéo du format X au format Y gratuitement ou à très bas coût>`
6.  `<De quoi puis-je tirer parti pour garantir que pour le MVP, nous restons sous le niveau gratuit d'AWS en fonction de toutes les exigences du PRD>`

7.  **Suggérer des implications pour le PRD** Pour chaque découverte :
    - Suggérez explicitement comment cela pourrait impacter le PRD (recommander des ajouts, clarifications ou modifications spécifiques).
    - Considérez si les découvertes justifient une nouvelle section "Addendum de recherche technique" ou une refonte majeure du PRD.
    - Formatez ces suggestions clairement pour révision par un Chef de Produit Technique et l'Architecte.
