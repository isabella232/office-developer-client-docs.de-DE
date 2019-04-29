---
title: Informationen zu Tabellen Benachrichtigungen
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
# <a name="about-table-notifications"></a>Informationen zu Tabellen Benachrichtigungen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clients verlassen sich häufig auf Tabellen Benachrichtigungen, um Änderungen an Objekten zu erfahren, statt sich zu registrieren, um Benachrichtigungen direkt von den Objekten zu empfangen. Zu den typischen Änderungen, die dazu führen, dass Benachrichtigungen gesendet werden, gehört das Hinzufügen, löschen oder Ändern einer Zeile und jeder kritische Fehler. Wenn Benachrichtigungen eingehen, können Clients bestimmen, ob ein weiterer Aufruf zum erneuten Laden der Tabelle durchzuführen ist. 
  
Da Tabellen Benachrichtigungen asynchron sind, gibt es ein paar Probleme, die die Behandlung von Benachrichtigungen weniger als einfach machen können:
  
- Die in der [TABLE_NOTIFICATION](table_notification.md) -Struktur übergebenen Daten stellen möglicherweise nicht den aktuellen Status der Tabelle dar. Beispielsweise kann ein Client eine Änderung an einer Nachricht vornehmen und diese dann löschen. Der Nachrichtenspeicher Anbieter, der die Inhaltstabelle mit der Nachricht implementiert, sendet zwei Benachrichtigungen: ein TABLE_ROW_MODIFIED-Ereignis gefolgt von einem TABLE_ROW_DELETED-Ereignis. Je nach Benachrichtigung des Nachrichtenspeicher Anbieters kann der Client die TABLE_ROW_MODIFIED-Benachrichtigung nach dem Löschen der Zeile erhalten. 
    
- Der in einer Benachrichtigung enthaltene Spaltensatz kann sich vom aktuellen Spaltensatz der Tabelle unterscheiden. MAPI erfordert, dass der Benachrichtigungs Spaltensatz mit dem Spaltensatz übereinstimmt, der zum Zeitpunkt der Benachrichtigungsgenerierung wirksam war. Da ein Client [IMAPITable::](imapitable-setcolumns.md) SetColumns aufrufen kann, um den Spaltensatz jederzeit zu ändern, auch nach einer Benachrichtigung, werden die beiden Spaltensätze möglicherweise nicht synchronisiert. 
    
- Tabellen Benachrichtigungen werden nur für Zeilen gesendet, die Teil der Ansicht sind. Das heißt, wenn eine Zeile aufgrund einer Einschränkung aus der Ansicht ausgeschlossen wird oder weil sich die Tabelle in einem reduzierten Zustand befindet, wird keine Benachrichtigung gesendet, wenn sich diese Zeile ändert. Darüber hinaus werden keine Benachrichtigungen gesendet, um einen Client über eine Änderung des Kategorien Status zu informieren.
    
Clients sollten beachten, dass nicht alle Tabellen die TABLE_SORT_DONE-Benachrichtigung unterstützen und bereit sind, diese Bedingung zu behandeln:
  
1. Erzwingen, dass die Sortierung synchron ist.
    
2. Erneutes Laden der Zeilen der Tabelle, wenn [IMAPITable:: sortable](imapitable-sorttable.md) zurückgegeben wird. 
    
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

