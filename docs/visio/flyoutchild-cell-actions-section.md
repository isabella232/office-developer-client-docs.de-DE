---
title: Zelle "FlyoutChild" (Abschnitt "Aktionen")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80003
localization_priority: Normal
ms.assetid: b2405457-843c-0d46-5f4f-9c413826c3f1
description: Bestimmt, ob die Zeile ein untergeordnetes Erweiterungsmenü der letzten Zeile oberhalb befindlichen Zeile ist, bei der es sich nicht um eine untergeordnete Erweiterung handelt.
ms.openlocfilehash: 85524ea33258449f5c9ee0991ac9a64f8f0eebae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420864"
---
# <a name="flyoutchild-cell-actions-section"></a>Zelle "FlyoutChild" (Abschnitt "Aktionen")

Bestimmt, ob die Zeile ein untergeordnetes Erweiterungsmenü der letzten Zeile oberhalb befindlichen Zeile ist, bei der es sich nicht um eine untergeordnete Erweiterung handelt. 
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle FlyoutChild aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes. 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Aktionen. *Name* . FlyoutChildwhere-Aktionen.  *Name* ist der Name der Zeile Actions.  <br/> |
   
Wenn Sie einen Verweis auf die Zelle FlyoutChild aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionAction** <br/> |
|Zeilenindex:  <br/> |**visRowAction** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visActionFlyoutChild** <br/> |
   

