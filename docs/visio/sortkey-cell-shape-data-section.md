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
ms.openlocfilehash: 1dbc093f2cee509531b8148563fbdb1a777a349f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798174"
---
# <a name="sortkey-cell-shape-data-section"></a>Zelle "SortKey" (Abschnitt "Shape Data")

Enthält eine Zeichenfolge, die die Reihenfolge beeinflusst, in der Elemente im Fenster **Shape-Daten** aufgelistet werden. 
  
## <a name="remarks"></a>Bemerkungen

Die Berechnung zum Vergleich von Werten SortKey ist gebietsschemaspezifischen und zwischen Groß-und Kleinschreibung. Wenn beachtet werden, werden die Shape-Daten in der Zeilenreihenfolge aufgeführt. Shape-Daten, die keine Sortierschlüssel werden nach Shape-Daten aufgeführt, die einen Sortierschlüssel enthalten.
  
Nachfolgend finden Sie ein Beispiel für die Verwendung von Sortierschlüsseln, um die Shape-Daten im Fenster **Shape-Daten** in der folgenden Reihenfolge anzuzeigen: Artikelnummer, Menge, Preis. 
  
 *Zeile, Beschriftung* und *SortKey* verweisen auf Zellen in der Zeile mit Shape-Daten. In diesem Fall wurden die Shape-Datenzeilen benannt. 
  
|**Row**|**Label**|**SortKey**|
|:-----|:-----|:-----|
| Prop.Item  <br/> | Artikelnummer  <br/> | 1  <br/> |
| Prop.Price  <br/> | Preis  <br/> | 3  <br/> |
| Prop.Quan  <br/> | Menge  <br/> | 2  <br/> |
   
Wenn Sie einen Verweis auf die Zelle SortKey aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Eigenschaft.  *Name* . SortKey wobei Prop.  *Name* ist der Name der Zeile mit der benutzerdefinierten Eigenschaft  <br/> |
   
Wenn Sie einen Verweis auf die Zelle SortKey aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionProp** <br/> |
| Zeilenindex:  <br/> |**VisRowProp** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCustPropsSortKey** <br/> |
   

