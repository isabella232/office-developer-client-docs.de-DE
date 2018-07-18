---
title: Zelle "IsDropTarget" (Abschnitt "Group Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm495
localization_priority: Normal
ms.assetid: 8140fc7b-b99c-54bb-7af3-7de6fcdae7d3
description: Legt fest, ob das Shape durch Ablegen auf einer Gruppe dieser Gruppe hinzugefügt werden kann.
ms.openlocfilehash: 326ead15bcdc72797853daee797d8f08d459a638
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797234"
---
# <a name="isdroptarget-cell-group-properties-section"></a>IsDropTarget Cell (Group Properties Section)

Legt fest, ob das Shape durch Ablegen auf einer Gruppe dieser Gruppe hinzugefügt werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Ein Shape kann durch Ablegen auf einer Gruppe dieser Gruppe hinzugefügt werden.  <br/> |
|FALSE  <br/> |Das Shape kann auf der Gruppe nicht abgelegt werden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können diesen Wert auch festlegen, indem Sie die Gruppe auswählen, auf der Registerkarte [Entwickler](run-in-developer-mode-display-the-developer-tab.md) auf **Verhalten** klicken und anschließend das Kontrollkästchen **Abgelegte Shapes annehmen** aktivieren. 
  
Damit Sie einer Gruppe ein Shape durch Ablegen hinzufügen können, müssen Sie außerdem ein ähnliches Shape-Verhalten aktivieren. Sie müssen das Shape auswählen, auf der Registerkarte Entwickler auf Verhalten klicken und anschließend das Kontrollkästchen Shape beim Ablegen der Gruppe hinzufügen aktivieren. Dieser Wert wird in der Zelle IsDropSource im Abschnitt Miscellaneous gespeichert. 
  
Wenn Sie einen Verweis auf die Zelle IsDropTarget aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |IsDropTarget  <br/> |
   
Wenn Sie einen Verweis auf die Zelle IsDropTarget aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowGroup** <br/> |
|Zellenindex:  <br/> |**visGroupIsDropTarget** <br/> |
   

