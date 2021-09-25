---
title: Zelle "DisplayMode" (Abschnitt "Group Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251623
ms.localizationpriority: medium
ms.assetid: e6d72529-aa03-e94b-130c-79ed04336299
description: Bestimmt, wie das Gruppen-Shape und dessen Mitglieder angezeigt werden.
ms.openlocfilehash: 22989d22d0e8792e609027662750c4e9f9da73fa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590338"
---
# <a name="displaymode-cell-group-properties-section"></a>Zelle "DisplayMode" (Abschnitt "Group Properties")

Bestimmt, wie das Gruppen-Shape und dessen Mitglieder angezeigt werden.
  
|**Wert**|**Anzeigemodus**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Blendet das Gruppen-Shape und den Text aus.  <br/> |**visGrpDispModeNone** <br/> |
|1  <br/> |Zeigt das Gruppen-Shape hinter den Mitglieds-Shapes an.  <br/> |**visGrpDispModeBack** <br/> |
|2  <br/> |Zeigt das Gruppen-Shape vor den Mitglieds-Shapes an.  <br/> |**visGrpDispModeFront** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Sie können diesen Wert auch festlegen, indem Sie die Gruppe auswählen, auf der Registerkarte ["Entwicklertools"](run-in-developer-mode-display-the-developer-tab.md) in der Gruppe **"Shape-Design"** auf **"Verhalten"** klicken und dann in der **Gruppendatenliste** einen Anzeigemodus auswählen. 
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle "DisplayMode" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |DisplayMode  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle DisplayMode anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowGroup** <br/> |
|Zellenindex:  <br/> |**visGroupDisplayMode** <br/> |
   

