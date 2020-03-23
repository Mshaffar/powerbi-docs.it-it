---
title: Parametri URL nei report impaginati - Generatore report di Power BI
description: Questo argomento descrive gli usi comuni per i parametri dei report di Power BI Report Builder, le proprietà che è possibile impostare e molto altro ancora.
ms.service: powerbi
ms.subservice: report-builder
ms.topic: conceptual
author: maggiesMSFT
ms.author: maggies
ms.reviewer: cfinlan
ms.custom: ''
ms.date: 09/10/2019
ms.openlocfilehash: 35df214da19d5f35130408ce8128643f52682428
ms.sourcegitcommit: ced8c9d6c365cab6f63fbe8367fb33e6d827cb97
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/07/2020
ms.locfileid: "78922230"
---
# <a name="url-parameters-in-paginated-reports-in-power-bi"></a>Parametri URL nei report impaginati in Power BI

È possibile inviare comandi ai report impaginati in Power BI aggiungendo un parametro a un URL. È possibile, ad esempio, che il report sia stato visualizzato usando un set specifico di valori dei parametri del report. È possibile incapsulare queste informazioni nell'URL usando i parametri di accesso con URL predefiniti. Si può personalizzare ulteriormente il modo in cui Power BI elabora il report incorporando i parametri per il rendering dei formati o per l'aspetto della barra degli strumenti del report. Questo URL può quindi essere incollato direttamente in un messaggio di posta elettronica o in una pagina Web in modo che altri utenti possano visualizzare il report nello stesso modo nel browser. 

Ecco le azioni che è possibile eseguire tramite i parametri di accesso con URL: 

- Inviare parametri di report a un report. 
- Avviare l'esportazione del contenuto del report in un formato di file supportato. 
- Nascondere o visualizzare il riquadro dei parametri. 
- Specificare l'impostazione DeviceInfo. 

Per l'elenco completo dei comandi e delle impostazioni disponibili tramite l'accesso con URL, vedere  [Informazioni di riferimento per i parametri di accesso con URL](#url-access-parameter-reference) più avanti in questo articolo. 

## <a name="url-access-concepts"></a>Concetti relativi all'accesso con URL 

Le richieste URL per Power BI contengono parametri elaborati dal servizio. Il modo in cui il servizio gestisce le richieste URL dipende dai parametri, dai prefissi di parametro e dai tipi di elementi inclusi nell'URL. La funzionalità dell'URL per i report impaginati è compatibile con la maggior parte dei browser e delle applicazioni che supportano l'indirizzamento URL standard. 

## <a name="url-access-syntax"></a>Sintassi di accesso con URL 

Le richieste URL possono contenere più parametri, elencati in qualsiasi ordine. I parametri sono separati da una e commerciale (&). Le coppie nome/valore sono separate da un segno di uguale (=). ad esempio:

```
powerbiserviceurl?rp:parametervalueh&rdl:parameter=value  
```

## <a name="syntax-description"></a>Descrizione della sintassi 

### <a name="powerbiserviceurl"></a>powerbiserviceurl 

URL del servizio Web del tenant di Power BI. ad esempio: 

**&** Usato per separare le coppie di nome e valore dei parametri di accesso con URL.

**prefisso** Prefisso per il parametro URL (ad esempio, rp: o rdl:) che specifica un'azione nel servizio Power BI. 

> [!NOTE]
> I parametri di report richiedono un prefisso di parametro e fanno distinzione tra maiuscole e minuscole. 

**parameter** Nome del parametro. 

### <a name="value"></a>value 

Testo dell'URL corrispondente al valore del parametro usato. 

Per esempi relativi al passaggio di parametri di report nell'URL, vedere  [Passare un parametro del report in un URL](report-builder-url-pass-parameters.md).

## <a name="url-access-parameter-reference"></a>Informazioni di riferimento sui parametri di accesso con URL

È possibile usare i parametri seguenti come parte di un URL per configurare l'aspetto dei report impaginati in Power BI. I parametri più comuni sono elencati in questa sezione. I parametri non fanno distinzione tra maiuscole e minuscole e iniziano con il prefisso `rdl:` se correlati al formato di output.  

### <a name="report-commands-rdl"></a>Comandi del report (`rdl:`) 

**Formato di esportazione** Specifica il formato per il rendering e l'esportazione di un report. I valori disponibili sono:
 
- PPTX (PowerPoint)
- MHTML 
- IMMAGINE 
- EXCELOPENXML (EXCEL) 
- WORDOPENXML (WORD) 
- CSV 
- PDF 
- XML 

**Informazioni sul dispositivo** Si possono specificare parametri di output aggiuntivi per i formati di esportazione seguenti. 

PDF:

- rdl:AccessiblePDF=true/false
- rdl:Columns=integer
- rdl:ColumnSpacing=decimal(in)
- rdl:DpiX=integer
- rdl:DpiY=integer
- rdl:EndPage=integer
- rdl:HumanReadablePDF=true/false
- rdl:MarginBottom=decimal(in)
- rdl:MarginLeft=decimal(in)
- rdl:MarginRight=decimal(in)
- rdl:MarginTop=decimal(in)
- rdl:PageHeight=decimal(in)
- rdl:PageWidth=decimal(in)
    - rdl:StartPage=integer
    
CSV:

- rdl:Encoding=string
- rdl:ExcelMode=true/false
- rdl:FieldDelimiter=string
- rdl:FileExtension=string
- rdl:NoHeader=true/false
- rdl:Qualifier=string
- rdl:RecordDelimiter=string
- rdl:SuppressLineBreaks=true/false
    - rdl:UseFormattedValues=true/false
    
WORDOPENXML (WORD):

- rdl:AutoFit=string -> True/False/Never/Default
- rdl:ExpandToggles=true/false
- rdl:FixedPageWidth=true/false
- rdl:OmitHyperlinks=true/false
- rdl:OmitDrillthroughs=true/false

EXCELOPENXML (EXCEL):

- rdl:OmitDocumentMap=true/false
- rdl:OmitFormulas=true/false
    - rdl:SimplePageHeaders=true/false
    
PPTX (PowerPoint):
 
- rdl:Columns=integer
- rdl:ColumnSpacing=decimal(in)
- rdl:DpiX=integer
- rdl:DpiY=integer
- rdl:EndPage=integer
- rdl:MarginBottom=decimal(in)
- rdl:MarginLeft=decimal(in)
- rdl:MarginRight=decimal(in)
- rdl:MarginTop=decimal(in)
- rdl:PageHeight=decimal(in)
- rdl:PageWidth=decimal(in)
- rdl:StartPage=integer
    - rdl:UseReportPageSize=true/false

XML:

- rdl:XSLT=string
- rdl:MIMEType=string
- rdl:UseFormattedValues=true/false
- rdl:Indented=true/false
- rdl:OmitNamespace=true/false
- rdl:OmitSchema=true/false
- rdl:Encoding=string
- rdl:FileExtension=string
- rdl:Schema=true/false

## <a name="next-steps"></a>Passaggi successivi

- [Passare un parametro di report in un URL per un report impaginato in Power BI](report-builder-url-pass-parameters.md)
- [Che cosa sono i report impaginati in Power BI Premium?](paginated-reports-report-builder-power-bi.md)