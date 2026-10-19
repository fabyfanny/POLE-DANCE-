# Pole Studio — Condiviso (gratis)

Due spazi separati nello stesso sito, per **iPhone e Android**.

- **Insegnante:** `index.html` — crea figure, foto, schede tecniche, lezioni e note personali. Le modifiche restano sul dispositivo fino a quando decidi di pubblicare.
- **Allievi:** `allievi.html` — vedono le figure e le lezioni che selezioni, cercano per livello e segnano *Non iniziata*, *In studio* o *Padroneggiata*. I progressi sono privati e salvati **solo sul telefono di ciascun allievo**, non visibili dall'insegnante.

## INSTALLAZIONE CON GITHUB PAGES (COSTO: 0 €)

1. Su GitHub crea un **nuovo repository pubblico** `pole-studio` (non modificare Agenda Mia).
2. Estrai lo ZIP e trascina **il contenuto** della cartella, non la cartella intera, dentro **Add file → Upload files** del nuovo repository.
3. Verifica che `index.html`, `allievi.html`, `catalogo.json`, `app.js`, `allievi.js`, `style.css`, `allievi.css`, `sw.js` e `icons/` siano nella **radice** del repository. Conferma con **Commit changes** (o Propose changes, a seconda dell'interfaccia GitHub).
4. In **Settings → Pages**, scegli `Deploy from a branch → main → /(root)` e premi Save.
5. Aspetta *Your site is live*. Apri il link pubblico sul telefono con Safari → Condividi → Aggiungi alla schermata Home.
6. Il link per gli allievi termina con **`/allievi.html`**. Puoi copiarlo direttamente dalla sezione **Condividi** della tua app.

## COME PUBBLICARE NUOVE FIGURE E LEZIONI

1. Dall'**iPhone dell'insegnante** apri la tua app e crea o modifica figure e lezioni.
2. Vai in **Condividi**; spunta soltanto le figure e le lezioni che vuoi rendere pubbliche.
3. Premi **Scarica catalogo.json**. Il file contiene **solo** le figure e le lezioni selezionate; NON contiene le note private, il diario, i check dei passi o i progressi dell'insegnante. Controlla anche se le foto sono pubblicabili.
4. Dal Mac (puoi inviare il file con AirDrop o salvarlo su iCloud Drive), apri il repository su GitHub, vai in **Add file → Upload files**, carica **catalogo.json** nella radice al posto di quello precedente e conferma la modifica. La pubblicazione non è automatica, per la tua sicurezza.
5. Dopo che GitHub Pages ha aggiornato il sito (può richiedere qualche minuto), chiedi agli allievi di premere **Aggiorna**. Vedranno le nuove figure e lezioni, senza perdere i propri progressi.

**Se GitHub non consente di sostituire `catalogo.json` dall'interfaccia Upload files**, puoi usare l'app gratuita *GitHub Desktop*: clona il repository, sostituisci il file nella cartella locale, fai Commit e Push. In alternativa il file può essere aggiornato con Git da terminale. Non eliminare e ricreare il repository o cambiare l'URL.

## RISERVATEZZA E SICUREZZA

- Il repository GitHub Pages gratuito è **pubblico**: i contenuti condivisi possono essere visualizzati da chiunque conosca il link. Non pubblicare dati personali, foto di minori senza le autorizzazioni necessarie, note private o materiale che non hai diritto di condividere.
- Le aree non sono protette da password. La schermata dell'insegnante è **locale**, non un pannello amministratore autenticato. Gli allievi non possono modificare il catalogo online, perché GitHub richiede l'accesso del proprietario per pubblicare nuovi file.
- I progressi degli allievi non si sincronizzano su telefoni diversi. Ogni allievo può esportare/importare un backup dalla sezione **Altro**.
- Il catalogo pubblico incorpora le foto in un file JSON. GitHub limita il caricamento da browser a **25 MiB per file**. Se diventa troppo grande, riduci la quantità o la dimensione delle foto.
- Esegui regolarmente il **backup privato** dall'app insegnante: GitHub non salva automaticamente le tue bozze, immagini private e note.
- Con questa soluzione **tu non vedi i progressi dei singoli allievi**. Per avere account individuali, monitoraggio centralizzato e sincronizzazione automatica servirebbe una diversa architettura con database e accessi autenticati.

## Aggiornare l'app già pubblicata

Se usi già una versione precedente di Pole Studio sullo **stesso indirizzo GitHub Pages**, sostituisci i file del repository con quelli nuovi **senza cancellare i dati di Safari**. I dati esistenti sul dispositivo rimangono nell'IndexedDB (`pole-studio`). Fai comunque un backup prima dell'aggiornamento. Se crei un repository con un URL diverso, i vecchi contenuti locali non si trasferiscono automaticamente: usa Esporta/Ripristina backup.
