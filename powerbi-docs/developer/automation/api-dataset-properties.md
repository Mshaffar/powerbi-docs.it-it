---
title: Proprietà dei set di dati di Power BI
description: Informazioni sulle proprietà delle API dei set di dati di Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: conceptual
ms.date: 06/08/2018
ms.openlocfilehash: e74e390a5d228cb4a158d422cf0adab48b573cce
ms.sourcegitcommit: 87b7cb4a2e626711b98387edaa5ff72dc26262bb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2020
ms.locfileid: "79079670"
---
# <a name="dataset-properties"></a>Proprietà dei set di dati

La versione 1 corrente dell'API dei set di dati consente la creazione di un solo set di dati con un nome e una raccolta di tabelle. Ogni tabella può avere un nome e una raccolta di colonne. Ogni colonna ha un nome e un tipo di dati. Queste proprietà vengono notevolmente estese, in particolare con il supporto per le misure e le relazioni tra tabelle. L'elenco completo delle proprietà supportate per questa versione è il seguente:

> [!IMPORTANT]
> È possibile accedervi dalla pagina [Datasets Operation Groups](https://docs.microsoft.com/rest/api/power-bi/datasets) (Gruppi di operazioni di set di dati).

## <a name="dataset"></a>Set di dati

Nome  |Tipo  |Descrizione  |Sola lettura  |Obbligatorio
---------|---------|---------|---------|---------
id     |  Guid       | Identificatore univoco a livello di sistema per il set di dati.        | True        | False        
name     | Stringa        | Nome del set di dati definito dall'utente.        | False        | True        
tables     | Table[]        | Raccolta di tabelle.        |  False       | False        
relationships     | Relationship[]        | Raccolta di relazioni tra tabelle.        | False        |  False  
defaultMode     | Stringa        | Determina se il set di dati è sottoposto a push, trasmesso in streaming o entrambi, con valori di "Push" e "Streaming".         | False        |  False

## <a name="table"></a>Tabella

Nome  |Tipo  |Descrizione  |Sola lettura  |Obbligatorio
---------|---------|---------|---------|---------
name     | Stringa        |  Nome della tabella definito dall'utente. Viene inoltre usato come identificatore della tabella.       | False        |  True       
columns     |  column[]       |  Raccolta di colonne.       | False        |  True       
measures     | measure[]        |  Raccolta di misure.       | False        |  False       
isHidden     | Boolean        | Se true, la tabella verrà nascosta dagli strumenti client.        | False        | False        

## <a name="column"></a>Colonna

Nome  |Tipo  |Descrizione  |Sola lettura  |Obbligatorio
---------|---------|---------|---------|---------
name     |  Stringa        | Nome della colonna definito dall'utente.        |  False       | True       
dataType     |  Stringa       |  [Tipi di dati EDM](https://msdn.microsoft.com/library/ee382832.aspx) e restrizioni supportati. Vedere [Restrizioni del tipo di dati](#data-type-restrictions).      |  False       | True        
formatString     | Stringa        | Stringa che descrive come deve essere formattato il valore quando viene visualizzato. Per altre informazioni sulla formattazione delle stringhe, vedere [Contenuto di FORMAT_STRING](https://msdn.microsoft.com/library/ms146084.aspx).      | False        | False        
sortByColumn    | Stringa        |   Nome stringa di una colonna nella stessa tabella da usare per ordinare la colonna corrente.     | False        | False       
dataCategory     | Stringa        |  Valore stringa da usare per la categoria di dati che descrive i dati all'interno della colonna. Alcuni valori comuni includono: Address, City, Continent, Country, Image, ImageUrl, Latitude, Longitude, Organization, Place, PostalCode, StateOrProvince, WebUrl       |  False       | False        
isHidden    |  Boolean       |  Proprietà che indica se la visualizzazione della colonna è nascosta. Il valore predefinito è false.       | False        | False        
summarizeBy     | Stringa        |  Metodo di aggregazione predefinito per la colonna. I valori includono: default, none, sum, min, max, count, average, distinctCount     |  False       | False

## <a name="measure"></a>Misura

Nome  |Tipo  |Descrizione  |Sola lettura  |Obbligatorio
---------|---------|---------|---------|---------
name     | Stringa        |  Nome della misura definito dall'utente.       |  False       | True        
expression     | Stringa        | Espressione DAX valida.        | False        |  True       
formatString     | Stringa        |  Stringa che descrive come deve essere formattato il valore quando viene visualizzato. Per altre informazioni sulla formattazione delle stringhe, vedere [Contenuto di FORMAT_STRING](https://msdn.microsoft.com/library/ms146084.aspx).       | False        | False        
isHidden     | Stringa        |  Se true, la tabella verrà nascosta dagli strumenti client.       |  False       | False       

## <a name="relationship"></a>Relazione

Nome  |Tipo  |Descrizione  |Sola lettura  |Obbligatorio 
---------|---------|---------|---------|---------
name     | Stringa        | Nome della relazione definito dall'utente. Viene inoltre usato come identificatore della relazione.        | False       | True        
crossFilteringBehavior     | Stringa        |    La direzione del filtro della relazione: OneDirection (impostazione predefinita), BothDirections, Automatic       | False        | False        
fromTable     | Stringa        | Nome della tabella di chiave esterna.        | False        | True         
fromColumn    | Stringa        | Nome della colonna di chiave esterna.        | False        | True         
toTable    | Stringa        | Nome della tabella di chiave primaria.        | False        | True         
toColumn     | Stringa        | Nome della colonna di chiave primaria.        | False        | True        

## <a name="data-type-restrictions"></a>Restrizioni del tipo di dati

Queste restrizioni si applicano alla proprietà dataType.

Tipo di dati  |Restrizioni  
---------|---------
Int64     |   Int64.MaxValue e Int64.MinValue non sono consentiti.      
Double     |  Double.MaxValue e Double.MinValue non sono consentiti. NaN non supportato. +Infinity e -Infinity non supportati in alcune funzioni, ad esempio Min, Max.       
Boolean     |   True o False.
DateTime    |   Durante il caricamento dei dati, i valori vengono quantizzati con frazioni giornaliere fino a multipli interi di 1/300 secondi (3,33 ms).      
Stringa     |  Attualmente consente fino a 4000 caratteri per valore di stringa.
Decimal|precisione=28, scalabilità=4

## <a name="example"></a>Esempio
L'esempio di codice seguente include alcune di queste proprietà:

```json
{

  "name": "PushAdvanced",

  "tables": [

    {

      "name": "Date",

      "columns": [

        {

          "name": "Date",

          "dataType": "dateTime",

          "formatString": "dddd\\, mmmm d\\, yyyy",

          "summarizeBy": "none"

        }

      ]

    },

    {

      "name": "sales",

      "columns": [

        {

          "name": "Date",

          "dataType": "dateTime",

          "formatString": "dddd\\, mmmm d\\, yyyy",

          "summarizeBy": "none"

        },

        {

          "name": "Sales",

          "dataType": "int64",

          "formatString": "0",

          "summarizeBy": "sum"

        }

      ],

      "measures": [

        {

          "name": "percent to forecast",

          "expression": "SUM(sales[Sales])/SUM(forecast[forecast])",

          "formatString": "0.00 %;-0.00 %;0.00 %"

        }

      ]

    },

    {

      "name": "forecast",

      "columns": [

        {

          "name": "date",

          "dataType": "dateTime",

          "formatString": "m/d/yyyy",

          "summarizeBy": "none"

        },

        {

          "name": "forecast",

          "dataType": "int64",

          "formatString": "0",

          "summarizeBy": "sum"

        }

      ]

    }

  ],

  "relationships": [

    {

      "name": "2ea345ce-b147-436e-8ac2-9d3c4d82af8d",

      "fromTable": "sales",

      "fromColumn": "Date",

      "toTable": "Date",

      "toColumn": "Date",

      "crossFilteringBehavior": "bothDirections"

    },

    {

      "name": "5d95f419-e589-4345-9581-6e70670b1bba",

      "fromTable": "forecast",

      "fromColumn": "date",

      "toTable": "Date",

      "toColumn": "Date",

      "crossFilteringBehavior": "bothDirections"

    }

  ]

}
```