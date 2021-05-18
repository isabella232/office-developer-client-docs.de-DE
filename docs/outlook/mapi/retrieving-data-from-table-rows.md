---
title: Abrufen von Daten aus Tabellenzeilen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19a42794-a3a2-4336-af2a-473f24431252
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2f389d26ec80b9af3ed28c5eb85b589c9cbb26c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405254"
---
# <a name="retrieving-data-from-table-rows"></a>Abrufen von Daten aus Tabellenzeilen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das Abrufen von Zeilen aus einer Tabelle umfasst:
  
- Abrufen der Eigenschaftswerte für alle Spalten.
    
- Ändern der aktuellen Position.
    
Eine der erforderlichen Spalten in den meisten Tabellen ist eine Eintrags-ID , die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft, die zum Öffnen des Objekts verwendet werden kann, das die Zeile darstellt. Dieser Eintragsbezeichner ist in der Regel eine kurzfristige Eintrags-ID, die nicht über die Lebensdauer der Tabelle hinaus beibehalten wird. Es kann jedoch eine langfristige ID sein, wenn der Dienstanbieter, der die Tabelle implementieren, nur einen Typ von Eintrags-ID unterstützt.
  
Clients und Dienstanbieter können einen der folgenden Aufrufe zum Abrufen von Zeilen erstellen:
  
|||
|:-----|:-----|
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |Ruft eine angegebene Anzahl von Zeilen ab, die mit der aktuellen Zeile in Vorwärts- oder Rückwärtsrichtung beginnen.  <br/> |
|[HrQueryAllRows](hrqueryallrows.md) <br/> |Ruft alle Zeilen in einer Tabelle ab.  <br/> |
|[ITableData::HrQueryRow](itabledata-hrqueryrow.md) <br/> |Ruft eine Zeile in einer Tabelle entsprechend dem Wert der Indexspalte ab. **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) ist in der Regel die Indexspalte für eine Tabelle.  <br/> |
   
Wenn eine optionale Eigenschaft als eine der Spalten in einer Tabelle enthalten ist, verfügen einige der Zeilen möglicherweise über gültige Werte für die Spalte, andere nicht. Ob ein gültiger Wert für eine Spalte vorhanden ist, hängt davon ab, ob das Objekt, das die Informationen für die Zeile liefert, die Eigenschaft legt. Je nach Implementierung des Objekts kann eine nicht vorhandene Eigenschaft in der Tabelle als PR_NULL **(** [PidTagNull](pidtagnull-canonical-property.md)) oder als beliebiger Wert dargestellt werden. Benutzer von Tabellen müssen darauf achten, zwischen Eigenschaften zu unterscheiden, die nicht vorhanden sind und bedeutungslose Werte und Eigenschaften aufweisen, die vorhanden sind und gültige Werte aufweisen. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

