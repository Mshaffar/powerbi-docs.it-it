---
title: Configurare e gestire le capacità in Power BI Premium
description: Informazioni su come gestire Power BI Premium e abilitare l'accesso al contenuto per tutta l'organizzazione.
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: conceptual
ms.date: 05/11/2020
LocalizationGroup: Premium
ms.openlocfilehash: 6155453f00ae64eee2cf74db7426b36248def796
ms.sourcegitcommit: a72567f26c1653c25f7730fab6210cd011343707
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/19/2020
ms.locfileid: "83564410"
---
# <a name="configure-and-manage-capacities-in-power-bi-premium"></a>Configurare e gestire le capacità in Power BI Premium

La gestione di Power BI Premium comporta la creazione, la gestione e il monitoraggio delle capacità Premium. Questo articolo offre istruzioni dettagliate; per una panoramica delle capacità, vedere [Gestione delle capacità Premium](service-premium-capacity-manage.md).

Informazioni su come gestire le capacità Power BI Premium e Power BI Embedded che offrono risorse dedicate per il contenuto.

![Schermata di impostazioni della capacità di Power BI](media/service-admin-premium-manage/premium-capacity-management.png)

Il concetto di *capacità* è al cuore delle offerte di Power BI Premium e Power BI Embedded. Si tratta di un set di risorse riservate per l'uso esclusivo da parte dell'organizzazione. La capacità dedicata consente di pubblicare dashboard, report e set di dati per gli utenti dell'organizzazione senza dover acquistare licenze individuali, nonché di offrire prestazioni affidabili e coerenti per il contenuto ospitato nella capacità. Per altre informazioni, vedere [What is Power BI Pro?](service-premium-what-is.md) (Che cos'è Power BI Pro?).

## <a name="manage-capacity"></a>Gestire la capacità

Dopo aver acquistato i nodi della capacità di Microsoft 365, è necessario configurare la capacità nell'interfaccia di amministrazione di Power BI. Le capacità di Power BI Premium vengono gestite nella sezione **Impostazioni di capacità** del portale.

![Impostazioni di capacità all'interno del portale di amministrazione](media/service-admin-premium-manage/admin-portal-premium.png)

È possibile gestire una capacità selezionandone il nome per passare alla schermata di gestione relativa.

![Selezionare il nome della capacità per visualizzare la schermata di assegnazione della capacità](media/service-admin-premium-manage/capacity-assignment.png)

Se nessuna area di lavoro è stata assegnata alla capacità, verrà visualizzato un messaggio relativo all'[assegnazione di aree di lavoro alla capacità](#assign-a-workspace-to-a-capacity).

### <a name="setting-up-a-new-capacity-power-bi-premium"></a>Configurazione di una nuova capacità (Power BI Premium)

L'interfaccia di amministrazione indica il numero di *memorie centrali virtuali* (vCore) che sono state usate e sono ancora disponibili. Il numero totale di memorie centrali virtuali si basa sugli SKU Premium che sono stati acquistati. Ad esempio, se si acquista uno SKU P3 e uno SKU P2 si hanno 48 memorie centrali disponibili: 32 dallo SKU P3 e 16 dallo SKU P2.

![Memorie centrali virtuali usate e disponibili per Power BI Premium](media/service-admin-premium-manage/admin-portal-v-cores.png)

Se si hanno memorie centrali virtuali disponibili, configurare la nuova capacità eseguendo la procedura seguente.

1. Selezionare **Configura nuova capacità**.

1. Assegnare un nome alla capacità.

1. Definire chi è l'amministratore per la capacità.

1. Selezionare le dimensioni della capacità. Le opzioni disponibili dipendono dal numero di memorie centrali virtuali disponibili. Non è possibile selezionare un'opzione che è maggiore del numero disponibile.

    ![Dimensioni della capacità Premium disponibili](media/service-admin-premium-manage/premium-capacity-size.png)

1. Selezionare **Configura**.

    ![Configurare una nuova capacità](media/service-admin-premium-manage/set-up-capacity.png)

Gli amministratori della capacità, nonché gli amministratori di Power BI e gli amministratori globali, vedono quindi la capacità elencata nell'interfaccia di amministrazione.

### <a name="capacity-settings"></a>Impostazioni di capacità

1. All'interno della schermata di gestione della capacità Premium in **Azioni** selezionare l'**icona a forma di ingranaggio** per rivedere e aggiornare le impostazioni. 

    ![Azioni della capacità all'interno dell'area di gestione della capacità](media/service-admin-premium-manage/capacity-actions.png)

1. È possibile vedere chi sono gli amministratori del servizio, lo SKU/le dimensioni della capacità e in quale regione si trova la capacità.

    ![Impostazioni di capacità](media/service-admin-premium-manage/capacity-settings.png)

1. È anche possibile rinominare o eliminare una capacità.

    ![Pulsanti di eliminazione e applicazione per le impostazioni di capacità in Power BI Premium](media/service-admin-premium-manage/capacity-settings-delete.png)

> [!NOTE]
> Le impostazioni di capacità di Power BI Embedded vengono gestite nel portale di Microsoft Azure.

### <a name="change-capacity-size"></a>Modifica le dimensioni della capacità

Gli amministratori di Power BI e gli amministratori globali possono modificare la capacità di Power BI Premium. Gli amministratori della capacità che non sono amministratori di Power BI o amministratori globali non hanno questa possibilità.

1. Selezionare **Modifica le dimensioni della capacità**.

    ![Modificare le dimensioni della capacità di Power BI Premium](media/service-admin-premium-manage/change-capacity-size.png)

1. Nella schermata **Modifica le dimensioni della capacità** aggiornare o effettuare il downgrade della capacità in modo appropriato.

    ![Elenco a discesa per modificare le dimensioni della capacità di Power BI Premium](media/service-admin-premium-manage/change-capacity-size2.png)

    Gli amministratori possono creare, ridimensionare ed eliminare i nodi purché abbiano il numero necessario di memorie centrali virtuali.

    Non è possibile effettuare il downgrade degli SKU P agli SKU EM. È possibile passare il mouse sulle opzioni disabilitate per visualizzare una spiegazione.



> [!IMPORTANT]
> Se per la capacità Power BI Premium si riscontra un utilizzo elevato delle risorse, con conseguenti problemi di prestazioni o affidabilità, è possibile ricevere messaggi di posta elettronica di notifica per identificare e risolvere il problema. Per altre informazioni, vedere [Notifiche per capacità e affidabilità](service-interruption-notifications.md#capacity-and-reliability-notifications).


### <a name="manage-user-permissions"></a>Gestire le autorizzazioni utente

È possibile assegnare altri amministratori della capacità, nonché assegnare gli utenti che hanno le autorizzazioni di *assegnazione della capacità*, che potranno assegnare un'area di lavoro alla capacità se sono anche amministratori di tale area di lavoro, oltre ad assegnare l'*Area di lavoro personale* alla capacità. Gli utenti con autorizzazioni di assegnazione non avranno accesso all'interfaccia di amministrazione.

> [!NOTE]
> Per Power BI Embedded, gli amministratori della capacità vengono definiti nel portale di Microsoft Azure.

Sotto **Autorizzazioni utente** espandere **Utenti con autorizzazioni di assegnazione** e aggiungere gli utenti e i gruppi appropriati.

![Autorizzazioni utente per le capacità](media/service-admin-premium-manage/capacity-user-permissions2.png)

## <a name="assign-a-workspace-to-a-capacity"></a>Assegnare un'area di lavoro a una capacità

Esistono due modi per assegnare un'area di lavoro a una capacità: nell'interfaccia di amministrazione e da un'area di lavoro.

### <a name="assign-from-the-admin-portal"></a>Assegnazione dall'interfaccia di amministrazione

Gli amministratori della capacità, insieme agli amministratori di Power BI e agli amministratori globali, possono assegnare in blocco le aree di lavoro nella sezione di gestione della capacità Premium dell'interfaccia di amministrazione. Quando si gestisce una capacità, si può visualizzare una sezione **Aree di lavoro** che consente di assegnare le aree di lavoro.

![Area di assegnazione delle aree di lavoro della gestione della capacità](media/service-admin-premium-manage/capacity-manage-workspaces.png)

1. Selezionare **Assegna aree di lavoro**. Questa opzione è disponibile in più posizioni.

1. Selezionare un'opzione per **Apply to** (Applica a).

    ![Assegna aree di lavoro](media/service-admin-premium-manage/assign-workspaces.png)

   | Selezione | Descrizione |
   | --- | --- |
   | **Aree di lavoro in base agli utenti** | Quando si assegnano le aree di lavoro per utente o gruppo, tutte le aree di lavoro appartenenti a tali utenti vengono assegnate alla capacità Premium, tra cui l'area di lavoro personale dell'utente. Tali utenti ottengono automaticamente le autorizzazioni di assegnazione dell'area di lavoro.<br>Ciò include le aree di lavoro già assegnata a una capacità diversa. |
   | **Aree di lavoro specifiche** | Immettere il nome di un'area di lavoro specifica da assegnare alla capacità selezionata. |
   | **Aree di lavoro dell'intera organizzazione** | L'assegnazione di aree di lavoro dell'intera organizzazione alla capacità Premium comporta l'assegnazione di tutte le aree di lavoro e delle aree di lavoro personali all'interno dell'organizzazione a tale capacità Premium. In più, tutti gli utenti attuali e futuri saranno autorizzati a riassegnare singole aree di lavoro a questa capacità. |
   | | |

1. Selezionare **Applica**.

### <a name="assign-from-workspace-settings"></a>Eseguire l'assegnazione dalle impostazioni dell'area di lavoro

È anche possibile assegnare a una capacità Premium un'area di lavoro dalle impostazioni di quest'ultima. Per spostare un'area di lavoro nella capacità, è necessario avere le autorizzazioni di amministratore per tale area di lavoro, nonché le autorizzazioni di assegnazione di capacità per tale capacità. Gli amministratori dell'area di lavoro possono sempre rimuovere un'area di lavoro dalla capacità Premium.

1. Modificare un'area di lavoro selezionando i puntini di sospensione **(. . .)** e quindi selezionando **Modifica area di lavoro**.

    ![Menu di scelta rapida Modifica area di lavoro visualizzato selezionando i puntini di sospensione](media/service-admin-premium-manage/edit-app-workspace.png)

1. In **Modifica area di lavoro** espandere **Avanzate**.

1. Selezionare la capacità a cui si vuole assegnare questa area di lavoro.

    ![Elenco a discesa di selezione della capacità](media/service-admin-premium-manage/app-workspace-advanced.png)

1. Selezionare **Salva**.

Dopo il salvataggio, l'area di lavoro e il relativo contenuto vengono spostati nella capacità Premium senza alcuna interruzione dell'esperienza di utilizzo per gli utenti finali.

## <a name="power-bi-report-server-product-key"></a>Codice Product Key del Server di report Power BI

Nella scheda **Impostazioni di capacità** dell'interfaccia di amministratore di Power BI si avrà accesso al codice Product Key del Server di Report di Power BI. Questo sarà disponibile solo per gli amministratori globali o per gli utenti a cui è stato assegnato il ruolo di amministratore del servizio Power BI e se è stato acquistato uno SKU di Power BI Premium.

![Codice Product Key del Server di report di Power BI all'interno di Impostazioni di capacità](media/service-admin-premium-manage/pbirs-product-key.png)

Se si seleziona **Chiave del server di report di Power BI** viene visualizzata una finestra di dialogo contenente il codice Product Key. È possibile copiarlo e usarlo durante l'installazione.

![Codice Product Key del Server di report Power BI](media/service-admin-premium-manage/pbirs-product-key-dialog.png)

Per altre informazioni, vedere [Install Power BI Report Server](../report-server/install-report-server.md) (Installare il Server di report di Power BI).

## <a name="next-steps"></a>Passaggi successivi

[Gestione delle capacità Premium](service-premium-capacity-manage.md)

Altre domande? [Provare a rivolgersi alla community di Power BI](https://community.powerbi.com/)
