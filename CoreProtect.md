# Comandi ✨

Puoi accedere ai seguenti comandi utilizzando `/co`.

## Panoramica dei comandi 📜

| Comando             | Descrizione                      |
| ------------------ | -------------------------------- |
| `/co help`         | Mostra un elenco di comandi       |
| `/co inspect`      | Attiva/disattiva l'ispettore      |
| `/co lookup`       | Cerca dati del blocco             |
| `/co rollback`     | Ripristina dati del blocco        |
| `/co restore`      | Ripristina dati del blocco        |
| `/co purge`        | Elimina dati del blocco vecchi    |
| `/co reload`       | Ricarica il file di configurazione|
| `/co status`       | Visualizza lo stato del plugin    |
| `/co consumer`     | Attiva/disattiva l'elaborazione dei dati|

### Comandi Alias 🔄

| Comando   | Descrizione                                         |
| --------- | --------------------------------------------------- |
| `/co near` | Esegue una ricerca con un raggio di 5                |
| `/co undo` | Annulla un rollback/ripristino tramite l'azione opposta|

## Dettagli dei comandi ℹ️

### `/co help` ❓

Mostra un elenco di comandi nel gioco.

### `/co inspect` 🔍

Attiva l'ispettore. Digita nuovamente il comando per disattivarlo. Puoi anche usare semplicemente "/co i".

### `/co lookup` 🔎

Esegue una ricerca dei dati del blocco. La maggior parte dei parametri è facoltativa.

#### Parametri

- `u:<utente>`: Specifica l'utente(i) da cercare.
- `t:<tempo>`: Specifica l'intervallo di tempo da cercare.
- `r:<raggio>`: Specifica un'area di raggio per limitare la ricerca.
- `a:<azione>`: Limita la ricerca a una determinata azione.
- `i:<includi>`: Includi blocchi/entità specifiche nella ricerca.
- `e:<escludi>`: Escludi blocchi/entità dalla ricerca.
- `#<hashtag>`: Aggiungi un hashtag per eseguire azioni aggiuntive.

#### Paginazione

Se vengono restituite più pagine, utilizza il comando `/co lookup <pagina>` per passare alle pagine successive. Per modificare il numero di righe visualizzate in una pagina, usa `/co lookup <pagina>:<righe>`.

Esempio:
- `/co lookup u:Notch t:1h r:20 a:break i:diamond_block e:lava #preview` 🌟: Esegue una ricerca delle azioni di Notch nell'ultima ora in un raggio di 20 blocchi, limitato alle azioni di distruzione di blocchi di diamante, escludendo blocchi di lava. Mostra solo l'anteprima dei risultati.

### `/co rollback` ⏪

Esegue un ripristino dei dati del blocco. Utilizza gli stessi parametri di `/co lookup`.

Esempio:
- `/co rollback u:Notch,Intelli t:1h r:30 a:place,use i:diamond_block e:lava` ⚡️: Esegue un ripristino delle azioni di Notch e Intelli nell'ultima ora in un raggio di 30 blocchi, limitato alle azioni di posizionamento e utilizzo di blocchi di diamante, escludendo blocchi di lava.

### `/co restore` 🔄

Alias di `/co rollback`.

### `/co purge` 🗑️

Elimina i dati del blocco vecchi. Utilizza gli stessi parametri di `/co lookup`.

Esempio:
- `/co purge t:1w` 🚮: Elimina tutti i dati vecchi di una settimana.

### `/co reload` 🔄

Ricarica il file di configurazione del plugin.

### `/co status` ℹ️

Visualizza lo stato del plugin.

### `/co consumer` ⚙️

Attiva o disattiva l'elaborazione dei dati del blocco.

## Esempi di comandi 🌟

Di seguito sono riportati alcuni esempi di comandi utilizzando diversi parametri disponibili:

#### Esempi di comandi di lookup

Per impostazione predefinita, se non viene specificato un raggio, viene utilizzato un raggio di 5 blocchi, limitando la ricerca a 5 blocchi dalla posizione corrente del giocatore.

- `/co lookup u:Notch t:1h` 🔍: Esegue una ricerca delle azioni di Notch nell'ultima ora (con raggio predefinito di 5).
- `/co lookup u:Notch t:1h r:#globale #preview` 🔍: Esegue un'anteprima della ricerca delle azioni di Notch nell'ultima ora a livello globale.

#### Esempi di comandi di rollback

Per impostazione predefinita, se non viene specificato un raggio, viene utilizzato un raggio di 10 blocchi, limitando il ripristino entro 10 blocchi dalla posizione del giocatore.

- `/co rollback u:Notch,Intelli t:1h` ⏪: Esegue un ripristino delle azioni di Notch e Intelli nell'ultima ora (con raggio predefinito di 10).
- `/co rollback u:Notch,Intelli t:1h r:#globale #preview` ⏪: Esegue un'anteprima del ripristino delle azioni di Notch e Intelli nell'ultima ora a livello globale.
