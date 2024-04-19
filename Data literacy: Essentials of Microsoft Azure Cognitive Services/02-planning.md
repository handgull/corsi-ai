# Planning with cognitive services

Ora vedremo come pubblicare ed usare questi fantastici servizi.<br>
Per usare uno qualsiasi dei Cognitive Services si deve creare una risorsa appropriata in un Azure Subscription per definire un endpoint dove il service sarà consumato, fornire access keys per un accesso autenticato e per gestire le ricevute di utilizzo del servizio.

## Come disporre i servizi

Per disporre i servizi si hanno i seguenti modi disponibili:

- Disporre **individualmente** i servizi, questo approccio permette di avere un endpoint separato per ogni servizio per esempio per disporli in differenti regioni geografiche e di gestire le credenziali di accesso indipendentemente per ogni servizio. Questo approccio inoltre ti permette di avere ricevute di utilizzo separate per ogni servizio.
- Disporre una risorsa che supporta **diversi** Cognitive Services, per esempio potremmo creare una singoloa risorsa che utilizza Text Analytics, Computer Vision, Speech e altri servizi. Questo approccio ti permette di gestire un singolo set di credenziali per consumare diversi servizi in un singolo endpoint ed una singola fattura di utilizzo.

## Risorse necessarie all'utilizzo dei servizi

Per utilizzare concretamente questi servizi attraverso gli endpoint la nostra app ha bisogno delle seguenti informazioni:

- HTTPS **endpoint** URI (a cui il client manda la richiesta, è una REST API)
- Una **key** (per autenticare le chiamate)
- **Posizione** di dove la risorsa è hostata (richiesta ma non da tutti i servizi) per determinare quale azure datacenter deve essere usato

## REST APIs

Cognitive Services fornisce una REST API che le nostre applicazioni possono usare per utilizzare i servizi, nella maggior parte dei casi i servizi possono essere chiamati fornendo dati JSON in una chiamata HTTP.<br>
Possono esserci chiamate POST, GET, PUT ecc, le response sono in formato JSON. Il fatto che Cognitive Services usi le REST API lo rende compatibile con praticamente ogni tecnologia

## Cognitive Services SDKs

Nonostante ci siano le api rest, Cognitive Services fornisce anche delle SDK per i linguaggi più comuni che astraggono le Cognitive Services APIs, la disponibilità dell'SDK può variare da servizio a servizio.
