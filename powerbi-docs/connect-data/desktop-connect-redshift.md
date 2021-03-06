---
title: Connettersi a un database Amazon Redshift in Power BI Desktop
description: Connettersi con facilità e usare un database Amazon Redshift in Power BI Desktop
author: davidiseminger
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: conceptual
ms.date: 05/08/2019
ms.author: davidi
LocalizationGroup: Connect to data
ms.openlocfilehash: de172db743573e82700db9cf32c59d13c35aebc2
ms.sourcegitcommit: bfc2baf862aade6873501566f13c744efdd146f3
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/13/2020
ms.locfileid: "83347634"
---
# <a name="connect-to-an-amazon-redshift-database-in-power-bi-desktop"></a>Connettersi a un database Amazon Redshift in Power BI Desktop
In **Power BI Desktop** è possibile connettersi a un database **Amazon Redshift** e usare i dati sottostanti esattamente come qualsiasi altra origine dati in Power BI Desktop.

## <a name="connect-to-an-amazon-redshift-database"></a>Connettersi a un database Amazon Redshift
Per connettersi a un database **Amazon Redshift** selezionare **Recupera dati** nella barra multifunzione **Home** in Power BI Desktop. Quando si seleziona **Database** nelle categorie a sinistra viene visualizzato **Amazon Redshift**.

![](media/desktop-connect-redshift/connect_redshift_3.png)

Nella finestra **Amazon Redshift** che viene visualizzata digitare o incollare il nome del server e del database **Amazon Redshift**. Nel campo *Server* gli utenti possono specificare una porta nel seguente formato: *ServerURL:Port*

![](media/desktop-connect-redshift/connect_redshift_4.png)

Quando richiesto, inserire il nome utente e la password. Per evitare errori, usare il nome del server che corrisponde esattamente al certificato SSL. 

![](media/desktop-connect-redshift/connect_redshift_5.png)

Una volta stabilita la connessione, viene visualizzata una finestra **Strumento di navigazione** che mostra i dati disponibili sul server, in cui è possibile selezionare uno o più elementi da importare e usare in **Power BI Desktop**.

![](media/desktop-connect-redshift/connect_redshift_6.png)

Dopo avere effettuato le selezioni nella finestra **Strumento di navigazione** è possibile scegliere **Carica** per caricare i dati o **Modifica** per modificarli.

* Se si sceglie **Carica** viene chiesto se usare la modalità *Importa* o la modalità *DirectQuery* per caricare i dati. Per altre informazioni, vedere l'[articolo che descrive DirectQuery](desktop-use-directquery.md).
* Se si sceglie **Modifica**, viene visualizzato l'**Editor di Query** in cui è possibile applicare trasformazioni e filtri di vario tipo ai dati, molti dei quali vengono applicati al database **Amazon Redshift** stesso sottostante (se supportato).

## <a name="next-steps"></a>Passaggi successivi
È possibile connettersi a molti tipi di dati usando Power BI Desktop. Per altre informazioni sulle origini dati, vedere le risorse seguenti:

* [Che cos'è Power BI Desktop?](../fundamentals/desktop-what-is-desktop.md)
* [Origini dati in Power BI Desktop](desktop-data-sources.md)
* [Effettuare il data shaping e combinare i dati con Power BI Desktop](desktop-shape-and-combine-data.md)
* [Connettersi a cartelle di lavoro di Excel in Power BI Desktop](desktop-connect-excel.md)   
* [Immettere dati direttamente in Power BI Desktop](desktop-enter-data-directly-into-desktop.md)   
