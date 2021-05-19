---
title: Arbeiten mit mehrwertigen Spalten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 911a41c3-c10f-4473-8853-fafb56b721ba
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 34f19e279c86e0c0856d242cf2aa13d744d46f13
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420185"
---
# <a name="working-with-multivalued-columns"></a>Arbeiten mit mehrwertigen Spalten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine mehrwertige Spalte enthält die Daten einer mehrwertigen Eigenschaft, bei der es sich um eine Eigenschaft mit einem Array von Werten des Basistyps anstelle eines einzelnen Werts handelt. Da keine der Tabellen mehrwertige Eigenschaften in ihren Standardspaltensätzen enthält, sind mehrwertige Eigenschaften nur dann in einer Tabelle enthalten, wenn der Benutzer der Tabelle sie anfordert. 
  
Mehrwertige Spalten können in Tabellen angezeigt werden:
  
- In einer einzelnen Zeile, bei der alle Eigenschaftswerte in der Instanz einer einzelnen Spalte angezeigt werden. Dies ist die Standardeinstellung.
    
    - Oder -
    
- In einer Reihe von Zeilen mit einer Zeile für jeden Eigenschaftswerte. Jeder eindeutige Wert wird in der Spalte in seiner eigenen Zeile angezeigt, und es gibt so viele Zeilen wie Werte in der mehrwertigen Eigenschaft. Jede Zeile hat einen eindeutigen Wert für die **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) -Eigenschaft, aber die gleichen Werte für die anderen Spalten. Wenn eine Zeile mehr als eine Spalte mit mehreren Werten enthält, z. B. zwei Spalten mit  _M-_ bzw.  _N-Werten,_ werden  _M \* N-Instanzen_ der Zeile in der Tabelle angezeigt. 
    
Ein Tabellenbenutzer fordert den nicht standardmäßigen Anzeigetyp an, indem er die [IMAPITable::SetColumns-Methode](imapitable-setcolumns.md) aufruft, deren MVI_FLAG-Flag im Eigenschaftstyp der mehrwertigen Spalte festgelegt ist. Das MVI_FLAG ist eine Konstante, die als Ergebnis der Kombination der MV_FLAG- und MV_INSTANCE-Flags mit einem logischen **OR-Vorgang definiert** ist. Neben der Verwendung in **SetColumns** kann MVI_FLAG auch an [IMAPITable::SortTable](imapitable-sorttable.md) im  _parameter lpSortCriteria_ und [IMAPITable::Restrict](imapitable-restrict.md) im **ulPropTag-Element** des  _lpRestriction-Parameters_ übergeben werden. Wenn die MVI_FLAG übergeben wird, führt **SortTable** eine ähnliche Leistung wie **SetColumns** aus, fügt für jeden Wert in der mehrwertigen Spalte eine Zeile hinzu und sortiert die einzelnen Werte in den Instanzen. Für jeden Wert wird eine Zeile hinzugefügt. 
  
 **Restrict** erweitert die mehrwertige Spalte jedoch nicht in zusätzliche berechnete Zeilen. Eine mehrwertige Spalte mit MVI_FLAG Dienstanbieter angewiesen, diese Spalte beim Einschränken der Tabelle zu verwenden. Wenn in der Einschränkung ein Eigenschaftswert enthalten ist, muss es sich um ein einzelnes Werteigenschaftstag handelt, das mit dem Tag identisch ist, das von [IMAPITable::QueryRows](imapitable-queryrows.md) für die Spalte zurückgegeben würde. 
  
Tabellen implementierer sind nur erforderlich, um den Standardanzeigetyp zu unterstützen und können den MAPI_E_TOO_COMPLEX zurückgeben, wenn ein Aufrufer die andere Alternative anfordert. Die Möglichkeit, beide Anzeigetypen zu unterstützen, ist für Nachrichtenspeicheranbieter, die Ordnerinhaltstabellen implementieren, am wichtigsten. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

