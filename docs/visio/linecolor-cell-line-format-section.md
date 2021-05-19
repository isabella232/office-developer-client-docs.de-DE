---
title: Zelle "LineColor" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm535
localization_priority: Normal
ms.assetid: d857b48b-9a3d-a1e1-5ad2-6816a492c8ab
description: Definiert die Linienfarbe eines Shapes.
ms.openlocfilehash: d0b4ebee6d96bc67c9ca45e8a6194cb91ed6c7f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416937"
---
# <a name="linecolor-cell-line-format-section"></a>Zelle "LineColor" (Abschnitt "Line Format")

Definiert die Linienfarbe eines Shapes.
  
## <a name="remarks"></a>Hinweise

Geben Sie zum Festlegen der Linienfarbe eine Zahl zwischen 0 und 23 ein, bei der es sich um einen Index in einer Auflistung von Linienfarben handelt. Sie können die Linienfarbsammlung im Dialogfeld Linie anzeigen (klicken Sie auf der Registerkarte **Start** in der **Gruppe Shape** auf **Linie,** zeigen Sie auf **Gewichtung,** und klicken Sie dann auf **Weitere Linien**).  Sie können den Wert von LineColor auch im Dialogfeld **Zeile** festlegen. 
  
Verwenden Sie zum Eingeben einer benutzerdefinierten Farbe die RGB- oder HSL-Funktion. Der Wert einer benutzerdefinierten Farbe ist die RGB-Farbe, und RGB( *r, g, b*), anstatt eine Zahl, wird im ShapeSheet-Fenster angezeigt. Bei Verwendung in numerischen Vorgängen haben benutzerdefinierte Farben Werte von 24 und höher. 
  
Die Transparenz der Linienfarbe können Sie in der Zelle LineColorTrans festlegen.
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle LineColor anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |LineColor  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die LineColor-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowLine** <br/> |
|Zellenindex:  <br/> |**visLineColor** <br/> |
   

