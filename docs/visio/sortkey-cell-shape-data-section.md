---
title: Zelle "SortKey" (Abschnitt "Shape Data")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251345
localization_priority: Normal
ms.assetid: 67fa5389-f0b9-a9db-8d19-9b16e256dfa3
description: Enthält eine Zeichenfolge, die die Reihenfolge beeinflusst, in der Elemente im Fenster Shape-Daten aufgelistet werden.
ms.openlocfilehash: d166ea18a36f6a4101b8933fce804be2243954bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417854"
---
# <a name="sortkey-cell-shape-data-section"></a>Zelle "SortKey" (Abschnitt "Shape Data")

Enthält eine Zeichenfolge, die die Reihenfolge beeinflusst, in der Elemente im Fenster **Shape-Daten** aufgelistet werden. 
  
## <a name="remarks"></a>Bemerkungen

Die zum Vergleichen von SortKey-Werten verwendete Berechnung ist gebietsschemaspezifisch und die Groß-/Kleinschreibung wird nicht berücksichtigt. Wenn SortKey-Werte gleich sind, werden die Shape-Daten in der Zeilenreihenfolge aufgeführt. Shape-Daten ohne Sortierschlüssel werden nach Shape-Daten aufgelistet, die einen Sortierschlüssel enthalten.
  
Nachfolgend finden Sie ein Beispiel für die Verwendung von Sortierschlüsseln, um die Shape-Daten im Fenster **Shape-Daten** in der folgenden Reihenfolge anzuzeigen: Artikelnummer, Menge, Preis. 
  
 *Zeile, Beschriftung* und *SortKey* verweisen auf Zellen in der Shape-Datenzeile. In diesem Fall wurden diese Zeilen mit Shape-Daten mit einer Bezeichnung versehen. 
  
|**Row**|**Label**|**SortKey**|
|:-----|:-----|:-----|
| Prop. Item  <br/> | Artikelnummer  <br/> | 1  <br/> |
| Prop. Price  <br/> | Kurs  <br/> | 3  <br/> |
| Prop. Quan  <br/> | Anzahl  <br/> | 2  <br/> |
   
Wenn Sie einen Verweis auf die Zelle SortKey aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Prop.  *Name* . SortKey, wobei Prop.  *Name* ist der Name der benutzerdefinierten Eigenschaftszeile.  <br/> |
   
Wenn Sie einen Verweis auf die Zelle "SortKey" aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionProp** <br/> |
| Zeilenindex:  <br/> |**visRowProp** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCustPropsSortKey** <br/> |
   

