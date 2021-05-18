---
title: Zelle "AsianFont" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033764
localization_priority: Normal
ms.assetid: 45bfaaaa-52cc-f8b4-68e7-8b99e5788ce1
description: Enthält die Nummer der Schriftart, die zum Formatieren des Texts mit asiatischen Zeichen verwendet wird. Nummern von Schriftarten variieren entsprechend den im System installierten Schriftarten.
ms.openlocfilehash: 4af7e590a7bd0733ad622f3df259aa6c01837c4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406591"
---
# <a name="asianfont-cell-character-section"></a>Zelle "AsianFont" (Abschnitt "Character")

Enthält die Nummer der Schriftart, die zum Formatieren des Texts mit asiatischen Zeichen verwendet wird. Nummern von Schriftarten variieren entsprechend den im System installierten Schriftarten. 
  
## <a name="remarks"></a>Hinweise

Asiatische Schriftarten sind im Dialogfeld **Text** auf der Registerkarte **Schriftart** aufgelistet. (Klicken Sie auf der Registerkarte **Start** in der Gruppe **Schriftart** auf den Pfeil.) Diese Liste wird nur dann angezeigt, wenn Sie im Dialogfeld **Microsoft Office-Spracheinstellungen** eine Sprache mit asiatischen Zeichen oder komplexen Schriftzeichen hinzugefügt haben. (Klicken Sie auf **Start**, auf **Alle Programme**, auf **Microsoft Office** und auf **Microsoft Office Tools**, und klicken Sie dann auf **Microsoft Office-Spracheinstellungen**.)
  
Die Nummer 0 bedeutet, dass keine Schriftart festgelegt ist. Die Schriftart Latein oder Standardschriftarten werden verwendet, wenn sie die erforderlichen Zeichen enthalten.
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle AsianFont anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Char.AsianFont[ *i*  ] wobei  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle AsianFont nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionCharacter** <br/> |
|Zeilenindex:  <br/> |**visRowCharacter**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visCharacterAsianFont** <br/> |
   

