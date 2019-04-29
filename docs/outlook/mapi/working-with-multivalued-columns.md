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
  
Eine mehrwertige Spalte enthält die Daten einer mehrwertigen Eigenschaft, bei der es sich um eine Eigenschaft handelt, die ein Array von Werten des Basistyps anstelle eines einzelnen Werts aufweist. Da keine der Tabellen mehrwertige Eigenschaften in ihren Standardspalten Sätzen enthält, werden mehrwertige Eigenschaften nur dann in eine Tabelle aufgenommen, wenn Sie vom Benutzer der Tabelle angefordert werden. 
  
Mehrwertige Spalten können in Tabellen angezeigt werden:
  
- In einer einzelnen Zeile, wobei alle Eigenschaftswerte in der einzelnen Spalten Instanz angezeigt werden. Dies ist die Standardeinstellung.
    
    - Oder
    
- In einer Reihe von Zeilen mit einer Zeile für jeden der Eigenschaftswerte. Jeder eindeutige Wert wird in der Spalte in einer eigenen Zeile angezeigt, wobei es so viele Zeilen gibt, wie Werte in der mehrwertigen Eigenschaft vorhanden sind. Jede Zeile hat einen eindeutigen Wert für die **PR_INSTANCE_KEY** ([pidtaginstancekey (](pidtaginstancekey-canonical-property.md))-Eigenschaft, aber die gleichen Werte für die anderen Spalten. Wenn eine Zeile mehr als eine Spalte mit mehreren Werten enthält, beispielsweise zwei Spalten mit den Werten _m_ und _n_ , werden in der Tabelle _m\*N_ -Instanzen der Zeile angezeigt. 
    
Ein Tabellen Benutzer fordert den nicht standardmäßigen Anzeigetyp durch Aufrufen der [IMAPITable::](imapitable-setcolumns.md) SetColumns-Methode mit dem MVI_FLAG-Flag an, das im Eigenschaftentyp der mehrwertigen Spalte festgelegt ist. Das MVI_FLAG-Flag ist eine Konstante, die als Ergebnis der Kombination der MV_FLAG-und MV_INSTANCE-Flags mit einer logischen **or** -Operation definiert wird. Zusätzlich zur Verwendung in SetColumns kann MVI_FLAG **** auch an [IMAPITable:: sortable](imapitable-sorttable.md) im _lpSortCriteria_ -Parameter und [IMAPITable:: Restrict](imapitable-restrict.md) im **ulPropTag** -Element der _lpRestriction_ übergeben werden. Parameter. Wenn der MVI_FLAG übergeben wird **** , führt sortable ähnlich wie SetColumns aus, fügt eine Zeile für jeden Wert in der mehrwertigen Spalte hinzu und sortiert die einzelnen Werte in den Instanzen. **** Für jeden Wert wird eine Zeile hinzugefügt. 
  
 **Restrict**erweitert die mehrwertige Spalte jedoch nicht in zusätzliche berechnete Zeilen. Eine mehrwertige Spalte mit dem MVI_FLAG-Satz weist den Dienstanbieter an, diese Spalte beim Einschränken der Tabelle zu verwenden. Wenn in der Einschränkung ein Eigenschaftswert vorhanden ist, muss es sich um ein einzelnes Value-Eigenschaftentag handeln, das mit dem Wert identisch ist, der von [IMAPITable:: QueryRows](imapitable-queryrows.md) für die Spalte zurückgegeben würde. 
  
Tabellen Implementierer müssen nur den Standard Anzeigetyp unterstützen und können den MAPI_E_TOO_COMPLEX-Wert zurückgeben, wenn ein Aufrufer die andere Alternative anfordert. Die Möglichkeit zur Unterstützung beider Anzeigetypen ist für Nachrichtenspeicher Anbieter am wichtigsten, die Ordnerinhaltstabellen implementieren. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

