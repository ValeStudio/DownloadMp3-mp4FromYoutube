# Download Video e Audio da YouTube con yt-dlp in Google Colab

Questo progetto utilizza Google Colab per scaricare video e audio da YouTube utilizzando le librerie `yt-dlp` e `ffmpeg`. È progettato per essere semplice e intuitivo, permettendo di scegliere tra il download di singoli video o di intere playlist.

## Funzionalità

- Installazione automatica di `yt-dlp` e `ffmpeg`.
- Possibilità di scaricare singoli video o playlist.
- Opzioni per scegliere tra diversi formati audio e video disponibili.
- Conversione automatica in formato MP3 per audio e in MP4 per video.
- Compressione dei file scaricati in un archivio ZIP per un facile download.

## Prerequisiti

- Un browser web per accedere a Google Colab.
- Un account Google per utilizzare Google Colab.

## Come Utilizzare

1. **Apri Google Colab** e crea un nuovo notebook.
2. **Copia e incolla il codice** fornito nel notebook.
3. **Esegui le celle** per installare le librerie richieste e configurare l'ambiente.
4. **Scegli il tipo di download** (singolo video o playlist) e inserisci l'URL desiderato.
5. **Seleziona il formato** audio o video che vuoi scaricare.
6. Al termine del download, il file ZIP contenente i media sarà disponibile per il download.

## Esempio di Codice

```python
# Installa yt-dlp e ffmpeg in Google Colab
!pip install yt-dlp
!apt-get install ffmpeg

import os
import yt_dlp
from google.colab import files
import shutil

# Crea una cartella per i file audio
output_path = 'download_music_py'
if not os.path.exists(output_path):
    os.makedirs(output_path)
else:
    for filename in os.listdir(output_path):
        file_path = os.path.join(output_path, filename)
        if os.path.isfile(file_path):
            os.remove(file_path)

# Funzioni di download...
