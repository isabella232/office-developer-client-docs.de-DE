---
title: Zelle "IsSnapTarget" (Abschnitt "Group Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251626
localization_priority: Normal
ms.assetid: b58131f6-a566-d9ca-bad4-4f4b66e03aaf
description: Legt fest, ob der Einrastvorgang an einer Gruppe oder an einzelnen Shapes in dieser Gruppe erfolgt.
ms.openlocfilehash: cae3eab64be3a91c48ae9f7fb49aa2a321087f43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421445"
---
# <a name="issnaptarget-cell-group-properties-section"></a>Zelle "IsSnapTarget" (Abschnitt "Group Properties")

Legt fest, ob der Einrastvorgang an einer Gruppe oder an einzelnen Shapes in dieser Gruppe erfolgt.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Einrasten an Shapes in einer Gruppe aktivieren.  <br/> |
|FALSE  <br/> |Nur an der Gruppe einrasten.  <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können diesen Wert auch festlegen, indem Sie die Gruppe auswählen, auf der Registerkarte [Entwickler](run-in-developer-mode-display-the-developer-tab.md) auf **Verhalten** klicken und anschließend das Kontrollkästchen **An Mitglieds-Shapes einrasten** aktivieren. 
  
Verwenden Sie folgendes, um einen Verweis auf die Zelle IsSnapTarget anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |IsSnapTarget  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die IsSnapTarget-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowGroup** <br/> |
|Zellenindex:  <br/> |**visGroupIsSnapTarget** <br/> |
   

