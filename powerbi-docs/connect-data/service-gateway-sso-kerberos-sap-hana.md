---
title: Usare Kerberos per il Single Sign-On (SSO) a SAP HANA
description: Configurare il server SAP HANA per abilitare SSO dal servizio Power BI
author: arthiriyer
ms.author: arthii
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-gateways
ms.topic: conceptual
ms.date: 10/10/2019
LocalizationGroup: Gateways
ms.openlocfilehash: 52a729399b6826ad165ef41469cafd5ce2a1dcd5
ms.sourcegitcommit: 0e9e211082eca7fd939803e0cd9c6b114af2f90a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/13/2020
ms.locfileid: "83283325"
---
# <a name="use-kerberos-for-single-sign-on-sso-to-sap-hana"></a>Usare Kerberos per il Single Sign-On (SSO) a SAP HANA

Questo articolo descrive come configurare l'origine dati SAP HANA per abilitare SSO dal servizio Power BI.

> [!NOTE]
> Prima di provare ad aggiornare un report basato su SAP HANA che usa l'accesso Single Sign-On Kerberos, completare sia i passaggi descritti in questo articolo che quelli descritti in [Configurare l'accesso SSO basato su Kerberos](service-gateway-sso-kerberos.md).

## <a name="enable-sso-for-sap-hana"></a>Abilitare SSO per SAP HANA

Per abilitare SSO per SAP HANA, seguire questa procedura:

1. Verificare che nel server SAP HANA sia in esecuzione la versione minima richiesta. Ciò dipende dal livello della piattaforma del server SAP HANA:
   - [HANA 2 SPS 01 Rev 012.03](https://launchpad.support.sap.com/#/notes/2557386)
   - [HANA 2 SPS 02 Rev 22](https://launchpad.support.sap.com/#/notes/2547324)
   - [HANA 1 SP 12 Rev 122.13](https://launchpad.support.sap.com/#/notes/2528439)

2. Nel computer gateway installare il driver ODBC SAP HANA più recente. La versione minima è la versione ODBC per HANA 2.00.020.00 di agosto 2017.

3. Verificare che il server SAP HANA sia stato configurato per il Single Sign-On basato su Kerberos. Per altre informazioni sulla configurazione della funzionalità SSO per SAP HANA con Kerberos, vedere [Single Sign-on Using Kerberos](https://help.sap.com/viewer/b3ee5778bc2e4a089d3299b82ec762a7/2.0.03/1885fad82df943c2a1974f5da0eed66d.html) (Single Sign-on tramite Kerberos) nella guida alla sicurezza di SAP HANA. Vedere anche i collegamenti in tale pagina, in particolare SAP Note 1837331 - HOWTO HANA DBSSO Kerberos/Active Directory.

È consigliabile eseguire anche questi passaggi aggiuntivi che possono contribuire a migliorare le prestazioni:

1. Nella directory di installazione del gateway trovare e aprire questo file di configurazione: Microsoft.PowerBI.DataMovement.Pipeline.GatewayCore.dll.config.

2. Trovare la proprietà `FullDomainResolutionEnabled` e impostarne il valore su `True`.

    ```xml
    <setting name=" FullDomainResolutionEnabled " serializeAs="String">
          <value>True</value>
    </setting>
    ```

A questo punto, [eseguire un report di Power BI](service-gateway-sso-kerberos.md#run-a-power-bi-report).

## <a name="next-steps"></a>Passaggi successivi

Per altre informazioni sul gateway dati locale e su DirectQuery, vedere le risorse seguenti:

* [Informazioni sul gateway dati locale](/data-integration/gateway/service-gateway-onprem)
* [DirectQuery in Power BI](desktop-directquery-about.md)
* [Data sources supported by DirectQuery](power-bi-data-sources.md) (Origini dati supportate da DirectQuery)
* [DirectQuery e SAP BW](desktop-directquery-sap-bw.md)
* [DirectQuery e SAP HANA](desktop-directquery-sap-hana.md)
