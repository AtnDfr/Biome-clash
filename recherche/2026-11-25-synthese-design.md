# Recherche de design : synthèse (25 novembre 2026)

But : éclairer les choix du jalon Proto de Biome Clash avant d'écrire les exigences.
Chaque conclusion indique sa **fiabilité** :
- **forte** : source officielle ou propos directs du concepteur, confirmés par une autre source ;
- **moyenne** : une seule bonne source, ou une analyse sérieuse mais indirecte ;
- **faible** : article de presse ou de fan, non confirmé.

Les liens sont en bas de page. Ce document n'est pas une spec : il sert à décider.

---

## 1. Le rythme : pourquoi l'énergie marche

**Ce que disent les sources**
- Clash Royale : la partie dure 3 minutes. L'élixir est doublé dans la 3e minute. En cas
  d'égalité, une prolongation de 2 minutes suit, avec un élixir doublé puis triplé. Fiabilité
  **forte** (page d'aide officielle de Supercell, notes de mise à jour officielles).
- En 2016, l'élixir se rechargeait d'1 point toutes les 2 secondes, jusqu'à 10. Fiabilité
  **moyenne** (analyse de M. Katkoff, chiffres peut-être changés depuis).
- L'énergie crée trois décisions :
  1. **On ne peut pas tout poser d'un coup.** Il faut choisir quoi poser maintenant.
  2. **L'échange** : contrer une attaque en dépensant moins d'énergie que l'adversaire donne un
     avantage pour contre-attaquer. Fiabilité **forte** (aide officielle de Supercell, guides
     concordants, analyse de Katkoff).
  3. **Le défenseur est avantagé**, car l'attaquant montre ses cartes en premier. Et en début de
     partie, dépenser sans rien savoir de l'adversaire est risqué. Fiabilité **moyenne**
     (Katkoff).
- Hearthstone : le mana est garanti à chaque tour (+1 par tour, maximum 10). Selon B. Brode,
  le jeu est donc moins aléatoire que d'autres, et l'équipe doit travailler pour que les parties
  ne se ressemblent pas. Fiabilité **forte** (propos de Brode, repris par deux médias).

**Le cas « une carte posée l'est pour de bon » (ton idée)**
- Aucun grand jeu mobile ne l'utilise tel quel. Les jeux de stratégie sur PC qui s'en
  approchent :
  - *Fleet Command* : les pertes sont définitives, donc chaque unité compte et chaque
    déploiement est un pari.
  - *World in Conflict* : un budget fixe, qui ne se recharge que quand ses unités meurent.
  - Fiabilité **moyenne** (Wikipédia, une analyse de blog).
- Le risque que j'avais signalé (tout poser d'un coup, ou attendre sans rien faire) n'est
  documenté nulle part comme tel. C'est une déduction de ma part. Mais il est cohérent avec
  l'observation de Katkoff : sans élixir à dépenser, attendre l'autre devient la meilleure
  stratégie.

**Ce que j'en conclus**
- L'énergie n'est pas là par habitude. Elle fixe le rythme et rend chaque pose coûteuse, donc
  réfléchie. Elle force aussi la fin de partie (énergie doublée, prolongation).
- Ton idée et l'énergie ne s'opposent pas. On peut garder « chaque carte ne sert qu'une fois »
  **et** une énergie qui fixe le rythme. Voir les options dans le message.

## 2. Les cartes : combien, et à quel point compliquées

- Clash Royale : deck de 8, main de 4. La carte jouée revient en fin de cycle. Fiabilité
  **forte** (plusieurs sources concordantes).
- Marvel Snap : deck de 12 cartes, 6 tours, un seul type de carte. Fiabilité **forte** (Brode,
  conférence GDC 2023).
- **Simplicité** : selon Brode, au-delà de 8 mots à l'écran, les joueurs ne lisent plus. Une carte
  de Hearthstone en compte 9 en moyenne, une carte de Snap 11. Son conseil : « Simplifiez, même si
  votre équipe vous déteste. » Fiabilité **forte** (GDC 2023, rapporté par mobilegamer.biz).
- **Profondeur sans complexité** : le but est des cartes simples qui se combinent pour créer de la
  profondeur. Rendre une carte compliquée est facile, la rendre simple et profonde est le vrai
  travail. Fiabilité **forte** (texte de Brode, 2017).
- Peu de types d'unités facilitent l'équilibrage, et une unité connue reste lisible dans un autre
  contexte. Fiabilité **moyenne** (M. Gallant, analyse de Clash Royale).

**Conclusion :** 8 à 12 cartes, chacune avec un rôle clair et au plus une phrase d'effet.

## 3. Les biomes : lisibles et justes

- **Le hasard « avant la décision » plaît, celui « après la décision » frustre plus.** Brode
  distingue :
  - le hasard **d'entrée** : on décide face à un tirage déjà connu ;
  - le hasard **de sortie** : on décide, puis le hasard dit si on a eu raison.
  Les lieux de Marvel Snap, tirés au hasard et révélés avant de jouer, sont le hasard d'entrée.
  Fiabilité **forte** (Brode à la GDC, deux sources).
- **Tes biomes tirés au hasard et visibles au début sont exactement du hasard d'entrée.** C'est
  le bon type, et un argument fort pour ton concept.
- **Esquive et précision en pourcentage sont du hasard de sortie.** Un archer qui rate trois tirs
  de suite agace, sauf si on montre les chances, comme le fait XCOM. Fiabilité **moyenne** (blogs
  de design concordants, pas d'étude solide).
- **Lisibilité sur petit écran** : l'équipe de Warcraft Rumble a retiré des détails des décors,
  car on ne distinguait plus les unités. Fiabilité **forte** (propos du directeur du jeu, Pocket
  Tactics, 2023).
- Advance Wars montre l'effet du terrain par un simple nombre d'étoiles (0 à 5). Fiabilité
  **moyenne** (wiki de fans, Wikipédia).

**Conclusion :**
- Des effets de biome **fixes et visibles**, sans hasard : dégâts, PV, vitesse, portée.
- « L'archer vise mal en forêt » devient « −30 % de portée en forêt », plutôt que « 30 % de
  chances de rater ».
- Un effet par biome et par unité, affiché par une icône ou une flèche verte ou rouge.

## 4. Les familles et les synergies

- Dans Teamfight Tactics, un bonus de famille se déclenche par paliers (2, 4, 6 unités).
  Riot a dû retirer des objets qui permettaient d'atteindre trop vite les gros paliers.
  Fiabilité **moyenne** (blog officiel de Riot, mais un autre genre de jeu).
- Le système « pierre-feuille-ciseaux » (chaque unité bat un type et perd contre un autre) est
  un bon point de départ d'équilibrage : aucune unité n'est imbattable. Fiabilité **moyenne**
  (plusieurs articles de design, avis partagés sur ses limites).

**Conclusion :**
- Un seul palier au Proto : 2 unités de la même famille dans un couloir.
- Un bonus simple, en une phrase.
- Le couloir ajoute une couche : bonne unité, bon biome, bonne paire.

## 5. Durée et fin de partie

- Clash Royale : 3 minutes, puis jusqu'à 2 minutes de prolongation (voir section 1). Fiabilité
  **forte**.
- Brode cite comme une force de Clash Royale la certitude de finir une partie en moins de
  5 minutes. Fiabilité **forte** (GDC 2023).
- Marvel Snap : environ 3 minutes par partie. Fiabilité **faible** (presse, pas de chiffre
  officiel trouvé).

**Conclusion :** viser 3 minutes avec un chrono, une énergie accélérée à la fin, puis une courte
prolongation. Une partie doit tenir à coup sûr en moins de 5 minutes.

## 6. Le marché et les échecs récents

- En 2025, la stratégie est le seul genre mobile à progresser en revenus, en téléchargements et
  en temps de jeu. Mais elle est menée par des jeux 4X (*Last War*, *Whiteout Survival*).
  Fiabilité **forte** (Sensor Tower, rapport 2026).
- Les téléchargements mobiles baissent depuis 2020. Les genres sont tenus par des jeux installés,
  difficiles à détrôner. Fiabilité **moyenne** (Sensor Tower, interview de Deconstructor of Fun).
- **Des jeux de grands studios dans ce créneau ont échoué :**
  - *Clash Mini* (pose sur une grille, Supercell) : arrêté en 2024, « bon jeu, mais pas celui
    dont on rêvait ».
  - *Squad Busters* (Supercell) : arrêté en 2025-2026. Supercell regrette : « On aurait dû passer
    plus de temps à rendre le cœur du jeu vraiment prêt. »
  - *Warcraft Rumble* (couloirs, Blizzard) : fin du contenu en juillet 2025, faute d'engagement
    et de fidélité des joueurs.
  - Fiabilité **forte** (communiqués officiels de Supercell, presse spécialisée).
- *Clash Royale* a connu un fort regain en 2025, porté surtout par le retour d'anciens joueurs.
  Fiabilité **moyenne** (Deconstructor of Fun, SQURS sur l'API publique).

**Conclusion :**
- Le cœur du jeu doit être amusant avant tout le reste. C'est exactement le rôle du Proto.
- L'originalité (les biomes) est ton atout. Une copie de Clash Royale n'a aucune chance face à
  l'original.

## Limites de cette recherche

- Je n'ai pas trouvé de chiffre officiel récent sur la vitesse de l'élixir. La page d'aide de
  Supercell refuse l'accès automatique.
- Aucune source ne donne la durée des sessions ni la fidélité des joueurs pour ce genre précis.
- Aucun jeu mobile connu n'a testé « cartes à usage unique + temps réel ». C'est à la fois un
  risque et une chance de se démarquer : seul le Proto le dira.

## Sources
- Supercell, aide Clash Royale (élixir, échange d'élixir) :
  https://support.clashroyale.com/hc/en-us/articles/49484936933403-Elixir ·
  https://support.clashroyale.com/hc/en-us/articles/49484904683803-1v1-Battle
- Supercell, notes de mise à jour (prolongation) :
  https://supercell.com/en/games/clashroyale/blog/release-notes/november-update
- M. Katkoff, *Clash Royale – Deconstructing Supercell's Next Billion Dollar Game* (2016) :
  https://www.gamedeveloper.com/design/clash-royale---deconstructing-supercell-s-next-billion-dollar-game
- M. Gallant, *Clash Royale's Economical Design* (2017) :
  https://gangles.ca/2017/04/24/clash-royale-economical-design/
- B. Brode à la GDC 2023, mobilegamer.biz :
  https://mobilegamer.biz/second-dinners-ben-brode-reveals-marvel-snaps-recipe-for-success-literally/
- B. Brode sur le hasard dans Hearthstone (2018) :
  https://www.gamedeveloper.com/design/stick-or-twist-balancing-randomness-and-strategy-in-i-hearthstone-i-
- B. Brode, complexité et profondeur (2017) :
  https://www.hearthpwn.com/news/2195-ben-brode-on-defining-complexity-depth-and-design
- Wayward Strategy, *Time as a Resource: World in Conflict* :
  https://waywardstrategy.com/2015/07/20/time-as-a-resource-part-3-world-in-conflict/
- Fleet Command : https://en.wikipedia.org/wiki/Fleet_Command
- Warcraft Rumble, interview Pocket Tactics (2023) : https://www.pockettactics.com/warcraft-rumble/interview
- Fin de Warcraft Rumble : https://en.wikipedia.org/wiki/Warcraft_Rumble ·
  https://www.pocketgamer.biz/blizzard-ends-warcraft-rumble-development-as-company-reportedly-hit-by-up-to-100-job-losses
- Fin de Clash Mini : https://supercell.com/en/news/clash-mini-ending-development/
- Fin de Squad Busters :
  https://mobilegamer.biz/why-not-just-keep-squad-busters-alive-but-on-autopilot-supercell-explains/ ·
  https://supercell.com/en/news/squad-busters-faq/
- Riot, *Monsters Attack! Learnings* :
  https://teamfighttactics.leagueoflegends.com/en-us/news/dev/dev-teamfight-tactics-monsters-attack-learnings/
- Pierre-feuille-ciseaux : https://www.gamedeveloper.com/design/rock-paper-scissors-design-in-strategy-games
- Advance Wars, terrain : https://en.wikipedia.org/wiki/Advance_Wars
- Sensor Tower, *State of Gaming 2026* : https://sensortower.com/report/state-of-gaming-2026
- Deconstructor of Fun (2025) : https://www.deconstructoroffun.com/blog/2025/6/5/the-state-of-mobile-gaming-2025 ·
  https://www.deconstructoroffun.com/blog/2025/12/5/was-clash-royales-second-wind-paid-or-organic
- SQURS, joueurs de Clash Royale (2025) : https://blog.squrs.com/clashroyale/playerbase_snapshot_202509
