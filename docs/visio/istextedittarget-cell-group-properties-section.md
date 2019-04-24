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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314917"
---
# <a name="istextedittarget-cell-group-properties-section"></a>Zelle "IsTextEditTarget" (Abschnitt "Group Properties")

Definiert die Textzuweisung für eine Gruppe.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Dem Gruppen-Shape wird Text hinzugefügt.  <br/> |
|FALSE  <br/> |Text wird dem Shape in der obersten Gruppe des Stapels hinzugefügt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können diesen Wert auch festlegen, indem Sie die Gruppe auswählen, auf der Registerkarte [Entwickler](run-in-developer-mode-display-the-developer-tab.md) auf **Verhalten** klicken und anschließend das Kontrollkästchen **Text der Gruppe bearbeiten** aktivieren. 
  
Bei Gruppen, die mit Versionen vor Visio 2000 erstellt wurden, ist der Standardwert FALSE vorgegeben. Ab Visio 2000-Versionen wird der Standardwert TRUE verwendet. 
  
Wenn Sie einen Verweis auf die Zelle IsTextEditTarget aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |IsTextEditTarget  <br/> |
   
Wenn Sie einen Verweis auf die Zelle IsTextEditTarget aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowGroup** <br/> |
|Zellenindex:  <br/> |**visGroupIsTextEditTarget** <br/> |
   

