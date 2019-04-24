---
title: Zelle "Flags" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033782
localization_priority: Normal
ms.assetid: 898bf89d-d00f-9769-a89d-787ef708eca5
description: Gibt an, ob die Textrichtung von links nach rechts oder von rechts nach links verläuft.
ms.openlocfilehash: af1e79b13d3d8bab2e7271eb79e68cf931871806
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346221"
---
# <a name="flags-cell-paragraph-section"></a>Zelle "Flags" (Abschnitt "Paragraph")

Gibt an, ob die Textrichtung von links nach rechts oder von rechts nach links verläuft.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Die Textrichtung verläuft von links nach rechts (Standardwert).  <br/> |
|1  <br/> |Die Textrichtung verläuft von rechts nach links.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Wert in dieser Zelle entspricht der Einstellung **Richtung** auf der Registerkarte **Absatz** im Dialogfeld **Text** (Klicken Sie auf der Registerkarte **Start** auf den Pfeil für die **Schriftart** ), der nur angezeigt wird, wenn eine Sprache, die den Text komplexer Skripts verwendet, im Dialogfeld **Microsoft Office-Spracheinstellungen** hinzugefügt. (Klicken Sie auf **Start**, **Alle Programme**, **Microsoft Office**, Microsoft Office- **Tools**und dann auf **Microsoft Office-Spracheinstellungen**.) 
  
Wenn Sie einen Verweis auf die Zelle Flags aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Para. Flags [ *i* ] wobei *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Flags aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionParagraph** <br/> |
|Zeilenindex:  <br/> |**visRowParagraph** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visFlags** <br/> |
   

