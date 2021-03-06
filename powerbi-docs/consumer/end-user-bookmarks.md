---
title: Panoramica dei segnalibri nei report del servizio Power BI
description: Panoramica della documentazione per i segnalibri nel servizio Power BI.
author: mihart
ms.service: powerbi
ms.subservice: powerbi-consumer
ms.topic: conceptual
ms.date: 02/18/2020
ms.author: mihart
LocalizationGroup: Create reports
ms.openlocfilehash: 7b8945dc229d2aaf6227e18bb8f444c03bf200f2
ms.sourcegitcommit: 0e9e211082eca7fd939803e0cd9c6b114af2f90a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/13/2020
ms.locfileid: "83279803"
---
# <a name="what-are-bookmarks"></a>Che cosa sono i segnalibri?

[!INCLUDE[consumer-appliesto-ynnm](../includes/consumer-appliesto-ynnm.md)]

[!INCLUDE [power-bi-service-new-look-include](../includes/power-bi-service-new-look-include.md)]

I segnalibri acquisiscono la visualizzazione attualmente configurata di una pagina del report, tra cui filtri, filtri dei dati e lo stato degli oggetti visivi. Quando si seleziona un segnalibro, Power BI consente di tornare a tale visualizzazione. Esistono due tipi di segnalibri, quelli creati dall'utente e quelli creati dai *progettisti* di report. Qualsiasi utente di Power BI può creare segnalibri personali. Tuttavia, per poter usare i segnalibri creati da altri utenti è necessario avere una licenza di Power BI Pro o Premium. [Quali licenze sono disponibili?](end-user-license.md)

## <a name="use-bookmarks-to-share-insights-and-build-stories-in-power-bi"></a>Usare i segnalibri per condividere informazioni dettagliate e creare storie in Power BI 
I segnalibri possono avere diversi usi. Supponiamo di aver trovato un'informazione interessante che non si vuole perdere: creando un segnalibro, sarà possibile tornarvi in seguito. Se è necessario allontanarsi e non si vuole perdere il lavoro corrente, creare un segnalibro. È anche possibile creare un segnalibro per la visualizzazione predefinita del report, in modo che, ogni volta che vi si torna, si apra prima quella visualizzazione della pagina del report. 

È anche possibile creare una raccolta di segnalibri, disporli nell'ordine desiderato e successivamente passare da un segnalibro all'altro in una presentazione per evidenziare una serie di informazioni dettagliate che narrano una storia.  

![Per visualizzare il riquadro dei segnalibri, selezionarlo dalla barra multifunzione.](media/end-user-bookmarks/power-bi-select-bookmark.png)

## <a name="open-bookmarks"></a>Aprire i segnalibri
Per aprire il riquadro Segnalibri, selezionare **Segnalibri** > **Mostra altri segnalibri** dalla barra dei menu. Per tornare alla visualizzazione originale pubblicata del report, selezionare **Ripristina impostazioni predefinite**.

### <a name="report-bookmarks"></a>Segnalibri report
Se il *progettista* del report ha incluso segnalibri, sarà possibile trovarli sotto l'intestazione **Segnalibri report**. In questa pagina del report sono presenti due segnalibri, B1 e B2. 

> [!NOTE]
> Per visualizzare i report condivisi è necessario avere Power BI Pro o Premium. 

![Visualizzare i segnalibri del report.](media/end-user-bookmarks/power-bi-report.png)

Selezionare un segnalibro per passare a tale visualizzazione del report. 

![Video che mostra la selezione dei segnalibri del report.](media/end-user-bookmarks/power-bi-bookmarks.gif)

### <a name="personal-bookmarks"></a>Segnalibri personali

Quando si crea un segnalibro, insieme al segnalibro stesso vengono salvati gli elementi seguenti:

* Pagina corrente
* Filters
* Filtri dei dati, inclusi il tipo (ad esempio elenco o menu a discesa) e lo stato del filtro dei dati
* Stato della selezione degli oggetti visivi (ad esempio filtri con evidenziazione incrociata)
* Ordinamento
* Posizione drill
* Visibilità (di un oggetto, usando il riquadro **Selezione**)
* Modalità messa a fuoco o **In evidenza** di qualsiasi oggetto visibile

Configurare una pagina di report nel modo in cui si vuole che venga visualizzata nel segnalibro. Dopo aver disposto la pagina del report e gli oggetti visivi nel modo desiderato, per aggiungere un segnalibro selezionare **Aggiungi** nel riquadro **Segnalibri**. In questo esempio sono stati aggiunti alcuni filtri per l'area e la data. 

![Aggiungere segnalibri personali.](media/end-user-bookmarks/power-bi-bookmark-personal.png)

**Power BI** crea un segnalibro personale e gli assegna un nome generico o un nome immesso dall'utente. Per *rinominare*, *eliminare* o *aggiornare* un segnalibro, selezionare i puntini di sospensione accanto al nome del segnalibro e quindi scegliere un'azione dal menu visualizzato.

Una volta creato un segnalibro, è possibile visualizzarlo selezionando il segnalibro nel riquadro **Segnalibri**. 

![Aggiungere segnalibri personali.](media/end-user-bookmarks/power-bi-bookmark-west.png)


<!--
## Arranging bookmarks
As you create bookmarks, you might find that the order in which you create them isn't necessarily the same order you'd like to present them to your audience. No problem, you can easily rearrange the order of bookmarks.

In the **Bookmarks** pane, simply drag-and-drop bookmarks to change their order, as shown in the following image. The yellow bar between bookmarks designates where the dragged bookmark will be placed.

![Change bookmark order by drag-and-drop](media/desktop-bookmarks/bookmarks_06.png)

The order of your bookmarks can become important when you use the **View** feature of bookmarks, as described in the next section. 

-->

## <a name="bookmarks-as-a-slide-show"></a>Segnalibri come presentazione
Per presentare o visualizzare i segnalibri in un determinato ordine, selezionare **Visualizza** dal riquadro **Segnalibri** per iniziare una presentazione.

Quando si passa alla modalità **Visualizzazione**, è necessario tenere conto degli aspetti seguenti:

- Il nome del segnalibro viene visualizzato nella barra del titolo del segnalibro nella parte inferiore dell'area di disegno.
- Le frecce disponibili nella barra del titolo del segnalibro consentono di passare al segnalibro precedente o successivo.
- Per uscire dalla modalità **Visualizzazione**, selezionare **Esci** nel riquadro **Segnalibri** o la **X** nella barra del titolo del segnalibro.

![Presentazione dei segnalibri](media/end-user-bookmarks/power-bi-slideshow.png)

Nella modalità **Visualizzazione** è possibile chiudere il riquadro **Segnalibri** (facendo clic sulla X nel riquadro stesso) per lasciare più spazio alla presentazione. Sempre nella modalità **Visualizzazione**, tutti gli oggetti visivi sono interattivi e disponibili per l'evidenziazione incrociata, come accade normalmente quando si interagisce con essi. 

<!--
## Visibility - using the Selection pane
With the release of bookmarks, the new **Selection** pane is also introduced. The **Selection** pane provides a list of all objects on the current page and allows you to select the object and specify whether a given object is visible. 

![Enable the Selection pane](media/desktop-bookmarks/bookmarks_08.png)

You can select an object using the **Selection** pane. Also, you can toggle whether the object is currently visible by clicking the eye icon to the right of the visual. 

![Selection pane](media/desktop-bookmarks/bookmarks_09.png)

When a bookmark is added, the visible status of each object is also saved based on its setting in the **Selection** pane. 

It's important to note that **slicers** continue to filter a report page, regardless of whether they are visible. As such, you can create many different bookmarks, with different slicer settings, and make a single report page appear very different (and highlight different insights) in various bookmarks.


## Bookmarks for shapes and images
You can also link shapes and images to bookmarks. With this feature, when you click on an object, it will show the bookmark associated with that object. This can be especially useful when working with buttons; you can learn more by reading the article about [using buttons in Power BI](../create-reports/desktop-buttons.md). 

To assign a bookmark to an object, select the object, then expand the **Action** section from the **Format Shape** pane, as shown in the following image.

![Add bookmark link to an object](media/desktop-bookmarks/bookmarks_10.png)

Once you turn the **Action** slider to **On** you can select whether the object is a back button, a bookmark, or a Q&A command. If you select bookmark, you can then select which of your bookmarks the object is linked to.

There are all sorts of interesting things you can do with object-linked bookmarking. You can create a visual table of contents on your report page, or you can provide different views (such as visual types) of the same information, just by clicking on an object.

When you are in editing mode you can use ctrl+click to follow the link, and when not in edit mode, simply click the object to follow the link. 


## Bookmark groups

Beginning with the August 2018 release of **Power BI Desktop**, you can create and use bookmark groups. A bookmark group is a collection of bookmarks that you specify, which can be shown and organized as a group. 

To create a bookmark group, hold down the CTRL key and select the bookmarks you want to include in the group, then click the ellipses beside any of the selected bookmarks, and select **Group** from the menu that appears.

![Create a bookmark group](media/desktop-bookmarks/bookmarks_15.png)

**Power BI Desktop** automatically names the group *Group 1*. Fortunately, you can just double-click on the name and rename it to whatever you want.

![Rename a bookmark group](media/desktop-bookmarks/bookmarks_16.png)

With any bookmark group, clicking on the bookmark group's name only expands or collapses the group of bookmarks, and does not represent a bookmark by itself. 

When using the **View** feature of bookmarks, the following applies:

* If the selected bookmark is in a group when you select **View** from bookmarks, only the bookmarks *in that group* are shown in the viewing session. 

* If the selected bookmark is not in a group, or is on the top level (such as the name of a bookmark group), then all bookmarks for the entire report are played, including bookmarks in any group. 

To ungroup bookmarks, just select any bookmark in a group, click the ellipses, and then select **Ungroup** from the menu that appears. 

![Ungroup a bookmark group](media/desktop-bookmarks/bookmarks_17.png)

Note that selecting **Ungroup** for any bookmark from a group takes all bookmarks out of the group (it deletes the group, but not the bookmarks themselves). So to remove a single bookmark from a group, you need to **Ungroup** any member from that group, which deletes the grouping, then select the members you want in the new group (using CTRL and clicking each bookmark), and select **Group** again. 
-->





## <a name="limitations-and-considerations"></a>Limitazioni e considerazioni
Per questa versione dei **segnalibri**, tenere presenti alcune limitazioni e considerazioni.

* La maggior parte degli oggetti visivi di Power BI dovrebbero funzionare bene con i segnalibri. Se si verificano problemi con i segnalibri e un oggetto visivo di Power BI, contattare l'autore di tale oggetto visivo di Power BI e richiedere l'aggiunta del supporto dei segnalibri all'oggetto visivo.
* Se si aggiunge un oggetto visivo in una pagina del report dopo aver creato un segnalibro, l'oggetto visivo verrà visualizzato nel suo stato predefinito. Questo significa anche se si aggiunge un filtro dei dati a una pagina in cui sono stati creati segnalibri in precedenza, il filtro dei dati si comporterà in base allo stato predefinito.
* Se il *progettista* del report aggiorna o ripubblica il report, in genere i segnalibri personali non ne saranno interessati. Se tuttavia il progettista apporta modifiche sostanziali al report, ad esempio la rimozione di campi usati da un segnalibro, al successivo tentativo di apertura del segnalibro verrà visualizzato un messaggio di errore. 

<!--
## Next steps
spotlight?
-->
