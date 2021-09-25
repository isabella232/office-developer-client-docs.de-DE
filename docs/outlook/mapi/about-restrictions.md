---
title: Informationen zu Einschränkungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e119fa20-08b8-4c8d-93fc-56037220890d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 127e88eef946a4cf9417adbc1860a492cfe825cd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557008"
---
# <a name="about-restrictions"></a>Informationen zu Einschränkungen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Einschränkung ist eine Möglichkeit, die Anzahl der Zeilen in einer Ansicht auf nur die Zeilen mit Werten für Spalten zu beschränken, die bestimmten Kriterien entsprechen. Es gibt viele verschiedene Möglichkeiten, Einschränkungen für Tabellen zu verwenden. Clientanwendungen können Einschränkungen verwenden, z. B. um ein Inhaltsverzeichnis nach Nachrichten zu filtern, die von einer bestimmten Person gesendet werden, um nach Zeilen zu suchen, die entweder keine Eigenschaft unterstützen oder eine Eigenschaft auf einen bestimmten Wert festgelegt haben, oder um nach doppelten Empfängern innerhalb einer Nachricht zu suchen. 
  
Die [IMAPITable::Restrict-](imapitable-restrict.md) und [IMAPITable::FindRow-Methoden](imapitable-findrow.md) werden verwendet, um Einschränkungen für eine Tabelle festzulegen. **Restrict** wendet die Einschränkung auf die Tabelle an, ohne Zeilen abzurufen. Um nur die Zeilen abzurufen, die die Einschränkung erfüllen, ist ein nachfolgender Aufruf von [IMAPITable::QueryRows](imapitable-queryrows.md) oder einer ähnlichen Methode erforderlich. **FindRow** wendet die Einschränkung an und ruft die erste Zeile in der Tabelle ab, die den Kriterien entspricht. **FindRow** wendet eine temporäre Einschränkung an, die nur für die Dauer des Anrufs vorhanden ist, während **Restrict** eine dauerhaftere Einschränkung anwendet. 
  
Einige Clients können eine Einschränkung mithilfe von Spalten erstellen, die nicht im aktuellen Spaltensatz enthalten sind. Die Unterstützung einer solchen Einschränkung ist optional, und Tabellen implementierer, die dies unterstützen, haben einen Mehrwert, insbesondere für Inhaltsverzeichnisse. Tabellen implementer that do not support it can return the MAPI_E_TOO_COMPLEX value from a **Restrict** call or the MAPI_E_NOT_FOUND value from a **FindRow** call. 
  
Clients sollten beachten, dass selbst wenn der Anbieter Einschränkungen für Spalten unterstützt, die nicht im aktuellen Spaltensatz enthalten sind, sie insgesamt eine bessere Leistung erzielen, indem sie die Spalten angeben, die sie in ihren Einschränkungen mit [IMAPITable::SetColumns](imapitable-setcolumns.md)verwenden möchten.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

