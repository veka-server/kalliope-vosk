# kalliope-vosk
implementation de VOSK pour Kalliope 

## Synopsis
Ajout du STT de vosk

## Avant l'installation
Avant tout installation de module il faut verifier que vous avez bien définis les chemin d'installation des nouveau modules.
Pour se faire, il faut modifier le fichier settings.yml et activer les "resource_directory" en adaptant les chemins evidement.
```bash
resource_directory:
  neuron: "/var/tmp/resources/neurons"
  stt: "resources/stt"
  tts: "resources/tts"
  trigger: "resources/trigger"
  signal: "resources/signal"
```

## Installation
```bash
kalliope install --git-url https://github.com/veka-server/kalliope-vosk.git
```

Ajouter dans le fichier settings.yml le nouveau stt
```yml
default_speech_to_text: "vosk"
```

```yml
  - vosk:
      language: "/.. chemin vers le dossier model .../model-fr"
      log_level: -1
```

## Desinstallation
```bash
kalliope uninstall --stt-name vosk
pip3 uninstall vosk
```

Pour plus d'info : https://kalliope-project.github.io/kalliope/brain/community_modules/
