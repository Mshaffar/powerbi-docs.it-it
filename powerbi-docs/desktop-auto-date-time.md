---
title: Data/ora automatica in Power BI Desktop
description: Informazioni sull'opzione di data/ora automatica in Power BI Desktop.
author: peter-myers
ms.reviewer: asaxton
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: conceptual
ms.date: 10/23/2019
ms.author: v-pemyer
ms.openlocfilehash: 7453854376923fbb55376182a8674e5f3d7d1b63
ms.sourcegitcommit: 64c860fcbf2969bf089cec358331a1fc1e0d39a8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/09/2019
ms.locfileid: "73878788"
---
# <a name="auto-datetime-in-power-bi-desktop"></a>Data/ora automatica in Power BI Desktop

Questo articolo è destinato a esperti di modellazione di dati che sviluppano modelli di importazione o compositi in Power BI Desktop.

## <a name="background"></a>Sfondo

_Data/ora automatica_ è un'opzione di caricamento dati disponibile in Power BI Desktop. Questa opzione facilita la creazione di report con funzionalità di Business Intelligence per le gerarchie temporali sulla base delle colonne della data caricate in un modello. In particolare, consente agli autori di report di filtrare, raggruppare ed eseguire il drill-down usando periodo di tempo di calendario senza richiedere all'esperto di modellazione di svilupparli in modo esplicito. I periodi di tempo del calendario includono anni, trimestri, mesi e giorni.

Quando l'opzione è abilitata, Power BI Desktop crea una tabella di data/ora automatica nascosta per ogni colonna della data, purché siano soddisfatte tutte le condizioni seguenti:

- La modalità di archiviazione tabelle è Importa
- Il tipo di dati della colonna è data o data/ora
- La colonna non è il lato "molti" di una relazione del modello

## <a name="how-it-works"></a>Come funziona

Ogni tabella di data/ora automatica è di fatto una [tabella calcolata](desktop-calculated-tables.md) che genera righe di dati tramite la funzione [CALENDAR](/dax/calendar-function-dax) di DAX. Ogni tabella include anche sei colonne calcolate: **Giorno**, **NumMese**, **Mese**, **NumTrimestre**, **Trimestre** e **Anno**.

> [!NOTE]
> I nomi e i valori delle colonne vengono convertiti e formattati in base alla [lingua del modello](supported-languages-countries-regions.md#choose-the-language-for-the-model-in-power-bi-desktop).

Viene inoltre creata una relazione tra la colonna **Data** della tabella di data/ora automatica e la colonna della data del modello.

La tabella di data/ora automatica viene caricata con gli anni di calendario completi che comprendono tutti i valori di data archiviati nella colonna della data del modello. Se, ad esempio, il primo valore in una colonna della data è il 20 marzo 2016 e l'ultimo valore è il 23 ottobre 2019, la tabella conterrà 1.461 righe. Rappresenta una riga per ogni data nei quattro anni di calendario compresi tra il 2016 e il 2019. Se si aggiorna il modello, viene aggiornata anche ogni tabella di data/ora automatica per assicurarsi che contenga sempre le date che includono i valori delle colonne della data.

Se fosse possibile visualizzare le righe di una tabella di data/ora automatica, l'aspetto sarebbe simile al seguente:

![Esempio dell'aspetto delle righe di una tabella di data/ora automatica. Visualizza sette colonne: Data, Giorno, NumMese, Mese, NumTrimestre, Trimestre e Anno. Visualizza 10 righe di dati che indicano le date comprese tra il 1° gennaio 2019 e il 10 gennaio 2019.](media/desktop-auto-date-time/auto-date-time-hidden-table-example-rows.png)

> [!NOTE]
> Le tabelle di data/ora automatica sono nascoste in modo permanente e risultano invisibili anche agli esperti di modellazione. Non sono visibili nel riquadro **Campi** o nel diagramma della visualizzazione modello e le relative righe non sono visibili nella visualizzazione dati. Non è inoltre possibile fare riferimento direttamente alla tabella e alla relativa colonna in espressioni DAX.

La tabella definisce anche una gerarchia, fornendo oggetti visivi con un percorso di drill-down nei livelli anno, trimestre, mese e giorno.

Se fosse possibile visualizzare una tabella di data/ora automatica nel diagramma della visualizzazione modello, l'aspetto sarebbe simile al seguente (le colonne correlate sono evidenziate):

![Esempio dell'aspetto di una tabella di data/ora automatica nascosta. Visualizza due tabelle: Sales e LocalDateTime. Le tabelle sono correlate in base alla colonna OrderDate della tabella Sales e alla colonna Date della tabella LocalDateTime. LocalDateTime definisce sette colonne: Data, Giorno, Mese, NumMese, Trimestre, NumTrimestre, Anno e una singola gerarchia. La gerarchia è denominata Gerarchia data ed è costituita da quattro livelli: Anno, Trimestre, Mese e Giorno.](media/desktop-auto-date-time/auto-date-time-hidden-table-example-diagram.png)

## <a name="work-with-auto-datetime"></a>Usare l'opzione di data/ora automatica

Quando esiste una tabella di data/ora automatica per una colonna della data (e tale colonna è visibile), gli autori del report non troveranno tale colonna come campo nel riquadro **Campi**. Troveranno invece un oggetto espandibile il cui nome è uguale a quello della colonna della data. È possibile identificare facilmente tale oggetto perché è decorato con un'icona di calendario. Quando gli autori del report espandono l'oggetto calendario, troveranno una gerarchia denominata **Gerarchia data**. Dopo aver espanso la gerarchia, troveranno quattro livelli: **Anno**, **Trimestre**, **Mese** e **Giorno**.

![Esempio del riquadro Campi, con la tabella Sales espansa aperta. Contiene un campo OrderDate, decorato con l'icona del calendario. È espansa e aperta e contiene una gerarchia denominata Gerarchia data. Anche tale gerarchia è espansa e contiene quattro livelli: Anno, Trimestre, Mese e Giorno.](media/desktop-auto-date-time/auto-date-time-fields-pane-example.png)

La gerarchia generata di data/ora automatica può essere usata per configurare un oggetto visivo in modo analogo alle normali gerarchie. È possibile configurare gli oggetti visivi usando l'intera gerarchia di **Gerarchia data** o livelli specifici della gerarchia.

È però disponibile una funzionalità aggiunta, non supportata dalle normali gerarchie. Quando si aggiunge la gerarchia di data/ora automatica, o un livello della gerarchia, a un oggetto visivo, l'autore del report può scegliere di usare alternativamente la gerarchia o la colonna della data. Questo approccio è utile per alcuni oggetti visivi, quando è necessario solo la colonna della data e non la gerarchia e i relativi livelli. Per iniziare, configurare il campo dell'oggetto visivo (fare clic con il pulsante destro del mouse sul campo dell'oggetto visivo oppure fare clic sulla freccia verso il basso) e quindi usare il menu di scelta rapida per passare dalla colonna della data a Gerarchia data e viceversa.

![Esempio di configurazione di un campo oggetto visivo per la gerarchia OrderDate. Nel menu di scelta rapida aperto sono visualizzate due opzioni che consentono di usare alternativamente la colonna OrderDate o Gerarchia data.](media/desktop-auto-date-time/auto-date-time-configure-visuals-fields.png)

I calcoli del modello, scritti in DAX, possono infine fare riferimento direttamente a una colonna della data o alle colonne nascoste della tabella di data/ora automatica.

La formula scritta in Power BI Desktop può fare riferimento a una colonna della data nel modo consueto. Per fare riferimento alle colonne della tabella di data/ora automatica, è invece necessario usare una speciale sintassi estesa. Per iniziare, fare riferimento alla colonna della data e quindi aggiungere un punto (.) dopo di essa. La funzionalità di completamento automatico della barra della formula consentirà quindi di selezionare una colonna della tabella di data/ora automatica.

![Esempio di immissione di un'espressione di misura DAX nella barra della formula. La formula finora è Date Count = COUNT(Sales[OrderDate]. e l'elenco di completamento automatico include tutte le sette colonne della tabella di data/ora automatica nascosta. Queste colonne sono: Data, Giorno, Mese, NumMese, Trimestre, NumTrimestre e Anno.](media/desktop-auto-date-time/auto-date-time-dax-auto-complete.png)

In Power BI Desktop un'espressione di misura valida può essere:

```dax
Date Count = COUNT(Sales[OrderDate].[Date])
```

> [!NOTE]
> Anche se questa espressione di misura è valida in Power BI Desktop, non corrisponde alla sintassi DAX corretta. Internamente, Power BI Desktop traspone l'espressione in modo che faccia riferimento all'effettiva colonna della tabella di data/ora automatica, che è nascosta.

## <a name="configure-auto-datetime-option"></a>Configurare l'opzione di data/ora automatica

È possibile configurare la data/ora automatica _a livello globale_ o per il _file corrente_. L'opzione globale si applica ai nuovi file di Power BI Desktop e può essere attivata o disattivata in qualsiasi momento. Per una nuova installazione di Power BI Desktop, entrambe le opzioni sono attivate per impostazione predefinita.

Anche l'opzione relativa al file corrente può essere attivata o disattivata in qualsiasi momento. Quando è attivata, le tabelle di data/ora automatica vengono create. Quando è disattivata, tutte le tabelle di data/ora automatica vengono rimosse dal modello.

> [!CAUTION]
> Prestare attenzione quando si disattiva l'opzione relativa al file corrente, in quanto implica la rimozione delle tabelle di data/ora automatica. Assicurarsi di correggere eventuali filtri di report danneggiati o gli oggetti visivi che sono stati configurati per usarli.

In Power BI Desktop selezionare _File > Opzioni e impostazioni > Opzioni_ e quindi selezionare la pagina **Globale** o **File corrente**. In una delle due pagine l'opzione è disponibile nella sezione **Funzionalità di Business Intelligence per le gerarchie temporali**.

![Configurazione delle opzioni di Power BI Desktop. La pagina Caricamento dati del gruppo GLOBALE è selezionata. Nella sezione Funzionalità di Business Intelligence per le gerarchie temporali l'opzione Data/ora automatica per nuovi file è selezionata.](media/desktop-auto-date-time/auto-date-time-configure-global-options.png)

## <a name="next-steps"></a>Passaggi successivi

Per altre informazioni sull'opzione di data/ora automatica e sugli argomenti correlati, vedere le risorse seguenti:

- [Impostare e usare tabelle data in Power BI Desktop](desktop-date-tables.md)
- Domande? [Provare a rivolgersi alla community di Power BI](https://community.powerbi.com/)