---
title: Filtrare un report in base alla posizione geografica in un'app Power BI per dispositivi mobili
description: Informazioni su come filtrare un report in base alla propria posizione geografica nelle app per dispositivi mobili di Microsoft Power BI, se il proprietario del report configura i tag geografici.
author: paulinbar
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: conceptual
ms.date: 03/11/2020
ms.author: painbar
ms.openlocfilehash: 7ee8887752f6a5161e0046e4aac1711f2ce64922
ms.sourcegitcommit: 0e9e211082eca7fd939803e0cd9c6b114af2f90a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/13/2020
ms.locfileid: "83276215"
---
# <a name="filter-a-report-by-geographic-location-in-the-power-bi-mobile-apps"></a>Filtrare un report in base alla posizione geografica nelle app Power BI per dispositivi mobili
Si applica a:

| ![iPhone](./media/mobile-apps-geographic-filtering/iphone-logo-50-px.png) | ![iPad](./media/mobile-apps-geographic-filtering/ipad-logo-50-px.png) | ![Telefono Android](./media/mobile-apps-geographic-filtering/android-phone-logo-50-px.png) | ![Tablet Android](./media/mobile-apps-view-dashboard/android-tablet-logo-50-px.png) | ![Telefono Windows](./media/mobile-apps-geographic-filtering/win-10-logo-50-px.png) |
|:--- |:--- |:--- |:--- |:--- |
| iPhone |iPad |Telefoni Android |Tablet Android |Telefoni Windows 10 |

Se quando si visualizza un report di Power BI in un dispositivo mobile viene visualizzata un'icona a forma di piccola puntina da disegno nell'angolo superiore destro, sarà possibile filtrare il report in base alla propria posizione geografica.

> [!NOTE]
> È possibile filtrare in base alla località solo se i nomi geografici del report sono in inglese, ad esempio "New York City" o "Germany". I tablet e i PC Windows 10 non supportano i filtri geografici, ma i telefoni Windows 10 sì.

>[!NOTE]
>Il supporto delle app Power BI per dispositivi mobili per i **telefoni con Windows 10 Mobile** non sarà più disponibile dal 16 marzo 2021. [Altre informazioni](https://go.microsoft.com/fwlink/?linkid=2121400)

## <a name="filter-your-report-by-your-geographic-location"></a>Filtrare il report in base alla propria posizione geografica
1. Aprire un report nell'app per dispositivi mobili di Power BI nel dispositivo mobile.
2. Se il report include dati geografici, viene visualizzato un messaggio che chiede di consentire a Power BI di accedere alla posizione. Fare clic su **Consenti** e quindi toccare di nuovo **Consenti**.
3. Toccare la puntina da disegno ![icona a forma di puntina](./media/mobile-apps-geographic-filtering/power-bi-mobile-geo-icon.png). È possibile filtrare per città, provincia o paese/area geografica, in base ai dati contenuti nel report. Il filtro elenca solo le opzioni corrispondenti alla posizione attuale.
   
    ![Filtro puntina da disegno](./media/mobile-apps-geographic-filtering/power-bi-mobile-geo-map-set-filter.png)

## <a name="why-dont-i-see-location-tags-on-a-report"></a>Perché non sono visibili i tag della posizione in un report?
Tutte e tre le condizioni seguenti devono essere soddisfatte per visualizzare i tag della posizione. 

* La persona che ha creato il report in Power BI Desktop deve aver [suddiviso in categorie i dati geografici](../../transform-model/desktop-mobile-geofiltering.md) per almeno una colonna, ad esempio città, stato o paese/area geografica.
* Ci si trova in una delle posizioni per cui esistono dati in tale colonna.
* Si sta usando uno di questi dispositivi mobili:
  * iOS (iPad, iPhone, iPod).
  * Android (telefono, tablet).
  * Telefono Windows 10 (altri dispositivi Windows 10, come i tablet e i PC, non supportano i filtri geografici).

Altre informazioni su come [impostare un filtro geografico](../../transform-model/desktop-mobile-geofiltering.md) in Power BI Desktop.

### <a name="next-steps"></a>Passaggi successivi
* [Connettersi ai dati di Power BI dal mondo reale](mobile-apps-data-in-real-world-context.md) con le app per dispositivi mobili
* [Categorizzazione dei dati in Power BI Desktop](../../transform-model/desktop-data-categorization.md) 
* Domande? [Provare a rivolgersi alla community di Power BI](https://community.powerbi.com/)
