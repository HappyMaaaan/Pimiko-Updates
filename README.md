# Pimiko — canal de mises à jour

Dépôt **public** de distribution : il contient uniquement les installateurs
Windows compilés et les fichiers de métadonnées (`latest.yml`, `.blockmap`)
utilisé par l'auto-updater intégré à Pimiko (electron-updater).

Le **code source** vit dans le dépôt privé
[HappyMaaaan/Pimiko](https://github.com/HappyMaaaan/Pimiko) et n'est pas
distribué ici.

## Installation

1. Téléchargez `Pimiko-x.y.z-x64.exe` depuis la dernière release.
2. Vérifiez l'empreinte si vous le souhaitez :
   `sha256sum -c` sur `SHA256SUMS.txt` (ou `Get-FileHash` sous PowerShell).
3. Exécutez l'installateur. C'est tout.

## Mises à jour

L'application vérifie une mise à jour **à chaque lancement** (puis toutes
les 4 h), la télécharge en arrière-plan et l'installe automatiquement à la
fermeture. Aucune action requise.

## Publication (mainteneurs)

Pousser un tag `vX.Y.Z` sur le dépôt privé lance la CI : build signé si
certificat présent, publication croisée des artefacts vers ce dépôt
(secret `UPDATES_TOKEN`).
