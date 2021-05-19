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
ms.openlocfilehash: 50f545b3cbd4f7e1541a7f5e8ca32c34d0429c5e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410791"
---
# <a name="isdroptarget-cell-group-properties-section"></a>Zelle "IsDropTarget" (Abschnitt "Group Properties")

Legt fest, ob das Shape durch Ablegen auf einer Gruppe dieser Gruppe hinzugefügt werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Ein Shape kann durch Ablegen auf einer Gruppe dieser Gruppe hinzugefügt werden.  <br/> |
|FALSE  <br/> |Das Shape kann auf der Gruppe nicht abgelegt werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können diesen Wert auch festlegen, indem Sie die Gruppe auswählen, auf der Registerkarte [Entwickler](run-in-developer-mode-display-the-developer-tab.md) auf **Verhalten** klicken und anschließend das Kontrollkästchen **Abgelegte Shapes annehmen** aktivieren. 
  
Um einer Gruppe ein Shape hinzuzufügen, indem Sie es in der Gruppe ablegen, müssen Sie auch ein ähnliches Formverhalten aktivieren. Sie müssen das Shape auswählen, [](run-in-developer-mode-display-the-developer-tab.md) **auf** der Registerkarte Entwickler auf Verhalten klicken und dann das Kontrollkästchen Shape zu Gruppen bei der **Dropdownliste** hinzufügen aktivieren. Dieser Wert wird in der Zelle IsDropSource im Abschnitt Verschiedene gespeichert. 
  
Verwenden Sie folgendes, um einen Verweis auf die Zelle IsDropTarget anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |IsDropTarget  <br/> |
   
Um einen Verweis auf die IsDropTarget-Zelle nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowGroup** <br/> |
|Zellenindex:  <br/> |**visGroupIsDropTarget** <br/> |
   

