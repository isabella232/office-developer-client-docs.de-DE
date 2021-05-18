---
title: Zelle "ComplexScriptFont" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60034
localization_priority: Normal
ms.assetid: e1cf9e97-101b-384f-65fe-0169c89dfccc
description: Enthält die Nummer der Schriftart, die zum Formatieren von Text mit komplexen Schriftzeichen verwendet wird. Nummern von Schriftarten variieren entsprechend den im System installierten Schriftarten.
ms.openlocfilehash: 5ec8deb59b875a01592b6d7b652204089ecf11e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404834"
---
# <a name="complexscriptfont-cell-character-section"></a>Zelle "ComplexScriptFont" (Abschnitt "Character")

Enthält die Nummer der Schriftart, die zum Formatieren von Text mit komplexen Schriftzeichen verwendet wird. Nummern von Schriftarten variieren entsprechend den im System installierten Schriftarten. 
  
## <a name="remarks"></a>Hinweise

Komplexe Schriftgrößen für Skripts werden auf der Registerkarte **Schriftart** im  Dialogfeld **Text** aufgeführt (klicken Sie auf der Registerkarte **Start** auf den Pfeil in der Gruppe Schriftart). Diese Liste wird nur angezeigt, wenn Sie eine Sprache mit  asiatischen oder komplexen Skriptzeichen im Dialogfeld Spracheinstellungen Microsoft Office hinzugefügt haben. (Klicken **Sie auf Start,** **klicken** Sie auf Alle Programme, **Microsoft Office**, klicken Sie **Microsoft Office Tools,** und klicken Sie **dann auf Microsoft Office Spracheinstellungen**.
  
Die Nummer Null (0) bedeutet, dass keine Schriftart festgelegt ist. Die Schriftart Latein oder die Standardschriftarten werden verwendet.
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle ComplexScriptSize anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Char.ComplexScriptFont[ *i*  ] wobei  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die ComplexScriptFont-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionCharacter** <br/> |
|Zeilenindex:  <br/> |**visRowCharacter**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visCharacterComplexScriptFont** <br/> |
   

