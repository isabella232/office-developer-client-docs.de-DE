---
title: Zelle "FillGradientDir" (Abschnitt "Gradient Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: e8156ff1-c540-44b8-8b69-ba4d54883260
description: Bestimmt die Richtung des Füllverlaufs. Ein Farbverlauf kann linear, radial, rechteckig oder einem Pfad folgen.
ms.openlocfilehash: 1b467798439383da9a18913ae2efc2e4ee5a08ea
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612834"
---
# <a name="fillgradientdir-cell-gradient-properties-section"></a>Zelle "FillGradientDir" (Abschnitt "Gradient Properties")

Bestimmt die Richtung des Füllverlaufs. Ein Farbverlauf kann linear, radial, rechteckig oder einem Pfad folgen. 
  
> [!NOTE]
> Ein linearer Farbverlauf ist der einzige Farbverlauf, der einen zusätzlichen Winkelwert akzeptiert (wie von der Zelle **FillGradientDir** bestimmt). Alle anderen Farbverlaufsrichtungen verfügen über voreingestellte Enumerationen. 
  
****

|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Linearer Farbverlauf. Die **Zelle "FillGradientAngle"** bestimmt die Richtung des Farbverlaufs.  <br/> |
|1-7  <br/> |Radiale Farbverläufe. Der Farbverlauf erstreckt sich von einem zentralen Punkt nach außen in einem Kreis.  <br/> |
|8-12  <br/> |Rechteckige Farbverläufe. Der Farbverlauf erstreckt sich als direktionale Linie von einem Ursprung mit einer rechteckigen Ausblendung.  <br/> |
|13  <br/> |Pfadverlauf.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Um einen Verweis auf die **Zelle FillGradientDir** anhand des Namens aus einer anderen Formel, anhand des Werts des **N-Attributs** eines **Cell-Elements** oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | FillGradientDir  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **Zelle "FillGradientDir"** anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowGradientProperties** <br/> |
| Zellenindex:  <br/> |**visFillGradientDir** <br/> |
   

