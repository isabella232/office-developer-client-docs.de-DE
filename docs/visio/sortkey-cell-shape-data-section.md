---
title: Zelle "SortKey" (Abschnitt "Shape Data")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251345
ms.localizationpriority: medium
ms.assetid: 67fa5389-f0b9-a9db-8d19-9b16e256dfa3
description: Enthält eine Zeichenfolge, die die Reihenfolge beeinflusst, in der Elemente im Fenster Shape-Daten aufgelistet werden.
ms.openlocfilehash: dc777cf087ba64ba96374e9363eb202be03a9060
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627380"
---
# <a name="sortkey-cell-shape-data-section"></a>Zelle "SortKey" (Abschnitt "Shape Data")

Enthält eine Zeichenfolge, die die Reihenfolge beeinflusst, in der Elemente im Fenster **Shape-Daten** aufgelistet werden. 
  
## <a name="remarks"></a>Bemerkungen

Die zum Vergleichen von SortKey-Werten verwendete Berechnung ist gebietsschemaspezifisch, und die Groß-/Kleinschreibung wird nicht beachtet. Wenn SortKey-Werte gleich sind, werden die Shape-Daten in der Zeilenreihenfolge aufgelistet. Shape-Daten ohne Sortierschlüssel werden nach Shape-Daten aufgelistet, die eine Sortiertaste enthalten.
  
Nachfolgend finden Sie ein Beispiel für die Verwendung von Sortierschlüsseln, um die Shape-Daten im Fenster **Shape-Daten** in der folgenden Reihenfolge anzuzeigen: Artikelnummer, Menge, Preis. 
  
 *Zeile, Beschriftung*  und  *SortKey*  beziehen sich auf Zellen in der Shape-Datenzeile. In diesem Fall wurden diese Zeilen mit Shape-Daten mit einer Bezeichnung versehen. 
  
|**Row**|**Label**|**Sortkey**|
|:-----|:-----|:-----|
| Prop.Item  <br/> | Artikelnummer  <br/> | 1  <br/> |
| Prop.Price  <br/> | Kurs  <br/> | 3  <br/> |
| Prop.Quan  <br/> | Anzahl  <br/> | 2  <br/> |
   
Verwenden Sie zum Abrufen eines Verweises auf die Zelle SortKey anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Prop.  *Name*  . SortKey where Prop.  *Name*  ist der Name der benutzerdefinierten Eigenschaftszeile.  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle SortKey anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionProp** <br/> |
| Zeilenindex:  <br/> |**visRowProp**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCustPropsSortKey** <br/> |
   

