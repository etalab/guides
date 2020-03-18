---
permalink: /producteurs-schemas/phase-construction
---

# Phase de construction

::: lexique Phase de construction
La phase de construction consiste à implémenter le schéma de données obtenu après la phase de concertation : choisir un standard, renseigner les fichiers requis, les tester et les diffuser.
:::

Durant cette phase, vous devez mobiliser des personnes possédant des compétences techniques. Cette phase consiste à transcrire les décisions prises lors de la phase de concertation dans des schémas en suivant des standards techniques.

## Choisir un standard

::: lexique Standard
On utilise les termes « normes » et « standards » pour décrire un référentiel commun et documenté destiné à harmoniser l’activité d’un secteur.
:::

Il existe plusieurs standards de schémas de données. Le standard est à choisir en fonction de la nature des données concernées et des habitudes de l’écosystème produisant ou réutilisant les données liées au schéma.

Les principaux standards sont les suivants :

- [Table Schema](https://frictionlessdata.io/specs/table-schema/) : schéma au format JSON, permettant de décrire des données tabulaires (sous forme de tableurs ou de CSV) ;
- [JSON Schema](https://json-schema.org) : schéma au format JSON, permettant de décrire des documents JSON ;
- [XML Schema Definition (XSD)](https://www.w3.org/TR/xmlschema11-1/) : schéma au format XML, permettant de décrire des documents XML.

Notez que tous ces standards sont supportés par [schema.data.gouv.fr](https://schema.data.gouv.fr).

::: warning Aller au-delà de la documentation texte
Un modèle de données décrit uniquement par du texte ou par un tableau se prive de nombreux avantages offerts par les schémas.

Les schémas décrits par des standards permettent, en plus d’une documentation textuelle ou sous forme d’un tableau, de valider que des données correspondent à un modèle de données, d’agréger des données similaires, de générer automatiquement des données respectant un schéma.
:::

## Créer votre schéma

Une fois un standard choisi, il faudra créer les fichiers requis pour modéliser vos données. La documentation de chaque standard décrit le contenu des fichiers à renseigner. Reportez-vous aux documentations respectives pour tirer parti des fonctionnalités avancées offertes : types de données et contraintes sur les valeurs en particulier.

Il est souvent possible de vérifier qu’un fichier correspond à un standard à l’aide d’outils en ligne ou en ligne de commande. Utilisez ces outils pour vérifier que vos productions correspondent au standard.

::: tip Exemples à votre disposition
Nous vous conseillons vivement de partir d’un schéma existant. Vous pouvez parcourir des fichiers de schémas sur [schema.data.gouv.fr](https://schema.data.gouv.fr) pour faciliter votre travail. Consultez par exemple [le fichier TableSchema décrivant les lieux de stationnement](https://schema.data.gouv.fr/schemas/etalab/schema-stationnement/latest/schema.json).
:::

## Documenter votre schéma

En complément du fichier du schéma, nous vous conseillons de rédiger a minima deux documents complémentaires :

- **une documentation générale** : vous indiquerez le contexte, les modalités de production des données, le cadre juridique, la finalité, les cas d’usage etc. Ce fichier est traditionnellement rédigé en Markdown et nommé `README.md` ;
- **un fichier répertoriant les changements** : permettant de suivre les modifications, d’une version à une autre. Ce fichier est traditionnellement rédigé en Markdown et nommé `CHANGELOG.md`.

La présence de ces fichiers représente un package complet (documentation, liste des changements et schéma technique), apprécié des réutilisateurs. [schema.data.gouv.fr](https://schema.data.gouv.fr) se repose sur ces éléments pour intégrer votre documentation et votre liste de changements sur une page web.

::: tip Exemples à votre disposition
Vous pouvez consulter [la documentation](https://github.com/etalab/schema-stationnement/blob/master/README.md) et [la liste des changements](https://github.com/etalab/schema-stationnement/blob/master/CHANGELOG.md) du schéma des lieux de stationnement.
:::


## Publier et diffuser votre schéma

Une fois votre schéma créé, il est nécessaire de le publier et de le diffuser pour que d’autres personnes puissent en bénéficier. Nous vous recommandons de publier vos schémas en tant que logiciels libres, sur votre forge de développement ou par le biais de [GitLab](https://about.gitlab.com) ou [GitHub](https://github.com).

Vous bénéficierez alors des avantages habituels des dépôts de code Git en ligne : historique des modifications, fonctionnalités de tickets ou de demandes de modifications. Utilisez un compte d’organisation (dédié à votre entreprise, direction, service, ministère) et non votre compte personnel afin d’assurer une URL stable dans le temps.

::: tip Exemples à votre disposition
Vous trouverez plusieurs dépôts Git de schémas sur [schema.data.gouv.fr](https://schema.data.gouv.fr). Consultez par exemple [le dépôt Git décrivant les lieux de stationnement](https://github.com/etalab/schema-stationnement) à l’aide d’un schéma TableSchema sur GitHub.
:::

## Référencer votre schéma sur schema.data.gouv.fr

Pour faciliter la découverte de votre schéma et des données sous-jacentes, nous vous recommandons de faire référencer votre schéma sur [schema.data.gouv.fr](https://schema.data.gouv.fr). Nous avons rédigé [une page dédiée](4-integration-schema-datagouv.md) à ce sujet décrivant les plus-values, prérequis et démarches à suivre.

## Faire évoluer votre schéma

Une fois votre schéma défini et implémenté, le travail ne s’arrête pas là. Au-delà du besoin de diffusion et de promotion, il est probable que vous deviez faire des modifications : clarifications de la documentation, corrections d’erreurs, évolutions du cadre réglementaire, etc. Autant de raisons où il est nécessaire de mettre en œuvre une nouvelle version.

Posséder un dépôt Git pour votre schéma vous permettra d’avoir plusieurs versions et tags. Notez que [schema.data.gouv.fr](https://schema.data.gouv.fr) supporte plusieurs versions pour un schéma et affiche les modifications effectuées au fur et à mesure, dès lors que ces modifications sont renseignées dans un fichier dédié.

## Points de sortie
À l’issue de cette phase, vous devriez :

- Avoir implémenté votre schéma dans un des standards reconnus ;
- Avoir publié votre travail en ligne, dans un répetoire Git dédié ;
- Avoir pris contact avec les équipes de schema.data.gouv.fr dans le but de référencer votre schéma si nécessaire.