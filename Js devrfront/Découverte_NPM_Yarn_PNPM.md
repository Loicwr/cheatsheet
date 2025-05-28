
## Découverte de "NPM", "Yarn" et "PNPM" 

### NPM ( Node Package Manager )

- Installé automatiquement avec Node.js
- Registre officiel des milions de packages
- Syntaxe simple et bien documentée

---

- Plus lent que ses concurents
- Structure node_modules parfait redondante
- Gestion des versions parfois imprévisible

### Yarn ( créé par facebook en 2016 pour pallier aux limitation npm )

- Plus rapide que NPM ( surtout les anciennes versions )
- Fichier yarn.lock pour des installations déterministes
- Interface utilisateur plus clair
- Excellente gestion des workspaces

---

- Parfois il y a des incompatibilités avec certains packages
- Deux versions majeures ( CLASSIC et BERRY ) peuvent créer de la confusion


## PNPM ( Performant NPM)
    le plus récent , axé sur la performance et l'éfficacité d'espaces disque

- Il est très rapide et économe en espace de disque
- Système de liens symboliques intelligent
- Compatible avec npm et yarn
- Gestion stricte des dépendances ( évite les " phantom dependices ")

---

- Moins populaire, communauté plus petite
-peut parfois poser des problèmes avec certain outils