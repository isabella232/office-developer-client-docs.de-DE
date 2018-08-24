---
title: Gruppieren und Einschränken von Tabellen in Nachrichtenspeicheranbietern
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01df4be4-98a1-4159-a06d-9ccf4337198f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ec1c07a8d2c88680ebd94cf8ecd6901ed86ad100
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578787"
---
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a>Gruppieren und Einschränken von Tabellen in Nachrichtenspeicheranbietern

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clientanwendungen können Benutzer häufig besser steuern, wie der Inhalt eines Ordners angezeigt wird. In der Regel ein Benutzer kann auswählen, dass Nachrichten entsprechend dem Wert der Nachrichteneigenschaften für eine oder mehrere gruppiert oder kann verhindern, dass Nachrichten auszuschließen, die bestimmte Kriterien erfüllen. Dies erfolgt mithilfe der [IMAPITable: IUnknown](imapitableiunknown.md) Schnittstelle. Clientanwendungen können einschränken, die Zeilen aus der Tabelle an beliebige erforderliche Kriterien gibt an, der Benutzer zurückgegeben. Speichern Sie daher, eine Nachricht Anbieter muss die folgenden **IMAPITable** -Methoden implementieren. 
  
|IMAPITable **-Methode **|**Beschreibung**|
|:-----|:-----|
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |Gibt die Tabelle Zeilen, die die angegebenen Kriterien entsprechen.  <br/> |
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |Gibt die Gruppe von Spalten in einer Tabelle oder die Gruppe von aktuell verwendeten Spalten zurück.  <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |Gibt eine oder mehrere Zeilen aus einer Tabelle, beginnend mit einer bestimmten Position zurück.  <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |Wendet die Einschränkung, die einer Tabelle, sodass nachfolgende Aufrufe von **FindRow** nur Zeilen zurück, die der Einschränkung entsprechen.  <br/> |
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |Gibt an, welche Spalten zurückgegeben werden sollen, wenn Zeilen aus der Tabelle abgerufen werden.  <br/> |
   
Einschränkungen können zur Implementierung komplex sein; Weitere Informationen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md). Weitere Informationen zum Implementieren der Tabellen finden Sie unter [MAPI-Tabellen](mapi-tables.md).
  
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

