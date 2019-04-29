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
ms.openlocfilehash: e8cb02a66f745530f12c7c8be56b9bdd771121b7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421893"
---
# <a name="isdropsource-cell-miscellaneous-section"></a>Zelle "IsDropSource" (Abschnitt "Miscellaneous")

Legt fest, ob das Shape durch Ablegen auf einer Gruppe dieser Gruppe hinzugefügt werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Das Shape kann durch Ablegen auf einer Gruppe dieser Gruppe hinzugefügt werden.  <br/> |
|FALSE  <br/> |Das Shape kann einer Gruppe nicht hinzugefügt werden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können diesen Wert auch festlegen, indem Sie das Shape auswählen, auf der Registerkarte [Entwickler](run-in-developer-mode-display-the-developer-tab.md) auf **Verhalten** klicken und anschließend das Kontrollkästchen **Shape beim Ablegen der Gruppe hinzufügen** aktivieren. 
  
Sie müssen nicht nur dieses Verhalten für ein Shape aktivieren, sondern auch, dass eine Gruppe Shapes akzeptiert, die hineingezogen werden. Wählen Sie dazu die Gruppe aus, klicken Sie auf der Registerkarte [Entwickler](run-in-developer-mode-display-the-developer-tab.md) auf **Verhalten** , und aktivieren Sie dann das Kontrollkästchen **verworfene Shapes akzeptieren** . Dieser Wert wird in der Zelle "IsDropTarget im Abschnitt Group Properties gespeichert. 
  
Wenn Sie einen Verweis auf die Zelle Zelle IsDropSource aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Zelle IsDropSource  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle IsDropSource aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowMisc** <br/> |
|Zellenindex:  <br/> |**visDropSource** <br/> |
   

