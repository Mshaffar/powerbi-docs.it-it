---
title: Integrazione di Azure Machine Learning in Power BI
description: Informazioni su come usare Machine Learning con Power BI
author: davidiseminger
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 05/31/2019
ms.author: davidi
LocalizationGroup: conceptual
ms.openlocfilehash: 1004549c37f4bff92e4a8b1d31b3844b7cdd0f2d
ms.sourcegitcommit: 0e9e211082eca7fd939803e0cd9c6b114af2f90a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/13/2020
ms.locfileid: "83330406"
---
# <a name="azure-machine-learning-integration-in-power-bi"></a>Integrazione di Azure Machine Learning in Power BI

Numerose organizzazioni usano modelli di **Machine Learning** per ottenere informazioni dettagliate e stime migliori sulle proprie attività aziendali. La possibilità di visualizzare e richiamare informazioni dettagliate da questi modelli in report, dashboard e altri strumenti di analisi facilita la distribuzione di queste informazioni agli utenti aziendali che ne hanno maggiormente bisogno.  Ora con Power BI è facile incorporare le informazioni dettagliate dei modelli ospitati in Azure Machine Learning, usando semplici movimenti di puntamento e clic.

Per usare questa funzionalità, un data scientist può semplicemente concedere all'analista di Power BI l'accesso al modello di Azure Machine Learning usando il portale di Azure.  Quindi, all'inizio di ogni sessione, Power Query individua tutti i modelli di Azure Machine Learning a cui l'utente ha accesso e li espone come funzioni dinamiche di Power Query.  L'utente può quindi richiamare queste funzioni accedendovi dalla barra multifunzione dell'editor di Power Query o richiamando direttamente la funzione M. Power BI inoltre invia in batch automaticamente le richieste di accesso quando richiama il modello di Azure Machine Learning per un set di righe, al fine di ottenere prestazioni migliori.

Questa funzionalità è attualmente supportata solo per i flussi di dati di Power BI e per Power Query online nel servizio Power BI.

Per altre informazioni sui flussi di dati, vedere [Preparazione dei dati self-service in Power BI](service-dataflows-overview.md).

Per altre informazioni su Azure Machine Learning, vedere:

- Panoramica:  [Cos'è Azure Machine Learning?](https://docs.microsoft.com/azure/machine-learning/service/overview-what-is-azure-ml)
- Guide di avvio rapido ed esercitazioni per Azure Machine Learning:  [Documentazione di Azure Machine Learning](https://docs.microsoft.com/azure/machine-learning/)

## <a name="granting-access-to-the-azure-ml-model-to-a-power-bi-user"></a>Concedere a un utente di Power BI l'accesso al modello di Azure Machine Learning

Per accedere a un modello di Azure Machine Learning da Power BI, l'utente deve avere accesso in **lettura** alla sottoscrizione di Azure.  Inoltre:

- Per i modelli di Machine Learning Studio (versione classica), accesso in **lettura** al servizio Web Machine Learning Studio (versione classica)
- Per i modelli di Machine Learning, accesso in **lettura** all'area di lavoro di Machine Learning

La procedura in questo articolo spiega come concedere a un utente di Power BI l'accesso a un modello ospitato nel servizio Azure Machine Learning, in modo che possa accedere a questo modello come una funzione di Power Query.  Per altre informazioni, vedere [Gestire l'accesso alle risorse di Azure usando il controllo degli accessi in base al ruolo e il portale di Azure](https://docs.microsoft.com/azure/role-based-access-control/role-assignments-portal).

1. Accedere al [portale di Azure](https://portal.azure.com).

2. Passare alla pagina **Sottoscrizioni**. La pagina **Sottoscrizioni** è disponibile nell'elenco **Tutti i servizi** nel menu del riquadro di spostamento del portale di Azure.

    ![Pagina Sottoscrizioni di Azure](media/service-machine-learning-integration/machine-learning-integration_01.png)

3. Selezionare la propria sottoscrizione.

    ![Selezionare la propria sottoscrizione](media/service-machine-learning-integration/machine-learning-integration_02.png)

4. Selezionare **Controllo di accesso (IAM)** e quindi il pulsante **Aggiungi**.

    ![Controllo di accesso (IAM)](media/service-machine-learning-integration/machine-learning-integration_03.png)

5. Selezionare **Lettore** come ruolo. Selezionare l'utente di Power BI a cui si vuole concedere l'accesso al modello di Azure Machine Learning.

    ![Selezionare Lettore come ruolo](media/service-machine-learning-integration/machine-learning-integration_04.png)

6. Selezionare **Salva**.

7. Ripetere i passaggi da 3 a 6 per assegnare all'utente il ruolo **Lettore** per l'accesso allo specifico servizio Web di Machine Learning Studio (versione classica) *o* all'area di lavoro di Machine Learning che ospita il modello.


## <a name="schema-discovery-for-machine-learning-models"></a>Individuazione dello schema per i modelli di Machine Learning

I data scientist usano principalmente Python per sviluppare, e persino per distribuire, i modelli di Machine Learning per Machine Learning.  A differenza di Machine Learning Studio (versione classica), che consente di automatizzare l'attività di creazione di un file di schema per il modello, nel caso di Machine Learning il data scientist deve generare esplicitamente il file di schema mediante Python.

Questo file di schema deve essere incluso nel servizio Web distribuito per i modelli di Machine Learning. Per generare automaticamente lo schema per il servizio Web, è necessario fornire un esempio di input/output nello script di ingresso per il modello distribuito. Vedere la sottosezione sulla [generazione automatica (facoltativa) degli schemi Swagger nei modelli di distribuzione con Azure Machine Learning](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-and-where#optional-define-model-web-service-schema) nella documentazione del servizio. Il collegamento include lo script di ingresso di esempio con le istruzioni per la generazione dello schema. 

In particolare, le funzioni *\@input_schema* e *\@output_schema* nello script di ingresso fanno riferimento ai formati degli esempi di input e output nelle variabili *input_sample* e *output_sample* e usano questi esempi per generare una specifica OpenAPI (Swagger) per il servizio Web durante la distribuzione.

Le istruzioni per la generazione dello schema tramite l'aggiornamento dello script di ingresso devono essere applicate anche ai modelli creati con gli esperimenti di Machine Learning automatizzati e utilizzando l'SDK di Azure Machine Learning.

> [!NOTE]
> I modelli creati usando l'interfaccia visiva di Azure Machine Learning attualmente non supportano la generazione dello schema, ma la supporteranno nelle versioni successive. 

## <a name="invoking-the-azure-ml-model-in-power-bi"></a>Richiamare il modello di Azure Machine Learning in Power BI

È possibile richiamare un modello di Azure Machine Learning al quale si ha accesso direttamente dall'editor di Power Query nel flusso di dati. Per accedere ai modelli di Azure Machine Learning, selezionare il pulsante **Modifica** relativo all'entità che si vuole arricchire con le informazioni dettagliate del modello di Azure Machine Learning, come illustrato nell'immagine seguente.

![Servizio Power BI - modifica dell'entità](media/service-machine-learning-integration/machine-learning-integration_05.png)

Selezionando il pulsante **Modifica** viene aperto l'editor di Power Query per le entità del flusso di dati.

![Editor di Power Query](media/service-machine-learning-integration/machine-learning-integration_06.png)

Selezionare il pulsante **Informazioni dettagliate sull'intelligenza artificiale** sulla barra multifunzione e quindi selezionare la cartella _Azure Machine Learning Models_ (Modelli di Azure Machine Learning) nel menu del riquadro di spostamento. Tutti i modelli di Azure Machine Learning a cui si ha accesso sono elencati qui come funzioni di Power Query. Inoltre, i parametri di input del modello di Azure Machine Learning vengono automaticamente mappati ai parametri della funzione di Power Query corrispondente.

Per richiamare un modello di Azure Machine Learning è possibile specificare una qualsiasi delle colonne dell'entità selezionata come input dall'elenco a discesa. Si può anche specificare un valore di costante da usare come input attivando l'icona della colonna a sinistra della finestra di dialogo di input.

![Selezionare la colonna](media/service-machine-learning-integration/machine-learning-integration_07.png)

Selezionare **Richiama** per visualizzare l'anteprima dell'output del modello di Azure Machine Learning come nuova colonna nella tabella delle entità. Il richiamo del modello verrà visualizzato anche come passaggio applicato per la query.

![Selezionare Richiama](media/service-machine-learning-integration/machine-learning-integration_08.png)

Se il modello restituisce più parametri di output, questi vengono raggruppati in un unico record nella colonna di output. È possibile espandere la colonna per produrre singoli parametri di output in colonne separate.

![Espandere la colonna](media/service-machine-learning-integration/machine-learning-integration_09.png)

Dopo il salvataggio del flusso di dati, il modello viene richiamato automaticamente ogni volta che il flusso di dati viene aggiornato con le righe nuove o modificate nella tabella delle entità.

## <a name="next-steps"></a>Passaggi successivi

Questo articolo ha fornito una panoramica sull'integrazione di Machine Learning nel servizio Power BI. Potrebbero essere interessanti e utili anche gli articoli seguenti. 

* [Esercitazione: Richiamare un modello di Machine Learning Studio (versione classica) in Power BI](../connect-data/service-tutorial-invoke-machine-learning-model.md)
* [Esercitazione: Uso di Servizi cognitivi in Power BI](../connect-data/service-tutorial-use-cognitive-services.md)
* [Servizi cognitivi in Power BI](service-cognitive-services.md)

Per altre informazioni sui flussi di dati, è possibile leggere questi articoli:
* [Creare e usare flussi di dati in Power BI](service-dataflows-create-use.md)
* [Uso delle entità calcolate in Power BI Premium](service-dataflows-computed-entities-premium.md)
* [Uso di flussi di dati con origini dati locali](service-dataflows-on-premises-gateways.md)
* [Risorse per sviluppatori per i flussi di dati Power BI](service-dataflows-developer-resources.md)
* [Integrazione di flussi di dati e Azure Data Lake (anteprima)](service-dataflows-azure-data-lake-integration.md)
