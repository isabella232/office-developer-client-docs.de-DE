---
title: Arbeiten mit Spalten mit mehreren Werten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 911a41c3-c10f-4473-8853-fafb56b721ba
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 78f6083cf17bb21152df1a7ea09825f3be7f0e37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572942"
---
# <a name="working-with-multivalued-columns"></a>Arbeiten mit Spalten mit mehreren Werten

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Mehrwertige Spalte enthält die Daten der eine mehrwertige Eigenschaft, die eine Eigenschaft, die ein Array von Werten vom Basistyp anstatt einen single-Wert aufweist. Weil keine der Tabellen die Spalte Standardgruppen mehrwertige Eigenschaften verwendet, sind mehrwertige Eigenschaften in einer Tabelle enthalten nur, wenn der Tabelle der Benutzer diese anfordert. 
  
Mehrwertige Spalten können in Tabellen angezeigt werden:
  
- In einer einzelnen Zeile mit allen der Eigenschaftswerte in der Instanz einspaltige angezeigt wird. Dies ist die Standardeinstellung.
    
    - Oder -
    
- In einer Reihe von Zeilen, mit der eine Zeile für jeden der Eigenschaftswerte. Wie viele Zeilen als dort Werte in der mehrwertigen Eigenschaft sind, wird in der Spalte in einer eigenen Zeile mit jedem eindeutiger Wert angezeigt. Jede Zeile enthält einen eindeutigen Wert für die **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))-Eigenschaft, aber die gleichen Werte für die anderen Spalten. Wenn eine Zeile mehr als eine Spalte mit mehreren Werten enthält, beispielsweise zwei Spalten mit _M_ und _N_ Werte, die jeweils dann _M\*N_ Instanzen der Zeile in der Tabelle angezeigt werden. 
    
Ein Tabelle Benutzer fordert die nicht standardmäßigen Art der Anzeige durch Aufrufen der [IMAPITable::SetColumns](imapitable-setcolumns.md) -Methode mit dem MVI_FLAG-Flag in den Eigenschaftstyp der mehrwertige Spalte festgelegt. Das Flag MVI_FLAG ist eine Konstante, die als Ergebnis der Kombination von die Flags MV_FLAG und MV_INSTANCE vorhanden und eine logische **OR** -Operation definiert. Neben den in **SetColumns**verwendet wird, kann MVI_FLAG auch an [SortTable](imapitable-sorttable.md) in den _LpSortCriteria_ -Parameter und die [Methode IMAPITable:: Restrict](imapitable-restrict.md) im **UlPropTag** -Member der _LpRestriction_ übergeben werden der Parameter. Wenn die MVI_FLAG übergeben, verhält **SortTable** wie **SetColumns**, eine Zeile für jeden Wert in der mehrwertigen Spalte hinzufügen und auf die einzelnen Werte in die Instanzen sortieren. Eine Zeile wird für jeden Wert hinzugefügt. 
  
 **Restrict**, wird jedoch nicht mehrwertige Spalte in zusätzliche berechnete Zeilen erweitert. Mehrwertige Spalte mit dem MVI_FLAG weist den Dienstanbieter, verwenden Sie diese Spalte in der Tabelle einschränken. Wenn der Wert einer Eigenschaft in der Einschränkung vorhanden ist, muss es sich ein einzelner Wert-Eigenschaftentag identisch mit demjenigen handeln, die für die Spalte von [IMAPITable::QueryRows](imapitable-queryrows.md) zurückgegeben wird. 
  
Tabelle Implementierer sind nur erforderlich, um die standardmäßige Art der Anzeige unterstützen und können den MAPI_E_TOO_COMPLEX-Wert zurück, wenn ein Anrufer die anderen Alternative anfordert. Die Möglichkeit zur Unterstützung von beide Arten von Anzeige ist wichtigste für Nachricht Anbieter Ordner Inhalt Tabellen implementieren. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

