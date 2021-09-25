---
title: Zelle "ShdwForegndTrans" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253253
ms.localizationpriority: medium
ms.assetid: c42d4d2e-f8f0-bc5b-6018-4bb4ffa81b64
description: Legt die Transparenzstufe für die Farbe fest, die für den Vordergrund (Pinselstrich) des Schattenfüllmusters des Shapes verwendet wird.
ms.openlocfilehash: 362e4271d44cc44741ef90dc04392b6dda908e51
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607682"
---
# <a name="shdwforegndtrans-cell-fill-format-section"></a>Zelle "ShdwForegndTrans" (Abschnitt "Fill Format")

Legt die Transparenzstufe für die Farbe fest, die für den Vordergrund (Pinselstrich) des Schattenfüllmusters des Shapes verwendet wird.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0 - 100  <br/> |Stellt die Transparenz in Prozent dar. Der Standardwert ist 0% (vollständig undurchsichtig).  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Werte werden auf ein halbes Prozent gerundet. Ein Wert von 100% bezeichnet völlige Transparenz. Obwohl ein Schatten mit einer vollständig transparenten Füllung auf dem Zeichenblatt wie ein Schatten ohne Füllung angezeigt wird, interagiert er mit anderen Objekten auf dem Zeichenblatt auf die gleiche Weise wie bei einer Transparenz von 0 %.
  
Sie können diesen Wert auch festlegen, indem Sie den Schieberegler im Dialogfeld **Schatten** verwenden (klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** auf **Schatten**, und klicken Sie dann auf **Schattenoptionen**). Dieser Wert bestimmt den Wert der Schattentransparenz sowohl für den Hintergrund als auch für den Vordergrund. Wenn Sie diese Werte unabhängig voneinander festlegen möchten, müssen Sie sie im ShapeSheet-Fenster eingeben.
  
Verwenden Sie zum Abrufen eines Verweises auf die Zelle "ShdwForegndTrans" anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ShdwForegndTrans  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ShdwForegndTrans anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowFill** <br/> |
|Zellenindex:  <br/> |**visFillShdwForegndTrans** <br/> |
   

