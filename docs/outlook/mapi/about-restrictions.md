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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322120"
---
# <a name="about-restrictions"></a>Informationen zu Einschränkungen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Einschränkung ist eine Möglichkeit, um die Anzahl der Zeilen in einer Ansicht auf die Zeilen mit Werten für Spalten zu begrenzen, die bestimmten Kriterien entsprechen. Es gibt viele verschiedene Möglichkeiten für die Verwendung von Einschränkungen mit Tabellen. Client Anwendungen können Einschränkungen verwenden, um beispielsweise eine Inhaltstabelle für Nachrichten zu filtern, die von einer bestimmten Person gesendet werden, nach Zeilen zu suchen, die keine Eigenschaft unterstützen oder eine Eigenschaft auf einen bestimmten Wert festgelegt haben, oder um nach doppelten Empfängern in einem Nachricht. 
  
Die [IMAPITable:: Restrict](imapitable-restrict.md) -und [IMAPITable:: FindRow](imapitable-findrow.md) -Methoden werden verwendet, um Einschränkungen für eine Tabelle festzulegen. **Restrict** wendet die Einschränkung auf die Tabelle an, ohne Zeilen abzurufen. Um nur die Zeilen abzurufen, die der Einschränkung entsprechen, ist ein nach folgender Aufruf von [IMAPITable:: QueryRows](imapitable-queryrows.md) oder einer ähnlichen Methode erforderlich. **FindRow** wendet die Einschränkung an und ruft die erste Zeile in der Tabelle ab, die den Kriterien entspricht. **FindRow** wendet eine temporäre Einschränkung an, die nur für die Dauer des Anrufs existiert, wohingegen **Restrict** eine dauerhaftere Einschränkung anwendet. 
  
Einige Clients können eine Einschränkung mithilfe von Spalten erstellen, die nicht in der aktuellen Spaltengruppe enthalten sind. Die Unterstützung einer solchen Einschränkung ist optional, und Tabellen Implementierer, die Sie unterstützen, fügen einen Wert hinzu, insbesondere für Inhaltstabellen. Tabellen Implementierer, die Sie nicht unterstützen, können den MAPI_E_TOO_COMPLEX-Wert aus einem **Restrict** -Aufruf oder aus dem MAPI_E_NOT_FOUND-Wert eines **FindRow** -Aufrufs zurückgeben. 
  
Clients sollten beachten, dass auch dann, wenn der Anbieter Einschränkungen für Spalten unterstützt, die nicht in der aktuellen Spaltengruppe enthalten sind, eine bessere Leistung erzielt werden, indem die Spalten angegeben werden, die Sie in ihren Einschränkungen mit [IMAPITable::](imapitable-setcolumns.md) SetColumns verwenden möchten. .
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

