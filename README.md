# Ospazio

**Plugin gratuito di stereo imaging multibanda di Valla Productions.**

Ospazio permette di controllare larghezza, distribuzione e bilanciamento stereo fino a **otto bande**, con analizzatore di spettro e visualizzazione della larghezza stereo in uscita.

**Versione 1.5.0**

## Download

Scegli il formato supportato dalla tua DAW:

| Sistema | Formato | Download |
| --- | --- | --- |
| Windows x64 | VST3 | [Ospazio-1.5.0-Windows-x64.vst3.zip](https://github.com/vallaproductionsoriginal-byte/Ospazio/releases/download/v1.5.0/Ospazio-1.5.0-Windows-x64.vst3.zip) |
| macOS Apple Silicon | VST3 | [Ospazio-1.5.0-macOS-arm64.vst3.zip](https://github.com/vallaproductionsoriginal-byte/Ospazio/releases/download/v1.5.0/Ospazio-1.5.0-macOS-arm64.vst3.zip) |
| macOS Apple Silicon | Audio Unit (AU) | [Ospazio-1.5.0-macOS-arm64.au.zip](https://github.com/vallaproductionsoriginal-byte/Ospazio/releases/download/v1.5.0/Ospazio-1.5.0-macOS-arm64.au.zip) |

[Pagina della release](https://github.com/vallaproductionsoriginal-byte/Ospazio/releases/tag/v1.5.0)

I tre archivi contengono i **plugin compilati**, con gli avvisi di licenza inclusi nei bundle. Il repository distribuisce questi download, il README e le licenze; **il codice sorgente non è pubblicato**.

## Funzioni principali

- Da una a otto bande, con controlli di Width, Spread, Depth e Gain.
- Controlli Phase Limit e Phase Align per ciascuna banda, insieme a limiter, solo, mute e bypass.
- Analizzatore di spettro e vista Stereo Width per osservare la larghezza stereo per frequenza.
- Divisione, unione e regolazione delle bande direttamente sullo spettro.
- Gain di ingresso e uscita, Dry/Wet, sidechain esterno e collegamento dei controlli tra bande.
- Preset, automazione e salvataggio dello stato nella sessione della DAW.

## Requisiti

| Sistema | Requisiti |
| --- | --- |
| Windows | Windows 10/11 x64 e DAW a 64 bit con supporto VST3. |
| macOS | Mac Apple Silicon (arm64), macOS 11.0 o successivo e DAW con supporto VST3 oppure AU. |

Per **Logic Pro** usa il formato **AU**. Le build Mac di questa release sono per Apple Silicon; non è inclusa una build Mac Intel.

## Installazione

1. Scarica ed estrai lo ZIP del formato scelto.
2. Copia **l'intera cartella del plugin**, conservando tutti i file al suo interno, nella cartella indicata qui sotto.
3. Riavvia la DAW ed esegui una nuova scansione dei plugin.

| Plugin | Bundle da copiare | Cartella di installazione |
| --- | --- | --- |
| Windows VST3 | `Ospazio.vst3` | `C:\Program Files\Common Files\VST3\` |
| Mac VST3 | `Ospazio.vst3` | `~/Library/Audio/Plug-Ins/VST3/` |
| Mac AU | `Ospazio.component` | `~/Library/Audio/Plug-Ins/Components/` |

Su Mac, apri **Finder → Vai → Vai alla cartella** e incolla il percorso; crea la cartella se manca. In Logic Pro cerca **Valla Productions → Ospazio** tra gli effetti Audio Unit e, se necessario, ripeti la scansione da Gestione plug-in. Il bundle AU mantiene l'estensione `.component`.

Su Windows puoi usare anche una cartella VST3 configurata nella DAW. Conserva la struttura `Ospazio.vst3\Contents\x86_64-win\Ospazio.vst3`. Il runtime Visual C++ è collegato staticamente al plugin.

I bundle Mac hanno firma locale ad hoc e non sono notarizzati da Apple. Il VST3 Windows non ha firma Authenticode.

## Verifica dei download

I checksum SHA-256 della build del 13 ottobre 2026 sono:

```text
c1a23484c6a657b4b7370b64497b23015aee7f103e9fa6b2b9e4020c4e8121c5  Ospazio-1.5.0-Windows-x64.vst3.zip
b9f29305971ec51ecb67ac771a4ca70b3eb462c34436775607d8734f520d7786  Ospazio-1.5.0-macOS-arm64.vst3.zip
c6953c6f261643ba13361b7be9245065665b2a6ffed953a27b3b68c4ce18c702  Ospazio-1.5.0-macOS-arm64.au.zip
```

Su macOS esegui `shasum -a 256 nome-archivio.zip`; su Windows usa `Get-FileHash .\nome-archivio.zip -Algorithm SHA256` in PowerShell. Sostituisci `nome-archivio.zip` con il file scaricato e confronta il risultato con la riga corrispondente.

I VST3 estratti dagli ZIP sono stati verificati con **453 controlli superati su macOS e 453 su Windows x64**, inclusi test DSP e caricamento nell'host VST3. La compatibilità dipende anche dalla DAW e dalla sua versione.

## Licenze e avvisi delle dipendenze

Copyright © 2026 Francesco Valla.

- [LICENSE](LICENSE): licenza MIT per le parti originali di Ospazio e la documentazione.
- [NOTICE.md](NOTICE.md): avvisi relativi a Ospazio, JUCE e agli altri componenti incorporati.
- [THIRD_PARTY_LICENSES.txt](THIRD_PARTY_LICENSES.txt): testi delle licenze e copyright delle dipendenze.

JUCE e le altre dipendenze mantengono le proprie licenze. Gli avvisi sono inclusi anche in ogni plugin, nella cartella `Contents/Resources/Licenses/`.

## Supporto

Per segnalare un problema, apri una [issue](https://github.com/vallaproductionsoriginal-byte/Ospazio/issues) indicando sistema operativo, DAW e versione, formato del plugin, frequenza di campionamento e passaggi per riprodurlo.
