---
title: Gruppieren und Einschränken von Tabellen in Nachrichtenspeicher Anbietern
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01df4be4-98a1-4159-a06d-9ccf4337198f
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8a45a9fd0d40c16d110fd52be1ac1117e1dd4d04
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299412"
---
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a>Gruppieren und Einschränken von Tabellen in Nachrichtenspeicher Anbietern

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Client Anwendungen ermöglichen Benutzern häufig eine gewisse Kontrolle darüber, wie der Inhalt eines Ordners angezeigt wird. NormalerWeise kann ein Benutzer festlegen, dass Nachrichten nach dem Wert einer oder mehrerer Nachrichteneigenschaften gruppiert werden sollen oder Nachrichten ausschließen, die bestimmten Kriterien entsprechen. Dies erfolgt über die [IMAPITable: IUnknown](imapitableiunknown.md) -Schnittstelle. Client Anwendungen können die Zeilen, die von der Tabelle zurückgegeben werden, auf die vom Benutzer angegebenen Kriterien einschränken. Daher muss ein Nachrichtenspeicher Anbieter die folgenden **IMAPITable** -Methoden implementieren. 
  
|IMAPITable * *-Methode * *|**Beschreibung**|
|:-----|:-----|
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |Gibt Tabellenzeilen zurück, die den angegebenen Kriterien entsprechen.  <br/> |
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |Gibt den Satz von Spalten in einer Tabelle oder der Gruppe der aktuell verwendeten Spalten zurück.  <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |Gibt eine oder mehrere Zeilen aus einer Tabelle ab einer bestimmten Position zurück.  <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |Wendet eine Einschränkung auf eine Tabelle an, sodass nachfolgende Aufrufe von **FindRow** nur Zeilen zurückgeben, die mit der Einschränkung übereinstimmen.  <br/> |
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |Gibt an, welche Spalten zurückgegeben werden sollen, wenn Zeilen aus der Tabelle abgerufen werden.  <br/> |
   
Einschränkungen können bei der Implementierung komplex sein; Weitere Informationen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md). Weitere Informationen zum Implementieren von Tabellen finden Sie unter [MAPI Tables](mapi-tables.md).
  
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

