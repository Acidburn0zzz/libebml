### EBML - Langage de balisage binaire extensible

EBML a été conçu pour être une extension binaire simplifiée de XML dans le but de stocker et de manipuler des données sous une forme hiérarchique avec des longueurs de champs variables.

Il utilise les mêmes paradigmes que les fichiers XML, ce qui signifie que la syntaxe et la sémantique sont séparées. Une bibliothèque EBML générique peut donc lire n’importe quel format basé sur celle-ci. L'interprétation des données dépend d'une application spécifique qui sait comment chaque élément (équivalent d'une balise XML) doit être traité.

Parmi tous les avantages de XML, il existe quelques limitations par rapport à ce que XML peut réaliser:

- Il n'existe actuellement aucun équivalent à une DTD ou à un schéma pour définir les éléments connus d'un document. Mais nous prévoyons d'ajouter un tel niveau.
- Aucune entité ne peut être définie, c'est-à-dire un élément qui serait remplacé par un autre contenu. Nous n'avons pas l'intention d'ajouter quelque chose comme ça pour l'instant.
- Pas d'inclusion externe d'autres fichiers (tels que CSS, images, etc.). Il pourrait facilement être ajouté en tant qu'élément "propriétaire" (non défini dans le format EBML de base).

Pour le reste, vous avez tous les avantages comme:

- Compatibilité ascendante lorsque le format est mis à jour. Quelque chose de rare dans les formats binaires, à moins que vous n'ayez de l'espace inutilisé dans le format d'origine.
- Taille illimitée des données binaires.
- Très efficace en termes de taille: seul l’espace requis pour une donnée est écrit (sauf si vous avez spécifiquement besoin de plus d’espace pour une meilleure mise à jour ultérieure).

Il existe également un inconvénient commun à propos de XML: il est très prolixe. C'est pourquoi vous devriez avoir autant que possible des valeurs par défaut / supposées dans votre format basé sur EBML. Donc, vous venez de décrire ce qui est vraiment nécessaire.

EBML a été créé à l'origine pour le projet [Matroska] (http://www.matroska.org). C'est donc naturellement le premier format basé sur EBML à exister. Nous vous encourageons donc à vérifier les spécifications pour savoir comment concevoir un format basé sur EBML.
