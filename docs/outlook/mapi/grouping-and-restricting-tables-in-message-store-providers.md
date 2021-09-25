---
title: Gruppieren und Einschränken von Tabellen in Nachrichtenanbietern Store
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 01df4be4-98a1-4159-a06d-9ccf4337198f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 01f4d8d6bc6516dd52092f38f4963fd4b4547d2c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551541"
---
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a>Gruppieren und Einschränken von Tabellen in Nachrichtenanbietern Store

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clientanwendungen ermöglichen Benutzern häufig eine gewisse Kontrolle darüber, wie der Inhalt eines Ordners angezeigt wird. In der Regel kann ein Benutzer auswählen, ob Nachrichten nach dem Wert einer oder mehrerer Nachrichteneigenschaften gruppiert werden sollen, oder Nachrichten ausschließen, die bestimmten Kriterien entsprechen. Dies geschieht mithilfe der [IMAPITable : IUnknown-Schnittstelle.](imapitableiunknown.md) Clientanwendungen können die von der Tabelle zurückgegebenen Zeilen auf die vom Benutzer angegebenen Kriterien beschränken. Daher muss ein Nachrichtenspeicheranbieter die folgenden **IMAPITable-Methoden** implementieren. 
  
|IMAPITable**-Methode**|**Beschreibung**|
|:-----|:-----|
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |Gibt Tabellenzeilen zurück, die den angegebenen Kriterien entsprechen.  <br/> |
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |Gibt den Satz von Spalten in einer Tabelle oder den Satz der aktuell verwendeten Spalten zurück.  <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |Gibt eine oder mehrere Zeilen aus einer Tabelle zurück, beginnend mit einer bestimmten Position.  <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |Wendet eine Einschränkung auf eine Tabelle an, sodass nachfolgende Aufrufe von **FindRow** nur Zeilen zurückgeben, die der Einschränkung entsprechen.  <br/> |
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |Gibt an, welche Spalten zurückgegeben werden sollen, wenn Zeilen aus der Tabelle abgerufen werden.  <br/> |
   
Die Implementierung von Einschränkungen kann komplex sein. Weitere Informationen finden Sie unter ["Einschränkungen".](about-restrictions.md) Weitere Informationen zum Implementieren von Tabellen finden Sie unter [MAPI Tables](mapi-tables.md).
  
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

