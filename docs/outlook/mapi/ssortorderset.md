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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: db19c3908c419b98b8deb71e2a86d0aa6eebe240
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344422"
---
# <a name="ssortorderset"></a>SSortOrderSet

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Auflistung von Sortierschlüsseln für eine Tabelle, die für die standardmäßige oder kategorisierte Sortierung verwendet wird.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Verwandte Makros:  <br/> |[CbNewSSortOrderSet](cbnewssortorderset.md), [CbSSortOrderSet](cbssortorderset.md), [SizedSSortOrderSet](sizedssortorderset.md) <br/> |
   
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
  
> Die Anzahl der [SSortOrder](ssortorder.md) -Strukturen, die im **einersortierreihenfolge** -Element enthalten sind. 
    
 **cCategories**
  
> Anzahl der Spalten, die als Category-Spalten festgelegt sind. Mögliche Werte reichen von NULL, die eine nicht kategorisierte oder Standardsortierung angibt, bis zu der vom **cSorts** -Element angegebenen Nummer. 
    
 **cExpanded**
  
> Die Anzahl der Kategorien, die in einem erweiterten Zustand beginnen, wobei alle Zeilen, die auf die Kategorie angewendet werden, in der Tabellenansicht sichtbar sind. Mögliche Werte liegen zwischen 0 und der von **cCategories**angegebenen Zahl.
    
 **Einersortierreihenfolge**
  
> Array von **SSortOrder** -Strukturen, die jeweils eine Sortierreihenfolge definieren. 
    
## <a name="remarks"></a>Bemerkungen

Eine **SSortOrderSet** -Struktur wird zum Definieren mehrerer Sortierreihenfolgen für die standardmäßige und kategorisierte Sortierung verwendet. 
  
Jede **SSortOrderSet** -Struktur enthält mindestens eine **SSortOrder** -Struktur, die die Richtung der Sortierung und die Spalte definiert, die als Sortierschlüssel verwendet wird. Für die kategorisierte Sortierung wird diese Spalte als Kategorie verwendet. Wenn der Wert des **cSorts** -Elements den Wert des **cCategories** -Elements überschreitet, gibt es mehr Sortierschlüssel als Kategorien, und Kategorien werden aus den Spalten erstellt, die zuerst im **SSortOrder** -Array angezeigt werden. 
  
Wenn **cSorts** beispielsweise auf 3 festgelegt ist und **cCategories** auf 2 festgelegt ist, werden die Spalten, die durch das **ulPropTag** -Element der ersten beiden Einträge im **SSortOrder** -Array beschrieben werden, als Category-Spalten verwendet. Der erste Eintrag dient als Gruppierung der obersten Ebene; der zweite Eintrag als sekundäre Gruppierung. Alle Zeilen, die mit den beiden rubrikengruppen übereinstimmen, werden mit dem im dritten Eintrag definierten Sortierschlüssel sortiert. 
  
Das **cExpanded** -Element gibt die Anzahl der Kategorien an, die zuerst erweitert werden. Wenn es mehrere Kategorien gibt, beginnt die Tabellen Implementierung mit der ersten Spalte, die als Kategorie festgelegt werden soll, und wird in sequenzieller Reihenfolge mit den nachfolgenden Category-Spalten fortgesetzt, bis die Anzahl der **cCategories** überschritten wurde. Wenn mehr Kategorien Spalten vorhanden sind als erweiterte Spalten, werden die Spalten für die Kategorie reduziert. Wenn **cExpanded** gleich NULL ist, steht der Tabellen Benutzer nur Überschriftenzeilen der obersten Ebene zur Anzeige zur Verfügung. Ist **cExpanded** gleich 1 kleiner als die Anzahl der Kategorien, sind alle Überschriftenzeilen und keine der Blattzeilen verfügbar. Wenn **cExpanded** der Anzahl von Kategorien entspricht, wird die Tabelle vollständig erweitert. 
  
Weitere Informationen zu standardmäßigen und kategorisierten Sortierungen finden Sie unter [Sortieren und kategorisieren](sorting-and-categorization.md).
  
## <a name="see-also"></a>Siehe auch



[SSortOrder](ssortorder.md)
  
[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::CollapseRow](imapitable-collapserow.md)


[MAPI-Strukturen](mapi-structures.md)

