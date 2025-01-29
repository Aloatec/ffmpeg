# ffmpeg

## Update le dépôt

### dépôt ffmpeg
- update la baseline: vcpkg x-update-baseline
- faire les modifications voulues dans vcpkg.json
- changer la version dans le workflow (Il ne faut pas que la version existe déjà)
- lancer le workflow
  
### dépôt vcpkg-registery

Dans portfile.cmake:
  - Mettre le hash du commit de la release créée par le workflow dans REF
  - Changer le hash des fichiers, pour cela
      - Soit télécharger les dossiers et dans powershell, Get-FileHash ./fichier.zip -Algorithm SHA512| Format-List
      - Soit fixer la valeur du hash à 0, et au lancement du fichier .cmake, vcpkg vous donnera le hash
  - Changer l'URLS pour qu'il corresponde aux fichiers de Release
  - En cas d'ajout de nouvelles features/nouvelles dépendences, mettre à jour l'ajout des fichiers

Après cela, il suffit de mettre à jour comme pour un dépôt classique.
  
