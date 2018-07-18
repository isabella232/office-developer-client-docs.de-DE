---
title: LineGradientDir Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c603f9a5-f887-47ce-90bb-d41ec2d1a6a1
description: Bestimmt die Richtung des Farbverlaufs Linie. Ein Farbverlauf kann linear, radial, rechteckigen verwendet werden, oder führen Sie einen Pfad.
ms.openlocfilehash: 6243d7a6b470db0915ba6fc462f05b72a9814f66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797335"
---
# <a name="linegradientdir-cell-gradient-properties-section"></a>LineGradientDir Cell (Gradient Properties Section)

Bestimmt die Richtung des Farbverlaufs Linie. Ein Farbverlauf kann linear, radial, rechteckigen verwendet werden, oder führen Sie einen Pfad. 
  
> [!NOTE]
> Ein linearer Farbverlauf ist die einzige Farbverlauf, der einen zusätzliche Angle-Wert (wie durch **LineGradientDir** Zelle festgelegt) akzeptiert. Alle anderen Farbverlauf Richtungen Voreinstellung Aufzählungen enthalten. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Linearer Farbverlauf Die Zelle **LineGradientAngle** bestimmt die Richtung des Farbverlaufs.  <br/> |
|1 bis 7  <br/> |Radial Verläufe. In einem Kreis erweitert von einem zentralen Punkt nach außen des Farbverlaufs.  <br/> |
|8 bis 12  <br/> |Rechteckige Verläufe. Der Farbverlauf erweitert als Richtungspfeile Linie vom Ursprung mit einem rechteckigen einblenden.  <br/> |
|13  <br/> |Pfadfarbverlauf.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **LineGradientDir** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LineGradientDir  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **LineGradientDir** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowGradientProperties** <br/> |
| Zellenindex:  <br/> |**visLineGradientDir** <br/> |
   

