# Cingolini

Gioco di carri armati in miniatura visto dall'alto: 80 missioni originali, colpi che rimbalzano, mine e 7 tipi di carri nemici. I progressi restano salvati nel browser.

Si gioca nel browser: https://selektor892.github.io/Tanks/

## Comandi

- **Computer:** WASD o frecce per muovere, mouse per mirare, clic per sparare, Spazio o clic destro per la mina, P o Esc per la pausa.
- **Telefono con giroscopio:** inclina per muovere, trascina il pollice destro per il mirino, tocca a sinistra per sparare, una spinta secca verso il basso per la mina. "Centra" ricalibra l'inclinazione.
- **Telefono senza sensori:** joystick a sinistra per muovere, joystick a destra per mirare (rilascia per sparare).

Tutto il gioco è in `index.html`, senza dipendenze.

## Multigiocatore

Dal menu "Multigiocatore" chi crea la stanza fa da host e riceve un codice di 5 caratteri e un link da condividere. Modalità: 1 contro 1, 2 contro 2, tutti contro tutti fino a 4. Vince chi arriva per primo a 3 o 5 round. Invio apre la chat durante la partita.

I giocatori si collegano direttamente tra loro (WebRTC) tramite [PeerJS](https://peerjs.com/), incluso in `peerjs.min.js` (licenza MIT, vedi `peerjs.LICENSE`). L'host deve tenere la scheda del gioco in primo piano: se la scheda va in background il browser rallenta la partita per tutti.
