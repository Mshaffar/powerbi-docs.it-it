---
title: Che cosa sono le app modello di Power BI? (anteprima)
description: Questo articolo è una panoramica del programma delle app modello di Power BI. Informazioni su come compilare app di Power BI con un uso minimo o nullo di codice e su come distribuire le app a qualsiasi cliente Power BI.
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 02/04/2019
ms.author: maggies
ms.openlocfilehash: 445f5f087bd9589b18f798e8db40a63b0ddceafe
ms.sourcegitcommit: 8207c9269363f0945d8d0332b81f1e78dc2414b0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2019
ms.locfileid: "56249993"
---
# <a name="what-are-power-bi-template-apps-preview"></a>Che cosa sono le app modello di Power BI? (anteprima)

Le nuove *app modello* di Power BI consentono ai partner Power BI di creare app Power BI con un uso minimo o nullo di codice e quindi di distribuire le app a qualsiasi cliente Power BI.  Questo articolo è una panoramica del programma delle app modello di Power BI.

Le app modello sostituiscono gli attuali pacchetti di contenuto dei servizi. I partner Power BI sono in grado di creare set di contenuti predefiniti per i clienti e di pubblicarli personalmente.  

È possibile compilare app modello che consentono ai clienti di connettersi e creare un'istanza con i propri account. In qualità di esperti di dominio, possono sbloccare i dati in modo da renderli facilmente utilizzabili dai loro utenti aziendali.  

Le app modello compilate dai partner vengono inviate al portale Cloud Partner e diventano quindi disponibili pubblicamente nella raccolta di app di Power BI (app.powerbi.com/getdata/services) e in Microsoft AppSource (appsource.microsoft.com). Ecco un esempio di esperienza di app modello pubblica.  

## <a name="overview"></a>Panoramica
Il processo generale per sviluppare e inviare un'app modello comprende diverse fasi, alcune delle quali possono prevedere più attività allo stesso tempo.


| Fase | Power BI Desktop |  |Servizio Power BI  |  |Portale Cloud Partner  |
|---|--------|--|---------|---------|---------|
| **1** | Compilare un modello di dati e un report in un file con estensione pbix |  | Creare un'area di lavoro. Importare un file con estensione pbix. Creare un dashboard complementare  |  | Registrarsi come partner |
| **2** |  |  | Creare un pacchetto di test ed eseguire la convalida interna        |  | |
| **3** | |  | Alzare al livello di pre-produzione il pacchetto di test per la convalida al di fuori del tenant di Power BI e inviarlo ad AppSource  |  | Con il pacchetto di pre-produzione, creare un'offerta di app modello di Power BI e avviare il processo di convalida |
| **4** | |  | Alzare al livello di produzione il pacchetto di pre-produzione |  | Procedere alla pubblicazione |

## <a name="requirements"></a>Requisiti

Per creare l'app modello, sono necessarie autorizzazioni specifiche. Per informazioni dettagliate, vedere Impostazioni app modello nel portale di amministrazione di Power BI. 

Per pubblicare un'app modello nel servizio Power BI e in AppSource, è necessario soddisfare i requisiti per [diventare un editore del Marketplace cloud](https://docs.microsoft.com/azure/marketplace/become-publisher).
 
## <a name="high-level-steps"></a>Passaggi di alto livello

Ecco i passaggi di alto livello. 

1. [Rivedere i requisiti](#requirements) per assicurarsi di soddisfarli. 

1. Creare un report in Power BI Desktop. Usare parametri, in modo che sia possibile salvare il report come file utilizzabile anche da altri utenti. 

1. Creare un'area di lavoro per l'app modello nel proprio tenant nel servizio Power BI (app.powerbi.com). 

1. Importare il file con estensione pbix e aggiungere contenuto, ad esempio un dashboard nell'app. 

1. Creare un pacchetto di test per testare l'app modello all'interno dell'organizzazione. 

1. Alzare l'app di test al livello di pre-produzione per inviarla alla convalida in AppSource e testarla al di fuori del proprio tenant. 

1. Inviare il contenuto alla piattaforma Cloud Partner per la pubblicazione. 

1. Pubblicare l'offerta in AppSource e passare l'app in produzione in Power BI.
2. È ora possibile iniziare a sviluppare la versione successiva nella stessa area di lavoro, in fase di pre-produzione. 

## <a name="requirements"></a>Requisiti

Per creare l'app modello, sono necessarie autorizzazioni specifiche. Per informazioni dettagliate, vedere [Impostazioni app modello nel portale di amministrazione](service-admin-portal.md#template-apps-settings-preview) di Power BI. 

Per pubblicare un'app modello nel servizio Power BI e in AppSource, è necessario soddisfare i requisiti per [diventare un editore del Marketplace cloud](https://docs.microsoft.com/azure/marketplace/become-publisher).

## <a name="tips"></a>Suggerimenti 

- Assicurarsi che l'app includa dati di esempio per consentire a tutti gli utenti di iniziare nel più breve tempo possibile. 
- Esaminare attentamente l'applicazione installandola nel proprio tenant e in un tenant secondario. Assicurarsi che i clienti possano visualizzare solo ciò che si vuole che visualizzino. 
- Usare AppSource come store online per ospitare l'applicazione. In questo modo può essere individuata da tutti gli utenti che usano Power BI. 
- Valutare la possibilità di offrire più app modello per scenari univoci separati. 
- Abilitare la personalizzazione dei dati, ad esempio supportare la personalizzazione delle connessioni e la configurazione dei parametri tramite il programma di installazione.

Per altri suggerimenti, vedere [Suggerimenti per la creazione di app modello in Power BI (anteprima)](service-template-apps-tips.md).

## <a name="support"></a>Supporto
Per il supporto durante lo sviluppo, usare [https://powerbi.microsoft.com/support](https://powerbi.microsoft.com/support). Questo sito viene monitorato e gestito attivamente. Le richieste dei clienti vengono indirizzate rapidamente al team appropriato.

## <a name="next-steps"></a>Passaggi successivi

[Creare un'app modello](service-template-apps-create.md)