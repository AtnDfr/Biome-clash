# Décisions

## 2026-11-25 : Phaser 3 + TypeScript, dans le navigateur, en mode portrait
- **Contexte :** le jeu vise le téléphone.
- **Options :** Phaser (web), Godot (natif), Unity.
- **Choix :** Phaser 3 + TypeScript, avec Vite pour lancer le jeu et Vitest pour les tests.
- **Pourquoi :** on teste sur téléphone avec un simple lien, et on peut en faire une appli plus tard
  (Capacitor) sans tout réécrire.
- **À revoir si :** les performances sur mobile ne suffisent pas.

## 2026-11-25 : un adversaire IA, pas de multijoueur avant la v1
- **Contexte :** le temps réel en ligne demande serveurs, synchronisation et matchmaking.
- **Choix :** une IA d'abord.
- **Pourquoi :** vérifier que le jeu est amusant avant d'investir dans le réseau.
- **À revoir si :** le MVP est fun et qu'on veut le faire tester entre amis.

## 2026-11-25 : les règles de base du combat
- **Choix :**
  - une énergie qui se recharge, et une carte qui coûte de l'énergie ;
  - un deck de 8 cartes et une main de 4, la carte jouée retournant sous le paquet ;
  - des biomes fixes pendant la partie, tirés au hasard, avec un bonus et un malus par unité ;
  - 2 ou 3 familles, la synergie se déclenchant quand deux unités de la même famille sont dans un
    même couloir ;
  - des parties d'environ 3 minutes ;
  - l'amélioration de la base en v1, mais un module de défense choisi avant la partie dès le MVP.
- **Pourquoi :** des règles simples et éprouvées, pour que l'originalité, les biomes par couloir,
  ressorte.
- **À revoir si :** le prototype montre que les biomes ne changent pas assez les décisions.
