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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359304"
---
# <a name="linecolor-cell-line-format-section"></a>Zelle "LineColor" (Abschnitt "Line Format")

Definiert die Linienfarbe eines Shapes.
  
## <a name="remarks"></a>Bemerkungen

Um die Linienfarbe festzulegen, geben Sie eine Zahl zwischen 0 und 23 ein, bei der es sich um einen Index in einer Auflistung von Linien Farben handelt. Sie können die Linien Farbsammlung im Dialogfeld **Linie** anzeigen (Klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** auf **Linie**, zeigen Sie auf **Gewicht**, und klicken Sie dann auf **Weitere Linien**). Sie können den Wert von Zelle LineColor auch im Dialogfeld **Leitung** festlegen. 
  
Verwenden Sie die RGB-oder die GSL-Funktion, um eine benutzerdefinierte Farbe einzugeben. Der Wert einer benutzerdefinierten Farbe ist ihre RGB-Farbe, und RGB ( *r, g, b*) anstelle einer Zahl wird im ShapeSheet-Fenster angezeigt. Bei numerischen Vorgängen haben benutzerdefinierte Farben Werte von 24 und höher. 
  
Die Transparenz der Linienfarbe können Sie in der Zelle LineColorTrans festlegen.
  
Wenn Sie einen Verweis auf die Zelle Zelle LineColor aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Zelle LineColor  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle LineColor aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowLine** <br/> |
|Zellenindex:  <br/> |**visLineColor** <br/> |
   

