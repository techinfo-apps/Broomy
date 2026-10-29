# Historique des versions

[English](CHANGELOG.md) · [简体中文](CHANGELOG.zh-CN.md) · [繁體中文](CHANGELOG.zh-TW.md) · [日本語](CHANGELOG.ja.md) · [한국어](CHANGELOG.ko.md) · [Español](CHANGELOG.es.md) · **Français**

## 1.2 — 2026-10-28

- **Déplacer**, une nouvelle page : les apps que vous utilisez peu et les gros fichiers non ouverts depuis un mois vont dans un dossier « Moved by Broomy » sur un disque externe, seulement après que vous les avez cochés et que vous avez confirmé. Chacun est copié et comparé à l’original avant que l’original aille dans la corbeille ; une app laisse un lien à son ancienne place. Si une étape échoue, rien n’est déplacé. **Remettre** les ramène de la même façon.
- Les apps ne vont que sur des disques SSD, et quand un disque n’indique pas s’il est SSD ou disque dur, c’est vous qui choisissez. Les apps de l’App Store ou d’un programme d’installation, et celles qui tournent en arrière-plan, restent où elles sont, avec la raison affichée.
- Une app déplacée sur un disque qui n’est pas branché compte toujours comme installée : ses données ne sont donc jamais proposées comme restes d’une app supprimée.
- **Désinstaller** trie selon le nombre de jours où vous avez utilisé chaque app sur les 90 derniers.
- **Noter les jours où vous ouvrez chaque app** (Réglages, désactivé par défaut) : conservé sur ce Mac pendant un an, et vous pouvez l’effacer.

## 1.1 — 2026-10-27

- **Plus de choses à nettoyer** : aperçus Xcode ; les caches que les apps faites avec des technologies web (comme VS Code, Slack et Discord) gardent dans leurs propres dossiers, ignorés tant que l’app est ouverte ; instantanés de l’émulateur Android ; caches des outils en ligne de commande ; dossiers de données d’apps qui ne sont plus installées ; images disque (.iso, .img) avec les fichiers d’installation. Les quatre derniers sont décochés au départ.
- **Vider la corbeille** depuis Nettoyage, l’Aperçu ou la barre des menus. C’est le Finder qui la vide, seulement quand vous cliquez et confirmez ; rien d’autre dans Broomy ne supprime quoi que ce soit définitivement.
- **Des pages plus calmes** : les boutons secondaires sont des icônes (leur nom s’affiche au survol) et la description de chaque catégorie se trouve derrière un ⓘ.
- **Désinstaller** peut trier les apps selon le peu de fois où vous les ouvrez.
- **Synchronisation des photos…** dans l’Aperçu explique comment suspendre Photos iCloud ou la désactiver sur ce Mac. Broomy ouvre seulement Photos ; il ne change jamais le réglage lui-même.
- Le bouton d’alimentation du panneau de la barre des menus ferme les fenêtres de Broomy et le garde dans la barre des menus ; pour quitter, faites un clic droit sur son icône.
- Le courrier écrit depuis À propos de Broomy commence son objet par [Broomy].

## 1.0 — 2026-10-21

Première version.
- **Une page par fonction, côte à côte** : Aperçu, Nettoyage, Désinstaller, Système, Santé du disque et Appareils. Balayez à deux doigts, cliquez sur la barre en haut, ou appuyez sur ⌘1…⌘6.
- **Nettoyage** : restes des outils de développement (Xcode, simulateurs, Gradle, Homebrew, caches de pip, npm, pnpm, Yarn, Bun, CocoaPods, Swift Package Manager, Go et Cargo, dossiers de compilation des anciens projets), caches et journaux des apps, programmes d’installation dans Téléchargements et sur le Bureau, et ce que des apps supprimées ont laissé. Tout va dans la corbeille.
- **Désinstaller** une app avec son conteneur, ses caches, ses réglages, l’état de ses fenêtres, ses données web et ses éléments d’ouverture.
- **Système et santé du disque** : CPU, mémoire, températures et ventilateurs ; ce que le SSD interne a écrit et son usure.
- **Appareils** : luminosité et volume de vos écrans, avec la raison et quoi essayer quand l’un d’eux ne peut pas être réglé ; sortie audio, molette de souris plus agréable, disques externes, USB et Thunderbolt.
- Dans la barre des menus si vous le souhaitez. Neuf langues. Aucun code réseau.
