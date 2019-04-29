---
title: Zelle "Prompt" (Abschnitt "User-Defined Cells")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm840
localization_priority: Normal
ms.assetid: d0f91e7d-2373-cfef-e105-fb17e77c7f2d
description: Gibt eine beschreibende Eingabeaufforderung bzw. einen Kommentar für die benutzerdefinierte Zelle an. Die Anwendung schließt den Ansagetext automatisch in Anführungszeichen () ein, um anzugeben, dass es sich um eine Textzeichenfolge handelt. Wenn Sie ein Gleichheitszeichen (=) eingeben und die Anführungszeichen weglassen, können Sie in diese Zelle eine Formel eingeben, die von der Anwendung ausgewertet wird.
ms.openlocfilehash: 7684025e03bd3f4f68893179b1df00cc0cb535e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435726"
---
# <a name="prompt-cell-user-defined-cells-section"></a>Zelle "Prompt" (Abschnitt "User-Defined Cells")

Gibt eine beschreibende Eingabeaufforderung bzw. einen Kommentar für die benutzerdefinierte Zelle an. Die Anwendung schließt den Aufforderungstext automatisch in Anführungszeichen (" ") ein, um anzuzeigen, dass es sich um eine Textzeichenfolge handelt. Wenn Sie ein Gleichheitszeichen (=) eingeben und die Anführungszeichen auslassen, können Sie eine Formel in diese Zelle eingeben, die von der Anwendung berechnet wird.
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle "Ansage" aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Benutzer.  *Name* . Benutzer aufFordern.  *Name* ist der Name der Zeile  <br/> |
   
Wenn Sie einen Verweis auf die Zelle "anSagen" aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionUser** <br/> |
| Zeilenindex:  <br/> |**visRowUser +** *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visUserPrompt** <br/> |
   

