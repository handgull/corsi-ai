# Configurare la sicurezza per una soluzione Cognitive Services

In questa lezione vedremo i diversi parametri di sicurezza proposti con Azure Cognitive Services.<br>
L'accesso ai Cognitive Services è ristretto tramite delle subscription keys, gestire queste chiavi è un argomento fondamentale per la sicurezza, ora vedremo il processo raccomandato.

Al posto di hard codare le subscription keys nel nostro codice è raccomandato di usare un servizio (Service Principal identity) per accedere al Azure Key Vault, da lì si potrà ottenere la Key e passarla dinamicamente a Cognitive Services.

Come layer addizionale di sicurezza le Key vanno cambiate regolarmente per proteggerti dal rischio che le key siano condivise con utenti non autorizzati.

Ogni cognitive service è messo a disposizione con 2 keys, questo permette di poter rigenerare le keys senza avere un interruzione dei servizi

## Steps per usare Azure Key Vault ed un Service Principal Identity

- Avere una risorsa Cognitive Services, questo genera 2 key che possono essere gestite da Azure CLI o dal portale
- Creare un Azure Key Vault ed aggiungere un secret, per fare questo bisogna andare nel Azure portal e cliccare su create a Key Vault resource. Quando la risorsa è creata, nel pannello di navigazione di sinistra selezionate Secrets poi generate import, name your secret ed associateci il valore di KEY 1
- Ora per accedere a un secret nella key vault la vostra applicazione deve usare un service principal che ha accesso ai secrets. Per esempio potete usare Azure CLI per creare un service principal e garantire l'accesso ai secrets nel key vault
- Infine dopo aver installato i package appropriati nella vostra app, tipicamente azure.identity e azure.security.keyvault.secrets sarete capaci di effettuare una richiesta ad Azure Key Vault per recuperare la vostra key

## Secure Cognitive Services usando Azure VNET

Azure Cognitive Services fornisce un layer di sicurezza aggiuntivo, una volta specificati i vostri Cognitive Services saranno accessibili soltanto tramite uno specifico sottoinsieme di reti tramite il request filtering dando il permesso solo a richieste che arrivano da determinati ip, range di ip o da una lista di sottoreti in Azure Virtual Networks (VNETs)
