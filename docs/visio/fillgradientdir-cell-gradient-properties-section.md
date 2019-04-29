---
title: Zelle "FillGradientDir" (Abschnitt "Gradient Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e8156ff1-c540-44b8-8b69-ba4d54883260
description: Bestimmt die Richtung des Füll Verlaufs. Ein Farbverlauf kann linear, radial, rechteckig oder einem Pfad folgen.
ms.openlocfilehash: 53aad056c7fc1674e00e142fd72a10134103b390
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406717"
---
# <a name="fillgradientdir-cell-gradient-properties-section"></a>Zelle "FillGradientDir" (Abschnitt "Gradient Properties")

Bestimmt die Richtung des Füll Verlaufs. Ein Farbverlauf kann linear, radial, rechteckig oder einem Pfad folgen. 
  
> [!NOTE]
> Ein linearer Farbverlauf ist der einzige Farbverlauf, der einen zusätzlichen Winkelwert (gemäß der **FillGradientDir** -Zelle) verwendet. Alle anderen graduellen Richtungen haben vordefinierte Enumerationen. 
  
****

|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Linearer Farbverlauf. Die **FillGradientAngle** -Zelle bestimmt die Richtung des Farbverlaufs.  <br/> |
|1-7  <br/> |Radiale Farbverläufe. Der Farbverlauf erstreckt sich von einem zentralen Punkt aus in einem Kreis.  <br/> |
|8-12  <br/> |Rechteckige Farbverläufe. Der Farbverlauf erstreckt sich als richtungsachse von einem Ursprung mit einem rechteckigen verblassen.  <br/> |
|13   <br/> |Pfad Gradient.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **FillGradientDir** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | FillGradientDir  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **FillGradientDir** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowGradientProperties** <br/> |
| Zellenindex:  <br/> |**visFillGradientDir** <br/> |
   

