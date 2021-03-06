---
title: Visualizzare report e indicatori KPI locali nelle app per dispositivi mobili di Power BI
description: L'app Power BI per dispositivi mobili consente di accedere in tempo reale a informazioni aziendali in locale usando dispositivi mobili abilitati per il tocco in SQL Server Reporting Services e nel server di report di Power BI.
author: paulinbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: conceptual
ms.date: 12/05/2019
ms.author: painbar
ms.openlocfilehash: 387f0cd4ecea59fd55af0a9eceff2272ddd8097b
ms.sourcegitcommit: 0e9e211082eca7fd939803e0cd9c6b114af2f90a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/13/2020
ms.locfileid: "83278860"
---
# <a name="view-on-premises-report-server-reports-and-kpis-in-the-power-bi-mobile-apps"></a>Visualizzare report e indicatori KPI locali dei server di report nelle app Power BI per dispositivi mobili

L'app Power BI per dispositivi mobili consente di accedere in tempo reale a informazioni aziendali in locale usando dispositivi mobili abilitati per il tocco nel server di report di Power BI e in SQL Server 2016 Reporting Services (SSRS).

Si applica a:

| ![iPhone](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/iphone-logo-50-px.png) | ![iPad](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/ipad-logo-50-px.png) | ![Telefono Android](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/android-phone-logo-50-px.png) | ![Tablet Android](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/android-tablet-logo-50-px.png) |
|:--- |:--- |:--- |:--- |
| iPhone |iPad |Telefoni Android |Tablet Android |


![Home page del server di report nelle app per dispositivi mobili](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-ipad-pbi-report-server-home.png)

## <a name="first-things-first"></a>Operazioni preliminari
**Le app per dispositivi mobili in cui visualizzare il contenuto di Power BI, non in cui crearlo.**

* Tutti gli autori di contenuti nell'organizzazione [creano report di Power BI con Power BI Desktop, quindi li pubblicano nel portale Web del server di report di Power BI](../../report-server/quickstart-create-powerbi-report.md). 
* È possibile creare [indicatori KPI nel portale Web](https://docs.microsoft.com/sql/reporting-services/working-with-kpis-in-reporting-services), organizzarli in cartelle e contrassegnare i Preferiti, per poterli trovare facilmente. 
* [Creare report per dispositivi mobili di Reporting Services](https://docs.microsoft.com/sql/reporting-services/mobile-reports/create-mobile-reports-with-sql-server-mobile-report-publisher) con SQL Server 2016 Enterprise Edition Mobile Report Publisher e pubblicarli nel [portale Web di Reporting Services](https://docs.microsoft.com/sql/reporting-services/web-portal-ssrs-native-mode).  

Quindi, nell'app Power BI per dispositivi mobili, connettersi a un massimo di cinque server di report per visualizzare i report e gli indicatori KPI di Power BI, organizzati in cartelle o raccolti come Preferiti. 

## <a name="explore-samples-in-the-mobile-apps-without-a-server-connection"></a>Esplorare gli esempi nelle app per dispositivi mobili senza una connessione al server
Anche se non si ha accesso a un portale Web di Reporting Services, è comunque possibile esplorare le funzionalità dei report per dispositivi mobili e agli indicatori KPI di Reporting Services. 

1. Toccare l'immagine del profilo nell'angolo in alto a sinistra e quindi toccare **impostazioni** nel pannello degli account visualizzato.

2. Nella pagina Impostazioni toccare **Esempi per Reporting Services** e quindi esplorare per interagire con gli indicatori KPI e i report per dispositivi mobili di esempio.
   
   ![Esempi di Reporting Services](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-iphone-ssrs-samples.png)

## <a name="connect-to-an-on-premises-report-server"></a>Connettersi a un server di report locale
È possibile visualizzare report di Power BI locali, report per dispositivi mobili di Reporting Services e indicatori KPI nelle app Power BI per dispositivi mobili. 

1. Nel dispositivo mobile aprire l'app Power BI.
2. Se non è ancora stato effettuato l'accesso a Power BI, toccare **Server di report**.
   
   ![Accedere a un server di report](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-connect-to-rs-login.png)
   
   Se è già stato eseguito l'accesso all'app Power BI, toccare l'immagine del profilo nell'angolo in alto a sinistra e quindi toccare **impostazioni** nel pannello degli account visualizzato.
3. Nella pagina Impostazioni toccare **Connetti al server**.
   
    ![Connetti al server](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-android-server-sign-in.png)

    L'app per dispositivi mobili deve accedere al server in qualche modo. Sono disponibili alcune modalità:
     * L'uso della stessa rete o della stessa VPN è la modalità più semplice.
     * È possibile usare un proxy applicazione Web per connettersi dall'esterno dell'organizzazione. Per informazioni dettagliate, vedere [Uso di OAuth per connettersi a Reporting Services](mobile-oauth-ssrs.md).
     * Aprire una connessione (porta) nel firewall.

4. Immettere l'indirizzo del server e assegnare al server un nome descrittivo, se si vuole. Usare questo formato per l'indirizzo del server:
   
     `https://<servername>/reports`
   
     OR
   
     `https://<servername>/reports`
   
   Includere **http** o **https** davanti alla stringa di connessione.
   
    ![Finestra di dialogo Connetti al server](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-ios-connect-to-server-dialog.png)
5. Dopo aver digitato l'indirizzo del server e il nome descrittivo facoltativo, toccare **Connetti** e quindi immettere il nome utente e la password quando richiesto.
6. Il nome del server è ora visualizzato nel riquadro Account (in questo esempio è "Work server").
   
   ![Server di report nel riquadro di spostamento](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-iphone-left-nav-report-server.png)

## <a name="connect-to-an-on-premises-report-server-in-ios-or-android"></a>Connettersi a un server di report locale in iOS o Android

Se si sta visualizzando Power BI nell'app per dispositivi mobili iOS o Android, l'amministratore IT potrebbe aver definito un criterio di configurazione dell'app. In tal caso, l'esperienza di connessione al server di report risulta semplificata e non sarà necessario specificare molte informazioni quando ci si connette a un server di report. 

1. Viene visualizzato un messaggio che informa che l'app per dispositivi mobili è configurata con un server di report. Toccare **Accedi**.

    ![Accedere al server di report](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-config-server-sign-in.png)

2.  Nella pagina **Connetti al server** il server di report è già compilato. Toccare **Connetti**.

    ![Dettagli del server di report compilati](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-ios-remote-configure-connect-server.png)

3. Digitare una password per l'autenticazione e quindi toccare **Accedi**. 

    ![Dettagli del server di report compilati](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-config-server-address.png)

È ora possibile visualizzare e interagire con gli indicatori KPI e i report di Power BI archiviati nel server di report.

## <a name="view-power-bi-reports-and-kpis-in-the-power-bi-app"></a>Visualizzare report e indicatori KPI di Power BI nell'app Power BI
I report di Power BI, i report per dispositivi mobili di Reporting Services e gli indicatori KPI vengono visualizzati nelle stesse cartelle in cui si trovano nel portale Web di Reporting Services. 

* Toccare un report di Power BI ![Icona del report di Power BI](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-rs-mobile-report-icon.png). per aprirlo in modalità orizzontale e interagire con esso nell'app Power BI.

    > [!NOTE]
  > Attualmente l'esecuzione di drill-down e drill-up non è abilitata nei report di Power BI in un Server di report di Power BI.
  
    ![Report di Power BI](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-iphone-report-server-report.png)
* In Power BI Desktop, i proprietario dei report possono [ottimizzare un report](../../create-reports/desktop-create-phone-report.md) per le app Power BI per dispositivi mobili. Sul telefono cellulare, i report ottimizzati hanno un layout e un'icona speciale, ![Icona del report ottimizzato di Power BI](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-rs-mobile-optimized-icon.png).
  
    ![Report ottimizzato di Power BI per dispositivi mobili](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-rs-mobile-optimized-report.png)
* Toccare un indicatore KPI per visualizzarlo in modalità messa a fuoco.
  
    ![Indicatore KPI in modalità messa a fuoco](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/pbi_ipad_ssmrp_tile.png)

## <a name="view-your-favorite-kpis-and-reports"></a>Visualizzare i report e gli indicatori KPI preferiti
È possibile contrassegnare gli indicatori KPI e i report come preferiti nel portale Web e quindi visualizzarli in un'unica cartella nel dispositivo mobile, assieme ai dashboard di Power BI preferiti.

* Toccare **Preferiti** sulla barra di spostamento.
  
   ![Preferiti nel riquadro di spostamento](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-ipad-faves-pbi-report-server-update.png)
  
   Gli indicatori KPI e i report preferiti dal portale Web si trovano tutti in questa pagina, assieme ai dashboard di Power BI nel servizio Power BI:
  
   ![Report e dashboard di Power BI nella pagina Preferiti](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-ipad-favorites.png)

## <a name="remove-a-connection-to-a-report-server"></a>Rimuovere una connessione a un server di report
1. Aprire il riquadro Account e toccare **Impostazioni**.
2. Toccare il nome del server a cui non si vuole essere connessi.
3. Toccare **Rimuovi server**.

## <a name="next-steps"></a>Passaggi successivi
* [Che cos'è Power BI?](../../fundamentals/power-bi-overview.md)  
* Domande? [Provare a rivolgersi alla community di Power BI](https://community.powerbi.com/)
