---
title: Usare oggetti visivi di Power BI basati su R in Power BI
description: Usare oggetti visivi di Power BI basati su R in Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.topic: conceptual
ms.subservice: powerbi-custom-visuals
ms.date: 07/27/2018
LocalizationGroup: Create reports
ms.openlocfilehash: 6f9518ee367ed9dc39e70fcff71a47f47df59c1f
ms.sourcegitcommit: 0e9e211082eca7fd939803e0cd9c6b114af2f90a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/13/2020
ms.locfileid: "83336179"
---
# <a name="use-r-powered-power-bi-visuals-in-power-bi"></a>Usare oggetti visivi di Power BI basati su R in Power BI

In **Power BI Desktop** e nel **servizio Power BI** è possibile usare oggetti visivi di Power BI basati su R senza conoscere R né creare script R. Ciò consente di sfruttare la potenza analitica e degli oggetti visivi di R, nonché gli script R, senza conoscere R o dover programmare manualmente.

Per usare gli oggetti visivi di Power BI basati su R, è prima di tutto necessario selezionare e scaricare l'oggetto visivo personalizzato R dalla raccolta di [**AppSource**](https://appsource.microsoft.com/marketplace/apps?product=power-bi-visuals&page=1) di **oggetti visivi di Power BI** per Power BI.

![Oggetto visivo R 1a](media/desktop-r-powered-custom-visuals/powerbi-r-powered-custom-viz_1a.png)

Le sezioni seguenti descrivono come selezionare, caricare e usare oggetti visivi basati su R in **Power BI Desktop**.

## <a name="use-r-power-bi-visuals"></a>Usare oggetti visivi di Power BI basati su R

Per usare gli oggetti visivi di Power BI basati su R, scaricare ogni oggetto visivo dalla raccolta di **oggetti visivi di Power BI** e quindi usare tale oggetto come qualsiasi altro tipo di oggetto visivo in **Power BI Desktop**. Per ottenere gli oggetti visivi di Power BI, si può procedere in due modi: è possibile scaricarli dal sito **AppSource** online oppure esplorarli e scaricarli da **Power BI Desktop**. 

### <a name="get-power-bi-visuals-from-appsource"></a>Ottenere oggetti visivi di Power BI da AppSource

Di seguito è indicata la procedura per esplorare e selezionare gli oggetti visivi dal sito **AppSource** online:

1. Passare alla raccolta di oggetti visivi di Power BI disponibile all'indirizzo [https://appsource.microsoft.com](https://appsource.microsoft.com/). Selezionare la casella di controllo *Power BI apps* in *Affina in base al prodotto* e quindi fare clic sul collegamento **Visualizza tutti**.

   ![Oggetto visivo R 2a](media/desktop-r-powered-custom-visuals/powerbi-r-powered-custom-viz_2a.png)

2. Nella pagina della raccolta degli [oggetti visivi di Power BI](https://appsource.microsoft.com/marketplace/apps?product=power-bi-visuals&page=1) selezionare **Oggetti visivi di Power BI** nell'elenco Componenti aggiuntivi nel riquadro sinistro.

   ![Oggetto visivo R 2b](media/desktop-r-powered-custom-visuals/powerbi-r-powered-custom-viz_2b.png)

3. Selezionare l'**oggetto visivo** nella raccolta. Si verrà reindirizzati a una pagina che descrive l'oggetto visivo. Fare clic sul pulsante **Scarica adesso** per scaricarlo.

   > [!NOTE]
    > Per la creazione in **Power BI Desktop**, è necessario disporre di R installato sul computer locale. Se gli utenti vogliono visualizzare un oggetto visivo basato su R nel **servizio Power BI**, non è necessario che R sia installato localmente.

   ![Oggetto visivo R 3a](media/desktop-r-powered-custom-visuals/powerbi-r-powered-custom-viz_3a.png)

   Non è necessario installare R per usare oggetti visivi di Power BI basati su R nel **servizio Power BI**. Tuttavia, se si vogliono usare oggetti visivi di Power BI basati su R in **Power BI Desktop** è *necessario* installare R nel computer locale. È possibile scaricare R dai percorsi seguenti:

   * [CRAN](https://cran.r-project.org/)
   * [MRO](https://mran.microsoft.com/)

4. Dopo aver scaricato l'oggetto visivo, in modo analogo al download di un file dal browser, passare a **Power BI Desktop**, fare clic su **Altre opzioni** (...) nel riquadro **Visualizzazioni** e selezionare **Importa da file**.

   ![Oggetto visivo R 4a](media/desktop-r-powered-custom-visuals/powerbi-r-powered-custom-viz_4a.png)
5. Viene visualizzato un avviso in merito all'importazione di un oggetto visivo personalizzato, come illustrato nella figura seguente:

   ![Oggetto visivo R 5](media/desktop-r-powered-custom-visuals/powerbi-r-powered-custom-viz_5.png)
6. Individuare il puntno in cui è stato l'oggetto visivo è stato salvato e selezionare il file. Le visualizzazioni personalizzate di **Power BI Desktop** hanno l'estensione pbiviz.

   ![Oggetto visivo R 6](media/desktop-r-powered-custom-visuals/powerbi-r-powered-custom-viz_6.png)
7. Quando si torna a Power BI Desktop, è possibile visualizzare il nuovo tipo di oggetto visivo nel riquadro **Visualizzazioni**.

   ![Oggetto visivo R 7](media/desktop-r-powered-custom-visuals/powerbi-r-powered-custom-viz_7.png)
8. Quando si importa il nuovo oggetto visivo (o si apre un report che contiene un oggetto visivo basato su R), **Power BI Desktop** installa i pacchetti R necessari.

   ![Oggetto visivo R 8](media/desktop-r-powered-custom-visuals/powerbi-r-powered-custom-viz_8.png)

9. Da qui, è possibile aggiungere all'oggetto visivo dati e altri oggetti visivi di **Power BI Desktop**. Al termine, è possibile visualizzare l'oggetto visivo nell'area di disegno. Nell'elemento visivo seguente, l'oggetto visivo **Forecasting** basato su R è stato usato con le proiezioni sul tasso di nascita delle Nazioni Unite (oggetto visivo a sinistra).

    ![Oggetto visivo R 10](media/desktop-r-powered-custom-visuals/powerbi-r-powered-custom-viz_10.png)

    Come per qualsiasi altro oggetto visivo di **Power BI Desktop**, è possibile pubblicare il report con i relativi oggetti visivi basati su R nel **servizio Power BI** e condividerlo con altri utenti.

    Controllare spesso la raccolta di oggetti visivi, poiché ne vengono aggiunti continuamente di nuovi.

### <a name="get-power-bi-visuals-from-within-power-bi-desktop"></a>Ottenere oggetti visivi di Power BI da **Power BI Desktop**

1. È anche possibile ottenere gli oggetti visivi di Power BI dall'interno di **Power BI Desktop**. In **Power BI Desktop** fare clic con il pulsante destro del mouse sui puntini di sospensione (...) nel riquadro **Visualizzazioni** e scegliere **Importa dal Marketplace**.

   ![Oggetto visivo R 4a](media/desktop-r-powered-custom-visuals/powerbi-r-powered-custom-viz_4a.png)

2. Verrà visualizzata la finestra di dialogo **Oggetti visivi di Power BI**, in cui è possibile scorrere gli oggetti visivi di Power BI disponibili e selezionare quello desiderato. È possibile eseguire una ricerca in base al nome, selezionare una categoria o semplicemente scorrere l'elenco di oggetti visivi disponibili. Una volta individuato l'oggetto visivo desiderato, fare clic su **Aggiungi** per aggiungerlo a **Power BI Desktop**.

   ![Oggetto visivo R 12](media/desktop-r-powered-custom-visuals/powerbi-r-powered-custom-viz_12.png)

## <a name="contribute-r-powered-power-bi-visuals"></a>Condividere oggetti visivi di Power BI basati su R

Se si creano oggetti visivi basati su R personalizzati da usare nei report, è possibile condividerli con tutti, aggiungendo l'oggetto visivo personalizzato alla **raccolta di oggetti visivi di Power BI**. I contributi vengono eseguiti tramite GitHub secondo la procedura seguente:

* [Contributo alla raccolta di oggetti visivi di Power BI basati su R](https://github.com/Microsoft/PowerBI-visuals#building-r-powered-custom-visual-corrplot)

## <a name="troubleshoot-r-powered-power-bi-visuals"></a>Risolvere i problemi relativi agli oggetti visivi di Power BI basati su R

Per il corretto funzionamento degli oggetti visivi di Power BI basati su R occorre rispettare determinate dipendenze. Quando gli oggetti visivi di Power BI basati su R non vengono eseguiti o caricati correttamente, il problema è in genere uno dei seguenti:

* Il motore R è mancante
* Errori nello script R su cui si basa l'oggetto visivo
* I pacchetti R sono mancanti o non aggiornati

La sezione seguente descrive i passaggi di risoluzione dei problemi che è possibile eseguire per trovare una soluzione ai problemi riscontrati.

### <a name="missing-or-outdated-r-packages"></a>Pacchetti R mancanti o non aggiornati

Quando si prova a installare un oggetto visivo personalizzato basato su R, possono verificarsi errori in caso di pacchetti R mancanti o obsoleti. Ciò può dipendere da uno dei motivi seguenti:

* L'installazione di R non è compatibile con il pacchetto R
* Le impostazioni del firewall, del software antivirus o del proxy impediscono la connessione di R a Internet
* La connessione Internet è lenta o si verifica un problema di connessione Internet

Il team di Power BI è attivamente impegnato nel risolvere questi problemi prima che raggiungano l'utente e la prossima versione di Power BI Desktop incorporerà degli aggiornamenti per risolvere questi problemi. Fino ad allora, è possibile eseguire una o più delle seguenti operazioni per ridurre i problemi:

1. Rimuovere l'oggetto visivo personalizzato, quindi installarlo di nuovo. Verrà avviata una nuova installazione dei pacchetti R.
2. Se l'installazione di R non è aggiornata, aggiornare l'installazione di R, quindi rimuovere e reinstallare l'oggetto visivo personalizzato come descritto nel passaggio precedente.

   Le versioni supportate di R sono elencate nella descrizione di ogni oggetto visivo personalizzato con tecnologia R, come illustrato nella figura seguente.

     ![Oggetto visivo R 11](media/desktop-r-powered-custom-visuals/powerbi-r-powered-custom-viz_11.png)
    > [!NOTE]
    > È possibile mantenere l'installazione di R originale e associare Power BI Desktop solo alla versione corrente installata. Passare a **File > Opzioni e impostazioni > Opzioni > Script R**.

3. Installare i pacchetti R manualmente, usando qualsiasi console di R. Di seguito è indicata la procedura per questo approccio:

   a.  Scaricare lo script di installazione dell'oggetto visivo basato su R e salvare il file in un'unità locale.

   b.  Dalla console di R, eseguire le operazioni seguenti:

       source("C:/Users/david/Downloads/ScriptInstallPackagesForForecastWithWorkarounds.R")

   Di seguito sono elencati i percorsi di installazione predefiniti:

       c:\Program Files\R\R-3.3.x\bin\x64\Rterm.exe (for CRAN-R)
       c:\Program Files\R\R-3.3.x\bin\x64\Rgui.exe (for CRAN-R)
       c:\Program Files\R\R-3.3.x\bin\R.exe (for CRAN-R)
       c:\Program Files\Microsoft\MRO-3.3.x\bin\R.exe (for MRO)
       c:\Program Files\Microsoft\MRO-3.3.x\bin\x64\Rgui.exe (for MRO)
       c:\Program Files\RStudio\bin\rstudio.exe (for RStudio)
4. Se la procedura precedente non funziona, provare a eseguire le operazioni seguenti:

   a. Usare **R Studio** e seguire i passaggi descritti al punto 3.b. sopra (eseguire la riga di script dalla console di R).

   b. Se il passaggio precedente non funziona, passare a **Strumenti > Opzioni globali > Pacchetti** in **R Studio** e attivare la casella di controllo **Usa libreria di Internet Explorer/proxy per HTTP**, quindi ripetere il passaggio 3.b. riportato in precedenza.

## <a name="next-steps"></a>Passaggi successivi

Esaminare le informazioni aggiuntive seguenti su R in Power BI.

* [Raccolta di oggetti visivi di Power BI](https://app.powerbi.com/visuals/)
* [Esecuzione di script R in Power BI Desktop](../connect-data/desktop-r-scripts.md)
* [Creare oggetti visivi R in Power BI Desktop](desktop-r-visuals.md)
* [Usare un IDE R esterno con Power BI](../connect-data/desktop-r-ide.md)
