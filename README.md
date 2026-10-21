# 📚 Appunti di Quantum Physics - A.A. 2026/2027

[🇬🇧 Read in English](README.en.md)

Benvenuti nella repository condivisa degli appunti del corso di Quantum Physics! Qui raccogliamo, scriviamo in **LaTeX** e aggiorniamo insieme il materiale delle lezioni.

---

## 🛠️ 1. Installazione e Configurazione Iniziale (Solo la prima volta)

Per scrivere e compilare gli appunti sul tuo computer devi installare **Git**, **Visual Studio Code** e un **compilatore LaTeX**. Segui la guida passo-passo per il tuo sistema operativo.

---

### 🪟 GUIDA PER WINDOWS

#### Passo 1.1: Installare Git
1. Vai sul sito ufficiale di Git: [git-scm.com/download/win](https://git-scm.com/download/win).
2. Il download dovrebbe partire in automatico (oppure clicca su *Click here to download manually* se usi versioni a 64-bit).
3. Apri il file scaricato (`.exe`) e clicca su **Avanti (Next)** in tutte le schermate, lasciando attive le impostazioni predefinite consigliate.

#### Passo 1.2: Installare Visual Studio Code (VS Code)
1. Vai sul sito ufficiale: [code.visualstudio.com](https://code.visualstudio.com/).
2. Clicca sul grande pulsante blu **Download for Windows** per scaricare l'installer.
3. Apri il file eseguibile scaricato. Durante l'installazione:
   * Accetta le condizioni della licenza.
   * Assicurati di spuntare la casella **"Aggiungi 'Apri con Code' al menu contestuale di Windows"** e **"Aggiungi a PATH"** (così il computer riconoscerà VS Code ovunque).
   * Clicca su **Installa** e poi su *Fine*.

#### Passo 1.3: Installare il compilatore LaTeX (MiKTeX + Strawberry Perl)
Per compilare i file `.tex` su Windows serve MiKTeX (il motore LaTeX) e Strawberry Perl (necessario a VS Code per automatizzare la generazione del PDF):
1. **Installa MiKTeX:** 
   * Vai su [miktex.org/download](https://miktex.org/download) e scarica l'installer per Windows.
   * Avvialo, accetta i termini e seleziona *Install MiKTeX only for me* (o per tutti gli utenti).
   * Nella schermata dei pacchetti mancanti, seleziona **Yes** alla voce *"Install missing packages on-the-fly"* (eviterà errori se usi pacchetti particolari). Al termine, chiudi l'installazione.
2. **Aggiorna MiKTeX:**
   * Apri il menu Start di Windows, cerca e apri **MiKTeX Console**.
   * Clicca su **Updates** nel menu a sinistra, poi su **Check for updates**. Se ci sono aggiornamenti, clicca su **Update now**.
3. **Installa Strawberry Perl (OBBLIGATORIO per Windows):**
   * Vai su [strawberryperl.com](https://strawberryperl.com/).
   * Scarica la versione raccomandata a 64-bit (`.msi` installer).
   * Apri il file scaricato e clicca su *Avanti* fino al completamento dell'installazione.
4. **Riavvia il computer** per rendere effettive le modifiche.

---

### 🍎 GUIDA PER MAC (macOS)

#### Passo 1.1: Installare Git
1. Apri l'app **Terminale** sul Mac (premi `Cmd + Spazio`, digita "Terminale" e premi Invio).
2. Scrivi il comando `git --version` e premi Invio.
3. Se Git non è installato, macOS aprirà automaticamente una finestra che ti chiederà di installare gli *Strumenti da riga di comando (Command Line Tools)*. Clicca su **Installa** e attendi il termine del download.

#### Passo 1.2: Installare Visual Studio Code (VS Code)
1. Vai sul sito ufficiale: [code.visualstudio.com](https://code.visualstudio.com/).
2. Clicca sul pulsante di download per Mac (seleziona la versione *Universal* o quella specifica per il tuo processore Apple Silicon / Intel).
3. Apri la cartella *Download* e trascina l'icona di **Visual Studio Code** dentro la cartella **Applicazioni**.

#### Passo 1.3: Installare il compilatore LaTeX (MacTeX)
Su Mac esiste un pacchetto completo che include tutto il necessario senza configurazioni aggiuntive:
1. Vai sul sito del MacTeX: [tug.org/mactex/mactex-download.html](https://tug.org/mactex/mactex-download.html).
2. Clicca sul link **`MacTeX.pkg`** per avviare il download (è un file pesante, circa 5 GB, poiché include già tutti i pacchetti di simboli e font matematici).
3. Una volta completato il download, apri il file `.pkg` e segui la procedura guidata di installazione cliccando sempre su *Continua* e inserendo la password del Mac quando richiesto. *(Nota: su macOS il supporto a Perl è già integrato nativamente nel sistema).*

---

### ⚙️ Configurare VS Code (Valido per Windows e Mac)

Una volta installati tutti i programmi, apri **Visual Studio Code** e completa questi ultimi passaggi:

1. **Installa l'estensione LaTeX Workshop:**
   * Clicca sull'icona **Extensions** nella barra laterale a sinistra (i quattro quadratini, oppure premi `Ctrl + Shift + X` su Windows / `Cmd + Shift + X` su Mac).
   * Digita **`LaTeX Workshop`** (sviluppata da *James Yu*) e clicca su **Install**.
2. **Configura Git con il tuo nome e la tua email:**
   * Dal menu in alto di VS Code seleziona **Terminal** -> **New Terminal**.
   * Nel pannello del terminale in basso, incolla questi due comandi (sostituendo i dati tra virgolette con il tuo nome reale e la mail associata al tuo account GitHub) e premi Invio dopo ciascuno:
     ```bash
     git config --global user.name "Tuo Nome"
     git config --global user.email "tua-email@esempio.com"
     ```
3. **Collega il tuo account GitHub a VS Code:**
   * Clicca sull'icona del **Profilo** (ingranaggio o omino in basso a sinistra nella barra laterale di VS Code).
   * Clicca su **Sign in with GitHub to use...** e autorizza l'accesso tramite la pagina del browser che si aprirà in automatico.

---

## 📥 2. Come scaricare la Repository su VS Code (Clonazione)

1. Apri VS Code.
2. Premi `Ctrl + Shift + P` (su Windows) oppure `Cmd + Shift + P` (su Mac) per aprire la barra dei comandi in alto.
3. Digita **`Git: Clone`** e premi Invio.
4. Seleziona **Clone from GitHub** (oppure incolla direttamente l'URL di questa pagina web).
5. Seleziona la repository dalla lista che compare e scegli una cartella vuota sul tuo computer in cui salvarla.
6. Quando VS Code ti chiede in basso a destra se desideri aprire la cartella clonata, clicca su **Open**.

---

## 📄 3. Come sono organizzati i file LaTeX e come compilare il PDF

Per evitare che due persone modifichino lo stesso file contemporaneamente creando conflitti, gli appunti sono organizzati in questo modo:

* **`main.tex`**: è il file principale. Contiene solo l'impostazione grafica, i pacchetti (`\usepackage`), l'indice e i richiami alle singole lezioni (`\input{lezioni_ita/lezioneXX.tex}`). **Non scrivere gli appunti direttamente qui dentro.**
* **Cartella `lezioni_ita/`**: contiene un file separato per ogni lezione (es. `lezione01.tex`, `lezione02.tex`). Qui dentro va scritto solo il testo della lezione (partendo direttamente da `\section{...}`), **senza** rimettere `\documentclass` o `\begin{document}`.
* **Cartella `immagini/`**: contiene tutte le immagini o schemi richiamati negli appunti.

### Come generare e vedere il PDF su VS Code:
1. Quando scrivi e salvi un file `.tex` (`Ctrl + S` su Windows / `Cmd + S` su Mac), *LaTeX Workshop* avvierà la compilazione automatica in background.
2. Per vedere l'anteprima del PDF affiancata al codice, apri il file `main.tex` e clicca sull'icona **View LaTeX PDF** in alto a destra (il foglio con la lente d'ingrandimento). Scegli se visualizzarlo in una tab interna di VS Code o nel browser.
3. *Nota importante:* Il file PDF finale compilato (`main.pdf`) resta salvato solo sul tuo computer per consentirti di leggere l'anteprima; viene automaticamente ignorato da Git (grazie al file `.gitignore` impostato su `TeX`) per evitare conflitti e blocchi durante la sincronizzazione con i colleghi.

---

## 🔄 4. Come lavorare insieme (Flusso quotidiano)

Per non sovrascrivere il lavoro degli altri, segui **sempre** questi 4 passaggi nell'ordine esatto ogni volta che apri VS Code per studiare o aggiungere appunti:

### Passo A: Scarica le modifiche degli altri (`Pull`) — *FALLO SEMPRE PRIMA DI INIZIARE*
Prima di scrivere qualsiasi riga di testo, assicurati di avere l'ultima versione aggiornata:
1. Clicca sull'icona **Source Control** nella barra a sinistra (quella con i tre pallini collegati da linee, oppure premi `Ctrl + Shift + G`).
2. Clicca sui tre puntini **`...`** in alto nel pannello Source Control -> **Pull**. *(In alternativa, puoi cliccare sull'icona delle frecce circolari di sincronizzazione in basso a sinistra nella barra di stato).*

### Passo B: Scrivi o modifica gli appunti
* Apri il file della lezione su cui devi lavorare (dentro la cartella `lezioni/`) oppure creane uno nuovo e aggiungilo in `main.tex` tramite il comando `\input{lezioni/nomefile.tex}`.
* Salva il file (`Ctrl + S` o `Cmd + S`) e controlla dal pannello PDF che la compilazione avvenga senza errori.

### Passo C: Registra le tue modifiche locali (`Commit`)
Quando hai finito di scrivere o sistemare una lezione:
1. Torna nel pannello **Source Control** a sinistra: vedrai l'elenco dei file modificati sotto la voce *Changes*.
2. Passa il mouse sopra la voce *Changes* e clicca sul simbolo **`+`** (*Stage All Changes*) per aggiungere i file pronti per il salvataggio.
3. Nella casella di testo **Message** in alto, scrivi un messaggio breve ma chiaro che spiega cosa hai fatto (es. `Aggiunti appunti lezione 04 su matrici e vettori`).
4. Clicca sul grande pulsante blu **Commit**.

### Passo D: Invia le modifiche online (`Push`)
1. Subito dopo aver fatto il Commit, il pulsante blu cambierà etichetta in **Sync Changes** (o **Push**). Cliccaci sopra.
2. Le tue modifiche verranno caricate sulla repository online di GitHub, pronte per essere scaricate dai tuoi colleghi.

---

## 🌿 5. Lavorare su modifiche grandi senza fare danni (Branch)

Se tu o un tuo collega dovete fare una revisione profonda, riorganizzare i capitoli o scrivere molte pagine di prova, **non lavorate direttamente sul ramo principale (`main`)**, ma create un ramo separato:
1. Clicca sul nome del ramo attuale (solitamente **`main`**) che vedi in basso a sinistra nella barra di stato di VS Code.
2. Nel menu a tendina che compare in alto, seleziona **+ Create new branch...**.
3. Dagli un nome descrittivo senza spazi (es. `revisione-analisi` o `aggiunta-esercizi`) e premi Invio.
4. Lavora normalmente facendo i tuoi *Commit* e *Push* su questo nuovo ramo (cliccando su *Publish Branch* la prima volta).
5. Quando il lavoro è completo e verificato, vai sulla pagina web di GitHub della repository e apri una **Pull Request** per unire in modo sicuro il tuo ramo al `main`.

---

## ⚖️ Licenza

Quest'opera è distribuita con Licenza **[Creative Commons Attribuzione - Non commerciale - Condividi allo stesso modo 4.0 Internazionale (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.it)**.

* **Sei libero di:** condividere, copiare e ridistribuire il materiale con qualsiasi mezzo e formato per qualsiasi fine non commerciale.
* **Alle seguenti condizioni:** devi riconoscere una menzione di paternità adeguata agli autori originali, indicare se sono state effettuate modifiche, non puoi utilizzare il materiale a scopo di lucro e, se remixi o trasformi il materiale, devi distribuire i tuoi contributi con la stessa identica licenza del materiale originario.
