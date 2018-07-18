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
ms.openlocfilehash: 6086a45108b88475e250c4d833ab4b740f33b8e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797328"
---
# <a name="linecolor-cell-line-format-section"></a>LineColor Cell (Line Format Section)

Definiert die Linienfarbe eines Shapes.
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie die Linienfarbe festlegen möchten, geben Sie eine Zahl von 0 bis 23 ein. Dies ist ein Index für eine Sammlung von Linienfarben. Sie können diese Sammlung von Linienfarben im Dialogfeld Linie anzeigen (klicken Sie dazu auf der Registerkarte Start in der Gruppe Shape auf Linie, zeigen Sie auf Linienbreite, und klicken Sie dann auf Weitere Linien). Sie können den Wert für die Zelle LineColor auch im Dialogfeld Linie festlegen. 
  
Um eine benutzerdefinierte Farbe eingeben möchten, verwenden Sie die RGB oder HSL-Funktion. Der Wert einer benutzerdefinierten Farbe ist ihre RGB-Farbe und RGB ( *R, g, b*), anstatt eine Zahl in das ShapeSheet-Fenster angezeigt werden. Bei Verwendung in numerischen Operationen haben benutzerdefinierte Farben Werte von 24 und höher. 
  
Die Transparenz der Linienfarbe können Sie in der Zelle LineColorTrans festlegen.
  
Wenn Sie einen Verweis auf die Zelle LineColor aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |LineColor  <br/> |
   
Wenn Sie einen Verweis auf die Zelle LineColor aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowLine** <br/> |
|Zellenindex:  <br/> |**visLineColor** <br/> |
   

