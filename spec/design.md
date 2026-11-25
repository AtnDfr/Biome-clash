# Design

<Chaque section cite les ids des exigences qu'elle couvre (par exemple R2.1). Toute exigence de
`requirements.md` apparaît dans au moins une section. Écris pour quelqu'un qui ne code pas, sauf la
section Technique.>

## Vue d'ensemble
<Comment se déroule une partie, du début à la fin, en quelques lignes. Comment on gagne, comment on
perd.>

## Boucle de jeu
<Ce que le joueur fait encore et encore : par exemple « regarder sa main → choisir une carte →
choisir un couloir → la poser → observer le combat → recommencer ». Et la boucle plus longue,
entre les parties, s'il y en a une (récompenses, amélioration, nouveau deck).>

## Contrôles
<Chaque geste (toucher, glisser, appui long, touche) et son effet. Pour le mobile : la taille des
zones touchables et l'orientation.>

## Écrans et états
<Chaque écran (accueil, deck, partie, pause, victoire, défaite…) et ce qui fait passer de l'un à
l'autre.>

## Éléments du jeu
<Les objets du jeu et leur rôle : unités, bases, terrain, projectiles…>

## Règles et cas limites
<Toutes les règles : déplacements, combat, ciblage, victoire, égalité, fin du temps. Et les cas
limites : deux unités qui arrivent en même temps, main vide, ressource à zéro, abandon.>

## Contenu
<Les listes du jeu, sous forme de tableaux. Par exemple les cartes :>

| Carte | Famille | Coût | PV | Dégâts | Vitesse | Biome + | Biome − | Effet |
|---|---|---|---|---|---|---|---|---|
| <nom> | <famille> | <n> | <n> | <n> | <lente/normale/rapide> | <biome> | <biome> | <effet spécial> |

<Et de la même façon : les biomes et leurs effets, les familles et leurs synergies, les modules de
la base, les niveaux…>

## Équilibrage
<Les valeurs de référence et leurs raisons : durée cible d'une partie, recharge de la ressource,
force d'un bonus de biome… Toutes ces valeurs vivent dans un seul fichier de données du jeu.>

## Adversaire (IA)
<Comment l'adversaire choisit ses cartes et ses couloirs, et ses niveaux de difficulté.>

## Progression
<Ce qui reste d'une partie à l'autre : déblocages, améliorations, sauvegarde. Écris « Aucune pour ce
jalon. » s'il n'y en a pas.>

## Look et son
<Seulement une fois que le jeu est amusant avec des formes simples. Direction artistique, palette
avec les codes couleur, tailles, animations, sons, musique. Liste des images à produire.>

## Technique
<Pour l'IA et pour toi plus tard :>
- **Moteur et langage :** <par exemple Phaser 3 + TypeScript>
- **Organisation du code :** <dossiers et rôle de chacun>
- **Données :** <où sont les cartes, les biomes, les valeurs d'équilibrage>
- **Sauvegarde :** <où et quoi>
- **Tests :** <ce qui est testé automatiquement et comment lancer les tests>
- **Lancer le jeu :** <la commande, et comment le tester sur téléphone>

## Plan de test manuel
<Une ligne par critère d'acceptation, jamais plusieurs ids sur la même ligne. Chaque ligne est une
action dans le jeu et un résultat visible.>
- R1.1 : <étapes en jouant> → <ce qu'on doit voir>
