## Ledger Mod README.md

### Comandi di Ledger Mod 📜

1. `/ledger search` 🕵️
   - Argomenti: `<query>`
   - Permessi: `ledger.search`
   - Descrizione: Cerca nel registro delle modifiche del mondo in base ai criteri specificati nella query. La query può includere diversi parametri come `player`, `action`, `block`, `radius`, `time`, `world`, e `location` . Ad esempio, per cercare le modifiche fatte da un giocatore specifico, utilizza `/ledger search player:<nome_giocatore>` .

2. `/ledger rollback` ⏪
   - Argomenti: `<query>`
   - Permessi: `ledger.rollback`
   - Descrizione: Annulla le modifiche al mondo in base ai criteri specificati nella query. La query può includere gli stessi parametri di `/ledger search` . Ad esempio, per annullare le modifiche fatte da un giocatore specifico, utilizza `/ledger rollback player:<nome_giocatore>` .

3. `/ledger restore` ⏩
   - Argomenti: `<query>`
   - Permessi: `ledger.restore`
   - Descrizione: Ripristina le modifiche al mondo precedentemente annullate in base ai criteri specificati nella query. La query può includere gli stessi parametri di `/ledger search` . Ad esempio, per ripristinare le modifiche fatte da un giocatore specifico, utilizza `/ledger restore player:<nome_giocatore>` .

4. `/ledger inspect` 🔍
   - Argomenti: `[on|off]`
   - Permessi: `ledger.inspect`
   - Descrizione: Attiva o disattiva la modalità di ispezione per visualizzare le informazioni sulle modifiche al mondo. Quando la modalità di ispezione è attiva, clicca con il tasto destro del mouse su un blocco per visualizzare le informazioni sulle modifiche relative a quel blocco.

5. `/ledger reload` 🔄
   - Argomenti: Nessuno
   - Permessi: `ledger.reload`
   - Descrizione: Ricarica la configurazione di Ledger dal file `config/ledger.toml` .

### Note aggiuntive 📌

- Ledger Mod richiede Fabric API e fabric-language-kotlin per funzionare correttamente.
- La configurazione di Ledger si trova nel file `config/ledger.toml` .
- Tutti i comandi di Ledger hanno un fallback sul livello di permesso 3, nel caso in cui non si desideri installare un mod di permessi.
