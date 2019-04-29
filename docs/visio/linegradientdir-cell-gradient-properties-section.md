---
title: Zelle "LineGradientDir" (Abschnitt "Gradient Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c603f9a5-f887-47ce-90bb-d41ec2d1a6a1
description: Bestimmt die Richtung des Linien Verlaufs. Ein Farbverlauf kann linear, radial, rechteckig oder einem Pfad folgen.
ms.openlocfilehash: 05dcc6904a4e67d97c632dba44635936b1c14049
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417987"
---
# <a name="linegradientdir-cell-gradient-properties-section"></a>Zelle "LineGradientDir" (Abschnitt "Gradient Properties")

Bestimmt die Richtung des Linien Verlaufs. Ein Farbverlauf kann linear, radial, rechteckig oder einem Pfad folgen. 
  
> [!NOTE]
> Ein linearer Farbverlauf ist der einzige Farbverlauf, der einen zusätzlichen Winkelwert (gemäß der **LineGradientDir** -Zelle) verwendet. Alle anderen graduellen Richtungen haben vordefinierte Enumerationen. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Linearer Farbverlauf. Die **LineGradientAngle** -Zelle bestimmt die Richtung des Farbverlaufs.  <br/> |
|1-7  <br/> |Radiale Farbverläufe. Der Farbverlauf erstreckt sich von einem zentralen Punkt aus in einem Kreis.  <br/> |
|8-12  <br/> |Rechteckige Farbverläufe. Der Farbverlauf erstreckt sich als richtungsachse von einem Ursprung mit einem rechteckigen verblassen.  <br/> |
|13   <br/> |Pfad Gradient.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **LineGradientDir** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LineGradientDir  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **LineGradientDir** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowGradientProperties** <br/> |
| Zellenindex:  <br/> |**visLineGradientDir** <br/> |
   

