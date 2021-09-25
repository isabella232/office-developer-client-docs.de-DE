---
title: Zelle "AsianFont" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033764
ms.localizationpriority: medium
ms.assetid: 45bfaaaa-52cc-f8b4-68e7-8b99e5788ce1
description: Enthält die Nummer der Schriftart, die zum Formatieren des Texts mit asiatischen Zeichen verwendet wird. Nummern von Schriftarten variieren entsprechend den im System installierten Schriftarten.
ms.openlocfilehash: f7a831707e79d0afd2fdc08c21d5f074148902b5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603900"
---
# <a name="asianfont-cell-character-section"></a>Zelle "AsianFont" (Abschnitt "Character")

Enthält die Nummer der Schriftart, die zum Formatieren des Texts mit asiatischen Zeichen verwendet wird. Nummern von Schriftarten variieren entsprechend den im System installierten Schriftarten. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Asiatische Schriftarten sind im Dialogfeld **Text** auf der Registerkarte **Schriftart** aufgelistet. (Klicken Sie auf der Registerkarte **Start** in der Gruppe **Schriftart** auf den Pfeil.) Diese Liste wird nur dann angezeigt, wenn Sie im Dialogfeld **Microsoft Office-Spracheinstellungen** eine Sprache mit asiatischen Zeichen oder komplexen Schriftzeichen hinzugefügt haben. (Klicken Sie auf **Start**, auf **Alle Programme**, auf **Microsoft Office** und auf **Microsoft Office Tools**, und klicken Sie dann auf **Microsoft Office-Spracheinstellungen**.)
  
Die Nummer 0 bedeutet, dass keine Schriftart festgelegt ist. Die Schriftart Latein oder Standardschriftarten werden verwendet, wenn sie die erforderlichen Zeichen enthalten.
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle AsianFont anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Char.AsianFont[ *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle AsianFont anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionCharacter** <br/> |
|Zeilenindex:  <br/> |**visRowCharacter**  +   *i* where *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visCharacterAsianFont** <br/> |
   

