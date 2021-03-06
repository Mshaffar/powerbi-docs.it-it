---
title: Log delle modifiche per il server di report Power BI
description: Questo log delle modifiche è relativo al server di report di Power BI ed elenca i nuovi elementi e le correzioni di bug per ogni versione.
ms.author: jaimeta
author: jtarquino
ms.reviewer: maggies
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: conceptual
ms.date: 04/08/2020
ms.openlocfilehash: abe0b97a4c4f593f8bb22be8b72c12295d0f656c
ms.sourcegitcommit: 7aa0136f93f88516f97ddd8031ccac5d07863b92
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/05/2020
ms.locfileid: "81006458"
---
# <a name="change-log-for-power-bi-report-server"></a>Log delle modifiche per il server di report Power BI

Questo log delle modifiche è relativo al server di report di Power BI ed elenca i nuovi elementi e le correzioni di bug per ogni versione.

Per informazioni dettagliate sulle nuove funzionalità, vedere [Novità del Server di report di Power BI](whats-new.md). 


## <a name="january-2020"></a>Gennaio 2020
- **Server di report di Power BI**
    - *Versione: 1.6.7364.4075 (build 15.0.1102.777), data di rilascio: 2 marzo 2020*
         - Correzioni di bug
           -  Correzione per i report di Power BI che non vengono caricati per determinate origini dati
           -  Correzione per il percorso di download del collegamento del Server di report di Power BI Desktop dal portale
           -  Correzione per DynamicImageDPI per il rendering di Excel
           -  Correzione per le connessioni Oracle con impostazioni cultura dei thread non corrette in determinati scenari multiutente (vedere [Documentazione di UseInstalledUICulture](https://docs.microsoft.com/power-bi/report-server/connect-data-sources) per altri dettagli)
           -  Correzione per il valore predefinito di CustomHeaders che causa errori per l'incorporamento di report
           -  Correzione per i nomi di parametri SQL generati in modo errato in determinati casi
    - *Versione: 1.6.7327.3007 (build 15.0.1102.759), data di rilascio: 23 gennaio 2020*
         - Funzionalità
            -  Esportare in Excel da report di Power BI.
           -  Supporto di set di dati di Power BI Premium per report impaginati.
           -  Supporto di AltText (testo alternativo) per gli elementi di report impaginati.
           -  Supporto per intestazioni personalizzate.
           -  Supporto di Istanza gestita di database SQL di Azure come catalogo.
           -  Transparent Data Encryption per il catalogo.
        - Aggiornamenti per la sicurezza
        - Correzioni di bug
            - Correzioni per l'accessibilità per utilità per la lettura dello schermo, il rendering dei report e gli spostamenti tramite tastiera.
            - Correzione per il salvataggio di titoli di report a più byte.
            - Correzione per la registrazione dettagliata che influisce sull'affidabilità del server di report.
          - Correzione per garantire la disponibilità di dati in tempo reale nei report di Power BI su dispositivi mobili.
          - Correzione per l'applicazione dell'evidenziazione incrociata tra oggetti visivi nell'esportazione filtrata di report di Power BI.
          - Correzione per la scrittura del piè di pagina durante l'esportazione in Word con espressione per la visibilità per i report impaginati. 
     
- **Power BI Desktop (ottimizzato per il server di report di Power BI)**
    - *Versione: 2.76.5678.1521 (gennaio 2020), data di rilascio: 23 gennaio 2020* (nuova build e nuova versione)
        - Include modifiche necessarie per la connessione a Server di report di Power BI (gennaio 2020)        


## <a name="september-2019"></a>Settembre 2019
- **Server di report di Power BI**
    - *Versione: 1.6.7236.4246 (build 15.0.1102.646), data di rilascio: 25 ottobre 2019*
        - Aggiornamenti per la sicurezza
        - Correzioni di bug
            - Correzione per .NET Framework 4.7 non installato.
            - Correzione per i report impaginati per Teradata con parametri multivalore con errore 110083.
            - La correzione per il valore URLRoot non funziona se sono presenti più binding di URL del servizio Web e uno di essi è https://+80/reportserver.
          - Correzione per i valori dei parametri multivalore per report impaginati che vengono visualizzati all'esterno dell'area del report.
          
    - *Versione: 1.6.7221.30698 (build 15.0.1102.620), data di rilascio: 9 ottobre 2019*
        - Correzioni di bug
            - Correzione per l'oggetto visivo personalizzato Filtro testo.
            - Correzione per le prestazioni dei filtri dei dati a discesa.
            - Correzione per la rimozione di informazioni personali dalla telemetria.
          - Correzione per gli URL perché non ci sia distinzione tra maiuscole e minuscole.
          
    - *Versione 1.6.7206.38019 (build 15.0.1102.597), data di rilascio: 26 settembre 2019*
        - Aggiornamenti per la sicurezza
        - Correzioni di bug
           - Report impaginati
             - Correzione dei problemi di accessibilità riscontrati durante l'uso di Internet Explorer e Microsoft Edge.
             - Correzione di problemi di SAP HANA durante il test della connessione.
             - Correzione dei problemi rilevati durante l'inserimento di un elenco di indirizzi di posta elettronica.
             - Correzione per i report di Power BI che usano un'origine dati DirectQuery e l'autenticazione integrata.
             - Correzione per i report impaginati per il rendering con i parametri di filtro quando lo snapshot è abilitato.
             - Correzione della doppia esecuzione di stored procedure durante l'esecuzione del report.
             - Correzione per l'account del servizio predefinito a cui vengono concesse autorizzazioni di accesso di SQL Server, quando l'account del servizio personalizzato è configurato per l'esecuzione di Server di report di Power BI.
             - Correzione per l'accesso ai modelli durante l'aggiornamento nel fuso orario giapponese.
             - Correzione per i modelli non aggiornati quando viene caricata una nuova versione del report durante l'aggiornamento.
             - Correzione per i valori dei parametri che contengono il carattere '&'.
         - Programmabilità
             - Aggiornamento dell'API Web /PowerBIReports({Id})/DataSources (PATCH) per consentire gli aggiornamenti della stringa di connessione.
         
- **Power BI Desktop (ottimizzato per il server di report di Power BI)**
    - *Versione: 2.73.5586.1501 (settembre 2019), data di rilascio: 25 ottobre 2019*
        - Correzioni di bug
            - Correzione per la telemetria.
            
    - *Versione: 2.73.5586.1241 (settembre 2019), data di rilascio: 9 ottobre 2019*
        - Correzioni di bug
            - Correzione per l'oggetto visivo personalizzato Filtro testo.
            - Correzione per le prestazioni dei filtri dei dati a discesa.
            - Correzione per la rimozione di informazioni personali dalla telemetria.
            
    - *Versione: 2.73.5586.821 (settembre 2019), data di rilascio: 26 agosto 2019* (nuova build e nuova versione)
        - Include modifiche necessarie per la connessione a Server di report di Power BI (settembre 2019)

    
## <a name="may-2019"></a>Maggio 2019

- **Server di report di Power BI**          
    - *Versione 1.5.7074.36177 (build 15.0.1102.371), data di rilascio: 21 maggio 2019*
        - Correzioni di bug
            - Report impaginati
                - Correzione per abilitare sempre l'incorporamento di tipi di carattere in pdf.
                - Correzione per impostare i cookie inviati in https come sicuri
                - Correzione di errori di pop up causati da errori di script
                - Correzione di problemi di visualizzazione con app per dispositivi mobili nei telefoni Android
                - Correzione dello strumento di spostamento temporale per report dispositivi mobili in modo che siano visualizzati i numeri di settimana corretti indipendentemente dall'inizio dell'anno fiscale
                - Aggiunta della proprietà configurabile "RestrictedResourceMimeTypeForUpload" per consentire agli amministratori di specificare tipi di MIME esclusi
         - Funzionalità
            - Aggiunta del supporto per gli oggetti visivi attendibili in PBIRS

- **Power BI Desktop (ottimizzato per il server di report di Power BI)**
    - *Versione: 2.69.5467.1801 (maggio 2019), data di rilascio: 21 maggio 2019*
        - Correzioni di bug
            - Correzione per evitare la reintroduzione delle credenziali durante il caricamento di file PBIX in PBIRS
            - Correzioni per l'apertura di documenti con # nel nome file
            - Aggiunta del collegamento per tornare indietro nella navigazione in modo più semplice nella finestra di selezione PBIRS
            - Correzione della modalità a contrasto elevato in PBIRS in modo da visualizzare il pulsante Indietro, visualizzazione di messaggi di avviso relativi agli oggetti visivi.
            - Correzioni dell'interfaccia utente nel riquadro di selezione, scalabilità del canvas.

    - *Versione: 2.69.5467.5201 (maggio 2019), data di rilascio: 30 luglio 2019*
        - Correzioni di bug
            - Correzione per la registrazione dei dati di telemetria non corretta

## <a name="january-2019"></a>Gennaio 2019

- **Server di report di Power BI**          
    - *Versione 1.4.7024.16477 (build 15.0.1102.299), data di rilascio: 28 marzo 2019*
        - Correzioni di bug
            - Report di Power BI
                - Risolto il problema con le credenziali di base quando si usa DirectQuery per SAP Hana e SAP BW
                - Risolto l'errore restituito dal feed OData "Non è stato possibile caricare il file o l'assembly Microsoft.OData.Core.NetFX35.V7"

- **Server di report di Power BI**            
    - *Versione 1.4.6969.7395 (build 15.0.1102.235), data di rilascio: 30 gennaio 2019*
        - Correzioni di bug
            - Report di Power BI
                - Risolto il problema con le credenziali di base quando si usa DirectQuery
                - Correzione per le relazioni bidirezionali con i filtri di sicurezza a livello di riga applicati
                - Correzione per i dati non aggiornati dopo un aggiornamento del modello in un ambiente scale-out
                - Correzione per la doppia barra di scorrimento per la tabella o la matrice in Firefox 63 +
                - Correzione delle dimensioni dell'icona + /-in Internet Explorer
            - Report impaginati
                - Correzione del problema di aggiornamento dell'utilizzo di un'origine dati condivisa per un report

    - *Versione 1.4.6960.38798 (build 15.0.1102.222), data di rilascio: 22 gennaio 2019*
        - Funzionalità
            - Report di Power BI 
                - Supporto della sicurezza a livello di riga
                - Espandere e comprimere le intestazioni di riga di matrice
                - Copia e incolla tra file con estensione pbix
                - Guide intelligenti per l'allineamento
                - Supporto per le funzionalità di SAP BW Connector 2.0
            - Administrators
                - Possibilità di limitare le estensioni delle risorse caricabili nel server di report
                - Possibilità di limitare gli schemi di collegamento ipertestuale supportati
            - Programmazione
                - Nuova API Web: /PowerBIReports({Id})/DataModelRoles (GET)
                - Nuova API Web: /PowerBIReports({Id})/DataModelRoleAssignments (GET & PUT)
                - Vedere [Power BI Report Server REST API](https://app.swaggerhub.com/apis/microsoft-rs/PBIRS/2.0) (API REST di Server di report di Power BI) per altri dettagli
        - Correzioni di bug
            - Vulnerabilità HTML Injection
            - L'esportazione in formato PDF non visualizza il simbolo dell'euro
            - Il salvataggio di una password con più origini dati nei report di Power BI rende non valide le password non modificate
            - Problemi di visualizzazione degli oggetti visivi nell'app Power BI per dispositivi mobili dopo l'inattività

- **Power BI Desktop (ottimizzato per il server di report di Power BI)**
    - *Versione: 2.65.5313.1562 (gennaio 2019), data di rilascio: 30 gennaio 2019*
        - Il collegamento e le icone aggiunte rimangono dopo la disinstallazione di Server di report di Power BI
        - Correzione per l'aggiunta di Server di report di Power BI al menu Start con testo nero su un'icona nera

    - *Versione: 2.65.5313.1421 (gennaio 2019), data di rilascio: 22 gennaio 2019* (nuova build e nuova versione)
        - Include modifiche necessarie per la connessione a Server di report di Power BI (gennaio 2019) 
    - *Versione: 2.65.5313.5141 (gennaio 2019), data di rilascio: 31 luglio 2019* (nuova build e nuova versione)
        - Correzioni di bug
            - Correzione per la registrazione dei dati di telemetria non corretta

## <a name="august-2018"></a>Agosto 2018

- **Server di report di Power BI**
    - *Versione 1.3.6816.37243 (build 15.0.2.557), data di rilascio: 30 agosto 2018*
        - Correzioni di bug
            - Risolto un problema a causa del quale un reindirizzamento dell'associazione non veniva aggiornato durante l'aggiornamento dalle versioni precedenti di Server di report di Power BI e i clienti vedevano:      
            *`
            Failed to load expression host assembly. Details: Could not load file or assembly 'Microsoft.ReportingServices.ProcessingObjectModel, Version=2018.7.0.0, Culture=neutral, PublicKeyToken=89845dcd8080cc91' or one of its dependencies. The located assembly's manifest definition does not match the assembly reference. (Exception from HRESULT: 0x80131040) (rsErrorLoadingExprHostAssembly)
             `*
             
            - Il bug relativo alla trasparenza dell'etichetta dati è stato corretto.
            
    - *Versione 1.3.6801.38816 (build 15.0.2.540), data di rilascio: 15 agosto 2018*
        - Funzionalità
            - È ora disponibile il supporto di DirectQuery SSO SAP HANA per i report di Power BI
            - API per oggetti visivi personalizzati fornita con questa versione - Versione 1.13.0
            - Per gli oggetti visivi di Power BI verrà eseguito il fallback a una versione precedente compatibile con la versione corrente dell'API server (se disponibile)

- **Power BI Desktop (ottimizzato per il server di report di Power BI)**
    - *Versione: 2.61.5192.641 (agosto 2018), data di rilascio: 15 agosto 2018*
        - Include modifiche necessarie per la connessione a Server di report di Power BI (agosto 2018)         
    - *Versione: 2.61.5192.7701 (agosto 2018), data di rilascio: 8 agosto 2019* (nuova build e nuova versione)
        - Correzioni di bug
            - Correzione per la registrazione dei dati di telemetria non corretta
            
## <a name="march-2018"></a>Marzo 2018

- **Server di report di Power BI**
    - *Versione 1.2.6690.34729 (build 15.0.2.402), data di rilascio: 27 aprile 2018*
        - Correzioni di bug
            - Abilitazione della migrazione dei cataloghi di SQL Server Reporting Services 2017
            - Per i report di Power BI (PBIX)
                - Possibilità di aggiornare i report quando un server è configurato per l'uso dell'autenticazione personalizzata
                - La modifica delle proprietà di un report non comporta la reimpostazione delle credenziali dell'origine dati
            - Per i report impaginati (RDL)
                - L'uso di `Lookup()` o di funzioni derivate come `LookupSet()` e `MultiLookup()` nelle espressioni RDL non genera più un risultato `#Error`
                - I report collegati rispettano le dimensioni di pagina del report di destinazione durante la stampa
                - Possibilità di creare sottoscrizioni per i report collegati che usano parametri a cascata
                - Possibilità di modificare i valori predefiniti dei parametri multivalore quando si usa Internet Explorer 11
                - Possibilità di modificare le opzioni di recapito delle sottoscrizioni guidate dai dati
                - Possibilità di visualizzare e modificare le sottoscrizioni durante l'esecuzione della sottoscrizione
                - L'impostazione delle credenziali dell'origine dati non comporta la rimozione delle stringhe di connessione basate su espressioni
            - Per gli indicatori KPI
                - Le linee di tendenza vengono aggiornate quando vengono aggiornati i dati
            - Miglioramenti generali alla stabilità​​

    - *Versione 1.2.6660.39920 (build 15.0.2.389), data di rilascio: 28 marzo 2018*
        - Correzioni di bug
            - Per i report di Power BI (PBIX), correzione per l'esportazione dei dati non funzionanti da oggetti visivi di Power BI
            - Per i report di Power BI (PBIX), correzione per i filtri URL non funzionanti
            - Per i report impaginati (RDL), correzione per la visualizzazione non corretta delle immagini in Internet Explorer 11 dopo l'aggiornamento alla versione di marzo del Server di report di Power BI

    - *Versione 1.2.6648.38132 (build 15.0.2.378), data di rilascio: 19 marzo 2018*
        - Aggiornamenti per la sicurezza
        - Miglioramenti all'accessibilità
        - Correzioni di bug
            - Per i report impaginati (RDL), correzione della visibilità di parametri in un report collegato che viene ripristinato dopo la modifica delle proprietà
            - Correzione del portale web con l'autenticazione personalizzata basata su form che ignora il cookie di scadenza scorrevole
            - Correzione dell'esportazione in Word che consente di creare altezze di righe diverse se il contenuto delle righe è vuoto
            - Per i report impaginati (RDL), correzione della stringa di connessione basata sull'espressione che viene eliminata quando vengono modificate le credenziali della sorgente dati
            - Correzione della capacità di usare l'indicatore KPI con valori di testo
            - Per i report impaginati (RDL), correzione della capacità di assegnare un nuovo set di dati a un report impaginato (RDL) esistente
            - Altre correzioni di stabilità e usabilità

- **Power BI Desktop (ottimizzato per il server di report di Power BI)**
    - Versione: 2.56.5023.1043 (marzo 2018), data di rilascio: 19 marzo 2018
        - Include modifiche necessarie per la connessione al server di report di Power BI (marzo 2018)

## <a name="october-2017"></a>Ottobre 2017

- **Server di report di Power BI**
    - *Versione 1.1.6582.41691 (build 14.0.600.442), data di rilascio: 10 gennaio 2018*
        - Aggiornamenti per la sicurezza
        - Correzioni di bug
            - Correzione di Model.GetParameters che restituisce l'errore 400
            - Correzione dell'impostazione del set di dati condiviso sui report impaginati esistenti (RDL)
            - Correzione di ExecutionNotFoundException durante l'esportazione in formato PDF di report con valori di parametri diversi

    - *Versione 1.1.6551.5155 (build 14.0.600.438), data di rilascio: 11 dicembre 2017*
        - Correzioni di bug
            - Errore durante il salvataggio dei dati dopo l'aggiornamento per determinati report di Power BI Desktop.

    - *Versione 1.1.6530.30789 (build 14.0.600.437), data di rilascio: 17 novembre 2017*
        - Correzioni di bug
            - Correzione per gli scenari di autenticazione di base 
            - Correzione per i giorni della settimana che non erano selezionabili nella pagina della pianificazione per le sottoscrizioni, i piani di aggiornamento della cache e gli snapshot della cronologia nel portale
            - Per i report impaginati (RDL), è stata apportata una correzione per le espressioni nella casella di testo con la proprietà CanGrow impostata su false che comportavano la mancata visualizzazione dei colori e la visualizzazione non corretta dei tipi di carattere
            - Per i report di Power BI (PBIX) è stata apportata una correzione per l'aggiunta delle legende ai grafici a linee che mostrano un oggetto visivo vuoto

    - *Versione 1.1.6514.9163 (build 14.0.600.434), data di rilascio: 1 novembre 2017*
        - Correzioni di bug
            - Soluzione per i problemi di affidabilità per i report PBIX di dimensioni superiori a 500 MB
            - Soluzione per i problemi di caricamento dati per i report PBIX di dimensioni superiori a 1 GB

    - *Versione 1.1.6513.3500 (build 14.0.600.433), data di rilascio: 31 ottobre 2017*
        - Funzionalità
            - Supporto per il modello di dati incorporato
            - Visualizzazione della cartella di lavoro di Excel (con integrazione di Office Online Server abilitata)
            - Aggiornamento pianificato dei dati (PBIX)
            - Supporto per DirectQuery
            - Supporto per file di grandi dimensioni (fino a 2 GB)
            - API REST pubblica
            - Supporto per set di dati condivisi in Power BI Desktop (tramite OData)
            - Supporto del parametro URL per i file PBIX
            - Miglioramenti all'accessibilità

- **Power BI Desktop (ottimizzato per il server di report di Power BI)**
    - *Versione: 2.51.4885.3981 (ottobre 2017), data di rilascio: 10 aprile 2018*
        - Aggiornamenti per la sicurezza

    - *Versione: 2.51.4885.2501 (ottobre 2017), data di rilascio: 10 gennaio 2018*
        - Aggiornamenti per la sicurezza

    - *Versione: 2.51.4885.1423 (ottobre 2017), data di rilascio: 17 novembre 2017*
        - Correzioni di bug
            - Correzione alla versione di Power BI Desktop a 32 bit che non può essere eseguita nei sistemi operativi x86
            - Per i report di Power BI (PBIX) è stata apportata una correzione per mostrare le linee della griglia dell'asse x
            - Altre correzioni di bug minori

    - *Versione: 2.51.4885.1041 (ottobre 2017), data di rilascio: 31 ottobre 2017*
        - Funzionalità
            - Include modifiche necessarie per la connessione al server di report di Power BI (ottobre 2017)

## <a name="june-2017"></a>giugno 2017

- **Server di report di Power BI**
    - *Build 14.0.600.309, data di rilascio: 10 gennaio 2018*
        - Aggiornamenti per la sicurezza

    - *Build 14.0.600.305, data di rilascio: 19 settembre 2017*  
        - Correzioni di bug
            - Aggiornamento al [controllo Web di Bing Maps](https://msdn.microsoft.com/library/mt712542.aspx) più recente

    - *Build 14.0.600.301, data di rilascio: 11 luglio 2017*
        - Correzioni di bug
            - Il tag `{{UserId}}` si risolve nelle credenziali archiviate anziché nell'utente che esegue il report in Report di Power BI
            - Non è possibile eseguire il rendering di alcune immagini nei report del server di report di Power BI
            - Non è possibile modificare il nome di un report di Power BI nel server di report di Power BI
            - Non è possibile caricare gli oggetti visivi di Power BI nell'applicazione Power BI per dispositivi mobili (è necessario reinstallare l'app per dispositivi mobili per cancellare la cache locale)

    - *Build 14.0.600.271, data di rilascio: 12 giugno 2017*
        - Versione iniziale del server di report di Power BI

- **Power BI Desktop (ottimizzato per il server di report di Power BI)**
    - *Versione: 2.47.4766.4901 (giugno 2017), data di rilascio: 10 gennaio 2018*
        - Aggiornamenti per la sicurezza

## <a name="next-steps"></a>Passaggi successivi

[Che cos'è Server di report di Power BI?](get-started.md)
[Panoramica amministratore](admin-handbook-overview.md)  
[Installare il server di report di Power BI](install-report-server.md)  
[Scaricare Generatore report](https://www.microsoft.com/download/details.aspx?id=53613)  
[Scaricare la versione più recente di SQL Server Data Tools](https://go.microsoft.com/fwlink/?LinkID=616714)

Altre domande? [Provare a rivolgersi alla community di Power BI](https://community.powerbi.com/)
