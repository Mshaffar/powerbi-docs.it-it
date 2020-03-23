---
title: Incorporare report o dashboard dalle app
description: Informazioni su come integrare o incorporare un report o un dashboard da un'app Power BI e non da un'area di lavoro.
author: KesemSharabi
ms.author: kesharab
ms.topic: how-to
ms.service: powerbi
ms.subservice: powerbi-developer
ms.custom: mvc
ms.date: 11/27/2018
ms.openlocfilehash: 34c5e825a589fc3f9ba9ecd7e9fe1d6b137e1cfd
ms.sourcegitcommit: a175faed9378a7d040a08ced3e46e54503334c07
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/18/2020
ms.locfileid: "79494631"
---
# <a name="embed-reports-or-dashboards-from-apps"></a>Incorporare report o dashboard dalle app

In Power BI, è possibile creare app per riunire dashboard e report correlati, tutti in un'unica posizione. Quindi vengono pubblicate in ampi gruppi di persone all'interno dell'organizzazione. L'utilizzo di tali app è pertinente quando tutti gli utenti sono utenti di Power BI. Pertanto, è possibile condividere contenuto con loro usando le app di Power BI. In questo articolo sono riportati alcuni rapidi passaggi per incorporare contenuti in un'applicazione di terze parti da un'app di Power BI pubblicata.

## <a name="grab-a-report-embedurl-for-embedding"></a>Catturare un URL di incorporamento di report per l'incorporamento

1. Creare un'istanza di applicazione in un'area di lavoro utente, **Area di lavoro personale**. Condividere per il proprio utilizzo o guidare un altro utente a passare attraverso questo flusso.

2. Aprire il report desiderato nel servizio Power BI.

3. Passare a **File** > **Incorpora In SharePoint Online** e individuare l'URL di incorporamento di report. Un esempio di URL di incorporamento è illustrato nello screenshot seguente. In alternativa, chiamare l'API REST GetReports/GetReport ed estrarre il campo dell'URL di incorporamento di report corrispondente dalla risposta. La chiamata REST non deve avere un identificatore di area di lavoro come componente dell'URL perché è stata creata un'istanza dell'app nell'area di lavoro dell'utente.

    ![Incorporare contenuti dalle app](media/embed-from-apps/embed-from-app.png)

4. Usare l'URL di incorporamento recuperato nel passaggio 3 con JavaScript SDK.

## <a name="grab-a-dashboard-embedurl-for-embedding"></a>Catturare un URL di incorporamento di dashboard per l'incorporamento

1. Creare un'istanza di applicazione in un'area di lavoro utente, **Area di lavoro personale**. Condividere per il proprio utilizzo o guidare un altro utente a passare attraverso questo flusso.

2. Chiamare l'API REST GetDashboards ed estrarre il campo URL di incorporamento di dashboard corrispondente dalla risposta. La chiamata REST non deve avere un identificatore di area di lavoro come componente dell'URL perché è stata creata un'istanza dell'app nell'area di lavoro dell'utente.

3. Usare l'URL di incorporamento recuperato nel passaggio 2 con JavaScript SDK.

## <a name="next-steps"></a>Passaggi successivi

Vedere le procedure di incorporamento dalle aree di lavoro per i clienti di terze parti e l'organizzazione:

> [!div class="nextstepaction"]
>[Incorporare contenuto per i clienti di terze parti](embed-sample-for-customers.md)

> [!div class="nextstepaction"]
>[Incorporare contenuto per l'organizzazione](embed-sample-for-your-organization.md)