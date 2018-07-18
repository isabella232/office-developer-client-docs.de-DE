---
title: Zelle "FillBkgnd" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm365
localization_priority: Normal
ms.assetid: 603d698f-a025-538c-8767-18e7716a9a5f
description: Legt die Farbe fest, die für den Hintergrund (Füllbereich) des Füllmusters des Shapes verwendet wird.
ms.openlocfilehash: d1222026887313d7737a3a0ded9e798e9bf5ea30
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796994"
---
# <a name="fillbkgnd-cell-fill-format-section"></a>FillBkgnd Cell (Fill Format Section)

Legt die Farbe fest, die für den Hintergrund (Füllbereich) des Füllmusters des Shapes verwendet wird.
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie die Farbe festlegen möchten, geben Sie eine Zahl von 0 bis 23 ein.
  
Wenn Sie eine benutzerdefinierte Farbe eingeben möchten, verwenden Sie die Funktionen RGB bzw. HSL. Der Wert einer benutzerdefinierten Farbe ist ihre RGB-Farbe, daher wird im ShapeSheet-Fenster statt einer Zahl der RGB-Wert (r, g, b) angezeigt. Bei Verwendung von numerischen Operationen haben benutzerdefinierte Farben Werte von 24 und höher. 
  
Die Fülltransparenz für den Hintergrund können Sie in der Zelle FillBkgndTrans festlegen. 
  
Wenn Sie einen Verweis auf die Zelle FillBkgnd aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | FillBkgnd  <br/> |
   
Wenn Sie einen Verweis auf die Zelle FillBkgnd aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowFill** <br/> |
| Zellenindex:  <br/> |**visFillBkgnd** <br/> |
   

