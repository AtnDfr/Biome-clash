# Requirements

## Vision

**Nom provisoire :** Biome Clash

**En une phrase :** un jeu de cartes en temps réel sur trois couloirs, où le biome de chaque couloir
rend tes unités plus fortes ou plus faibles : la question n'est pas seulement « quand jouer cette
carte », mais « où ».

**Pour qui :** des joueurs mobiles qui aiment les parties courtes et la stratégie de cartes
(stratégie en temps réel + deck-building).

**Support :** téléphone en mode portrait, joué dans le navigateur (installable plus tard). Testé
aussi sur ordinateur. · **Durée d'une partie :** environ 3 minutes.

**Ce qui doit le rendre amusant :**
- Lire les biomes : poser la bonne unité dans le bon couloir change le combat.
- Les synergies : deux unités de la même famille dans un couloir deviennent plus fortes ensemble.
- Le rythme : l'énergie qui se recharge force à choisir entre attaquer maintenant et garder de quoi
  répondre.

**Ce que le jeu ne fera pas (pour l'instant) :**
- Pas de multijoueur en ligne avant la v1 : on joue contre une IA.
- Pas d'achats, pas de compte, pas de serveur.
- Pas d'amélioration de la base entre les parties avant la v1.

## Hypothèses
- La carte a 3 couloirs verticaux. Chaque couloir a un biome (par exemple plaine, jungle, forêt),
  fixé pour toute la partie et tiré au hasard à chaque partie.
- Chaque unité a un biome favorable (bonus) et un biome défavorable (malus), par exemple +20 % et
  −20 %. Les valeurs exactes se règlent à l'équilibrage.
- Une énergie se recharge avec le temps, chaque carte a un coût en énergie.
- Le deck fait 8 cartes, la main 4 ; la carte jouée retourne sous le paquet.
- Les unités ont 2 ou 3 familles. Deux unités de la même famille dans un même couloir déclenchent
  une synergie.
- Les unités avancent seules dans leur couloir et attaquent ce qu'elles rencontrent.
- On gagne en détruisant la base ennemie. Si le temps est écoulé, la base la moins abîmée gagne.
- Pour le MVP, avant chaque partie, le joueur choisit un module de défense pour sa base (canon, mur
  ou soin).

## Glossaire
- **Couloir** : une des 3 voies verticales où avancent les unités.
- **Biome** : le terrain d'un couloir, qui modifie les unités selon leur affinité.
- **Famille** : un groupe d'unités qui ont une synergie entre elles.
- **Énergie** : la ressource qui se recharge et qui sert à jouer les cartes.
- **Base** : la construction à détruire, une par joueur.
- **Module de défense** : l'arme ou l'équipement choisi pour sa base avant la partie (MVP).

## Exigences

<À écrire avec l'IA, en commençant par le jalon Proto : 3 couloirs, 3 biomes, 6 unités, l'énergie,
une IA très simple, deux bases, des formes simples. Ce jalon doit prouver une seule chose :
choisir le couloir selon son biome est amusant.>

## Idées pour plus tard
- Améliorer sa base entre les parties et choisir plusieurs armes (v1).
- Progression entre les parties, déblocage de cartes (v1).
- Biomes qui changent pendant la partie (à tester après le MVP).
- Multijoueur en ligne, classements, événements (plus tard).
- Publication sur les stores (plus tard).
