---
title: Informationen zu Einschränkungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e119fa20-08b8-4c8d-93fc-56037220890d
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d7294527fcd557ae2d4824b9a3215ff464f62c2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791230"
---
# <a name="about-restrictions"></a>Informationen zu Einschränkungen

  
  
**Betrifft**: Outlook 
  
Eine Einschränkung ist eine Möglichkeit zur Begrenzung der Anzahl der Zeilen in einer Ansicht, um nur die Zeilen mit Werten für Spalten, die bestimmte Kriterien erfüllen. Es gibt viele verschiedene Möglichkeiten für die Verwendung von Einschränkungen mit Tabellen. Clientanwendungen können Einschränkungen, beispielsweise zum Filtern einer Inhaltstabelle für Nachrichten, die von einer bestimmten Person, Zeilen suchen, die entweder eine Eigenschaft nicht unterstützt, oder eine Eigenschaft auf einen bestimmten Wert festgelegt haben, oder für doppelte Empfänger innerhalb einer Nachricht. 
  
Die [Methode IMAPITable:: Restrict](imapitable-restrict.md) und [IMAPITable](imapitable-findrow.md) Methoden werden verwendet, um Einschränkungen für eine Tabelle festzulegen. **Restrict** gilt die Einschränkung für die Tabelle ohne Abrufen von Zeilen. Um nur die Zeilen abrufen, die die Einschränkung entsprechen, ist ein nachfolgender Aufruf [IMAPITable::QueryRows](imapitable-queryrows.md) oder einer ähnlichen Methode erforderlich. **FindRow** gilt die Einschränkung und ruft die erste Zeile in der Tabelle, die den Kriterien entspricht. **FindRow** wendet die temporäre Einschränkung, die nur für die Dauer des Anrufs, vorhanden ist, **Restrict** eine permanente Beschränkung gilt. 
  
Einige Clients können erstellen Sie eine Einschränkung von Spalten, die nicht in der aktuellen Spalte festgelegt sind. Unterstützung für diese Beschränkung ist optional und Implementierer Tabelle, die sie unterstützen Hinzufügen eines Werts, insbesondere für Inhalt Tabellen. Tabelle-Implementierung, die nicht unterstützen kann den Wert MAPI_E_TOO_COMPLEX aus einen Anruf **Restrict** oder den Wert des MAPI_E_NOT_FOUND aus einen Anruf **FindRow** zurückgegeben. 
  
Clients sollten beachten, dass, auch wenn der Anbieter das Einschränkungen auf Spalten in der aktuellen Spalte Gruppe nicht unterstützt, sie eine bessere Leistung insgesamt erhalten durch Angeben der Spalten, die sie in ihre Einschränkungen mit [IMAPITable::SetColumns](imapitable-setcolumns.md) verwenden möchten .
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

