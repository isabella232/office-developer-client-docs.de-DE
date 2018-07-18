---
title: Informationen zu Tabellenbenachrichtigungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00c9c6c2-fc21-4b9c-91fa-629450a22d37
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3dfc67c8bcd899396da5371c614fd221cd9b2251
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791229"
---
# <a name="about-table-notifications"></a>Informationen zu Tabellenbenachrichtigungen

  
  
**Betrifft**: Outlook 
  
Clients nutzen häufig Tabelle Benachrichtigungen von Änderungen an Objekten anstelle von Erhalt von Benachrichtigungen direkt über die Objekte registrieren erfahren. Typische Änderungen, die dazu führen, dass Benachrichtigungen gesendet werden umfassen die hinzufügen, löschen oder Änderung einer Zeile und keinen kritischen Fehler. Wenn Benachrichtigungen eingehen, können Clients bestimmen, ob stellen Sie einen weiteren Anruf die Tabelle erneut geladen werden soll. 
  
Da Tabelle Benachrichtigungen asynchron sind, sind einige Probleme, die Behandlung Benachrichtigungen kleiner als unkomplizierte können:
  
- Die Daten in der Struktur [TABLE_NOTIFICATION](table_notification.md) übergeben möglicherweise nicht am aktuellen Status der Tabelle darstellen. Ein Client kann beispielsweise eine Änderung vornehmen, um eine Nachricht und dann entscheiden, ihn zu löschen. Implementieren der Inhaltstabelle, die die Nachricht enthalten Anbieter die Nachricht sendet, zwei Benachrichtigungen: ein Ereignis TABLE_ROW_MODIFIED gefolgt von einem TABLE_ROW_DELETED-Ereignis. Je nachdem, wie der Nachricht Speicheranbieter Benachrichtigungen auftritt kann der Client TABLE_ROW_MODIFIED nach dem Löschen der Zeile eine Benachrichtigung. 
    
- Die Spalte in einer Benachrichtigung enthalten möglicherweise nicht mit der Tabelle aktuellen Spalte abweichen. MAPI erfordert, dass die Benachrichtigung Spalte Festlegen der Spalte entsprechen, die zum Zeitpunkt gültig war, die die Benachrichtigung generiert wurde. Da es für einen Client aufrufen, [IMAPITable::SetColumns](imapitable-setcolumns.md) zum Ändern der Spalte festlegen, können Sie jederzeit möglich ist – einschließlich nach einer Benachrichtigung – im zweispaltiges wird möglicherweise nicht synchronisiert. 
    
- Tabelle Benachrichtigungen werden nur für Zeilen gesendet, die Teil der Ansicht sind. D. h., wird eine Zeile aus der Ansicht aufgrund einer Einschränkung ausgeschlossen wird oder, da die Tabelle in einem reduzierten Zustand befindet, keine Benachrichtigung gesendet, wenn diese Zeile geändert wird. Darüber hinaus sind keine Benachrichtigungen gesendet, um einen Client über eine Änderung in der Kategorie Zustand zu informieren.
    
Clients Beachten Sie, dass nicht alle Tabellen die Benachrichtigung TABLE_SORT_DONE unterstützen und sollte Seien Sie diese Bedingung durch behandeln:
  
1. Erzwingen die Sortierung synchrone sein.
    
2. Die Zeilen der Tabelle Neuladen, wenn [SortTable](imapitable-sorttable.md) zurückgegeben. 
    
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

