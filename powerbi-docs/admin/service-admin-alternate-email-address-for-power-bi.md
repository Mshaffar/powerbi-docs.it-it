---
title: Usare un indirizzo di posta elettronica alternativo
description: Usare un indirizzo di posta elettronica alternativo
author: kfollis
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 04/23/2019
ms.author: kfollis
LocalizationGroup: Troubleshooting
ms.openlocfilehash: 6c6bbf8476087532fd3a049a0e4bde3191892325
ms.sourcegitcommit: a72567f26c1653c25f7730fab6210cd011343707
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/19/2020
ms.locfileid: "83564054"
---
# <a name="use-an-alternate-email-address"></a>Usare un indirizzo di posta elettronica alternativo

Quando si effettua l'iscrizione per Power BI, si specifica un indirizzo di posta elettronica. Per impostazione predefinita, Power BI usa questo indirizzo per inviare aggiornamenti sull'attività nel servizio, ad esempio per inviare gli inviti di condivisione.

In alcuni casi, potrebbe essere necessario recapitare questi messaggi a un indirizzo di posta elettronica diverso da quello con cui è stata effettuata l'iscrizione. Questo articolo illustra come specificare un indirizzo alternativo in Microsoft 365 e in PowerShell. L'articolo spiega anche come Azure Active Directory (Azure AD) risolve un indirizzo di posta elettronica.

> [!NOTE]
> Specificare un indirizzo alternativo, non influisce sull'indirizzo di posta elettronica usato da Power BI per aggiornamenti del servizio, newsletter e altre comunicazioni promozionali. Queste comunicazioni vengono inviate sempre all'indirizzo di posta elettronica usato per l'iscrizione a Power BI.

## <a name="use-microsoft-365"></a>Usare Microsoft 365

Per specificare un indirizzo alternativo in Microsoft 365, seguire questa procedura.

1. Aprire la pagina [Info personali](https://portal.office.com/account/#personalinfo) dell'account. Se l'app lo richiede, accedere con l'indirizzo di posta elettronica e la password usati per Power BI.

1. Nel menu di sinistra selezionare **Info personali**.

1. Nella sezione **Dettagli contatto** selezionare **Modifica**.

    Se non è possibile modificare i dettagli, significa che l'indirizzo di posta elettronica dell'utente è gestito dall'amministratore. Contattare l'amministratore per aggiornare l'indirizzo di posta elettronica.

    ![Dettagli contatto](media/service-admin-alternate-email-address-for-power-bi/contact-details.png)

1. Nel campo **Indirizzo di posta elettronica alternativo** immettere l'indirizzo di posta elettronica da usare in Microsoft 365 per gli aggiornamenti di Power BI.

## <a name="use-powershell"></a>Usare PowerShell

Per specificare un indirizzo alternativo in PowerShell, usare il comando [Set-AzureADUser](/powershell/module/azuread/set-azureaduser/).

```powershell
Set-AzureADUser -ObjectId john@contoso.com -OtherMails "otheremail@somedomain.com"
```

## <a name="email-address-resolution-in-azure-ad"></a>Risoluzione degli indirizzi di posta elettronica in Azure AD

Per acquisire un token di incorporamento di Azure AD per Power BI è possibile usare tre tipi diversi di indirizzo di posta elettronica:

* L'indirizzo di posta elettronica principale associato all'account Azure AD di un utente

* L'indirizzo di posta elettronica UPN (UserPrincipalName)

* L'attributo della matrice dell'*altro indirizzo di posta*

Power BI seleziona l'indirizzo di posta elettronica da usare in base alla sequenza seguente:

1. Se l'attributo relativo alla posta elettronica è presente nell'oggetto utente di Azure AD, Power BI usa questo attributo per l'indirizzo di posta elettronica.

1. Se l'indirizzo di posta elettronica UPN *non* è un indirizzo di posta elettronica di un dominio **\*.onmicrosoft.com** (l'informazione dopo il simbolo "\@"), Power BI usa questo attributo per l'indirizzo di posta elettronica.

1. Se l'attributo della matrice dell'*altro indirizzo di posta elettronica* è presente nell'oggetto utente di Azure AD, Power BI usa il primo indirizzo di posta elettronica in questo elenco, perché questo attributo può contenere un elenco di indirizzi di posta elettronica.

1. Se non è presente nessuna delle condizioni precedenti viene usato l'indirizzo UPN.

Altre domande? [Provare la community di Power BI](https://community.powerbi.com/)