---
title: Portale di amministrazione di Power BI
description: Il portale di amministrazione consente la gestione del tenant di Power BI nell'organizzazione. Include elementi come le metriche di utilizzo, l'accesso all'interfaccia di amministrazione di Microsoft 365 e le impostazioni.
author: kfollis
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: conceptual
ms.date: 04/27/2020
ms.author: kfollis
ms.custom: seodec18
LocalizationGroup: Administration
ms.openlocfilehash: b08184e92730bd3a42a91424883d07cecec82549
ms.sourcegitcommit: a72567f26c1653c25f7730fab6210cd011343707
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/19/2020
ms.locfileid: "83564473"
---
# <a name="administering-power-bi-in-the-admin-portal"></a>Amministrazione di Power BI nel portale di amministrazione

Il portale di amministrazione consente di gestire un *tenant* Power BI per l'organizzazione. Il portale include elementi come le metriche di utilizzo, l'accesso all'interfaccia di amministrazione di Microsoft 365 e le impostazioni.

Il portale di amministrazione completo è accessibile a tutti gli utenti amministratori globali o a cui è stato assegnato il ruolo di amministratore del servizio Power BI. Se non si ha uno di questi ruoli, nel portale saranno visualizzate solo le **impostazioni di capacità**. Per altre informazioni sul ruolo di amministratore del servizio Power BI, vedere [Informazioni sul ruolo di amministratore di Power BI](service-admin-role.md).

## <a name="how-to-get-to-the-admin-portal"></a>Come accedere al portale di amministrazione

Per ottenere l'accesso al portale di amministrazione di Power BI, l'account deve essere contrassegnato come **Amministratore globale** in Microsoft 365 o in Azure Active Directory (Azure AD) o avere ricevuto il ruolo di amministratore del servizio Power BI. Per altre informazioni sul ruolo di amministratore del servizio Power BI, vedere [Informazioni sul ruolo di amministratore di Power BI](service-admin-role.md). Per accedere al portale di amministrazione di Power BI, eseguire le operazioni seguenti.

1. Selezionare l'icona a forma di ingranaggio delle impostazioni in alto a destra nella pagina del servizio Power BI.

1. Selezionare **Portale di amministrazione**.

    ![Impostazioni per il portale di amministrazione](media/service-admin-portal/powerbi-admin-settings.png)

Nel portale sono presenti nove schede. Il resto di questo articolo fornisce informazioni su ognuna di queste schede.

![Navigazione nel portale di amministrazione](media/service-admin-portal/powerbi-admin-landing-page.png)

* [Metriche di utilizzo](#usage-metrics)
* [Utenti](#users)
* [Log di controllo](#audit-logs)
* [Impostazioni tenant](#tenant-settings)
* [Impostazioni capacità](#capacity-settings)
* [Codici di incorporamento](#embed-codes)
* [Oggetti visivi dell'organizzazione](#organizational-visuals)
* [Archiviazione del flusso di dati (anteprima)](#dataflowStorage)
* [Aree di lavoro](#workspaces)
* [Personalizzazione](#custom-branding)

## <a name="usage-metrics"></a>Metriche di utilizzo

La scheda **Metriche di utilizzo** consente di monitorare l'utilizzo di Power BI per l'organizzazione. Consente inoltre di vedere quali sono gli utenti e i gruppi più attivi all'interno di Power BI per l'organizzazione. 

> [!NOTE]
> Al primo accesso al dashboard o quando si accede di nuovo al dashboard dopo un lungo periodo di inutilizzo, è probabile che venga visualizzata una schermata di caricamento mentre viene caricato il dashboard.

Al termine del caricamento del dashboard vengono visualizzate due sezioni di riquadri. La prima sezione include i dati di utilizzo per i singoli utenti e la seconda sezione ha informazioni simili per i gruppi all'interno dell'organizzazione.

Di seguito è riportata la suddivisione dei dati visualizzati in ogni riquadro:

* Conteggio distinto di tutti i dashboard, i report e i set di dati nell'area di lavoro dell'utente.
  
    ![Conteggio distinto di dashboard, report e set di dati](media/service-admin-portal/powerbi-admin-usage-metrics-number-tiles.png)

* Dashboard più utilizzato in base al numero di utenti che possono accedervi. Ad esempio, se si ha un dashboard condiviso con 3 utenti e tale dashboard è stato aggiunto anche a un pacchetto di contenuto a cui sono connessi due utenti diversi, il conteggio è 6 (1 + 3 + 2).
  
    ![Dashboard più utilizzati](media/service-admin-portal/powerbi-admin-usage-metrics-top-dashboards.png)

* Il contenuto più popolare a cui si sono connessi gli utenti. Si tratta di qualsiasi contenuto accessibile per gli utenti tramite il processo Recupera dati, quindi pacchetti di contenuto SaaS, pacchetti di contenuto aziendali, file o database.
  
    ![Pacchetti più utilizzati](media/service-admin-portal/powerbi-admin-usage-metrics-top-connections.png)

* Una visualizzazione dei principali utenti in base al numero di dashboard che hanno: sia i dashboard creati da loro che quelli condivisi con loro.
  
    ![Principali utenti - dashboard](media/service-admin-portal/powerbi-admin-usage-metrics-top-users-dashboards.png)

* Una visualizzazione dei principali utenti in base al numero di report che hanno.
  
    ![Principali utenti - report](media/service-admin-portal/powerbi-admin-usage-metrics-top-users-reports.png)

La seconda sezione mostra lo stesso tipo di informazioni, ma in base ai gruppi. In questo modo è possibile stabilire quali sono i gruppi più attivi all'interno dell'organizzazione e quale tipo di contenuto usano.

Con queste informazioni è possibile ottenere informazioni dettagliate reali in merito alla modalità d'uso di Power BI all'interno dell'organizzazione ed è possibile individuare gli utenti e i gruppi particolarmente attivi nell'organizzazione.

## <a name="control-usage-metrics"></a>Controllare le metriche di utilizzo

I report sulle metriche di utilizzo sono una funzionalità che l'amministratore di Power BI o Microsoft 365 può attivare o disattivare. Gli amministratori hanno un controllo granulare sugli utenti che hanno accesso alle metriche di utilizzo. Questa funzionalità è **attiva** per impostazione predefinita per tutti gli utenti dell'organizzazione.

Gli amministratori possono anche stabilire se gli autori di contenuti possono vedere i dati per utente nelle metriche di utilizzo. 

Vedere [Monitorare le metriche di utilizzo per dashboard e report di Power BI](../collaborate-share/service-usage-metrics.md) per informazioni dettagliate su tali report.

### <a name="usage-metrics-for-content-creators"></a>Metriche di utilizzo per i creatori di contenuti

1. Nel portale di amministrazione selezionare **Impostazioni tenant** > **Metriche di utilizzo per i creatori di contenuti**.

    ![Metriche di utilizzo nelle impostazioni del tenant nel portale di amministrazione](media/service-admin-portal/power-bi-admin-usage-metrics.png)

1. Abilitare (o disabilitare) le metriche di utilizzo > **Applica**.

    ![Metriche di utilizzo abilitate](../collaborate-share/media/service-usage-metrics/power-bi-tenant-settings-updated.png)


### <a name="per-user-data-in-usage-metrics"></a>Dati per utente nelle metriche di utilizzo

Per impostazione predefinita, i dati per utente sono abilitati nelle metriche di utilizzo e le informazioni sull'account del consumer di contenuto sono incluse nel report delle metriche. Se non si vogliono includere queste informazioni per alcuni o tutti gli utenti, disabilitare la funzionalità per specifici gruppi di sicurezza o per un'intera organizzazione. Le informazioni sull'account vengono quindi visualizzate nel report come *Senza nome*.

![Dati di utilizzo per utente](media/service-admin-portal/power-bi-admin-per-user-usage-data.png)

### <a name="delete-all-existing-usage-metrics-content"></a>Eliminare tutto il contenuto delle metriche di utilizzo esistente

Quando si disabilitano le metriche di utilizzo per l'intera organizzazione, gli amministratori possono anche scegliere una o entrambe le opzioni seguenti:

- **Elimina tutto il contenuto della metrica di utilizzo esistente** per eliminare tutti i report esistenti e i riquadri di dashboard creati usando report sulle metriche di utilizzo e set di dati. Questa opzione rimuove completamente l'accesso ai dati delle metriche di utilizzo per tutti gli utenti dell'organizzazione che le usano. 
- **Elimina tutti i dati per utente nel contenuto della metrica di utilizzo corrente**. Questa opzione rimuove completamente l'accesso ai dati per utente per tutti gli utenti dell'organizzazione che potrebbe già usarli. 

Occorre prestare attenzione, perché l'eliminazione del contenuto delle metriche di utilizzo e per utente esistente è irreversibile.

## <a name="users"></a>Utenti

Gli utenti, i gruppi e gli amministratori di Power BI vengono gestiti nell'interfaccia di amministrazione di Microsoft 365. La scheda **Utenti** offre un collegamento all'interfaccia di amministrazione per il tenant.

![Passare all'interfaccia di amministrazione di Microsoft 365](media/service-admin-portal/powerbi-admin-manage-users.png)

## <a name="audit-logs"></a>Log di controllo

I log di controllo di Power BI vengono gestiti nel Centro sicurezza e conformità di Office 365. La scheda **Log di controllo** offre un collegamento al Centro sicurezza e conformità per il tenant. [Altre informazioni](service-admin-auditing.md)

Per usare i log di controllo, assicurarsi che l'impostazione [**Creare log di controllo per la verifica interna delle attività e ai fini della conformità**](#create-audit-logs-for-internal-activity-auditing-and-compliance) sia abilitata.

## <a name="tenant-settings"></a>Impostazioni tenant

La scheda **Impostazioni tenant** consente di controllare in modo dettagliato le funzionalità rese disponibili per l'organizzazione. Se i dati sensibili rappresentano una criticità, è possibile che alcune delle funzionalità non siano adatte all'organizzazione o che per un determinato gruppo sia preferibile rendere disponibile solo una specifica funzionalità.

L'immagine seguente mostra diverse impostazioni della scheda **Impostazioni tenant**.

![Impostazioni tenant](media/service-admin-portal/powerbi-admin-tenant-settings.png)

> [!NOTE]
> Possono essere necessari fino a 10 minuti affinché la modifica di un'impostazione diventi effettiva per tutti gli utenti del tenant.

Le impostazioni possono avere tre stati:

* **Disabilitato per l'intera organizzazione**: nessuno all'interno dell'organizzazione può usare questa funzionalità.

    ![Impostazione per disabilitare la funzionalità per tutti](media/service-admin-portal/powerbi-admin-tenant-settings-disabled.png)

* **Abilitato per l'intera organizzazione**: tutti all'interno dell'organizzazione possono usare questa funzionalità.

    ![Impostazione per abilitare la funzionalità per tutti](media/service-admin-portal/powerbi-admin-tenant-settings-enabled.png)

* **Abilitato per un subset dell'organizzazione**: uno specifico subset di utenti o gruppi all'interno dell'organizzazione può usare questa funzionalità.

    È possibile abilitare la funzionalità per l'intera organizzazione, ad eccezione di un gruppo specifico di utenti.

    ![Impostazione per abilitare la funzionalità per un subset](media/service-admin-portal/powerbi-admin-tenant-settings-enabled-except.png)

    È anche possibile abilitare la funzionalità solo per un gruppo specifico di utenti e disabilitarla per un altro gruppo di utenti. Con questo approccio si è certi che alcuni utenti non abbiano accesso alla funzionalità anche se fanno parte del gruppo autorizzato.

    ![Impostazione per abilitare la funzionalità con eccezioni](media/service-admin-portal/powerbi-admin-tenant-settings-enabled-except2.png)

Le sezioni successive forniscono una panoramica dei diversi tipi di impostazioni del tenant.

## <a name="help-and-support-settings"></a>Impostazioni per Guida e supporto tecnico

### <a name="publish-get-help-information"></a>Pubblica informazioni su "Supporto"

Gli utenti dell'organizzazione possono usare le risorse interne di Guida e supporto tecnico tramite il menu della Guida di Power BI. In particolare, questi parametri modificano il comportamento delle voci di menu Informazioni, Community e Guida.

Inoltre, specificando un URL per le richieste di licenza, è possibile personalizzare l'URL di destinazione del pulsante **Aggiorna account**. Gli utenti senza una licenza di Power BI Pro possono visualizzare questo pulsante nella finestra di dialogo **Aggiorna a Power BI Pro** e nella pagina **Gestisci archivio personale**. Inoltre, Power BI non offre più il pulsante **Prova gratuitamente la versione Pro** in questa finestra di dialogo o nella pagina dell'archivio. In questo modo si garantisce che gli utenti vengano guidati in modo affidabile da Power BI attraverso i processi definiti nell'organizzazione tramite la soluzione di gestione delle licenze.

![Impostazione per abilitare la funzionalità con eccezioni](media/service-admin-portal/powerbi-admin-tenant-settings-gethelp.png)

### <a name="receive-email-notifications-for-service-outages-or-incidents"></a>Ricevi notifiche di posta elettronica per interruzioni del servizio o eventi imprevisti

I gruppi di sicurezza abilitati per la posta elettronica riceveranno notifiche di posta elettronica se si verifica un'interruzione del servizio o un evento imprevisto che interessa il tenant. Vedere altre informazioni sulle [notifiche di interruzione del servizio](service-interruption-notifications.md).

## <a name="workspace-settings"></a>Impostazioni dell'area di lavoro

In **Impostazioni tenant** il portale di amministrazione ha due sezioni per il controllo delle aree di lavoro:

- Creare l'esperienza delle nuove aree di lavoro.
- Usare set di dati in tutte le aree di lavoro.

### <a name="create-the-new-workspaces"></a>Creare le nuove aree di lavoro

Le aree di lavoro sono posizioni in cui gli utenti possono collaborare a dashboard, report e altro contenuto. Gli amministratori usano l'impostazione **Crea aree di lavoro (nuova esperienza delle aree di lavoro)** per indicare quali utenti dell'organizzazione possono creare aree di lavoro. Gli amministratori possono consentire a qualsiasi utente dell'organizzazione o a nessuno di questi di creare aree di lavoro con la nuova esperienza. Possono anche limitare la creazione ai membri di gruppi di sicurezza specifici. Vedere altre informazioni sulle [aree di lavoro](../collaborate-share/service-new-workspaces.md).

:::image type="content" source="media/service-admin-portal/power-bi-admin-workspace-settings.png" alt-text="Creare l'esperienza delle nuove aree di lavoro":::

Per le aree di lavoro classiche basate su gruppi di Microsoft 365, l'amministrazione continua ad avvenire nel portale di amministrazione e in Azure Active Directory.

> [!NOTE]
> Per impostazione predefinita, l'impostazione **Crea aree di lavoro (nuova esperienza delle aree di lavoro)** consente la creazione di nuove aree di lavoro di Power BI solo agli utenti autorizzati a creare gruppi di Microsoft 365. Assicurarsi di impostare un valore nel portale di amministrazione di Power BI per garantire che le aree di lavoro possano essere create solo dagli utenti appropriati.

**Elenco delle aree di lavoro**

Il portale di amministrazione ha un'altra sezione di impostazioni relative alle aree di lavoro nel tenant. In tale sezione è possibile ordinare e filtrare l'elenco di aree di lavoro e visualizzare i dettagli per ognuna di esse. Per informazioni dettagliate, vedere [Aree di lavoro](#workspaces) in questo articolo.

**Pubblicare pacchetti di contenuto e app**

Nel portale di amministrazione è anche possibile controllare gli utenti autorizzati a distribuire le app nell'organizzazione. Per informazioni dettagliate, vedere [Pubblicare pacchetti di contenuto e app per l'intera organizzazione](#publish-content-packs-and-apps-to-the-entire-organization) in questo articolo.

### <a name="use-datasets-across-workspaces"></a>Usa i set di dati in tutte le aree di lavoro

Gli amministratori possono controllare quali utenti dell'organizzazione possono usare set di dati in tutte le aree di lavoro. Se questa impostazione è abilitata, gli utenti hanno comunque bisogno dell'autorizzazione di compilazione necessaria per un set di dati specifico.

:::image type="content" source="media/service-admin-portal/power-bi-admin-datasets-workspaces.png" alt-text="Usare set di dati in tutte le aree di lavoro":::

Per altre informazioni, vedere [Introduzione ai set di dati in aree di lavoro diverse](../connect-data/service-datasets-across-workspaces.md).


## <a name="export-and-sharing-settings"></a>Impostazioni di esportazione e condivisione

### <a name="share-content-with-external-users"></a>Condividi contenuti con utenti esterni

Gli utenti interni all'organizzazione possono condividere dashboard, report e app con utenti esterni all'organizzazione. Altre informazioni sulla [condivisione esterna](../collaborate-share/service-share-dashboards.md#share-a-dashboard-or-report-outside-your-organization).

![Impostazione per gli utenti esterni](media/service-admin-portal/powerbi-admin-sharing-external-02.png)

La figura seguente mostra il messaggio che viene visualizzato al momento della condivisione con un utente esterno.

![Condivisione con un utente esterno](media/service-admin-portal/powerbi-admin-sharing-external.png)  

> [!IMPORTANT]
> Questa opzione consente di controllare la possibilità per gli utenti di Power BI di invitare utenti esterni a diventare guest di Azure Active Directory B2B (Azure AD B2B) nell'organizzazione tramite Power BI. Quando questa funzionalità è abilitata, gli utenti che hanno il ruolo mittente dell'invito guest in Azure AD possono aggiungere indirizzi di posta elettronica esterni durante la condivisione di report, dashboard e app Power BI. Il destinatario esterno è invitato a partecipare all'organizzazione come utente guest B2B di Azure AD. Si noti che, quando si disabilita questa impostazione, gli utenti esterni che sono già utenti guest B2B di Azure AD nell'organizzazione continuano a essere visualizzati nelle interfacce utente di selezione utenti in Power BI e possono accedere ad elementi, aree di lavoro e app.

### <a name="publish-to-web"></a>Pubblica sul Web

L'impostazione **Pubblica sul Web** offre agli amministratori di tenant di Power BI opzioni che consentono agli utenti di creare codice di incorporamento per pubblicare report sul Web. Con questa funzionalità il report e i relativi dati vengono resi disponibili a chiunque sul Web. Vedere altre informazioni sulla [pubblicazione sul Web](../collaborate-share/service-publish-to-web.md).

> [!NOTE]
> Solo gli amministratori di Power BI possono consentire la creazione di nuovo codice di incorporamento per la pubblicazione sul Web. Le organizzazioni potrebbero avere codici di incorporamento esistenti. Vedere la sezione [Codici di incorporamento](service-admin-portal.md#embed-codes) nel portale di amministrazione per visualizzare i report attualmente pubblicati.

La figura seguente mostra il menu **Altre opzioni (...)** per un report quando l'impostazione **Pubblica sul Web** è abilitata.

![Pubblica sul Web nel menu Altre opzioni](media/service-admin-portal/power-bi-more-options-publish-web.png)

L'impostazione **Pubblica sul Web** nel portale di amministrazione offre opzioni per le quali gli utenti possono creare codici di incorporamento.

![Impostazione Pubblica sul Web](media/service-admin-portal/powerbi-admin-publish-to-web-setting.png)

Gli amministratori possono impostare **Pubblica sul Web** su **Abilitato** e **Scegliere la modalità di funzionamento dei codici di incorporamento** su **Consenti solo codici di incorporamento esistenti**. In questo caso gli utenti possono creare codici di incorporamento, ma devono contattare l'amministratore di Power BI per ottenere l'autorizzazione.

![Richiesta di Pubblica sul Web](../collaborate-share/media/service-publish-to-web/publish_to_web_admin_prompt.png)

Gli utenti possono vedere opzioni diverse nell'interfaccia utente in base all'impostazione di **Pubblica sul Web**.

|Feature |Abilitata per l'intera organizzazione |Disabilitata per l'intera organizzazione |Gruppi di sicurezza specifici   |
|---------|---------|---------|---------|
|**Pubblica sul Web** nel menu **Altre opzioni (...)** del report|Abilitata per tutti|Non visibile per tutti|Visibile solo per utenti o gruppi autorizzati.|
|**Gestisci codici di incorporamento** in **Impostazioni**|Abilitata per tutti|Abilitata per tutti|Abilitata per tutti<br><br>Opzione * **Elimina** solo per utenti o gruppi autorizzati.<br>Opzione * **Ottieni i codici** abilitata per tutti.|
|**Incorpora codici** nel portale di amministrazione|Stato indica una delle opzioni seguenti:<br>* Attivo<br>* Non supportato<br>* Bloccato|Stato indica **Disabilitato**|Stato indica una delle opzioni seguenti:<br>* Attivo<br>* Non supportato<br>* Bloccato<br><br>Se un utente non è autorizzato in base all'impostazione del tenant, lo stato indica **Violazione**.|
|Report pubblicati esistenti|Tutti abilitati|Tutti disabilitati|Il rendering di tutti i report viene continuato per tutti.|

### <a name="export-data"></a>Esporta dati

Gli utenti dell'organizzazione possono esportare dati da un riquadro o una visualizzazione. Questa impostazione controlla le funzionalità Analizza in Excel, di esportazione in file CSV, di download di set di dati (con estensione pbix) e Live Connect del servizio Power BI. Vedere altre informazioni sull'[esportazione di dati da un riquadro o da un oggetto visivo](../visuals/power-bi-visualization-export-data.md).

>[!NOTE]
> Prima dell'introduzione dell'impostazione Esporta in Excel, questa impostazione controllava anche l'esportazione dei dati in file di Excel. Per informazioni dettagliate, vedere la [nota in Esporta in Excel](#export-to-excel).

![Impostazione Esporta dati](media/service-admin-portal/powerbi-admin-portal-export-data-setting.png)

La figura seguente mostra l'opzione per esportare i dati da un riquadro.

![Esportare dati da un riquadro](media/service-admin-portal/powerbi-admin-export-data.png)

> [!NOTE]
> Se si disabilita **Esporta dati**, si impedisce anche agli utenti di usare la funzionalità [Analizza in Excel](../collaborate-share/service-analyze-in-excel.md) oltre alla connessione dinamica al servizio Power BI.

### <a name="export-to-excel"></a>Esporta in Excel

Gli utenti dell'organizzazione possono esportare i dati da una visualizzazione a un file di Excel.

![Impostazione Esporta in Excel](media/service-admin-portal/powerbi-admin-portal-export-to-excel-setting.png)

>[!IMPORTANT]
> Prima dell'introduzione dell'impostazione Esporta in Excel, l'esportazione in un file di Excel era controllata dall'impostazione Esporta dati. Pertanto, nei tenant esistenti prima dell'introduzione dell'impostazione Esporta in Excel, la prima volta che gli amministratori del tenant esaminano l'impostazione Esporta in Excel vedranno che sono presenti *Modifiche non applicate*. Per rendere effettiva la nuova impostazione, è necessario applicare queste modifiche. In caso contrario, l'esportazione in un file di Excel continuerà a essere controllata dall'impostazione Esporta dati.

### <a name="export-reports-as-powerpoint-presentations-or-pdf-documents"></a>Esporta report come presentazioni di PowerPoint o documenti PDF

Gli utenti dell'organizzazione possono esportare i report di Power BI come file di PowerPoint o documenti PDF. [Altre informazioni](../consumer/end-user-powerpoint.md)

La figura seguente illustra il menu **File** per un report quando l'impostazione **Esporta report come presentazioni di PowerPoint o documenti PDF** è abilitata.

![Esporta report come presentazioni di PowerPoint](media/service-admin-portal/powerbi-admin-powerpoint.png)

### <a name="print-dashboards-and-reports"></a>Stampare dashboard e report

Gli utenti dell'organizzazione possono stampare dashboard e report. [Altre informazioni](../consumer/end-user-print.md)

La figura seguente mostra l'opzione per stampare un dashboard.

![Stampa dashboard](media/service-admin-portal/powerbi-admin-print-dashboard.png)

La figura seguente mostra il menu **File** per un report quando l'impostazione **Stampare dashboard e report** è abilitata.

![Stampare il report](media/service-admin-portal/powerbi-admin-print-report.png)

### <a name="allow-external-guest-users-to-edit-and-manage-content-in-the-organization"></a>Consenti agli utenti guest esterni di modificare e gestire il contenuto dell'organizzazione

Gli utenti guest B2B di Azure AD possono modificare e gestire contenuti dell'organizzazione. [Altre informazioni](service-admin-azure-ad-b2b.md)

L'immagine seguente mostra l'opzione Consenti agli utenti guest esterni di modificare e gestire il contenuto dell'organizzazione.

![Consenti agli utenti guest esterni di modificare e gestire il contenuto dell'organizzazione](media/service-admin-portal/powerbi-admin-tenant-settings-b2b-guest-edit-manage.png)

Nel portale di amministrazione è anche possibile controllare gli utenti autorizzati a invitare utenti esterni nell'organizzazione. Per dettagli vedere [Condividi contenuti con utenti esterni](#export-and-sharing-settings) in questo articolo.

### <a name="email-subscriptions"></a>Sottoscrizioni di posta elettronica
Gli utenti dell'organizzazione possono creare sottoscrizioni di posta elettronica. Vedere altre informazioni sulle [sottoscrizioni](../collaborate-share/service-publish-to-web.md).

![Abilitare le sottoscrizioni di posta elettronica](media/service-admin-portal/power-bi-manage-email-subscriptions.png)

### <a name="featured-content"></a>Contenuti in primo piano

Consentire ad alcuni o a tutti gli autori di report nell'organizzazione di presentare il proprio contenuto nella sezione In primo piano della home page di Power BI. I nuovi utenti visualizzeranno il contenuto in primo piano nella parte superiore della home page di Power BI. Il contenuto in primo piano viene spostato verso il basso nella home page, man mano che gli utenti aggiungono elementi nelle sezioni **Preferiti**, **Frequenti** e **Recenti**. 

È consigliabile iniziare con un piccolo set di elementi in primo piano. Se si consente all'intera organizzazione di includere contenuto in primo piano nella home page, può diventare difficile tenere traccia di tutti i contenuti messi in evidenza. 

Dopo aver abilitato il contenuto in primo piano, è anche possibile gestirlo nel portale di amministrazione. Vedere [Gestire il contenuto in primo piano](#manage-featured-content) in questo articolo per informazioni sul controllo del contenuto in primo piano nel proprio dominio.

## <a name="content-pack-and-app-settings"></a>Impostazioni dell'app e del pacchetto di contenuto

### <a name="publish-content-packs-and-apps-to-the-entire-organization"></a>Pubblicare pacchetti di contenuto e app per l'intera organizzazione

Gli amministratori usano questa impostazione per determinare quali utenti possono pubblicare pacchetti di contenuto e app per l'intera organizzazione, invece che per gruppi specifici. Vedere altre informazioni sulla [pubblicazione di app](../collaborate-share/service-create-distribute-apps.md).

La figura seguente mostra l'opzione **Intera organizzazione** quando si crea un pacchetto di contenuto.

![Pubblicare il pacchetto di contenuto per l'organizzazione](media/service-admin-portal/powerbi-admin-publish-entire-org.png)

### <a name="create-template-apps-and-organizational-content-packs"></a>Creare app modello e pacchetti di contenuto dell'organizzazione

Gli utenti dell'organizzazione possono creare app modello e pacchetti di contenuto dell'organizzazione che usano set di dati basati su un'origine dati in Power BI Desktop. Vedere altre informazioni sulle [app modello](../connect-data/service-template-apps-create.md).

### <a name="push-apps-to-end-users"></a>Push delle app agli utenti finali

I creatori di report possono condividere le app direttamente con gli utenti finali senza necessità di installazione da [AppSource](https://appsource.microsoft.com). Vedere altre informazioni sull'[installazione automatica di app per gli utenti finali](../collaborate-share/service-create-distribute-apps.md#automatically-install-apps-for-end-users).

## <a name="integration-settings"></a>Impostazioni di integrazione

### <a name="use-analyze-in-excel-with-on-premises-datasets"></a>Usare Analizza in Excel con set di dati locali

Gli utenti dell'organizzazione possono usare Excel per visualizzare set di dati di Power BI locali e interagire con essi. [Altre informazioni](../collaborate-share/service-analyze-in-excel.md)

> [!NOTE]
> Se si disabilita l'impostazione **Esporta dati**, gli utenti non possono usare neanche la funzionalità **Analizza in Excel**.

### <a name="use-arcgis-maps-for-power-bi"></a>Usa Mappe ArcGIS per Power BI

Gli utenti dell'organizzazione possono usare la visualizzazione Mappe ArcGIS per Power BI offerta da Esri. [Altre informazioni](../visuals/power-bi-visualization-arcgis.md)

### <a name="use-global-search-for-power-bi-preview"></a>Usa la ricerca globale per Power BI (anteprima)

Gli utenti dell'organizzazione possono usare funzionalità di ricerca esterne basate su Ricerca di Azure.

## <a name="power-bi-visuals-settings"></a>Impostazioni degli oggetti visivi di Power BI

### <a name="add-and-use-power-bi-visuals"></a>Aggiungere e usare oggetti visivi di Power BI

Gli utenti dell'organizzazione possono interagire con gli oggetti visivi di Power BI e condividerli. [Altre informazioni](../developer/visuals/power-bi-custom-visuals.md)

> [!NOTE]
> Questa impostazione può essere applicata all'intera organizzazione o limitata a gruppi specifici.

Power BI Desktop (a partire dalla versione di marzo 2019) supporta l'uso di **Criteri di gruppo** per disabilitare l'uso di oggetti visivi di Power BI nei computer distribuiti di un'organizzazione.

<table>
<tr><th>Attributo</th><th>Valore</th>
</tr>
<td>chiave</td>
    <td>Software\Policies\Microsoft\Power BI Desktop\</td>
<tr>
<td>valueName</td>
<td>EnableCustomVisuals</td>
</tr>
</table>

Il valore 1 (decimale) abilita l'uso di oggetti visivi di Power BI in Power BI (opzione predefinita).

Il valore 0 (decimale) disabilita l'uso di oggetti visivi di Power BI in Power BI.

### <a name="allow-only-certified-visuals"></a>Consenti solo oggetti visivi personalizzati certificati

Gli utenti dell'organizzazione a cui sono state assegnate le autorizzazioni per aggiungere e usare gli oggetti visivi di Power BI, tramite l'impostazione "Aggiungi e usa oggetti visivi personalizzati", potranno usare solo [oggetti visivi di Power BI certificati](https://go.microsoft.com/fwlink/?linkid=2002010) (gli oggetti visivi non certificati verranno bloccati e verrà visualizzato un messaggio di errore quando vengono usati). 


Power BI Desktop (a partire dalla versione di marzo 2019) supporta l'uso di **Criteri di gruppo** per disabilitare l'utilizzo di oggetti visivi di Power BI non certificati nei computer distribuiti di un'organizzazione.

<table>
<tr><th>Attributo</th><th>Valore</th>
</tr>
<td>chiave</td>
    <td>Software\Policies\Microsoft\Power BI Desktop\</td>
<tr>
<td>valueName</td>
<td>EnableUncertifiedVisuals</td>
</tr>
</table>

Il valore 1 (decimale) abilita l'uso di oggetti visivi di Power BI non certificati in Power BI (opzione predefinita).

Il valore 0 (decimale) disabilita l'uso di oggetti visivi di Power BI non certificati in Power BI (questa opzione consente solo l'uso di [oggetti visivi di Power BI certificati](https://go.microsoft.com/fwlink/?linkid=2002010)).

## <a name="r-visuals-settings"></a>Impostazioni degli oggetti visivi R

### <a name="interact-with-and-share-r-visuals"></a>Interagire con gli oggetti visivi R e condividerli

Gli utenti dell'organizzazione possono interagire con gli oggetti visivi creati con script R e condividerli. [Altre informazioni](../visuals/service-r-visuals.md)

> [!NOTE]
> Questa impostazione si applica all'intera organizzazione e non può essere limitata a gruppi specifici.

## <a name="audit-and-usage-settings"></a>Impostazioni di controllo e utilizzo

### <a name="create-audit-logs-for-internal-activity-auditing-and-compliance"></a>Creare log di controllo per la verifica interna delle attività e la conformità

Gli utenti dell'organizzazione possono usare il controllo per monitorare le azioni eseguite da altri utenti dell'organizzazione in Power BI. [Altre informazioni](service-admin-auditing.md)

Questa impostazione deve essere abilitata per la registrazione delle voci del log di controllo. È possibile che tra l'abilitazione della funzione di controllo e la visualizzazione dei dati di controllo si verifichi un ritardo di un massimo di 48 ore. Se i dati non vengono visualizzati immediatamente, controllare i log di controllo successivamente. Un ritardo simile può verificarsi tra l'assegnazione dell'autorizzazione per la visualizzazione dei log di controllo e l'accesso ai log.

> [!NOTE]
> Questa impostazione si applica all'intera organizzazione e non può essere limitata a gruppi specifici.

### <a name="usage-metrics-for-content-creators"></a>Metriche di utilizzo per i creatori di contenuti

Gli utenti dell'organizzazione possono visualizzare le metriche di utilizzo dei dashboard e dei report creati. [Altre informazioni](../collaborate-share/service-usage-metrics.md)

### <a name="per-user-data-in-usage-metrics-for-content-creators"></a>Dati per utente nella metrica di utilizzo per i creatori di contenuti

La metrica di utilizzo per i creatori di contenuti esporrà i nomi visualizzati e gli indirizzi di posta elettronica degli utenti che accedono ai contenuti. [Altre informazioni](../collaborate-share/service-usage-metrics.md)

Per impostazione predefinita, i dati per utente sono abilitati nelle metriche di utilizzo e le informazioni sull'account del creatore di contenuto sono incluse nel report delle metriche. Se non si desidera raccogliere queste informazioni per tutti gli utenti, è possibile disabilitare la funzionalità per gruppi di sicurezza specificati o per un'intera organizzazione. Le informazioni sugli account degli utenti esclusi verranno quindi visualizzate nel report come *Senza nome*.

## <a name="dashboard-settings"></a>Impostazioni del dashboard

### <a name="data-classification-for-dashboards"></a>Classificazione dati per dashboard

Gli utenti dell'organizzazione possono contrassegnare i dashboard con classificazioni che ne indicano il livello di sicurezza. [Altre informazioni](../create-reports/service-data-classification.md)

> [!NOTE]
> Questa impostazione si applica all'intera organizzazione e non può essere limitata a gruppi specifici.

## <a name="developer-settings"></a>Impostazioni modalità sviluppatore

### <a name="embed-content-in-apps"></a>Incorpora il contenuto nelle app

Gli utenti dell'organizzazione possono incorporare i dashboard e i report di Power BI nelle applicazioni SaaS (Software as a Service). Se si disabilita questa impostazione, si impedisce agli utenti di usare le API REST per incorporare contenuto Power BI nelle loro applicazioni. [Altre informazioni](../developer/embedded/embedding.md)

### <a name="allow-service-principals-to-use-power-bi-apis"></a>Consenti alle entità servizio di usare le API Power BI

Le app Web registrate in Azure Active Directory (Azure AD) useranno un'entità servizio assegnata per accedere alle API Power BI senza un utente connesso. Per consentire a un'app di usare l'autenticazione dell'entità servizio, l'entità servizio deve essere inclusa in un gruppo di sicurezza consentito. [Altre informazioni](../developer/embedded/embed-service-principal.md)

> [!NOTE]
> Le entità servizio ereditano le autorizzazioni per tutte le impostazioni del tenant di Power BI dal relativo gruppo di sicurezza. Per limitare le autorizzazioni, creare un gruppo di sicurezza dedicato per le entità servizio e aggiungerlo all'elenco "Eccetto gruppi di sicurezza specifici" relativo alle impostazioni pertinenti abilitate di Power BI.

## <a name="dataflow-settings"></a>Impostazioni del flusso di dati

### <a name="create-and-use-dataflows"></a>Creare e usare flussi di dati

Gli utenti dell'organizzazione possono creare e usare flussi di dati. Per una panoramica dei flussi di dati, vedere [Preparazione dei dati self-service in Power BI](../transform-model/service-dataflows-overview.md). Per abilitare i flussi di dati in una capacità Premium, vedere [Configurare i carichi di lavoro](service-admin-premium-workloads.md).

> [!NOTE]
> Questa impostazione si applica all'intera organizzazione e non può essere limitata a gruppi specifici.

## <a name="template-apps-settings"></a>Impostazioni app modello

Tre impostazioni controllano la capacità delle app modello di pubblicare o installare app di modello.

![Impostazioni di app modello del portale di amministrazione di Power BI](media/service-admin-portal/power-bi-admin-portal-template-apps.png)

### <a name="publish-template-apps"></a>Pubblica app modello

Gli utenti dell'organizzazione possono creare aree di lavoro per app modello. È possibile controllare gli utenti che possono pubblicare app modello o distribuirle ai client esterni all'organizzazione tramite [AppSource](https://appsource.microsoft.com) o altri metodi di distribuzione.

![Portale di amministrazione di Power BI, impostazione Crea app modello](media/service-admin-portal/power-bi-admin-portal-template-app-settings.png)

### <a name="install-template-apps-listed-on-appsource"></a>Install template apps listed on AppSource (Installa app modello elencate in AppSource)

Gli utenti dell'organizzazione possono scaricare e installare le app modello **solo** da [AppSource](https://appsource.microsoft.com). È possibile controllare gli utenti o gruppi di sicurezza specifici che possono installare le app modello da AppSource.

![Portale di amministrazione di Power BI, impostazioni di installazione app modello](media/service-admin-portal/power-bi-admin-portal-template-app-settings-installer-appsource.png)

### <a name="install-template-apps-not-listed-on-appsource"></a>Installa app modello non elencate in AppSource

È possibile controllare gli utenti dell'organizzazione che possono scaricare e installare le app modello **non elencate in [AppSource](https://appsource.microsoft.com)** .

![Portale di amministrazione di Power BI, impostazioni di installazione app modello](media/service-admin-portal/power-bi-admin-portal-template-app-settings-installer-nonappsource.png)

## <a name="capacity-settings"></a>Impostazioni di capacità

### <a name="power-bi-premium"></a>Power BI Premium

La scheda **Power BI Premium** consente di gestire qualsiasi capacità di Power BI Premium (SKU EM o P) acquistata dall'organizzazione. La scheda **Power BI Premium** è visibile per tutti gli utenti dell'organizzazione, ma il suo contenuto è visibile solo per gli utenti ai quali è stato assegnato il ruolo di *Amministratore delle capacità* o a un utente che abbia autorizzazioni di assegnazione. Per gli utenti che non hanno autorizzazioni viene visualizzato il messaggio seguente.

![Nessun accesso alle impostazioni Premium](media/service-admin-portal/premium-settings-no-access.png)

### <a name="power-bi-embedded"></a>Power BI Embedded

La scheda **Power BI Embedded** consente di visualizzare le capacità di Power BI Embedded (SKU A) acquistate per il cliente. Poiché è possibile acquistare SKU A solo da Azure, [gestire le capacità incorporate in Azure](../developer/embedded/azure-pbie-create-capacity.md) dal **portale di Azure**.

Per altre informazioni su come gestire le impostazioni di Power BI Embedded (SKU) A, vedere [Che cos'è Azure Power BI Embedded](../developer/embedded/azure-pbie-what-is-power-bi-embedded.md).

## <a name="embed-codes"></a>Codici di incorporamento

Un amministratore può visualizzare i codici di incorporamento generati per il tenant per condividere i report pubblicamente. È anche possibile revocare o eliminare i codici. [Altre informazioni](../collaborate-share/service-publish-to-web.md)

![Codici di incorporamento nel portale di amministrazione di Power BI](media/service-admin-portal/embed-codes.png)

 ## <a name=""></a><a name="organizational-visuals">Oggetti visivi dell'organizzazione</a> 

La scheda **Oggetti visivi organizzazione** consente di distribuire e gestire gli oggetti visivi di Power BI all'interno dell'organizzazione. Con gli oggetti visivi dell'organizzazione, è possibile distribuire facilmente gli oggetti visivi proprietari nell'organizzazione, che gli autori dei report possono quindi individuare e importare nei report da Power BI Desktop. [Altre informazioni](../developer/visuals/power-bi-custom-visuals-organization.md)

> [!WARNING]
> Un oggetto visivo personalizzato può contenere codice rischioso a livello di sicurezza o privacy. Verificare che l'autore e l'origine dell'oggetto visivo personalizzato siano attendibili prima di distribuirlo nel repository dell'organizzazione.

La figura mostra tutti gli oggetti visivi di Power BI attualmente distribuiti nel repository di un'organizzazione.

![Oggetti visivi dell'organizzazione](media/service-admin-portal/power-bi-custom-visuals-organizational-admin-01.png)

### <a name="add-a-new-custom-visual"></a>Aggiungere un nuovo oggetto visivo personalizzato

Per aggiungere un nuovo oggetto visivo personalizzato all'elenco, seguire questa procedura. 

1. Nel riquadro di destra selezionare **Aggiungi un oggetto visivo personalizzato**.

    ![Modulo degli oggetti visivi di Power BI](media/service-admin-portal/power-bi-custom-visuals-organizational-admin-02.png)

1. Compilare il modulo **Aggiungi oggetto visivo personalizzato**:

    * **Scegli un file con estensione pbiviz** (obbligatorio): selezionare un file di oggetto visivo personalizzato da caricare. Sono supportati solo oggetti visivi di Power BI basati su API con controllo della versione (vedere qui cosa significa).

    Prima di caricare un oggetto visivo personalizzato è necessario controllarne sicurezza e privacy per assicurarsi che sia conforme agli standard della propria organizzazione.

    * **Assegna un nome all'oggetto visivo personalizzato** (obbligatorio): assegnare un titolo breve all'oggetto visivo in modo gli utenti di Power BI Desktop ne possano comprendere facilmente gli scopi

    * **Icona**: file dell'icona che viene visualizzata nell'interfaccia utente di Power BI Desktop.

    * **Descrizione**: breve descrizione dell'oggetto visivo per fornire più contesto e informazioni utili all'utente

1. Selezionare **Aggiungi** per avviare la richiesta di caricamento. Se ha esito positivo, il nuovo elemento viene visualizzato nell'elenco. In caso di esito negativo, viene visualizzato un messaggio di errore appropriato

### <a name="delete-a-custom-visual-from-the-list"></a>Eliminare un oggetto visivo personalizzato dall'elenco

Per eliminare definitivamente un oggetto visivo, selezionare l'icona del Cestino per l'oggetto visivo nel repository.

> [!IMPORTANT]
> L'eliminazione è irreversibile. Una volta eliminato, viene interrotto immediatamente il rendering dell'oggetto visivo nei report esistenti. Anche se lo stesso oggetto visivo viene caricato nuovamente, non sostituirà quello precedente eliminato. Gli utenti possono tuttavia importare nuovamente il nuovo oggetto visivo e sostituire l'istanza presente nei report.

### <a name="disable-a-custom-visual-in-the-list"></a>Disabilitare un oggetto visivo personalizzato nell'elenco

Per disabilitare l'oggetto visivo dall'archivio dell'organizzazione, selezionare l'icona a forma di ingranaggio. Nella sezione **Accesso** disabilitare l'oggetto visivo personalizzato.

Dopo avere disabilitato l'oggetto visivo, non ne verrà eseguito il rendering nei report esistenti e viene visualizzato il messaggio di errore riportato di seguito.

*Questo oggetto visivo personalizzato non è più disponibile. Per informazioni dettagliate, contattare l'amministratore.*

Tuttavia, gli oggetti visivi con segnalibro continuano a funzionare.

Dopo qualsiasi aggiornamento o modifica dell'amministratore, agli utenti di Power BI Desktop devono riavviare l'applicazione o aggiornare il browser nel servizio Power BI per vedere gli aggiornamenti.

### <a name="update-a-visual"></a>Aggiornare un oggetto visivo

Per aggiornare l'oggetto visivo dall'archivio dell'organizzazione, selezionare l'icona a forma di ingranaggio. Cercare e caricare una nuova versione dell'oggetto visivo.

Assicurarsi che l'ID dell'oggetto visivo rimanga invariato. Il nuovo file sostituisce il file precedente per tutti i report in tutta l'organizzazione. Tuttavia, se esiste la possibilità che la nuova versione dell'oggetto visivo comprometta l'utilizzo o la struttura di dati della versione precedente dell'oggetto visivo, evitare di sostituire la versione precedente. In questo caso, è invece necessario creare una nuova voce per la nuova versione dell'oggetto visivo. Ad esempio, aggiungere un nuovo numero di versione (versione x.x) al titolo del nuovo oggetto visivo presentato. In questo modo risulta chiaro che si tratta dello stesso oggetto visivo solo con un numero di versione aggiornato e che la funzionalità dei report esistenti non verrà compromessa. Assicurarsi anche in questo caso che l'ID dell'oggetto visivo rimanga invariato. Al successivo accesso al repository dell'organizzazione da Power BI Desktop, gli utenti possono importare la nuova versione e viene loro richiesto di sostituire la versione corrente disponibile nei report.

Per altre informazioni, vedere [Domande frequenti sugli oggetti visivi di Power BI dell'organizzazione](../developer/visuals/power-bi-custom-visuals-faq.md#organizational-power-bi-visuals).

## <a name=""></a><a name="dataflowStorage">Archiviazione del flusso di dati (anteprima)</a>

Per impostazione predefinita, i dati usati con Power BI vengono archiviati nello spazio di archiviazione interno fornito da Power BI. Con l'integrazione di flussi di dati e Azure Data Lake Storage Gen2 (ADLS Gen2), è possibile archiviare i flussi di dati nell'account di Azure Data Lake Storage Gen2 della propria organizzazione. Per altre informazioni, vedere [Integrazione di flussi di dati e Azure Data Lake (anteprima)](../transform-model/service-dataflows-azure-data-lake-integration.md).

## <a name="workspaces"></a>Aree di lavoro

Come amministratore, è possibile visualizzare le aree di lavoro esistenti nel tenant. È possibile ordinare e filtrare l'elenco delle aree di lavoro e visualizzare i dettagli per ognuna di esse. Le colonne della tabella corrispondono alle proprietà restituite dall'[API REST di amministrazione di Power BI](/rest/api/power-bi/admin) per le aree di lavoro. Le aree di lavoro personali sono di tipo **PersonalGroup**, le aree di lavoro classiche sono di tipo **Group** e le aree di lavoro della nuova esperienza sono di tipo **Workspace**. Per altre informazioni, vedere [Organizzare il lavoro nelle nuove aree di lavoro](../collaborate-share/service-new-workspaces.md).

Gli amministratori possono anche gestire e recuperare le aree di lavoro, usando il portale di amministrazione o i cmdlet di PowerShell. 

![Elenco delle aree di lavoro](media/service-admin-portal/workspaces-list.png)

Nella scheda **Aree di lavoro** viene visualizzato lo *stato* per ogni area di lavoro. Nella tabella seguente sono disponibili altri dettagli sul significato di tali stati.

|State  |Descrizione  |
|---------|---------|
| Attivo | Una normale area di lavoro. Non indica informazioni sull'utilizzo o il contenuto, ma segnala solo che l'area di lavoro stessa è "normale". |
| Orfana | Un'area di lavoro senza utente amministratore. |
| Eliminata | Un'area di lavoro eliminata. Se si desidera, per un massimo di 90 giorni vengono mantenuti metadati sufficienti per ripristinare l'area di lavoro. |
| Rimozione | È in corso l'eliminazione di un'area di lavoro, ma l'area di lavoro è ancora disponibile. Gli utenti possono eliminare le aree di lavoro personali, attivando lo stato Rimozione e poi Eliminata per gli elementi. |

## <a name="custom-branding"></a>Personalizzazione

In qualità di amministratore è possibile personalizzare l'aspetto di Power BI per l'intera organizzazione. Attualmente sono disponibili tre opzioni principali:

![Opzioni di personalizzazione](media/service-admin-portal/power-bi-custom-branding.png)

* **Caricare il logo**: Per risultati ottimali, caricare un logo salvato come file con estensione png, di dimensioni non superiori a 10 kB e con almeno 200 x 30 pixel.

* **Caricare l'immagine di copertina**: Per risultati ottimali, caricare un'immagine di copertina salvata come file con estensione jpg o png, di dimensioni non superiori a 1 MB e con almeno 1920 x 160 pixel.

* **Selezionare il colore del tema**: È possibile selezionare il tema in base a un codice hex #, RGB, un valore o dal pallet in dotazione.


Per altre informazioni, vedere [Personalizzazione per l'organizzazione](https://aka.ms/orgBranding).

![Elenco delle aree di lavoro](media/service-admin-portal/workspaces-list.png)

## <a name="manage-featured-content"></a>Gestire il contenuto in primo piano

L'amministratore del tenant può gestire tutti i report, i dashboard e le app presentati nella sezione In primo piano nella home page di Power BI per l'intera organizzazione.

- Nel portale di amministrazione selezionare **Contenuto in primo piano**.

Qui viene visualizzata una panoramica degli utenti che hanno inserito il contenuto nella sezione In primo piano, di quando è stato contrassegnato come in primo piano e di tutti i relativi metadati. Se un elemento sembra sospetto o si vuole pulire la sezione In primo piano, è possibile eliminare il contenuto presente in tale sezione in base alle esigenze.

Per informazioni sull'abilitazione del contenuto in primo piano, vedere [Contenuto in primo piano](#featured-content) in questo articolo.

## <a name="next-steps"></a>Passaggi successivi

[Amministrazione di Power BI nell'organizzazione](service-admin-administering-power-bi-in-your-organization.md)  
[Informazioni sul ruolo di amministratore di Power BI](service-admin-role.md)  
[Controllo di Power BI nell'organizzazione](service-admin-auditing.md)  

Altre domande? [Provare a rivolgersi alla community di Power BI](https://community.powerbi.com/)
