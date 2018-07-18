---
title: Tipps zur Leistungssteigerung-Tabelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac82f7e8-6453-4b4f-8223-3c23d09ca4c6
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2b14c4fe8cbbadb2ccdd6a2f7870a07d2f96a3c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795730"
---
# <a name="tips-for-better-table-performance"></a>Tipps zur Leistungssteigerung-Tabelle
  
**Betrifft**: Outlook 
  
Da viele Tabellenvorgänge zeitaufwendig sein können und es nicht möglich ist, Status anzugeben, ist es hilfreich, die folgenden Techniken zur Verbesserung der Leistung verwenden:
  
- **Stellen Sie [IMAPITable: IUnknown](imapitableiunknown.md) ruft in der richtigen Reihenfolge**
    
   Clients und Dienstanbieter können mit Tabellen in verschiedene Arten arbeiten. Sie können öffnen Sie die Tabelle und die Daten für alle Zeilen mit dem Spalte Standardsatz abruft und Sortierreihenfolge. Alternativ können sie diese Standardansicht der Tabelle ändern, indem die Spalte Set ändern, Ändern der Sortierreihenfolge oder zur Festlegung einer Einschränkung, um die Tabelle zu beschränken. Benutzer, die eine oder mehrere der folgenden Vorgänge ausführen, bevor Sie Daten abrufen möchten, sollten sie in der folgenden Reihenfolge ausführen:
    
    1. Definieren Sie eine Spalte mit [IMAPITable::SetColumns](imapitable-setcolumns.md)festgelegt.
        
    2. Richten Sie eine Einschränkung mit [Methode IMAPITable:: Restrict](imapitable-restrict.md).
        
    3. Definieren Sie eine Sortierreihenfolge mit [SortTable](imapitable-sorttable.md).
    
    Diese Aufgaben in der angegebenen Reihenfolge beschränkt die Anzahl der Zeilen und Spalten, die sortiert werden soll, wodurch die Leistung verbessert.
    
- **Verzögerung für einen Vorgang Wenn möglich mit dem TBL_BATCH-flag**
    
    Festlegen der TBL\_BATCH-Flag für eine Methode kann in der Tabelle Implementierung mehrere Aufrufe vor dem Bearbeiten auf jedem dieser erfassen. Stellen Sie anstelle von potenziell viele Anrufe auf einem Remoteserver. eine Tabelle Implementierer kann, stellen Sie alle Vorgänge gleichzeitig durchführen. Die Ergebnisse der Vorgänge werden nicht ausgewertet, bis sie benötigt werden. 
    
    Beispielsweise wenn ein Client ruft [Methode IMAPITable:: Restrict](imapitable-restrict.md) eine Einschränkung mit der TBL angeben\_BATCH-Kennzeichens, die Einschränkung müssen nicht wirksam, bis der Client [IMAPITable::QueryRows](imapitable-queryrows.md) zum Abrufen der Daten aufruft. Dies kann in der Tabelle-Implementierung die Arbeit in eine zwei Anrufe zu kombinieren. Benutzer, die die TBL nutzen Tabelle\_BATCH Flag sollten beachten Sie, dass unter diesen Umständen Fehlerbehandlung komplexer sein kann. 
    
    Da die Fehlerbehandlung von einer verzögerten Vorgang ähnelt der Fehlerbehandlung ist bei der MAPI\_DEFERRED_ERRORS Flag festgelegt ist, finden Sie weitere Informationen unter [Verzögern MAPI-Fehler](deferring-mapi-errors.md) . 
    
- **Lassen Sie einen Cache der am häufigsten verwendeten Eigenschaften**
    
    Dienstanbieter implementieren Tabellen können die Zeit verringern, die benötigt wird, um eine Ansicht zu erstellen, indem zwischengespeichert werden Kopien der häufig verwendeten Objekteigenschaften. Erstellen einer Kopie der diese Eigenschaften im Arbeitsspeicher speichert, müssen sie jedes Mal aus dem Objekt Abrufen der Ansicht muss neu erstellt werden.
    
## <a name="see-also"></a>Siehe auch

- [MAPI-Tabellen](mapi-tables.md)

