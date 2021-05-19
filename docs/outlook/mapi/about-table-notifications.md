---
title: Informationen zu Tabellenbenachrichtigungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00c9c6c2-fc21-4b9c-91fa-629450a22d37
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9a42ed1e196e8ac498ab5889b4419ff407db4748
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417952"
---
# <a name="about-table-notifications"></a>Informationen zu Tabellenbenachrichtigungen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clients verlassen sich häufig auf Tabellenbenachrichtigungen, um Änderungen an Objekten zu erfahren, anstatt sich für den direkten Empfang von Benachrichtigungen von den Objekten zu registrieren. Typische Änderungen, die dazu führen, dass Benachrichtigungen gesendet werden, umfassen das Hinzu-, Löschen oder Ändern einer Zeile sowie alle kritischen Fehler. Wenn Benachrichtigungen eintreffen, können Clients bestimmen, ob sie einen weiteren Aufruf zum Erneutladen der Tabelle senden möchten. 
  
Da Tabellenbenachrichtigungen asynchron sind, gibt es einige Probleme, die die Behandlung von Benachrichtigungen weniger einfach machen können:
  
- Die in der TABLE_NOTIFICATION [übergebenen](table_notification.md) Daten stellen möglicherweise nicht den aktuellen Zustand der Tabelle dar. Ein Client kann z. B. eine Änderung an einer Nachricht vor sich nehmen und dann entscheiden, sie zu löschen. Der Nachrichtenspeicheranbieter, der die Inhaltstabelle, in der die Nachricht enthalten ist, implementieren, sendet zwei Benachrichtigungen: ein TABLE_ROW_MODIFIED-Ereignis gefolgt von einem TABLE_ROW_DELETED Ereignis. Je nachdem, wie der Nachrichtenspeicheranbieter Benachrichtigungen einbekommt, erhält der Client die TABLE_ROW_MODIFIED nach dem Löschen der Zeile. 
    
- Der Spaltensatz, der in einer Benachrichtigung enthalten ist, kann sich vom aktuellen Spaltensatz der Tabelle unterscheiden. MAPI erfordert, dass der Benachrichtigungsspaltensatz mit dem Spaltensatz übereinstimmen, der zum Zeitpunkt der Benachrichtigung generiert wurde. Da ein Client [IMAPITable::SetColumns](imapitable-setcolumns.md) aufrufen kann, um den Spaltensatz jederzeit zu ändern , auch nach einer Benachrichtigung, werden die beiden Spaltensätze möglicherweise nicht synchronisiert. 
    
- Tabellenbenachrichtigungen werden nur für Zeilen gesendet, die Teil der Ansicht sind. Das heißt, wenn eine Zeile aufgrund einer Einschränkung aus der Ansicht ausgeschlossen wird oder sich die Tabelle in einem reduzierten Zustand befindet, wird keine Benachrichtigung gesendet, wenn diese Zeile geändert wird. Außerdem werden keine Benachrichtigungen gesendet, um einen Client über eine Änderung des Kategoriestatus zu informieren.
    
Clients sollten beachten, dass nicht alle Tabellen die Benachrichtigung TABLE_SORT_DONE unterstützen und bereit sein sollten, diese Bedingung zu behandeln:
  
1. Erzwingen, dass die Sortierung synchron ist.
    
2. Erneutes Laden der Zeilen der Tabelle, wenn [IMAPITable::SortTable zurückgegeben](imapitable-sorttable.md) wird. 
    
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

