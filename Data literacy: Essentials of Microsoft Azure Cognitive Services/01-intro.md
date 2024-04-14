# Introduzione

i Cognitive Services di Azure non sono come gli altri servizi offerti da Azure, sono fantastici servizi cloud-based pieni di strumenti AI che permettono allo sviluppatore di costruire applicazioni AI.

## Argomenti principali

Gli argomenti principali del corso saranno:

- Progettazione con i Cognitive Services
- Pubblicare una soluzione AI responsabile
- Implementare containers
- Configurare la sicurezza
- Monitorare Cognitive Services

## Prerequisiti

Per seguire questo corso si presuppone che voi abbiate familiarità con Azure, Azure Portal ed i concetti dell'AI.

## Come inizieremo

Inizieremo mostrando i casi d'uso di base ed i componenti di Azure Cognitive Services

# Azure Cognitive Services

## Cos'è l'AI?

Un software che ha abilità umane come:

- **La percezione visiva**
- L'**analisi del testo** estraendo significato semantico da un testo
- **Fare discorsi**
- **Prendere decisioni**, tramite l'accumulo di eperienze e imparando la correlazione tra due o più eventi

> La capacità di analisi del testo e quella di fare discorsi portano L'AI e gli umani a poter in qualche modo comunicare

## Cosa sono gli Azure Cognitive Services

I Cognitive Services sono un set di servizi Microsoft basati sul cloud che incapsulano strumenti AI, essi quindi non sono un singolo prodotto bensì una collezione di servizi individuali che puoi usare come mattoncini per costruire soffisticate ed intelligenti applicazioni.

I Cognitive Services offrono un ampia gamma di strumenti AI in svariate categorie.<br>
Per l'area del linguaggio abbiamo:

- **Text Analytics**: per l'analisi sentimentale
- **Translator**: per le traduzioni in più di 90 lingue supportate
- **Immersive Reader**, che aiuta i lettori di ogni livello a capire un testo con l'aiuto di audio e video
- **Language Understanding**, che permette di portare la comprensione del linguaggio naturale nelle nostre app, bot ecc
- **QnA Maker**: può creare un layer conversazionale sui tuoi dati fatto di domande e risposte per migliorare l'esperienza del cliente
- **Speech Service**: può trasformare audio in testo leggibile o fare il contrario, traduzioni di audio. Riconoscimento della persona che sta parlando tramite degli audio (funzione in preview)

Per l'area della visione (identificare ed analizzare contenuti video e immagini):

- **Computer Vision**, analizza il contenuto di immagini e video
- **Video Indexer**, analizza le immagini e i suoni di un video ed indicizza il suo contenuto
- **Custom Vision**: puoi customizzare il riconoscimento delle immagini per il tuo business model
- **Face**, per riconoscere ed identificare persone e emozioni nelle immagini.
- **Form Recognizer** per estrarre testi, coppie chiave valore e tabelle da documenti.

Per l'area decisionale:

- **Anomaly Detector** per identificare preventivamente anomalie e potenziali problemi.
- **Content Moderator** per scovare contenuti potenzialmente offensivi o non voluti
- **Metric Advisor**: (è in preview) monitora e analizza problemi
- **Personalizer**: per creare un esperienza utente personalizzata per ogni utente

C'è inoltre un area bot (Azure Bot Service)

Infine abbiamo Azure Cognitive Search (conosciuta anche come Azure Search), è un servizio cloud di ricerca che da al developer le API e gli strumenti per creare un ottima esperienza di ricerca in un contenuto privato ed eterogeneo.
Azure Cognitive Search semplifica il compito di aggiungere soffisticate soluzioni di recupero informazioni
