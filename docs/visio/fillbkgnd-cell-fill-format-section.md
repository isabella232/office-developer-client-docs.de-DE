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
ms.openlocfilehash: f4df5d2b44a50380c996b9b2e0f7cda7d212093b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436643"
---
# <a name="fillbkgnd-cell-fill-format-section"></a>Zelle "FillBkgnd" (Abschnitt "Fill Format")

Legt die Farbe fest, die für den Hintergrund (Füllbereich) des Füllmusters des Shapes verwendet wird.
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie die Farbe festlegen möchten, geben Sie eine Zahl von 0 bis 23 ein.
  
Verwenden Sie die RGB-oder die GSL-Funktion, um eine benutzerdefinierte Farbe einzugeben. Der Wert einer benutzerdefinierten Farbe ist ihre RGB-Farbe, und RGB (*r, g, b*) anstelle einer Zahl wird im ShapeSheet-Fenster angezeigt. Bei numerischen Vorgängen haben benutzerdefinierte Farben Werte von 24 und höher. 
  
Die Fülltransparenz für den Hintergrund können Sie in der Zelle FillBkgndTrans festlegen. 
  
Wenn Sie einen Verweis auf die Zelle Zelle FillBkgnd aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle FillBkgnd  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle FillBkgnd aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowFill** <br/> |
| Zellenindex:  <br/> |**visFillBkgnd** <br/> |
   

