---
title: Zelle "IsDropSource" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm490
localization_priority: Normal
ms.assetid: 3b20e6ef-f1ac-5bb0-5ac3-4df3ae5e9bf9
description: Legt fest, ob das Shape durch Ablegen auf einer Gruppe dieser Gruppe hinzugefügt werden kann.
ms.openlocfilehash: f2edfcb7cf9d21b2ecd97b335b07f30233903d5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797224"
---
# <a name="isdropsource-cell-miscellaneous-section"></a>IsDropSource Cell (Miscellaneous Section)

Legt fest, ob das Shape durch Ablegen auf einer Gruppe dieser Gruppe hinzugefügt werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Das Shape kann durch Ablegen auf einer Gruppe dieser Gruppe hinzugefügt werden.  <br/> |
|FALSE  <br/> |Das Shape kann einer Gruppe nicht hinzugefügt werden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können diesen Wert auch festlegen, indem Sie das Shape auswählen, auf der Registerkarte [Entwickler](run-in-developer-mode-display-the-developer-tab.md) auf **Verhalten** klicken und anschließend das Kontrollkästchen **Shape beim Ablegen der Gruppe hinzufügen** aktivieren. 
  
Darüber hinaus müssen Sie eine Gruppe aktivieren, damit Shapes darin abgelegt werden können. Wählen Sie dazu die entsprechende Gruppe aus, klicken Sie auf der Registerkarte Entwickler auf Verhalten, und aktivieren Sie anschließend das Kontrollkästchen Abgelegte Shapes annehmen. Dieser Wert wird in der Zelle IsDropTarget im Abschnitt Gruppeneigenschaften gespeichert. 
  
Wenn Sie einen Verweis auf die Zelle IsDropSource aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |IsDropSource  <br/> |
   
Wenn Sie einen Verweis auf die Zelle IsDropSource aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowMisc** <br/> |
|Zellenindex:  <br/> |**visDropSource** <br/> |
   

