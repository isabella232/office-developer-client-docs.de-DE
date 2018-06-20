---
title: FillGradientDir Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e8156ff1-c540-44b8-8b69-ba4d54883260
description: Bestimmt die Richtung des Farbverlaufs Füllung. Ein Farbverlauf kann linear, radial, rechteckigen verwendet werden, oder führen Sie einen Pfad.
ms.openlocfilehash: 9b4226892e70fcffe7a78d109bd852e6d4f93838
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796999"
---
# <a name="fillgradientdir-cell-gradient-properties-section"></a>FillGradientDir Cell (Gradient Properties Section)

Bestimmt die Richtung des Farbverlaufs Füllung. Ein Farbverlauf kann linear, radial, rechteckigen verwendet werden, oder führen Sie einen Pfad. 
  
> [!NOTE]
> Ein linearer Farbverlauf ist die einzige Farbverlauf, der einen zusätzliche Angle-Wert (wie durch **FillGradientDir** Zelle festgelegt) akzeptiert. Alle anderen Farbverlauf Richtungen Voreinstellung Aufzählungen enthalten. 
  
****

|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Linearer Farbverlauf Die Zelle **FillGradientAngle** bestimmt die Richtung des Farbverlaufs.  <br/> |
|1 bis 7  <br/> |Radial Verläufe. In einem Kreis erweitert von einem zentralen Punkt nach außen des Farbverlaufs.  <br/> |
|8 bis 12  <br/> |Rechteckige Verläufe. Der Farbverlauf erweitert als Richtungspfeile Linie vom Ursprung mit einem rechteckigen einblenden.  <br/> |
|13  <br/> |Pfadfarbverlauf.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle **FillGradientDir** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | FillGradientDir  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **FillGradientDir** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowGradientProperties** <br/> |
| Zellenindex:  <br/> |**visFillGradientDir** <br/> |
   

