---
title: Arbeiten mit mehrwertigen Spalten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 911a41c3-c10f-4473-8853-fafb56b721ba
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ee6b1f22b7eee25698bbc445c562bdbe849b38f9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578396"
---
# <a name="working-with-multivalued-columns"></a>Arbeiten mit mehrwertigen Spalten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine mehrwertige Spalte enthält die Daten einer mehrwertigen Eigenschaft, bei der es sich um eine Eigenschaft mit einem Array von Werten des Basistyps anstelle eines einzelnen Werts handelt. Da keine der Tabellen mehrwertige Eigenschaften in ihren Standardspaltensätzen enthält, sind mehrwertige Eigenschaften nur dann in einer Tabelle enthalten, wenn der Benutzer der Tabelle dies anfordert. 
  
Mehrwertige Spalten können in Tabellen angezeigt werden:
  
- In einer einzelnen Zeile, wobei alle Eigenschaftswerte in der Einzelspalteninstanz angezeigt werden. Dies ist die Standardeinstellung.
    
    - Oder -
    
- In einer Reihe von Zeilen mit einer Zeile für jeden Eigenschaftswert. Jeder eindeutige Wert wird in der Spalte in einer eigenen Zeile angezeigt, wobei so viele Zeilen vorhanden sind, wie Werte in der mehrwertigen Eigenschaft vorhanden sind. Jede Zeile hat einen eindeutigen Wert für die **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) -Eigenschaft, aber die gleichen Werte für die anderen Spalten. Wenn eine Zeile mehrere Spalten mit mehreren Werten enthält, z. B. zwei Spalten mit  _M-_ bzw.  _N-Werten,_ werden  _M \* N-Instanzen_ der Zeile in der Tabelle angezeigt. 
    
Ein Tabellenbenutzer fordert den nicht standardmäßigen Anzeigetyp an, indem er die [IMAPITable::SetColumns-Methode aufruft,](imapitable-setcolumns.md) wobei das MVI_FLAG Flag im Eigenschaftentyp der mehrwertigen Spalte festgelegt ist. Das MVI_FLAG Flag ist eine Konstante, die als Ergebnis der Kombination von MV_FLAG und MV_INSTANCE Flags mit einem logischen **OR-Vorgang** definiert wird. Zusätzlich zur Verwendung in **SetColumns** kann MVI_FLAG auch an [IMAPITable::SortTable](imapitable-sorttable.md) im  _Parameter lpSortCriteria_ und [IMAPITable::Restrict](imapitable-restrict.md) im **ulPropTag-Element** des  _lpRestriction-Parameters_ übergeben werden. Wenn die MVI_FLAG übergeben wird, führt **SortTable** eine ähnliche Leistung wie **SetColumns aus,** wobei für jeden Wert in der mehrwertigen Spalte eine Zeile hinzugefügt und nach den einzelnen Werten in den Instanzen sortiert wird. Für jeden Wert wird eine Zeile hinzugefügt. 
  
 **Restrict** erweitert die mehrwertige Spalte jedoch nicht in zusätzliche berechnete Zeilen. Eine mehrwertige Spalte mit dem MVI_FLAG Festgelegt weist den Dienstanbieter an, diese Spalte zum Einschränken der Tabelle zu verwenden. Wenn in der Einschränkung ein Eigenschaftswert vorhanden ist, muss es sich um ein Eigenschaftstag mit einem einzelnen Wert handeln, das mit dem Tag identisch ist, das von [IMAPITable::QueryRows](imapitable-queryrows.md) für die Spalte zurückgegeben wird. 
  
Tabellen implementers are only required to support the default type of display and can return the MAPI_E_TOO_COMPLEX value when a caller requests the other alternative. Die Möglichkeit, beide Anzeigetypen zu unterstützen, ist für Nachrichtenspeicheranbieter, die Ordnerinhaltstabellen implementieren, am wichtigsten. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

