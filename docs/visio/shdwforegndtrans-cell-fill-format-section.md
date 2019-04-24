---
title: Zelle "ShdwForegndTrans" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253253
localization_priority: Normal
ms.assetid: c42d4d2e-f8f0-bc5b-6018-4bb4ffa81b64
description: Legt die Transparenzstufe für die Farbe fest, die für den Vordergrund (Pinselstrich) des Schattenfüllmusters des Shapes verwendet wird.
ms.openlocfilehash: 0ef3ce525edcce4ccd61f36649ead512545eef58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349098"
---
# <a name="shdwforegndtrans-cell-fill-format-section"></a>Zelle "ShdwForegndTrans" (Abschnitt "Fill Format")

Legt die Transparenzstufe für die Farbe fest, die für den Vordergrund (Pinselstrich) des Schattenfüllmusters des Shapes verwendet wird.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0 - 100  <br/> |Stellt die Transparenz in Prozent dar. Der Standardwert ist 0% (vollständig undurchsichtig).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Werte werden auf ein halbes Prozent gerundet. Ein Wert von 100% bezeichnet völlige Transparenz. Obwohl ein Schatten mit einer vollständig transparenten Füllung auf dem Zeichenblatt als Schatten angezeigt wird, der keine Füllung aufweist, interagiert er mit anderen Objekten auf der Seite auf die gleiche Weise wie bei der Transparenz von 0%.
  
Sie können diesen Wert auch festlegen, indem Sie den Schieberegler im Dialogfeld **Schatten** verwenden (klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** auf **Schatten**, und klicken Sie dann auf **Schattenoptionen**). Dieser Wert bestimmt den Wert der Schattentransparenz sowohl für den Hintergrund als auch für den Vordergrund. Wenn Sie diese Werte unabhängig voneinander festlegen möchten, müssen Sie sie im ShapeSheet-Fenster eingeben.
  
Wenn Sie einen Verweis auf die Zelle Zelle ShdwForegndTrans aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Zelle ShdwForegndTrans  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle ShdwForegndTrans aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowFill** <br/> |
|Zellenindex:  <br/> |**visFillShdwForegndTrans** <br/> |
   

