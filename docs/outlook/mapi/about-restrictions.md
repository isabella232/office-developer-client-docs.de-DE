---
title: Informationen zu Einschränkungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e119fa20-08b8-4c8d-93fc-56037220890d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 139526937380273703a96f91f2bae02a79debc76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433108"
---
# <a name="about-restrictions"></a>Informationen zu Einschränkungen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Einschränkung ist eine Möglichkeit, die Anzahl der Zeilen in einer Ansicht auf die Zeilen mit Werten für Spalten zu beschränken, die bestimmten Kriterien entsprechen. Es gibt viele verschiedene Möglichkeiten für die Verwendung von Einschränkungen für Tabellen. Clientanwendungen können Einschränkungen verwenden, z. B. um eine Inhaltstabelle nach Nachrichten zu filtern, die von einer bestimmten Person gesendet wurden, um nach Zeilen zu suchen, die entweder keine Eigenschaft unterstützen oder eine Eigenschaft auf einen bestimmten Wert festgelegt haben, oder um nach doppelten Empfängern in einer Nachricht zu suchen. 
  
Die [Methoden IMAPITable::Restrict](imapitable-restrict.md) und [IMAPITable::FindRow](imapitable-findrow.md) werden zum Festlegen von Einschränkungen für eine Tabelle verwendet. **Restrict** wendet die Einschränkung auf die Tabelle an, ohne Zeilen abrufen zu müssen. Um nur die Zeilen abzurufen, die die Einschränkung erfüllen, ist ein nachfolgender Aufruf von [IMAPITable::QueryRows](imapitable-queryrows.md) oder einer ähnlichen Methode erforderlich. **FindRow** wendet die Einschränkung an und ruft die erste Zeile in der Tabelle ab, die den Kriterien entspricht. **FindRow** wendet eine temporäre Einschränkung an, die nur für die Dauer des Anrufs besteht, während **Restrict** eine dauerhaftere Einschränkung angewendet wird. 
  
Einige Clients können eine Einschränkung mithilfe von Spalten erstellen, die sich nicht im aktuellen Spaltensatz befinden. Die Unterstützung einer solchen Einschränkung ist optional, und Tabellen implementierer, die sie unterstützen, fügen einen Mehrwert hinzu, insbesondere für Inhaltstabellen. Table implementers that do not support it can return the MAPI_E_TOO_COMPLEX value from a **Restrict** call or the MAPI_E_NOT_FOUND value from a **FindRow** call. 
  
Clients sollten beachten, dass auch wenn der Anbieter Einschränkungen für Spalten unterstützt, die nicht im aktuellen Spaltensatz enthalten sind, insgesamt eine bessere Leistung erzielen, indem sie die Spalten angeben, die sie in ihren Einschränkungen mit [IMAPITable::SetColumns](imapitable-setcolumns.md)verwenden möchten.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

