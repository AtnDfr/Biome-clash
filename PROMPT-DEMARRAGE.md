Projet : « Biome Clash », un jeu de cartes en temps réel pour téléphone. Ce dépôt suit la méthode
« specs d'abord » : CLAUDE.md fixe tes règles de travail, GUIDE.md décrit la méthode, et spec/ fait
foi. Commence par lire en entier CLAUDE.md, GUIDE.md et les 4 fichiers de spec/. La vision, les
hypothèses, le glossaire et les décisions sont déjà écrits dans spec/requirements.md et
spec/decisions.md : ne les rediscute pas, sauf si tu y vois une contradiction.

LE JEU EN BREF
3 couloirs verticaux, chacun avec un biome (plaine, jungle, forêt…) tiré au hasard et fixe pendant
la partie. Le joueur pose des unités-cartes qui avancent seules et combattent en temps réel. Chaque
unité a un biome favorable (bonus) et un défavorable (malus). Deux unités de la même famille dans
un même couloir déclenchent une synergie. L'énergie se recharge et sert à payer les cartes. Le deck
fait 8 cartes et la main 4. On gagne en détruisant la base ennemie, et une partie dure environ
3 minutes. L'adversaire est une IA, sans multijoueur avant la v1.

TECHNIQUE
Phaser 3 + TypeScript + Vite, tests avec Vitest. Mode portrait, commandes tactiles (et souris
sur ordinateur). Toutes les valeurs d'équilibrage dans un seul fichier de données. La logique du
jeu (combat, biomes, synergies, énergie, IA) est séparée de l'affichage pour être testable sans
navigateur.

LA FEUILLE DE ROUTE
- Jalon Proto : 3 couloirs, 3 biomes, 6 unités, 2 familles, l'énergie, deux bases, une IA très
  simple, des formes de couleur, aucun menu. Il doit prouver une seule chose : choisir le couloir
  selon son biome est amusant.
- Jalon MVP (après le bilan du Proto) : 12 à 15 cartes, 2 ou 3 familles, construction du deck,
  choix d'un module de défense avant la partie (canon, mur ou soin), une IA correcte, les menus
  (accueil, deck, victoire, défaite), un look provisoire.
- v1 et plus tard : voir « Idées pour plus tard » dans requirements.md. Ne construis rien de tout
  ça sans que je le demande.

COMMENT ON TRAVAILLE (étapes une par une, et tu attends ma validation entre chacune)
1. Résume en 5 lignes ce que tu as compris, et liste ce qui manque ou reste flou pour le Proto.
2. Écris les exigences du jalon Proto dans spec/requirements.md (priorité Proto, critères
   « QUAND … ALORS le jeu DOIT … », un seul cas par critère), puis montre-les.
3. Écris spec/design.md pour le Proto : boucle de jeu, contrôles tactiles, règles et cas limites,
   le tableau des 6 unités (coût, PV, dégâts, vitesse, portée, famille, biome +, biome −), les
   3 biomes, les 2 synergies, l'IA, la section Technique (dossiers, fichier de données, commandes
   pour lancer le jeu et les tests) et le plan de test manuel (une ligne par critère).
4. Écris le bloc « Jalon : Proto » de spec/tasks.md : petites tâches, une sous-tâche par cas,
   des sous-tâches « test » pour la logique, et ma tâche de vérification à la fin.
5. Ensuite seulement : initialise le projet, puis construis les tâches que je nomme, par petits
   lots. Après chaque lot : lance les tests et le jeu, coche les tâches terminées, fais un
   commit qui cite les tâches et pousse-le sur la branche de travail.
6. Pour que je teste sur mon téléphone, explique-moi comment y ouvrir le jeu (par exemple un
   déploiement sur GitHub Pages).

Rappels : n'ajoute rien que la spec ne demande pas (une idée va dans « Idées pour plus tard »),
toute modification passe d'abord par les specs, et ne coche jamais ma tâche de vérification.
Réponds-moi en français, en phrases courtes.
