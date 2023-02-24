# Libreria per chiamate REST generiche

## Dipendenze

* [JSONText (testato con v1.7.0.118)](vipm://jdp_science_jsontext?repo_url=http://download.ni.com/evaluation/labview/lvtn/vipm)

## Descrizione
La libreria può essere usata per effettuare delle chiamate REST generiche, oppure essere ereditata per costruire dei Client REST più specifici.

L'autenticazione al momento è di tipo API Key (la chiave di accesso va messa direttamente in un token che viene memorizzato in un file locale ed usato, finchè rimane valido) e quindi la gestione, il rilascio ed il linking del token ad un utente è a cura del servizio web che viene chiamato.

Altri tipi di autenticazione possono essere implementati, reimplementando la Initialize.vi che chiama la Auth_Token.vi.
Nel caso in cui sia un'altra autenticazione token-based, si può poi mettere il tutto nell'header dell'handler e mantenere il resto così com'è.
