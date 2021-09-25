---
title: Zelle "Prompt" (Abschnitt "User-Defined Cells")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm840
ms.localizationpriority: medium
ms.assetid: d0f91e7d-2373-cfef-e105-fb17e77c7f2d
description: Gibt eine beschreibende Eingabeaufforderung bzw. einen Kommentar für die benutzerdefinierte Zelle an. Die Anwendung schließt den Eingabeaufforderungstext automatisch in Anführungszeichen () ein, um anzugeben, dass es sich um eine Textzeichenfolge handelt. Wenn Sie ein Gleichheitszeichen (=) eingeben und die Anführungszeichen weglassen, können Sie eine Formel in diese Zelle eingeben, die von der Anwendung ausgewertet wird.
ms.openlocfilehash: 158925e01f710053998189367a9182b2b3eda4b0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623180"
---
# <a name="prompt-cell-user-defined-cells-section"></a>Zelle "Prompt" (Abschnitt "User-Defined Cells")

Gibt eine beschreibende Eingabeaufforderung bzw. einen Kommentar für die benutzerdefinierte Zelle an. Die Anwendung schließt den Aufforderungstext automatisch in Anführungszeichen (" ") ein, um anzuzeigen, dass es sich um eine Textzeichenfolge handelt. Wenn Sie ein Gleichheitszeichen (=) eingeben und die Anführungszeichen auslassen, können Sie eine Formel in diese Zelle eingeben, die von der Anwendung berechnet wird.
  
## <a name="remarks"></a>Bemerkungen

Um einen Verweis auf die Eingabeaufforderungszelle anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Benutzer.  *Name*  . Eingabeaufforderung, wobei Benutzer.  *Name*  ist der Zeilenname  <br/> |
   
Um einen Verweis auf die Eingabeaufforderungszelle anhand des Indexes aus einem Programm abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionUser** <br/> |
| Zeilenindex:  <br/> |**visRowUser +** *i*            where  *i*  = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visUserPrompt** <br/> |
   

