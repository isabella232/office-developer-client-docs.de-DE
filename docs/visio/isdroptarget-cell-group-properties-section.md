---
title: Zelle "IsDropTarget" (Abschnitt "Group Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm495
ms.localizationpriority: medium
ms.assetid: 8140fc7b-b99c-54bb-7af3-7de6fcdae7d3
description: Legt fest, ob das Shape durch Ablegen auf einer Gruppe dieser Gruppe hinzugefügt werden kann.
ms.openlocfilehash: 9e604165427e8e08768f1e8137438a1de87cc214
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598479"
---
# <a name="isdroptarget-cell-group-properties-section"></a>Zelle "IsDropTarget" (Abschnitt "Group Properties")

Legt fest, ob das Shape durch Ablegen auf einer Gruppe dieser Gruppe hinzugefügt werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Ein Shape kann durch Ablegen auf einer Gruppe dieser Gruppe hinzugefügt werden.  <br/> |
|FALSE  <br/> |Das Shape kann auf der Gruppe nicht abgelegt werden.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Sie können diesen Wert auch festlegen, indem Sie die Gruppe auswählen, auf der Registerkarte [Entwickler](run-in-developer-mode-display-the-developer-tab.md) auf **Verhalten** klicken und anschließend das Kontrollkästchen **Abgelegte Shapes annehmen** aktivieren. 
  
Um einer Gruppe ein Shape hinzuzufügen, indem Sie es in der Gruppe ablegen, müssen Sie auch ein ähnliches Shape-Verhalten aktivieren. Sie müssen das Shape auswählen, auf der Registerkarte ["Entwicklertools"](run-in-developer-mode-display-the-developer-tab.md) auf **"Verhalten"** klicken und dann beim Ablegen das **Kontrollkästchen "Shape zu Gruppen hinzufügen"** aktivieren. Dieser Wert wird in der Zelle "IsDropSource" im Abschnitt "Miscellaneous" gespeichert. 
  
Um einen Verweis auf die Zelle "IsDropTarget" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |IsDropTarget  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle "IsDropTarget" anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowGroup** <br/> |
|Zellenindex:  <br/> |**visGroupIsDropTarget** <br/> |
   

