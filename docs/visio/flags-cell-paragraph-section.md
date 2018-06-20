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
ms.openlocfilehash: b471d08556bedf68ce75595b9c211758297e8352
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797010"
---
# <a name="flags-cell-paragraph-section"></a>Flags Cell (Paragraph Section)

Gibt an, ob die Textrichtung von links nach rechts oder von rechts nach links verläuft.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Die Textrichtung verläuft von links nach rechts (Standardwert).  <br/> |
|1  <br/> |Die Textrichtung verläuft von rechts nach links.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Wert in dieser Zelle entspricht der Einstellung **Richtung** auf der Registerkarte **Absatz** im Dialogfeld **Text** (auf der Registerkarte **Start** , klicken Sie auf den Pfeil neben **Schriftart** ), die angezeigt wird, wenn eine Sprache, die komplexe verwendet Text Skripts wurde Klicken Sie im Dialogfeld **Microsoft Office-Spracheinstellungen** hinzugefügt. (Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft Office**, klicken Sie auf **Microsoft Office Tools**, und klicken Sie dann auf **Microsoft Office-Spracheinstellungen**.) 
  
Wenn Sie einen Verweis auf die Zelle Flags nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Para.Flags [ *i* ] wobei *i* = < 1 >, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Flags aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionParagraph** <br/> |
|Zeilenindex:  <br/> |**VisRowParagraph** +  *i* wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visFlags** <br/> |
   

