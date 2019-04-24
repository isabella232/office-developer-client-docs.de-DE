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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327797"
---
# <a name="tips-for-better-table-performance"></a>Tipps für eine bessere Tabellenleistung
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Da viele der Tabellenvorgänge zeitaufwändig sein können und es keine Möglichkeit gibt, den Fortschritt anzugeben, empfiehlt es sich, die folgenden Techniken zur Verbesserung der Leistung zu verwenden:
  
- **Make [IMAPITable: IUnknown](imapitableiunknown.md) Calls in der richtigen Reihenfolge**
    
   Clients und Dienstanbieter können mit Tabellen auf verschiedene Arten arbeiten. Sie können die Tabelle öffnen und die Daten für alle Zeilen mit dem standardmäßigen Spaltensatz und der Sortierreihenfolge abrufen. Alternativ können Sie diese Standardansicht der Tabelle ändern, indem Sie den Spaltensatz ändern, die Sortierreihenfolge ändern oder eine Einschränkung einrichten, um den Bereich der Tabelle einzugrenzen. Tabellen Benutzer, die einen oder mehrere dieser Vorgänge vor dem Abrufen von Daten ausführen möchten, sollten diese in der folgenden Reihenfolge ausführen:
    
    1. Definieren Sie einen Spaltensatz mit [IMAPITable::](imapitable-setcolumns.md)SetColumns.
        
    2. Richten Sie eine Einschränkung mit [IMAPITable:: Restrict](imapitable-restrict.md)ein.
        
    3. Definieren Sie eine Sortierreihenfolge mit [IMAPITable:: sortable](imapitable-sorttable.md).
    
    Wenn Sie diese Aufgaben in dieser Reihenfolge durchführen, wird die Anzahl der Zeilen und Spalten begrenzt, die sortiert werden, wodurch die Leistung verbessert wird.
    
- **VerZögern eines Vorgangs mit dem TBL_BATCH-Flag, wenn möglich**
    
    Das Festlegen des\_TBL-Batch-Flags für eine Methode ermöglicht es der Tabellen Implementierung, mehrere Aufrufe zu sammeln, bevor Sie auf eine dieser Methoden reagieren. Statt potenziell viele Aufrufe an einen Remoteserver zu senden; eine Tabellen Implementierung kann eine erstellen, die alle Vorgänge gleichzeitig ausführt. Die Ergebnisse der Vorgänge werden erst ausgewertet, wenn Sie benötigt werden. 
    
    Wenn ein Client beispielsweise [IMAPITable:: Restrict](imapitable-restrict.md) anruft, um eine Einschränkung mit der TBL\_-Batch-flaggruppe anzugeben, muss die Einschränkung erst wirksam werden, wenn der Client [IMAPITable:: QueryRows](imapitable-queryrows.md) zum Abrufen der Daten aufruft. Dies ermöglicht es der Tabellen Implementierung, die Arbeit zweier Aufrufe zu einem zu kombinieren. Tabellen Benutzer, die das TBL\_-Batch-Flag nutzen, sollten beachten, dass die Fehlerbehandlung unter diesen Bedingungen komplexer sein kann. 
    
    Da die Behandlung von Fehlern aus einem verzögerten Vorgang mit dem Behandeln der Fehler vergleichbar ist\_, wenn das MAPI-DEFERRED_ERRORS-Flag festgelegt ist, finden Sie weitere Informationen unter Zurückstellen von [MAPI-Fehlern](deferring-mapi-errors.md) . 
    
- **Speichern eines Caches häufig verwendeter Eigenschaften**
    
    Dienstanbieter, die Tabellen implementieren, können die Zeit zum Erstellen einer Ansicht verringern, indem Sie Kopien der häufig verwendeten Objekteigenschaften Zwischenspeichern. Wenn Sie eine Kopie dieser Eigenschaften im Arbeitsspeicher behalten, müssen Sie jedes Mal aus dem Objekt abgerufen werden, wenn die Ansicht neu erstellt werden muss.
    
## <a name="see-also"></a>Siehe auch

- [MAPI-Tabellen](mapi-tables.md)

