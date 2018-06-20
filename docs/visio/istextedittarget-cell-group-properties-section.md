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
ms.openlocfilehash: 65baf90254f6b213efea04739d8e4a66952b2856
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797262"
---
# <a name="istextedittarget-cell-group-properties-section"></a>IsTextEditTarget Cell (Group Properties Section)

Definiert die Textzuweisung für eine Gruppe.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Dem Gruppen-Shape wird Text hinzugefügt.  <br/> |
|FALSE  <br/> |Text wird dem Shape in der obersten Gruppe des Stapels hinzugefügt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können diesen Wert auch festlegen, indem Auswählen der Gruppe auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) **Verhalten** klicken und anschließend das Kontrollkästchen **Text der Gruppe bearbeiten** . 
  
Bei Gruppen, die mit Versionen vor Visio 2000 erstellt wurden, ist der Standardwert FALSE vorgegeben. Ab Visio 2000-Versionen wird der Standardwert TRUE verwendet. 
  
Wenn Sie einen Verweis auf die Zelle IsTextEditTarget nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |IsTextEditTarget  <br/> |
   
Wenn Sie einen Verweis auf die Zelle IsTextEditTarget aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowGroup** <br/> |
|Zellenindex:  <br/> |**visGroupIsTextEditTarget** <br/> |
   

