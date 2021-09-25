---
title: Zelle "ComplexScriptFont" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60034
ms.localizationpriority: medium
ms.assetid: e1cf9e97-101b-384f-65fe-0169c89dfccc
description: Enthält die Nummer der Schriftart, die zum Formatieren von Text mit komplexen Schriftzeichen verwendet wird. Nummern von Schriftarten variieren entsprechend den im System installierten Schriftarten.
ms.openlocfilehash: c5bba5bcc8881717647f74127d745286615fe660
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566017"
---
# <a name="complexscriptfont-cell-character-section"></a>Zelle "ComplexScriptFont" (Abschnitt "Character")

Enthält die Nummer der Schriftart, die zum Formatieren von Text mit komplexen Schriftzeichen verwendet wird. Nummern von Schriftarten variieren entsprechend den im System installierten Schriftarten. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Komplexe Schriftgraden sind auf der Registerkarte **"Schriftart"** im Dialogfeld **"Text"** aufgeführt (klicken Sie auf der Registerkarte **"Start"** in der Gruppe **"Schriftart"** auf den Pfeil). Diese Liste wird nur angezeigt, wenn Sie im Dialogfeld Microsoft Office **Spracheinstellungen** eine Sprache hinzugefügt haben, die asiatische oder komplexe Skriptzeichen enthält. (Klicken Sie auf **"Start",** auf **"Alle Programme",** auf **Microsoft Office,** auf **Microsoft Office "Extras"** und dann auf **Microsoft Office "Spracheinstellungen".**
  
Die Nummer Null (0) bedeutet, dass keine Schriftart festgelegt ist. Die Schriftart Latein oder die Standardschriftarten werden verwendet.
  
Um einen Verweis auf die Zelle "ComplexScriptSize" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Char.ComplexScriptFont[ *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ComplexScriptFont anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionCharacter** <br/> |
|Zeilenindex:  <br/> |**visRowCharacter**  +   *i* where *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visCharacterComplexScriptFont** <br/> |
   

