---
title: Gruppieren und Einschränken von Tabellen in Nachrichtenanbietern Store Anbieter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01df4be4-98a1-4159-a06d-9ccf4337198f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8a45a9fd0d40c16d110fd52be1ac1117e1dd4d04
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428984"
---
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a>Gruppieren und Einschränken von Tabellen in Nachrichtenanbietern Store Anbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clientanwendungen ermöglichen Benutzern häufig eine gewisse Kontrolle darüber, wie der Inhalt eines Ordners angezeigt wird. In der Regel kann ein Benutzer festlegen, dass Nachrichten nach dem Wert einer oder mehreren Nachrichteneigenschaften gruppieren oder Nachrichten ausschließen, die bestimmten Kriterien entsprechen. Dies erfolgt mithilfe der [IMAPITable : IUnknown-Schnittstelle.](imapitableiunknown.md) Clientanwendungen können die aus der Tabelle zurückgegebenen Zeilen auf die vom Benutzer angegebenen Kriterien beschränken. Daher muss ein Nachrichtenspeicheranbieter die folgenden **IMAPITable-Methoden** implementieren. 
  
|IMAPITable**-Methode**|**Beschreibung**|
|:-----|:-----|
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |Gibt Tabellenzeilen zurück, die den angegebenen Kriterien entsprechen.  <br/> |
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |Gibt den Satz von Spalten in einer Tabelle oder den Satz der derzeit verwendeten Spalten zurück.  <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |Gibt eine oder mehrere Zeilen aus einer Tabelle ab einer bestimmten Position zurück.  <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |Wendet eine Einschränkung auf eine Tabelle an, sodass nachfolgende Aufrufe von **FindRow** nur Zeilen zurückgeben, die der Einschränkung entsprechen.  <br/> |
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |Gibt an, welche Spalten zurückgegeben werden sollen, wenn Zeilen aus der Tabelle abgerufen werden.  <br/> |
   
Einschränkungen können komplex implementiert werden. Weitere Informationen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md). Weitere Informationen zum Implementieren von Tabellen finden Sie unter [MAPI Tables](mapi-tables.md).
  
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

