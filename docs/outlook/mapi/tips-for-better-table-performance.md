---
title: Tipps für eine bessere Tabellenleistung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ac82f7e8-6453-4b4f-8223-3c23d09ca4c6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 74ab2cfde01d1aeabee3567b556ece6325ccd003
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590919"
---
# <a name="tips-for-better-table-performance"></a>Tipps für eine bessere Tabellenleistung
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Da viele der Tabellenvorgänge zeitaufwändig sein können und es keine Möglichkeit gibt, den Fortschritt anzugeben, ist es hilfreich, die folgenden Techniken zur Verbesserung der Leistung zu verwenden:
  
- **[IMAPITable ausführen: IUnknown-Aufrufe](imapitableiunknown.md) in der richtigen Reihenfolge**
    
   Clients und Dienstanbieter können auf unterschiedliche Weise mit Tabellen arbeiten. Sie können die Tabelle öffnen und die Daten für alle Zeilen mithilfe des Standardspaltensatzes und der Sortierreihenfolge abrufen. Alternativ können sie diese Standardansicht der Tabelle ändern, indem sie den Spaltensatz ändern, die Sortierreihenfolge ändern oder eine Einschränkung einrichten, um den Bereich der Tabelle einzugrenzen. Tabellenbenutzer, die vor dem Abrufen von Daten einen oder mehrere dieser Vorgänge ausführen möchten, sollten diese in der folgenden Reihenfolge ausführen:
    
    1. Definieren sie einen Spaltensatz mit [IMAPITable::SetColumns](imapitable-setcolumns.md).
        
    2. Einrichten einer Einschränkung mit [IMAPITable::Restrict](imapitable-restrict.md).
        
    3. Definieren Sie eine Sortierreihenfolge mit [IMAPITable::SortTable](imapitable-sorttable.md).
    
    Wenn Sie diese Aufgaben in dieser Reihenfolge ausführen, wird die Anzahl der Zeilen und Spalten, die sortiert werden, begrenzt, wodurch die Leistung verbessert wird.
    
- **Verzögern eines Vorgangs mithilfe der TBL_BATCH-Kennzeichnung, wenn möglich**
    
    Das Festlegen des \_ TBL-BATCH-Flags für eine Methode ermöglicht es dem Tabellen implementer, mehrere Aufrufe zu erfassen, bevor er auf einen dieser Aufrufe angewendet wird. Anstatt potenziell viele Anrufe an einen Remoteserver zu tätigen; Ein Tabellen-Implementierer kann eine Tabelle erstellen und alle Vorgänge gleichzeitig ausführen. Die Ergebnisse der Vorgänge werden erst ausgewertet, wenn sie benötigt werden. 
    
    Wenn ein Client beispielsweise [IMAPITable::Restrict](imapitable-restrict.md) aufruft, um eine Einschränkung mit dem \_ TBL BATCH-Flag anzugeben, muss die Einschränkung erst wirksam werden, wenn der Client [IMAPITable::QueryRows aufruft,](imapitable-queryrows.md) um die Daten abzurufen. Auf diese Weise kann der Tabellen implementer die Arbeit von zwei Aufrufen in einem kombinieren. Tabellenbenutzer, die das TBL \_ BATCH-Flag nutzen, sollten beachten, dass die Fehlerbehandlung unter diesen Bedingungen komplexer sein kann. 
    
    Da die Behandlung der Fehler bei einem verzögerten Vorgang der Behandlung der Fehler ähnelt, wenn das \_ MAPI-DEFERRED_ERRORS-Kennzeichen festgelegt ist, finden Sie unter ["Zurückstellen von MAPI-Fehlern"](deferring-mapi-errors.md) weitere Informationen. 
    
- **Beibehalten eines Caches häufig verwendeter Eigenschaften**
    
    Dienstanbieter, die Tabellen implementieren, können die Zeit zum Erstellen einer Ansicht verkürzen, indem Kopien häufig verwendeter Objekteigenschaften zwischengespeichert werden. Wenn Sie eine Kopie dieser Eigenschaften im Arbeitsspeicher speichern, müssen sie jedes Mal aus dem Objekt abgerufen werden, wenn die Ansicht neu erstellt werden muss.
    
## <a name="see-also"></a>Siehe auch

- [MAPI-Tabellen](mapi-tables.md)

