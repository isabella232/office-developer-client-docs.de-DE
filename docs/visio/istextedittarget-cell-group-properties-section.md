---
title: Zelle "IsTextEditTarget" (Abschnitt "Group Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251627
localization_priority: Normal
ms.assetid: 355cef8b-9213-479a-af95-b591f4bc51ad
description: Definiert die Textzuweisung für eine Gruppe.
ms.openlocfilehash: 78a70dc0398745765bca12a1e768390b35fce8ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432646"
---
# <a name="istextedittarget-cell-group-properties-section"></a>Zelle "IsTextEditTarget" (Abschnitt "Group Properties")

Definiert die Textzuweisung für eine Gruppe.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Dem Gruppen-Shape wird Text hinzugefügt.  <br/> |
|FALSE  <br/> |Text wird dem Shape in der obersten Gruppe des Stapels hinzugefügt.  <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können diesen Wert auch festlegen, indem Sie die Gruppe auswählen, auf der Registerkarte [Entwickler](run-in-developer-mode-display-the-developer-tab.md) auf **Verhalten** klicken und anschließend das Kontrollkästchen **Text der Gruppe bearbeiten** aktivieren. 
  
Bei Gruppen, die mit Versionen vor Visio 2000 erstellt wurden, ist der Standardwert FALSE vorgegeben. Ab Visio 2000-Versionen wird der Standardwert TRUE verwendet. 
  
Verwenden Sie folgendes, um einen Verweis auf die Zelle IsTextEditTarget anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |IsTextEditTarget  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die IsTextEditTarget-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowGroup** <br/> |
|Zellenindex:  <br/> |**visGroupIsTextEditTarget** <br/> |
   

