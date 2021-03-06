---
title: 'Servizio di terze parti: Connettore di Google Analytics'
description: 'Servizio di terze parti: Connettore di Google Analytics per Power BI Desktop'
author: davidiseminger
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: conceptual
ms.date: 05/08/2019
ms.author: davidi
LocalizationGroup: Connect to data
ms.openlocfilehash: 4b279ebb1ae4ae34f1b9832883ddde5d804a7ace
ms.sourcegitcommit: 0e9e211082eca7fd939803e0cd9c6b114af2f90a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/13/2020
ms.locfileid: "83304048"
---
# <a name="use-the-google-analytics-connector-for-power-bi-desktop"></a>Usare il connettore di Google Analytics per Power BI Desktop
> [!NOTE]
> Il pacchetto di contenuto e il connettore di Google Analytics in Power BI Desktop si basano sull'API Core Reporting di Google Analytics. e di conseguenza le funzionalità e la disponibilità potrebbero variare nel tempo.

È possibile connettersi ai dati di Google Analytics usando il connettore di **Google Analytics**. Per eseguire la connessione, seguire questa procedura:

1. In **Power BI Desktop** selezionare **Recupera dati** nella scheda **Home** della barra multifunzione.
2. Nella finestra **Recupera dati** selezionare **Servizi online** nelle categorie nel riquadro a sinistra.
3. Selezionare **Google Analytics** dalle selezioni nel riquadro a destra.
4. Nella parte inferiore della finestra selezionare **Connetti**.  
   ![](media/service-google-analytics-connector/tps_googleanalytics_1.png)

Viene visualizzata una finestra di dialogo che spiega che il connettore è un servizio di terze parti, avvisa che le funzionalità e la disponibilità possono variare nel tempo e fornisce altri chiarimenti.  
![](media/service-google-analytics-connector/tps_googleanalytics_2.png)

Quando si seleziona **Continua**, viene chiesto di accedere a Google Analytics.  
![](media/service-google-analytics-connector/tps_googleanalytics_3.png)

Dopo avere immesso le credenziali, viene chiesto di fornire l'accesso offline a Power BI. In questo modo **Power BI Desktop** viene usato per accedere ai dati di Google Analytics.  

Dopo avere accettato, **Power BI Desktop** mostra che è stato eseguito l'accesso.  
![](media/service-google-analytics-connector/tps_googleanalytics_5.png)

Selezionare **Connetti**. I dati di Google Analytics vengono connessi a **Power BI Desktop** e caricati.  
![](media/service-google-analytics-connector/tps_googleanalytics_6.png)

## <a name="changes-to-the-api"></a>Modifiche all'API
Anche se abbiamo tentato di rilasciare aggiornamenti in funzione di tutte le modifiche apportate, è possibile che le modifiche all'API incidano sui risultati delle query generate. In alcuni casi, alcune query potrebbero non essere più supportate. A causa di questa dipendenza non è possibile garantire i risultati delle query quando si usa questo connettore.

Maggiori dettagli sulle modifiche all'API di Google Analytics sono disponibili nel relativo [changelog](https://developers.google.com/analytics/devguides/changelog).

