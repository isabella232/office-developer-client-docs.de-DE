---
title: Zelle "DisplayMode" (Abschnitt "Group Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251623
localization_priority: Normal
ms.assetid: e6d72529-aa03-e94b-130c-79ed04336299
description: Bestimmt, wie das Gruppen-Shape und dessen Mitglieder angezeigt werden.
ms.openlocfilehash: a49d7a38eac75a2845de0ca3ad22f7cbf79a63df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413185"
---
# <a name="displaymode-cell-group-properties-section"></a>Zelle "DisplayMode" (Abschnitt "Group Properties")

Bestimmt, wie das Gruppen-Shape und dessen Mitglieder angezeigt werden.
  
|**Wert**|**Anzeigemodus**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Blendet das Gruppen-Shape und den Text aus.  <br/> |**visGrpDispModeNone** <br/> |
|1  <br/> |Zeigt das Gruppen-Shape hinter den Mitglieds-Shapes an.  <br/> |**visGrpDispModeBack** <br/> |
|2  <br/> |Zeigt das Gruppen-Shape vor den Mitglieds-Shapes an.  <br/> |**visGrpDispModeFront** <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können diesen Wert auch festlegen,  indem Sie die Gruppe [](run-in-developer-mode-display-the-developer-tab.md) auswählen, auf der Registerkarte Entwickler in der Gruppe **Shape-Entwurf** auf Verhalten klicken und dann in der Datenliste Gruppe einen Anzeigemodus **auswählen.** 
  
Um einen Verweis auf die Zelle DisplayMode anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |DisplayMode  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle DisplayMode nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowGroup** <br/> |
|Zellenindex:  <br/> |**visGroupDisplayMode** <br/> |
   

