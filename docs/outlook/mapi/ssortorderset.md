---
title: SSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSortOrderSet
api_type:
- COM
ms.assetid: e7f9be6a-92e7-44a8-93ee-b087713a31df
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: db19c3908c419b98b8deb71e2a86d0aa6eebe240
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438099"
---
# <a name="ssortorderset"></a>SSortOrderSet

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Auflistung von Sortierschlüsseln für eine Tabelle, die für die standard- oder kategorisierte Sortierung verwendet wird.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Makros:  <br/> |[CbNewsSortOrderSet](cbnewssortorderset.md), [CbSSortOrderSet](cbssortorderset.md), [SizedSSortOrderSet](sizedssortorderset.md) <br/> |
   
```cpp
typedef struct _SSortOrderSet
{
  ULONG cSorts;
  ULONG cCategories;
  ULONG cExpanded;
  SSortOrder aSort[MAPI_DIM];
} SSortOrderSet, FAR *LPSSortOrderSet;

```

## <a name="members"></a>Elemente

 **cSorts**
  
> Anzahl der [SSortOrder-Strukturen,](ssortorder.md) die im **aSort-Element enthalten** sind. 
    
 **cCategories**
  
> Anzahl der Spalten, die als Kategoriespalten festgelegt sind. Mögliche Werte reichen von Null, was eine nicht kategorisierte oder standardsortierte Sortierung angibt, bis zur vom **cSorts-Element angegebenen** Nummer. 
    
 **cExpanded**
  
> Anzahl der Kategorien, die in einem erweiterten Zustand beginnen, wobei alle Zeilen, die für die Kategorie gelten, in der Tabellenansicht angezeigt werden. Mögliche Werte liegen zwischen 0 und der durch **cCategories angegebenen Zahl.**
    
 **aSort**
  
> Array von **SSortOrder-Strukturen,** die jeweils eine Sortierreihenfolge definieren. 
    
## <a name="remarks"></a>Hinweise

Eine **SSortOrderSet-Struktur** wird zum Definieren mehrerer Sortierreihenfolgen für die standard- und kategorisierte Sortierung verwendet. 
  
Jede **SSortOrderSet-Struktur** enthält mindestens eine **SSortOrder-Struktur,** die die Sortierrichtung und die Spalte definiert, die als Sortierschlüssel verwendet wird. Für die kategorisierte Sortierung wird diese Spalte als Kategorie verwendet. Wenn der Wert des **cSorts-Members** den Wert des **cCategories-Members** überschreitet, gibt es mehr Sortierschlüssel als Kategorien, und Kategorien werden aus den Spalten erstellt, die zuerst im **SSortOrder-Array** angezeigt werden. 
  
Wenn **cSorts** beispielsweise auf 3 und **cCategories** auf 2 festgelegt ist, werden die Spalten, die vom **ulPropTag-Element** der ersten beiden Einträge im **SSortOrder-Array** beschrieben werden, als Kategoriespalten verwendet. Der erste Eintrag dient als Kategoriegruppe auf oberster Ebene. der zweite Eintrag als sekundäre Gruppierung. Alle Zeilen, die mit den beiden Kategoriespalten übereinstimmen, werden mithilfe des im dritten Eintrag definierten Sortierschlüssels sortiert. 
  
Das **cExpanded-Element** gibt die Anzahl der Kategorien an, die zunächst erweitert werden. Wenn mehrere Kategorien enthalten sind, beginnt die Tabellenimplementierung mit der ersten Spalte, die als Kategorie festgelegt werden soll, und wird in sequenzieller Reihenfolge mit den nachfolgenden Kategoriespalten fortgesetzt, bis die Anzahl der **CCategories** überschritten wurde. Wenn mehr Kategoriespalten als erweiterte Spalten enthalten sind, werden die Kategoriespalten reduziert. Wenn **cExpanded** gleich Null ist, steht dem Tabellenbenutzer nur die Überschriftenzeile auf oberster Ebene zur Anzeige zur Verfügung. Wenn **cExpanded** gleich 1 kleiner als die Anzahl der Kategorien ist, sind alle Überschriftenzeilen und keine der Blattzeilen verfügbar. Wenn **cExpanded** gleich der Anzahl der Kategorien ist, wird die Tabelle vollständig erweitert. 
  
Weitere Informationen zur standard- und kategorisierten Sortierung finden Sie unter [Sorting and Categorization](sorting-and-categorization.md).
  
## <a name="see-also"></a>Siehe auch



[SSortOrder](ssortorder.md)
  
[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::CollapseRow](imapitable-collapserow.md)


[MAPI-Strukturen](mapi-structures.md)

