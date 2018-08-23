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
ms.openlocfilehash: 7b8690871dbe5b7234645f00cabab9c65706141e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573446"
---
# <a name="retrieving-data-from-table-rows"></a>Abrufen von Daten aus Tabellenzeilen

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Abrufen von Zeilen aus einer Tabelle umfasst:
  
- Abrufen der Eigenschaftswerte für alle Spalten.
    
- Ändern der aktuellen Position.
    
Einer der erforderlichen Spalten in den meisten Tabellen ist eine Eintrags-ID – die Eigenschaft **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) –, die verwendet werden kann, um das Objekt zu öffnen, das die Zeile darstellt. Dieses Eintrags-ID ist in der Regel eine kurzfristige Eintrags-ID, eine, die nicht über die Lebensdauer der Tabelle beibehalten wird. Es kann jedoch ein langfristige Bezeichner sein, wenn der Dienstanbieter Implementieren der Tabelle nur ein Typ von Eintrags-ID unterstützt.
  
Clients und Dienstanbieter können einen der folgenden Aufrufe abzurufenden Zeilen vornehmen:
  
|||
|:-----|:-----|
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |Ruft eine angegebene Anzahl von Zeilen beginnend mit der aktuellen Zeile in vorwärts oder rückwärts ausgeführt.  <br/> |
|[HrQueryAllRows](hrqueryallrows.md) <br/> |Ruft alle Zeilen in einer Tabelle ab.  <br/> |
|[ITableData::HrQueryRow](itabledata-hrqueryrow.md) <br/> |Ruft eine Zeile in einer Tabelle entsprechend dem Wert der Index-Spalte. **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) ist in der Regel die Indexspalte für eine Tabelle.  <br/> |
   
Wenn eine optionale Eigenschaft als eine der Spalten in einer Tabelle enthalten ist, möglicherweise einige der Zeilen gültige Werte für die Spalte haben, während andere Benutzer nicht möglicherweise. Gibt an, ob ein gültiger Wert für eine Spalte vorhanden ist, hängt davon ab, ob das Objekt, und geben Sie Informationen für die Zeile die-Eigenschaft festgelegt wird. Je nach der Implementierung des Objekts kann eine nicht vorhandene Eigenschaft in der Tabelle als **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) oder ein beliebiger Wert dargestellt werden. Benutzer von Tabellen müssen achten unterscheiden zwischen Eigenschaften, die nicht vorhanden sind und keine Bedeutung Werte und Eigenschaften, die vorhanden und sind gültige Werte. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

