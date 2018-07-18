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
description: Gibt eine beschreibende Eingabeaufforderung bzw. einen Kommentar für die benutzerdefinierte Zelle an. Die Anwendung schließt den Prompt Text automatisch in Anführungszeichen (), um anzugeben, dass es sich um eine Textzeichenfolge ist. Wenn Sie ein Gleichheitszeichen (=) eingeben und die Anführungszeichen auslassen, können Sie eine Formel in dieser Zelle eingeben, die die Anwendung ausgewertet wird.
ms.openlocfilehash: a7f8757af3e324a89f49bf5d19185b7a22173ff5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797749"
---
# <a name="prompt-cell-user-defined-cells-section"></a>Prompt Cell (User-Defined Cells Section)

Gibt eine beschreibende Eingabeaufforderung bzw. einen Kommentar für die benutzerdefinierte Zelle an. Die Anwendung schließt den Aufforderungstext automatisch in Anführungszeichen (" ") ein, um anzuzeigen, dass es sich um eine Textzeichenfolge handelt. Wenn Sie ein Gleichheitszeichen (=) eingeben und die Anführungszeichen auslassen, können Sie eine Formel in diese Zelle eingeben, die von der Anwendung berechnet wird.
  
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle Prompt aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Benutzer.  *Name* . Prompt Where Benutzer.  *Name* ist der Zeilenname  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Prompt aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionUser** <br/> |
| Zeilenindex:  <br/> |**VisRowUser +** *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visUserPrompt** <br/> |
   

