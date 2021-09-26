---
title: Zelle "LineColor" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm535
ms.localizationpriority: medium
ms.assetid: d857b48b-9a3d-a1e1-5ad2-6816a492c8ab
description: Definiert die Linienfarbe eines Shapes.
ms.openlocfilehash: 8b3381ead5299420b429cc200daa0450f3f0c0a6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618672"
---
# <a name="linecolor-cell-line-format-section"></a>Zelle "LineColor" (Abschnitt "Line Format")

Definiert die Linienfarbe eines Shapes.
  
## <a name="remarks"></a>Bemerkungen

Um die Linienfarbe festzulegen, geben Sie eine Zahl zwischen 0 und 23 ein, bei der es sich um einen Index in eine Auflistung von Linienfarben handelt. You can view the line color collection in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**). Sie können den Wert von LineColor auch im Dialogfeld **Linie** festlegen. 
  
Verwenden Sie die RGB- oder HSL-Funktion, um eine benutzerdefinierte Farbe einzugeben. Der Wert einer benutzerdefinierten Farbe ist die RGB-Farbe, und RGB( *r, g, b*) anstelle einer Zahl wird im ShapeSheet-Fenster angezeigt. Bei verwendung in numerischen Vorgängen weisen benutzerdefinierte Farben Werte von 24 und höher auf. 
  
Die Transparenz der Linienfarbe können Sie in der Zelle LineColorTrans festlegen.
  
Um einen Verweis auf die Zelle "LineColor" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Linecolor  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle "LineColor" anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowLine** <br/> |
|Zellenindex:  <br/> |**visLineColor** <br/> |
   

