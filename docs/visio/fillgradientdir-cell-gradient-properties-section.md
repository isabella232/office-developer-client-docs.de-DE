---
title: Zelle "FillGradientDir" (Abschnitt "Gradient Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e8156ff1-c540-44b8-8b69-ba4d54883260
description: Bestimmt die Richtung des Füllverlaufs. Ein Farbverlauf kann linear, radial, rechteckig oder einem Pfad folgen.
ms.openlocfilehash: 53aad056c7fc1674e00e142fd72a10134103b390
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406717"
---
# <a name="fillgradientdir-cell-gradient-properties-section"></a>Zelle "FillGradientDir" (Abschnitt "Gradient Properties")

Bestimmt die Richtung des Füllverlaufs. Ein Farbverlauf kann linear, radial, rechteckig oder einem Pfad folgen. 
  
> [!NOTE]
> Ein linearer Farbverlauf ist der einzige Farbverlauf, der einen zusätzlichen Winkelwert benötigt (wie durch die **FillGradientDir-Zelle** bestimmt). Alle anderen Verlaufsrichtungen verfügen über vordefinierte Enumerationen. 
  
****

|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Linearer Farbverlauf. Die **Zelle FillGradientAngle** bestimmt die Richtung des Farbverlaufs.  <br/> |
|1-7  <br/> |Radiale Farbverläufe. Der Farbverlauf erstreckt sich von einem zentralen Punkt aus nach außen in einem Kreis.  <br/> |
|8-12  <br/> |Rechteckige Farbverläufe. Der Farbverlauf erstreckt sich als richtungsförmige Linie von einem Ursprung mit einer rechteckigen Ausblendung.  <br/> |
|13  <br/> |Pfadverlauf.  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die **FillGradientDir-Zelle** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | FillGradientDir  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **FillGradientDir-Zelle** nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowGradientProperties** <br/> |
| Zellenindex:  <br/> |**visFillGradientDir** <br/> |
   

