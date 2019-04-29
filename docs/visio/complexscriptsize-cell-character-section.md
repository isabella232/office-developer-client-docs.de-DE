---
title: Zelle "ComplexScriptSize" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033768
localization_priority: Normal
ms.assetid: f58687d7-2ba4-ff77-0bcc-3106867d89de
description: Der Schriftgrad zum Formatieren von Text mit komplexen Schriftzeichen.
ms.openlocfilehash: 38b01c4a0142c7eca2923ee9b13963eaa1a62830
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428438"
---
# <a name="complexscriptsize-cell-character-section"></a>Zelle "ComplexScriptSize" (Abschnitt "Character")

Der Schriftgrad zum Formatieren von Text mit komplexen Schriftzeichen. 
  
## <a name="remarks"></a>Bemerkungen

Schriftgrößen für komplexe Schriftarten werden im Dialogfeld **Text** auf der Registerkarte **Schriftart** angezeigt (Klicken Sie auf der Registerkarte **Start** in der Gruppe **Schriftart** auf den Pfeil). Diese Liste wird nur angezeigt, wenn Sie im Dialogfeld **Microsoft Office-Spracheinstellungen** eine Sprache hinzugefügt haben, die asiatische oder komplexe Schriftzeichen enthält. (Klicken Sie auf **Start**, **Alle Programme**, **Microsoft Office**, Microsoft Office- **Tools**und dann auf **Microsoft Office-Spracheinstellungen**.
  
Sie können diesen Wert als explizite Größe in Punkt oder als Prozentsatz angeben. Wenn Sie einen Prozentsatz angeben, basiert der Wert auf dem Wert in der Zelle Größe. Der Standardwert von 0 (Null) bedeutet 100 %. 
  
Wenn Sie einen Verweis auf die Zelle Zelle ComplexScriptSize aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Char. Zelle ComplexScriptSize [ *i* ] wobei *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle ComplexScriptSize aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionCharacter** <br/> |
|Zeilenindex:  <br/> |**visRowCharacter** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visCharacterComplexScriptSize** <br/> |
   

