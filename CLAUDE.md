# Règles de travail pour l'IA

Ce projet suit la méthode « specs d'abord ». Les specs sont dans `spec/` et font foi.

## Avant de coder
- Lis `spec/requirements.md`, `spec/design.md` et `spec/tasks.md` en entier.
- Construis uniquement les tâches demandées par l'utilisateur. S'il n'en nomme aucune, propose la
  prochaine tâche non cochée du jalon en cours et attends son accord.
- Si la spec est floue ou contradictoire, dis-le avec les ids concernés au lieu d'inventer.

## Pendant le build
- N'ajoute rien que la spec ne demande pas. Une idée qui te semble utile va dans « Idées pour plus
  tard » de `requirements.md`, pas dans le code.
- Toutes les valeurs d'équilibrage (coûts, points de vie, dégâts, vitesses, bonus) vont dans le
  fichier de données prévu par la section Technique de `design.md`.
- Écris les tests automatiques prévus par les sous-tâches « test ».
- Après chaque lot : lance les tests et le jeu, et corrige ce qui casse.

## Après le build
- Coche dans `spec/tasks.md` uniquement les sous-tâches terminées et vérifiées. Ne coche jamais la
  tâche « Vérification du jalon » : elle appartient à l'utilisateur.
- Fais un rapport court : ce qui marche, les tâches cochées, ce qui reste, et 3 à 5 lignes du plan
  de test à essayer.

## Une demande de changement
Toute modification du jeu passe d'abord par les specs :
1. Mets à jour l'exigence, la section du design et sa ligne du plan de test.
2. Décoche la tâche touchée et ajoute une sous-tâche qui décrit le changement.
3. Montre ce qui change et attends la validation avant de coder.

Exception : un bug où le jeu ne fait pas ce que la spec dit déjà. Ajoute seulement la sous-tâche
de correction, puis corrige.
