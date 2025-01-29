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
  - 
