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
ms.openlocfilehash: e8d85ba55c5aa2f3780ad8e04cf1326cd7c35865
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575938"
---
# <a name="ssortorderset"></a>SSortOrderSet

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Definiert eine Auflistung von Sortierschlüsseln für eine Tabelle, die für die Standard- oder kategorisierte Sortierung verwendet wird.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
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
  
> Anzahl der [SSortOrder](ssortorder.md) -Strukturen, die im **aSort** -Member enthalten sind. 
    
 **cCategories**
  
> Anzahl der Spalten, die die Kategorie Spalten festgelegt sind. Mögliche Werte reichen von 0 (null), die eine Sortierung nicht kategorisiert oder standard angibt, der durch die **cSorts** Mitglied angegebenen Nummer. 
    
 **cExpanded**
  
> Anzahl der Kategorien, die im erweiterten Zustand, starten, in dem alle Zeilen, die für die Kategorie gelten in der Tabellenansicht angezeigt werden. Mögliche Werte reichen von 0 bis auf die Anzahl von **cCategories**angegeben.
    
 **aSort**
  
> Array von **SSortOrder** -Strukturen, jede eine Sortierreihenfolge definieren. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine **SSortOrderSet** Struktur wird für die Definition mehrerer Sortierreihenfolgen für die Standard- und kategorisierte Sortierung verwendet. 
  
Jede **SSortOrderSet** -Datenstruktur enthält mindestens eine **SSortOrder** Struktur definieren die Richtung der Sortierung und die Spalte, die als Sortierschlüssel verwendet werden. Diese Spalte wird für die kategorisierten Sortierung als die Kategorie verwendet. Wenn der Wert des Elements **cSorts** den Wert des Elements **cCategories** überschreitet, es sind weitere Sortierschlüsseln als Kategorien, und Kategorien aus der Spalten, die im Array **SSortOrder** ersten angezeigt werden erstellt werden. 
  
Wenn **cSorts** auf 3 festgelegt ist und **cCategories** auf 2 festgelegt wird, werden die Spalten beschrieben, die von der **UlPropTag** Mitglied die ersten beiden Einträge im Array **SSortOrder** wie die Kategorie Spalten verwendet. Der erste Eintrag dient als die Kategorie der obersten Ebene gruppieren; der zweite Eintrag als sekundäre Gruppierung. Alle Zeilen, die die Spalten zwei Kategorie entsprechen werden mit den Sortierschlüssel definiert im dritten Eintrag sortiert. 
  
Das **cExpanded** -Element gibt die Anzahl der Rubriken, die auf den ersten erweitert werden. Wenn mehrere Kategorien vorhanden sind, wird die Implementierung der Tabelle beginnt mit der ersten Spalte, als Kategorie festgelegt werden sollen und sequenziell mit den nachfolgenden Kategorie Spalten wird fortgesetzt, bis die Anzahl der **cCategories** überschritten wurde. Wenn mehrere Kategorie Spalten als erweiterte Spalten vorhanden sind vorhanden sind, werden die Spalten Kategorie reduziert. Wenn **cExpanded** gleich NULL ist, steht nur die oberste Ebene Überschrift-Zeile der Tabelle Benutzer für die Anzeige. Wenn **cExpanded** eins kleiner ist als die Anzahl der Rubriken gleich ist, sind alle Überschriftenzeilen und keine Endknoten Zeile verfügbar. Wenn die Anzahl der Rubriken **cExpanded** entspricht, wird die Tabelle vollständig erweitert. 
  
Weitere Informationen zu Standard- und kategorisierten Sortieren finden Sie unter [Sortieren und Kategorisierung](sorting-and-categorization.md).
  
## <a name="see-also"></a>Siehe auch



[SSortOrder](ssortorder.md)
  
[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::CollapseRow](imapitable-collapserow.md)


[MAPI-Strukturen](mapi-structures.md)

