<div align="center">

<img src="assets/icon.png" width="128" alt="Icona di Vocalis">

# Vocalis

**Player karaoke MIDI/KAR per macOS, Windows, Linux e Android, ispirato a vanBasco, pensato per le serate dal vivo.**
Regia sul computer, testi a schermo intero su monitor o TV, prenotazioni dei cantanti dal telefono.

🇮🇹 Italiano · [🇬🇧 English](README.en.md)

[**⬇️ Scarica l'ultima versione**](../../releases/latest) · [🌐 Sito dell'app](https://www.enricofanucchi.com/it/app/vocalis?utm_source=github&utm_campaign=readme) · [💜 Sostieni il progetto](https://github.com/sponsors/kikoz85)

<img src="assets/screenshots/player.png" width="560" alt="Il Player di Vocalis">

</div>

---

## Indice

- [Perché Vocalis](#perché-vocalis)
- [Download e installazione](#download-e-installazione)
- [Funzionalità](#funzionalità)
- [Screenshot](#screenshot)
- [Temi](#temi)
- [Primi passi](#primi-passi)
- [Scorciatoie da tastiera](#scorciatoie-da-tastiera)
- [Segnalare un problema](#segnalare-un-problema)
- [Sostieni Vocalis](#sostieni-vocalis)
- [Crediti e licenze](#crediti-e-licenze)

## Perché Vocalis

Le basi karaoke `.mid` e `.kar` sono leggere, si trasportano di tonalità senza perdita di qualità e contengono già il testo sincronizzato. Vocalis le suona con un sintetizzatore integrato e riprende l'impostazione dei player classici come vanBasco: finestre piccole e affiancabili, display LCD, fader e un mixer a 16 canali. La grafica è moderna e si cambia con i temi.

Le priorità sono **velocità e affidabilità**: avvio rapido, audio senza glitch e ricerca istantanea in librerie da migliaia di brani.

**Vocalis è gratuito.** Se ti è utile, puoi [sostenerne lo sviluppo](#sostieni-vocalis).

## Download e installazione

**In arrivo sugli store** (con aggiornamenti automatici dallo store):

- **Mac App Store** *(in revisione da Apple)*: macOS 10.15+, Apple Silicon e Intel.
- **Microsoft Store** *(in revisione da Microsoft)*: Windows 10/11, x64 e ARM64, firmato da Microsoft.
- **Google Play** *(in test chiuso)*: Android 8.0+, telefoni e tablet, anche in modalità desktop (Samsung DeX).

I link verranno aggiunti qui appena le app saranno pubblicate.

**Da GitHub**: gli installer sono nella pagina [**Releases**](../../releases/latest) e si aggiornano dall'app.

| Sistema | File | Note |
|---|---|---|
| **macOS** 10.15+ — Apple Silicon (M1, M2, M3, M4…) | `Vocalis_x.y.z_aarch64.dmg` | Apri il DMG e trascina Vocalis in Applicazioni. |
| **macOS** 10.15+ — Intel | `Vocalis_x.y.z_x64.dmg` | Apri il DMG e trascina Vocalis in Applicazioni. |
| **Windows** 10/11 (64 bit) | `Vocalis_x.y.z_x64-setup.exe` oppure `.msi` | Installer classico o MSI. |
| **Windows 11 ARM** (ARM64) | `Vocalis_x.y.z_arm64-setup.exe` oppure `.msi` | Snapdragon X, Surface Pro, Windows in Parallels sui Mac. |
| **Linux** (x86_64 e ARM64) | `.deb` (Debian/Ubuntu), `.rpm` (Fedora/openSUSE) oppure `.AppImage`: `amd64`/`x86_64` per PC Intel/AMD, `arm64`/`aarch64` per ARM (es. Raspberry Pi 64 bit) | Per l'AppImage: rendilo eseguibile e avvialo. |

> **Primo avvio.**
> - **macOS**: i DMG sono **firmati con certificato Developer ID e notarizzati da Apple** (dalla versione 1.4.2): Vocalis si apre con un doppio clic, senza avvisi.
> - **Windows**: gli installer di GitHub non sono ancora firmati, quindi la prima volta può comparire SmartScreen: premi *Ulteriori informazioni* → **Esegui comunque**. La versione del Microsoft Store, in arrivo, sarà firmata da Microsoft.

Vocalis include già un SoundFont General MIDI completo: suona subito, senza configurazione.

## Funzionalità

### Riproduzione
- File **MIDI** (`.mid`, `.midi`, `.rmi`) e **KAR** (`.kar`), aperti con doppio clic, trascinamento o dalla libreria.
- **Sintetizzatore SoundFont integrato**, con **GeneralUser GS** incluso.
- **Fedeltà Roland GS / Yamaha XG**: Vocalis legge le impostazioni contenute nelle basi (riverbero, chorus, kit di batteria su qualunque canale) e le fa suonare come previsto da chi le ha scritte.
- **Download manager dei SoundFont**: catalogo di 8 banchi adatti al karaoke (FluidR3, MuseScore General, Shan SGM e altri), con verifica di integrità, pausa e ripresa.
- **Chiave** (trasposizione in semitoni), **tempo** e **volume**, con preset salvati per brano.
- **MIDI Out verso DAW e strumenti** (Ableton Live, Logic Pro, Cubase, FL Studio, Reaper, Bitwig, GarageBand…): il brano intero esce sulla porta MIDI che scegli, con tutti i 16 canali, i SysEx, la trasposizione e il mixer di Vocalis già applicati. Basta una porta virtuale (Driver IAC su macOS, loopMIDI su Windows, ALSA su Linux) per suonare la base con i tuoi strumenti virtuali, registrarla o elaborarla nella DAW. Oppure va a un modulo o a una tastiera esterna, o al synth di sistema. C'è anche il **MIDI IN** da tastiera, con il **Live mode** per suonare sopra la base.
- **Integrazione nativa con MicTune**: Vocalis trova da solo la porta di MicTune e ci si ricollega se MicTune viene aperto dopo, riavviato o aggiornato. Gli invia la melodia (canale 4) e i cori per le armonie (canale 5), sincronizzati con l'audio che esce dalle casse, e in più tonalità, BPM e trasposizione del brano (MicTune Link). La correzione della voce segue così la nota giusta del brano, non una scala fissa.
- **Cori riconosciuti e gestiti a parte**: Vocalis trova da solo i canali dei cori nel MIDI o nel KAR, dal nome della traccia («Cori», «Choir», «Backing», «BV», «Armonie»…) o dallo strumento vocale General MIDI (Choir Aahs, Voice Oohs, Synth Voice). Li invia su un canale separato da quello della melodia (il 5 per MicTune), così l'armonizzatore crea le seconde voci sulle note giuste del brano. Puoi tenerli muti nell'audio per sentire solo le armonie generate dalla tua voce; Setup mostra quali canali sono stati riconosciuti nel brano in corso.
- **Guida melodica anche con altri software e dispositivi, non solo MicTune**: MicTune è integrato in modo nativo, ma la guida funziona con qualsiasi programma o apparecchio che riceve note MIDI. Melodia e cori, riconosciuti da soli nel file e trasposti come la base, possono uscire anche su una porta separata da quella della base. Vanno a un auto-tune o armonizzatore hardware, oppure a una traccia della DAW con un plugin che riceve le note via MIDI. Canali di invio e sincronia sono regolabili. Melodia e cori possono restare muti nell'audio.
- **Mixer a 16 canali** con mute, solo, volume e cambio strumento al volo.
- **VU meter e analizzatore di spettro stile Winamp**.
- Coda con **autoplay, shuffle, scan** e **repeat** (off / tutti / brano), più il **mini player**.

### Karaoke
- Testi **sincronizzati sillaba per sillaba**, con colorazione progressiva di quanto è già stato cantato.
- **2 o 4 righe** per pagina, a capo automatico delle righe lunghe e rimozione di crediti e intestazioni.
- Riconoscimento automatico della **codifica dei testi** (UTF-8, Latin-1, Windows-1252), salvata per brano.
- **Personalizzazione completa**: font, colori, effetti di evidenziazione e sfondo in tinta unita, gradiente o immagine.
- **Sfondi animati**: note musicali, aurora, stelle, bolle, gradiente in movimento e spettro musicale.
- **Conto alla rovescia** prima dell'attacco della voce e **anteprima del brano successivo** in scaletta.
- **Secondo schermo**: la finestra Karaoke si apre a schermo intero sul monitor scelto.

### Serate dal vivo
- **Libreria** con ricerca istantanea, preferiti, brani recenti, più cartelle sorgente e conteggio delle esecuzioni.
- **Scalette** salvate, con import ed export `.m3u` e chiave/tempo memorizzati per ogni voce.
- **Testi e prenotazioni in rete locale**: i testi si seguono da qualunque browser della sala e il pubblico prenota il proprio turno dal telefono tramite **QR code**.
- **Riconoscimento degli accordi** sul piano virtuale (notazione inglese o italiana) e stima della tonalità.

### Interfaccia
- **Multi-finestra**: Player, Karaoke, Playlist, Libreria, Piano, Output, Control, Regia e Setup, con disposizione salvata e supporto multi-monitor.
- **6 temi** inclusi, più **temi personalizzati** da file.
- **Italiano e inglese**, scelti in base alla lingua del sistema o in *Setup → Generale → Lingua*; la pagina delle prenotazioni e quella dei testi per la TV usano la lingua del telefono o del browser.

## Screenshot

Ogni finestra è mostrata con un tema diverso.

| Finestra | |
|---|---|
| **Karaoke** — testo sillabato su sfondo animato «Note musicali» | <img src="assets/screenshots/karaoke.png" width="480" alt="Finestra Karaoke con note musicali"> |
| **Regia** — brano, chiave/tempo/volume, scaletta, mixer, SoundFont, rete *(tema Aurora)* | <img src="assets/screenshots/regia.png" width="480" alt="Regia"> |
| **MIDI Output** — 16 canali con strumento, VU, volume e note in tempo reale *(tema Palco)* | <img src="assets/screenshots/output.png" width="480" alt="MIDI Output"> |
| **Piano** — note suonate, accordi riconosciuti, tonalità, live mode *(tema Palco)* | <img src="assets/screenshots/piano.png" width="480" alt="Piano"> |
| **Libreria** — ricerca, preferiti, recenti *(tema Vocalis)* | <img src="assets/screenshots/library.png" width="400" alt="Libreria"> |
| **Setup** — scelta del tema *(tema Corallo)* | <img src="assets/screenshots/setup.png" width="400" alt="Setup, scheda Aspetto"> |
| **Setup › Audio / MIDI** — base su porta virtuale per la DAW (IAC), guida melodica e cori verso MicTune o altri processori *(tema Palco)* | <img src="assets/screenshots/setup-midi.png" width="300" alt="Setup, MIDI Out e guida melodica"> |
| **Playlist** *(tema Smeraldo)* · **Control** *(tema Acciaio)* | <img src="assets/screenshots/playlist.png" width="230" alt="Playlist"> <img src="assets/screenshots/control.png" width="150" alt="Control"> |
| **Mini player** — VU, titolo scorrevole e trasporto essenziale *(tema Smeraldo)* | <img src="assets/screenshots/player-mini.png" width="420" alt="Mini player"> |

### Sfondi animati della finestra Karaoke

| Note musicali | Aurora |
|---|---|
| <img src="assets/screenshots/karaoke.png" width="400" alt="Sfondo note musicali"> | <img src="assets/screenshots/karaoke-aurora.png" width="400" alt="Sfondo aurora"> |
| **Stelle** | **Spettro musicale** |
| <img src="assets/screenshots/karaoke-stars.png" width="400" alt="Sfondo stelle"> | <img src="assets/screenshots/karaoke-spectrum.png" width="400" alt="Sfondo spettro musicale"> |

## Temi

Sei temi inclusi, applicati subito a tutte le finestre (menu ♪ → Tema, oppure Setup → Aspetto):

| | |
|---|---|
| <img src="assets/screenshots/theme-vocalis.png" width="400" alt="Tema Vocalis"><br>**Vocalis** — scuro, accenti ciano e viola | <img src="assets/screenshots/theme-aurora.png" width="400" alt="Tema Aurora"><br>**Aurora** — chiaro argento-lilla |
| <img src="assets/screenshots/theme-palco.png" width="400" alt="Tema Palco"><br>**Palco** — luce bassa, display ambra | <img src="assets/screenshots/theme-acciaio.png" width="400" alt="Tema Acciaio"><br>**Acciaio** — rack metallico blu |
| <img src="assets/screenshots/theme-smeraldo.png" width="400" alt="Tema Smeraldo"><br>**Smeraldo** — verde bosco, display lime | <img src="assets/screenshots/theme-corallo.png" width="400" alt="Tema Corallo"><br>**Corallo** — crema-pesca, accenti corallo |

Puoi creare **temi tuoi**: Setup → Aspetto → *Esporta come modello* salva i colori del tema attivo in un file da modificare e rimettere nella cartella dei temi (*Apri cartella temi*).

## Primi passi

1. **Apri un brano**: trascina un `.kar` o `.mid` sul Player (o sulla finestra Karaoke), oppure usa il pulsante 📂.
2. **Mostra i testi**: pulsante **KARAOKE**. In Regia → Brano scegli il monitor e passi a schermo intero.
3. **Costruisci la libreria**: Libreria → *Sorgenti* → aggiungi le cartelle con le basi; la ricerca diventa istantanea.
4. **Prepara la scaletta**: aggiungi i brani alla Playlist; chiave e tempo si salvano su ogni voce.
5. **Suono**: Regia → SoundFont per scaricare e attivare un banco diverso da quello incluso. In Setup → Audio/MIDI scegli l'uscita: synth interno, synth di sistema o strumento MIDI esterno.
6. **Prenotazioni**: Regia → Rete & prenotazioni avvia il servizio in rete locale e mostra il QR code da proiettare in sala.

## Scorciatoie da tastiera

| Scorciatoia | Azione |
|---|---|
| **Spazio** | Play / Pausa |
| **⌘K** (Ctrl+K su Windows/Linux) | Mostra / nascondi testi |
| **⌘← / ⌘→** | Indietro / avanti di 5 secondi |
| **⌘.** | Stop |
| **⌘⇧R** | Apri la Regia |

## Segnalare un problema

Hai trovato un bug o hai un'idea? Apri una segnalazione nella sezione [**Issues**](../../issues), indicando sistema operativo, versione di Vocalis e, se possibile, i passaggi per riprodurre il problema.

## Sostieni Vocalis

Vocalis è gratuito e sviluppato nel tempo libero. Se lo usi nelle tue serate e vuoi aiutarne lo sviluppo (nuove funzioni, firma degli installer, supporto a più piattaforme), puoi diventare sponsor:

<a href="https://github.com/sponsors/kikoz85"><img src="https://img.shields.io/badge/Sponsor-%E2%9D%A4-db61a2?logo=githubsponsors&logoColor=white&style=for-the-badge" alt="Sponsor su GitHub"></a>

Grazie! 🎤

## Crediti e licenze

- Vocalis è **gratuito**; il codice sorgente non è pubblico. © kikoz85.
- Include il SoundFont **GeneralUser GS** di S. Christian Collins ([licenza GeneralUser GS v2.0](https://www.schristiancollins.com/generaluser.php)).
- Gli altri SoundFont del catalogo si scaricano su richiesta dalla fonte originale; ognuno mantiene la propria licenza, indicata nell'app.
- Vocalis **non distribuisce basi musicali**: legge i file dell'utente.
- L'interfaccia si ispira all'esperienza d'uso di vanBasco's Karaoke Player, con grafica originale. «Roland GS» e «Yamaha XG» sono marchi dei rispettivi proprietari.
