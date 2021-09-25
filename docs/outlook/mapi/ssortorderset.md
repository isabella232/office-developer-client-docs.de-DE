---
title: SSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SSortOrderSet
api_type:
- COM
ms.assetid: e7f9be6a-92e7-44a8-93ee-b087713a31df
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e65635a8e5ea51bfb3c8a083160ed346cf7dcfc2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566409"
---
# <a name="ssortorderset"></a>SSortOrderSet

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Auflistung von Sortierschlüsseln für eine Tabelle, die für die Standard- oder kategorisierte Sortierung verwendet wird.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Makros:  <br/> |[CbNewsSortOrderSet](cbnewssortorderset.md), [CbsSortOrderSet](cbssortorderset.md), [SizedSSortOrderSet](sizedssortorderset.md) <br/> |
   
```cpp
typedef struct _SSortOrderSet
{
  ULONG cSorts;
  ULONG cCategories;
  ULONG cExpanded;
  SSortOrder aSort[MAPI_DIM];
} SSortOrderSet, FAR *LPSSortOrderSet;

```

## <a name="members"></a>Members

 **cSorts**
  
> Anzahl der [SSortOrder-Strukturen,](ssortorder.md) die im **aSort-Element** enthalten sind. 
    
 **cCategories**
  
> Anzahl der Spalten, die als Rubrikenspalten festgelegt sind. Mögliche Werte reichen von Null, was eine nicht kategorisierte oder standardsortierte Sortierung angibt, bis zu der vom **cSorts-Element angegebenen** Zahl. 
    
 **cExpanded**
  
> Anzahl der Kategorien, die in einem erweiterten Zustand beginnen, wobei alle Zeilen, die für die Kategorie gelten, in der Tabellenansicht angezeigt werden. Mögliche Werte liegen zwischen 0 und der durch **cCategories angegebenen** Zahl.
    
 **aSort**
  
> Array von **SSortOrder-Strukturen,** die jeweils eine Sortierreihenfolge definieren. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine **SSortOrderSet-Struktur** wird verwendet, um mehrere Sortierreihenfolgen für die Standard- und kategorisierte Sortierung zu definieren. 
  
Jede **SSortOrderSet-Struktur** enthält mindestens eine **SSortOrder-Struktur,** die die Sortierrichtung und die Spalte definiert, die als Sortierschlüssel verwendet wird. Für die kategorisierte Sortierung wird diese Spalte als Kategorie verwendet. Wenn der Wert des **cSorts-Elements** den Wert des **cCategories-Elements** überschreitet, gibt es mehr Sortierschlüssel als Kategorien, und Kategorien werden anhand der Spalten erstellt, die zuerst im **SSortOrder-Array** angezeigt werden. 
  
Wenn z. **B. cSorts** auf 3 und **cCategories** auf 2 festgelegt ist, werden die Spalten, die vom **ulPropTag-Element** der ersten beiden Einträge im **SSortOrder-Array** beschrieben werden, als Kategoriespalten verwendet. Der erste Eintrag dient als Kategoriegruppierung auf oberster Ebene. der zweite Eintrag als sekundäre Gruppierung. Alle Zeilen, die den beiden Kategoriespalten entsprechen, werden mithilfe der im dritten Eintrag definierten Sortiertaste sortiert. 
  
Das **Element "cExpanded"** gibt die Anzahl der Kategorien an, die zuerst erweitert werden. Wenn mehrere Kategorien vorhanden sind, beginnt die Tabellenimplementierung mit der ersten Spalte, die als Kategorie festgelegt werden soll, und wird in sequenzieller Reihenfolge mit den nachfolgenden Kategoriespalten fortgesetzt, bis die Anzahl der **cCategories** überschritten wurde. Wenn mehr Rubrikenspalten vorhanden sind als erweiterte Spalten, werden die Rubrikenspalten reduziert. Wenn **cExpanded** gleich Null ist, steht dem Tabellenbenutzer nur die Überschriftenzeile der obersten Ebene zur Anzeige zur Verfügung. Wenn **cExpanded** gleich 1 kleiner als die Anzahl der Kategorien ist, sind alle Überschriftenzeilen und keine der blattförmigen Zeilen verfügbar. Wenn **cExpanded** gleich der Anzahl der Kategorien ist, wird die Tabelle vollständig erweitert. 
  
Weitere Informationen zur standard- und kategorisierten Sortierung finden Sie unter [Sortieren und Kategorisieren.](sorting-and-categorization.md)
  
## <a name="see-also"></a>Siehe auch



[SSortOrder](ssortorder.md)
  
[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::CollapseRow](imapitable-collapserow.md)


[MAPI-Strukturen](mapi-structures.md)

