---
title: Tipps für eine bessere Tabellenleistung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac82f7e8-6453-4b4f-8223-3c23d09ca4c6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 82be33090a63f24c430007d9759045c365961f5d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412513"
---
# <a name="tips-for-better-table-performance"></a>Tipps für eine bessere Tabellenleistung
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Da viele Tabellenvorgänge zeitaufwändig sein können und keine Möglichkeit zum Angeben des Fortschritts besteht, ist es hilfreich, die folgenden Techniken zur Verbesserung der Leistung zu verwenden:
  
- **[ImAPITable erstellen: IUnknown-Aufrufe](imapitableiunknown.md) in der richtigen Reihenfolge**
    
   Clients und Dienstanbieter können auf unterschiedliche Weise mit Tabellen arbeiten. Sie können die Tabelle öffnen und die Daten für alle Zeilen mithilfe der Standardspaltensatz- und Sortierreihenfolge abrufen. Alternativ können sie diese Standardansicht der Tabelle ändern, indem sie den Spaltensatz ändern, die Sortierreihenfolge ändern oder eine Einschränkung festlegen, um den Bereich der Tabelle zu einentwickeln. Tabellenbenutzer, die einen oder mehrere dieser Vorgänge vor dem Abrufen von Daten ausführen möchten, sollten diese in der folgenden Reihenfolge ausführen:
    
    1. Definieren sie einen Spaltensatz mit [IMAPITable::SetColumns](imapitable-setcolumns.md).
        
    2. Richten Sie eine Einschränkung mit [IMAPITable::Restrict ein.](imapitable-restrict.md)
        
    3. Definieren Einer Sortierreihenfolge mit [IMAPITable::SortTable](imapitable-sorttable.md).
    
    Wenn Sie diese Aufgaben in dieser Reihenfolge ausführen, wird die Anzahl der Zeilen und Spalten begrenzt, die sortiert werden, wodurch die Leistung verbessert wird.
    
- **Verzögern eines Vorgangs mithilfe des TBL_BATCH, wenn möglich**
    
    Durch Festlegen des TBL BATCH-Kennzeichens für eine Methode kann der Tabellen implementier mehrere Aufrufe sammeln, bevor er auf einen \_ dieser Aufrufe einwirken kann. Statt potenziell viele Aufrufe an einen Remoteserver zu senden; Ein Tabellen implementier kann eins erstellen und alle Vorgänge gleichzeitig ausführen. Die Ergebnisse der Vorgänge werden erst ausgewertet, wenn sie benötigt werden. 
    
    Wenn ein Client beispielsweise [IMAPITable::Restrict](imapitable-restrict.md) aufruft, um eine Einschränkung mit dem TBL BATCH-Flagsatz anzugeben, muss die Einschränkung erst wirksam werden, wenn der Client \_ [IMAPITable::QueryRows](imapitable-queryrows.md) aufruft, um die Daten abzurufen. Auf diese Weise kann der Tabellen implementier die Arbeit von zwei Aufrufen in einem kombinieren. Tabellenbenutzer, die das TBL BATCH-Flag nutzen, sollten beachten, dass die Fehlerbehandlung unter diesen Bedingungen \_ komplexer sein kann. 
    
    Da die Behandlung der Fehler eines verzögerten Vorgangs der Behandlung der Fehler ähnelt, wenn das MAPI-DEFERRED_ERRORS festgelegt ist, finden Sie weitere Informationen unter \_ [Deferring MAPI Errors.](deferring-mapi-errors.md) 
    
- **Speichern eines Caches häufig verwendeter Eigenschaften**
    
    Dienstanbieter, die Tabellen implementieren, können die Zeit zum Erstellen einer Ansicht durch Zwischenspeichern von Kopien häufig verwendeter Objekteigenschaften mindern. Wenn Sie eine Kopie dieser Eigenschaften im Arbeitsspeicher speichern, müssen sie jedes Mal aus dem Objekt abgerufen werden, wenn die Ansicht neu erstellt werden muss.
    
## <a name="see-also"></a>Siehe auch

- [MAPI-Tabellen](mapi-tables.md)

