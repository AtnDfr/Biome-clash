# Guide : créer un jeu avec la méthode « specs d'abord »

Ce kit reprend la méthode de l'atelier (spec-driven coding) et l'adapte à un vrai projet de jeu.
Le principe ne change pas : **on écrit ce qu'on veut, on le valide, puis on le construit.** Les specs
sont la mémoire du projet, pour toi comme pour l'IA qui code avec toi.

## Les fichiers

| Fichier | Rôle | Quand le modifier |
|---|---|---|
| `spec/requirements.md` | La vision et **ce que le jeu doit faire** | À chaque nouvelle idée ou règle |
| `spec/design.md` | **Comment** le jeu fonctionne : règles, contenu, technique | À chaque décision de conception |
| `spec/tasks.md` | **L'ordre de construction**, par jalons jouables | À chaque nouveau jalon ou changement |
| `spec/decisions.md` | Le journal des décisions importantes et de leur raison | Quand tu tranches un choix difficile |
| `CLAUDE.md` | Les règles de travail pour l'IA (copie de `AI-INSTRUCTIONS.md`) | Rarement |

Les modèles sont dans `templates/`. Copie-les dans un dossier `spec/` à la racine de ton projet.

## Les priorités

Chaque exigence a une **priorité** :

- `Proto` : le strict nécessaire pour vérifier que l'idée est amusante. Formes simples, aucun menu.
- `MVP` : le premier jeu complet que quelqu'un d'autre peut tester du début à la fin.
- `v1` : la version que tu oses montrer publiquement.
- `Plus tard` : les bonnes idées qu'on garde, sans les construire maintenant.

Règles :
- Un jalon est **fini et jouable** avant que le suivant commence.
- Une exigence `Plus tard` n'est jamais construite « en passant ».
- Si une idée nouvelle arrive en cours de route, elle va d'abord dans `requirements.md` avec sa
  priorité. Par défaut, c'est `Plus tard`.

## Le cycle, pour chaque jalon

1. **Cadrer** : relis la vision. Qu'est-ce que ce jalon doit prouver ?
2. **Spécifier** : écris ou mets à jour les exigences du jalon, puis le design, puis les tâches.
3. **Valider les specs** (porte 1) : relis-les toi-même. Demande une revue à l'IA, ou mieux à une
   autre IA : elle doit signaler ce qui manque, ce qui se contredit, ce qui ne se teste pas.
4. **Construire** : par petites séries de tâches. L'IA coche les tâches faites, et les tests
   automatiques doivent passer.
5. **Tester en jouant** (porte 2) : suis le plan de test manuel de `design.md`, sur le vrai support
   (ton téléphone si c'est un jeu mobile).
6. **Ajuster l'équilibrage** : chiffres, vitesses, coûts. Note les valeurs retenues dans `design.md`.
7. **Look et son** (porte 3) : seulement une fois que le jalon est amusant avec des formes simples.

## La règle d'or : les specs avant le code

Toute modification du jeu (une règle, un chiffre, un bug, une nouvelle carte) passe d'abord par
les specs :

1. Mets à jour l'exigence, le design et le plan de test concernés.
2. Dans `tasks.md`, décoche la tâche touchée et ajoute une sous-tâche qui décrit le changement.
3. Valide, puis fais construire.

Exception : un bug où le jeu ne fait pas ce que la spec dit déjà. Dans ce cas, seule une
sous-tâche de correction est ajoutée dans `tasks.md`.

## Travailler avec l'IA

- Donne-lui `CLAUDE.md` : elle construit ce que disent les specs, rien de plus.
- Demande des lots de tâches précis : « construis les tâches 3 à 5 ».
- Demande-lui de **lancer le jeu et les tests** après chaque lot, pas seulement de relire le code.
- Quand elle propose une idée, elle l'ajoute en `Plus tard` au lieu de la coder.
- Commite après chaque lot validé (git), avec un message qui cite les tâches.

## Pour un jeu de stratégie ou de cartes : l'équilibrage

- Garde **toutes les valeurs** (points de vie, dégâts, coûts, vitesses, bonus de biome) dans un
  seul fichier de données du jeu, et leur tableau dans `design.md`.
- Une simulation automatique (IA contre IA, des centaines de parties) est un excellent test :
  aucune carte ne doit gagner presque à tous les coups.
- Change **un chiffre à la fois**, puis rejoue.

## Garder le projet en vie

- Le dossier `spec/` va dans git, avec le code.
- À chaque fin de jalon : relis la vision, range les idées en `Plus tard`, mets à jour
  `decisions.md`.
