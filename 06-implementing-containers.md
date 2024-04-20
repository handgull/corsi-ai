# Implementare container di Cognitive Services

I Cognitive Services sono parte dei servizi offerti da Azure, perciò sono disponibili come PaaS servizi cloud, comunque è anche possibile inglobare questi strumenti nei tuoi container.

## Considerazioni per la pubblicazione di un container

La latenza dovuta dai servizi può essere evitata con i container, avendo quindi i dati in locale.

- ci sono immagini disponibili per circa tutti i più comuni Cognitive Services
- Queste immagini possono essere deployate dove si vuole
- Ogni container contiene un sotto gruppo delle funzionalità dei Cognitive Services, per esempio non tutte le features di Text Analytics sono in un singolo container
- Dati sull'utilizzo e varie metriche sono invate ad azure per stabilire quanto si paga i Cognitive Services usati
