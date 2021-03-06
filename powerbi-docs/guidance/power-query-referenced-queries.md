---
title: Fare riferimento a query di Power Query
description: Indicazioni su come fare riferimento alle query di Power Query.
author: peter-myers
ms.reviewer: asaxton
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: conceptual
ms.date: 11/30/2019
ms.author: v-pemyer
ms.openlocfilehash: 242f1e44e3314af900d9f4d4e4fb7380b28b4103
ms.sourcegitcommit: 0e9e211082eca7fd939803e0cd9c6b114af2f90a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/13/2020
ms.locfileid: "83278676"
---
# <a name="referencing-power-query-queries"></a>Fare riferimento a query di Power Query

Questo articolo è destinato agli autori di modelli di dati che usano Power BI Desktop. Contiene istruzioni relative alla definizione delle query di Power Query che fanno riferimento ad altre query.

Ecco cosa significa: _Quando una query fa riferimento a una seconda query, è come se i passaggi della seconda query fossero combinati con i, ed eseguiti prima dei, passaggi della prima query._

Si supponga di usare diverse query: **Query1** recupera i dati da un servizio Web e il relativo caricamento è disabilitato. **Query2**, **Query3** e **Query4** fanno tutte riferimento a **Query1** e i relativi output vengono caricati nel modello di dati.

![Vista Dipendenze query con le query descritte nel paragrafo precedente.](media/power-query-referenced-queries/query-dependencies-web-service.png)

Quando il modello di dati viene aggiornato, spesso si presuppone che Power Query recuperi il risultato di **Query1** e che tale risultato venga usato dalle query di riferimento. Questa supposizione non è corretta. Di fatto, Power Query esegue **Query2**, **Query3** e **Query4** separatamente.

Si può pensare che in **Query2** siano incorporati i passaggi di **Query1**. Ciò vale anche per **Query3** e **Query4**. Il diagramma seguente presenta un'immagine più chiara del modo in cui vengono eseguite le query.

![Una versione modificata della vista Dipendenze query, che visualizza Query2, Query3 e Query4. In ognuna delle tre query è incorporata Query1.](media/power-query-referenced-queries/query-dependencies-web-service-concept.png)

**Query1** viene eseguita tre volte. Più esecuzioni possono rallentare l'aggiornamento dei dati e influire negativamente sull'origine dati.

L'uso della funzione [Table.Buffer](/powerquery-m/table-buffer) in **Query1** non eliminerà il recupero dei dati aggiuntivi. Questa funzione memorizza nel buffer una tabella e la tabella memorizzata nel buffer può essere usata solo all'interno della stessa esecuzione della query. Quindi, nell'esempio, se **Query1** viene memorizzata nel buffer quando viene eseguita **Query2**, i dati memorizzati nel buffer non possono essere usato quando vengono eseguite **Query3** e **Query4**. I dati verranno memorizzati nel buffer due volte di più. Questo risultato può di fatto comportare prestazioni negative, perché la tabella viene memorizzata nel buffer da ogni query di riferimento.

> [!NOTE]
> L'architettura di memorizzazione nella cache di Power Query è complessa e non è l'argomento principale di questo articolo. Power Query è in grado di memorizzare nella cache i dati recuperati da un'origine dati. Tuttavia, quando esegue una query può recuperare i dati dall'origine dati più di una volta.

## <a name="recommendations"></a>Consigli

In generale, si consiglia di fare riferimento alle query per evitare la duplicazione della logica nelle query. Tuttavia, come descritto in questo articolo, questo approccio di progettazione può contribuire a rallentare gli aggiornamenti dei dati e a sovraccaricare le origini dati.

Si consiglia invece di creare un [flusso di dati](../transform-model/service-dataflows-overview.md). L'uso di un flusso di dati può migliorare i tempi di aggiornamento e ridurre l'impatto sulle origini dati.

È possibile progettare il flusso di dati per incapsulare i dati di origine e le trasformazioni. Poiché il flusso di dati è un archivio permanente dei dati nel servizio Power BI, il recupero dei dati è rapido. Quindi, anche se facendo riferimento alle query vengono generate più richieste per il flusso di dati, è possibile migliorare i tempi di aggiornamento dei dati.

Nell'esempio, se **Query1** viene riprogettata come entità del flusso di dati, **Query2**, **Query3** e **Query4** possono utilizzarla come origine dati. Con questa progettazione, l'entità originata da **Query1** verrà valutata una sola volta.

## <a name="next-steps"></a>Passaggi successivi

Per altre informazioni correlate a questo articolo, vedere le risorse seguenti:

- [Preparazione dei dati self-service in Power BI](../transform-model/service-dataflows-overview.md)
- [Creazione e uso di flussi di dati in Power BI](../transform-model/service-dataflows-create-use.md)
- Domande? [Contattare la community di Power BI](https://community.powerbi.com/)
- Se si hanno suggerimenti, [Contribuire con idee per migliorare Power BI](https://ideas.powerbi.com/)
