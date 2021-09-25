---
title: Zelle "LineGradientDir" (Abschnitt "Gradient Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c603f9a5-f887-47ce-90bb-d41ec2d1a6a1
description: Bestimmt die Richtung des Linienverlaufs. Ein Farbverlauf kann linear, radial, rechteckig oder einem Pfad folgen.
ms.openlocfilehash: 716d38adf430ba142cc3d67fc6ba50fa435a85f9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603732"
---
# <a name="linegradientdir-cell-gradient-properties-section"></a>Zelle "LineGradientDir" (Abschnitt "Gradient Properties")

Bestimmt die Richtung des Linienverlaufs. Ein Farbverlauf kann linear, radial, rechteckig oder einem Pfad folgen. 
  
> [!NOTE]
> Ein linearer Farbverlauf ist der einzige Farbverlauf, der einen zusätzlichen Winkelwert akzeptiert (wie von der Zelle **"LineGradientDir"** bestimmt). Alle anderen Farbverlaufsrichtungen verfügen über voreingestellte Enumerationen. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Linearer Farbverlauf. Die Zelle **"LineGradientAngle"** bestimmt die Richtung des Farbverlaufs.  <br/> |
|1-7  <br/> |Radiale Farbverläufe. Der Farbverlauf erstreckt sich von einem zentralen Punkt nach außen in einem Kreis.  <br/> |
|8-12  <br/> |Rechteckige Farbverläufe. Der Farbverlauf erstreckt sich als direktionale Linie von einem Ursprung mit einer rechteckigen Ausblendung.  <br/> |
|13  <br/> |Pfadverlauf.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie Folgendes, um einen Verweis auf die **Zelle "LineGradientDir"** anhand des Namens aus einer anderen Formel, anhand des Werts des **N-Attributs** eines **Cell-Elements** oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LineGradientDir  <br/> |
   
Um einen Verweis auf die Zelle **"LineGradientDir"** anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowGradientProperties** <br/> |
| Zellenindex:  <br/> |**visLineGradientDir** <br/> |
   

