---
title: Abrufen von Daten aus Tabellenzeilen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 19a42794-a3a2-4336-af2a-473f24431252
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 902aa6b0471de78a5946b5fc89cbe87c874ce404
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624335"
---
# <a name="retrieving-data-from-table-rows"></a>Abrufen von Daten aus Tabellenzeilen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das Abrufen von Zeilen aus einer Tabelle umfasst Folgendes:
  
- Abrufen der Eigenschaftswerte für alle Spalten.
    
- Ändern der aktuellen Position.
    
Eine der erforderlichen Spalten in den meisten Tabellen ist ein Eintragsbezeichner – die **eigenschaft PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), die zum Öffnen des Objekts verwendet werden kann, das die Zeile darstellt. Dieser Eintragsbezeichner ist in der Regel ein kurzfristiger Eintragsbezeichner, der nicht über die Lebensdauer der Tabelle hinaus bestehen bleibt. Es kann jedoch ein langfristiger Bezeichner sein, wenn der Dienstanbieter, der die Tabelle implementiert, nur einen Eintragsbezeichnertyp unterstützt.
  
Clients und Dienstanbieter können einen der folgenden Aufrufe ausführen, um Zeilen abzurufen:
  
|||
|:-----|:-----|
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |Ruft eine angegebene Anzahl von Zeilen ab, die mit der aktuellen Zeile in vorwärts oder rückwärts beginnen.  <br/> |
|[HrQueryAllRows](hrqueryallrows.md) <br/> |Ruft alle Zeilen in einer Tabelle ab.  <br/> |
|[ITableData::HrQueryRow](itabledata-hrqueryrow.md) <br/> |Ruft eine Zeile in einer Tabelle entsprechend dem Wert ihrer Indexspalte ab. **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) ist in der Regel die Indexspalte für eine Tabelle.  <br/> |
   
Wenn eine optionale Eigenschaft als eine der Spalten in einer Tabelle enthalten ist, haben einige der Zeilen möglicherweise gültige Werte für die Spalte, andere nicht. Ob ein gültiger Wert für eine Spalte vorhanden ist, hängt davon ab, ob das Objekt, das die Informationen für die Zeile bereitstellt, die Eigenschaft festlegt. Je nach Implementierung des Objekts kann eine nicht vorhandene Eigenschaft in der Tabelle als **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) oder als beliebiger Wert dargestellt werden. Benutzer von Tabellen müssen sorgfältig zwischen Eigenschaften unterscheiden, die nicht vorhanden sind und bedeutungslose Werte und Eigenschaften aufweisen, die vorhanden sind und gültige Werte aufweisen. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

