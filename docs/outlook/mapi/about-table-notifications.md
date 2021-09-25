---
title: Informationen zu Tabellenbenachrichtigungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 00c9c6c2-fc21-4b9c-91fa-629450a22d37
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b950f013451dbe7e716cdffa3303ccc6bfb23976
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572207"
---
# <a name="about-table-notifications"></a>Informationen zu Tabellenbenachrichtigungen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clients verlassen sich häufig auf Tabellenbenachrichtigungen, um Änderungen an Objekten zu erfahren, anstatt sich für den Empfang von Benachrichtigungen direkt von den Objekten zu registrieren. Typische Änderungen, die dazu führen, dass Benachrichtigungen gesendet werden, umfassen das Hinzufügen, Löschen oder Ändern einer Zeile und alle kritischen Fehler. Beim Eintreffen von Benachrichtigungen können Clients ermitteln, ob ein weiterer Aufruf zum erneuten Laden der Tabelle ausgeführt werden soll. 
  
Da Tabellenbenachrichtigungen asynchron sind, gibt es einige Probleme, die die Behandlung von Benachrichtigungen unproblematisch machen können:
  
- Die in der [TABLE_NOTIFICATION](table_notification.md) Struktur übergebenen Daten stellen möglicherweise nicht den aktuellen Status der Tabelle dar. Beispielsweise kann ein Client eine Änderung an einer Nachricht vornehmen und dann entscheiden, sie zu löschen. Der Nachrichtenspeicheranbieter, der das Inhaltsverzeichnis implementiert, in dem die Nachricht enthalten war, sendet zwei Benachrichtigungen: ein TABLE_ROW_MODIFIED Ereignis gefolgt von einem TABLE_ROW_DELETED Ereignis. Je nachdem, wie der Nachrichtenspeicheranbieter Benachrichtigungen abgibt, erhält der Client möglicherweise die TABLE_ROW_MODIFIED Benachrichtigung nach dem Löschen der Zeile. 
    
- Der in einer Benachrichtigung enthaltene Spaltensatz unterscheidet sich möglicherweise vom aktuellen Spaltensatz der Tabelle. MapI erfordert, dass der Benachrichtigungsspaltensatz mit dem Spaltensatz übereinstimmt, der zum Zeitpunkt der Benachrichtigungsgenerierung wirksam war. Da es für einen Client möglich ist, [IMAPITable::SetColumns](imapitable-setcolumns.md) aufzurufen, um den Spaltensatz jederzeit – auch nach einer Benachrichtigung – zu ändern, werden die beiden Spaltensätze möglicherweise nicht synchronisiert. 
    
- Tabellenbenachrichtigungen werden nur für Zeilen gesendet, die Teil der Ansicht sind. Das heißt, wenn eine Zeile aufgrund einer Einschränkung aus der Ansicht ausgeschlossen wird oder sich die Tabelle in einem reduzierten Zustand befindet, wird keine Benachrichtigung gesendet, wenn sich diese Zeile ändert. Außerdem werden keine Benachrichtigungen gesendet, um einen Client über eine Änderung des Kategoriestatus zu informieren.
    
Clients sollten beachten, dass nicht alle Tabellen die TABLE_SORT_DONE Benachrichtigung unterstützen, und sie sollten darauf vorbereitet sein, diese Bedingung wie folgt zu behandeln:
  
1. Erzwingen, dass die Sortierung synchron ist.
    
2. Neuladen der Zeilen der Tabelle, wenn [IMAPITable::SortTable](imapitable-sorttable.md) zurückgegeben wird. 
    
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

