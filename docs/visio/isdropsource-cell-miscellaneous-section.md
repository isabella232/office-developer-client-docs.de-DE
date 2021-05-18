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
   
## <a name="remarks"></a>Hinweise

Sie können diesen Wert auch festlegen, indem Sie das Shape auswählen, auf der Registerkarte [Entwickler](run-in-developer-mode-display-the-developer-tab.md) auf **Verhalten** klicken und anschließend das Kontrollkästchen **Shape beim Ablegen der Gruppe hinzufügen** aktivieren. 
  
Zusätzlich zum Aktivieren dieses Verhaltens für ein Shape müssen Sie eine Gruppe auch zum Akzeptieren von Shapes aktivieren, die in dieses Shape gezogen werden. Wählen Sie dazu die Gruppe aus, [](run-in-developer-mode-display-the-developer-tab.md) **klicken** Sie auf der Registerkarte Entwickler auf Verhalten, und aktivieren Sie dann das Kontrollkästchen **Verworfene Shapes** akzeptieren. Dieser Wert wird in der Zelle IsDropTarget im Abschnitt Gruppeneigenschaften gespeichert. 
  
Um einen Verweis auf die Zelle IsDropSource anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |IsDropSource  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die IsDropSource-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowMisc** <br/> |
|Zellenindex:  <br/> |**visDropSource** <br/> |
   

