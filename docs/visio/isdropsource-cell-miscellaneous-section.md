---
title: Zelle "IsDropSource" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm490
ms.localizationpriority: medium
ms.assetid: 3b20e6ef-f1ac-5bb0-5ac3-4df3ae5e9bf9
description: Legt fest, ob das Shape durch Ablegen auf einer Gruppe dieser Gruppe hinzugefügt werden kann.
ms.openlocfilehash: c56b456f76f0f211648caf183e88380a23942dac
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628052"
---
# <a name="isdropsource-cell-miscellaneous-section"></a>Zelle "IsDropSource" (Abschnitt "Miscellaneous")

Legt fest, ob das Shape durch Ablegen auf einer Gruppe dieser Gruppe hinzugefügt werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Das Shape kann durch Ablegen auf einer Gruppe dieser Gruppe hinzugefügt werden.  <br/> |
|FALSE  <br/> |Das Shape kann einer Gruppe nicht hinzugefügt werden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können diesen Wert auch festlegen, indem Sie das Shape auswählen, auf der Registerkarte [Entwickler](run-in-developer-mode-display-the-developer-tab.md) auf **Verhalten** klicken und anschließend das Kontrollkästchen **Shape beim Ablegen der Gruppe hinzufügen** aktivieren. 
  
Zusätzlich zum Aktivieren dieses Verhaltens für ein Shape müssen Sie auch eine Gruppe aktivieren, um Shapes zu akzeptieren, die in das Shape gezogen werden. Wählen Sie dazu die Gruppe aus, klicken Sie auf der Registerkarte ["Entwicklertools"](run-in-developer-mode-display-the-developer-tab.md) auf **"Verhalten",** und aktivieren Sie dann das Kontrollkästchen **"Verworfene Shapes akzeptieren".** Dieser Wert wird in der Zelle "IsDropTarget" im Abschnitt "Gruppeneigenschaften" gespeichert. 
  
Verwenden Sie zum Abrufen eines Verweises auf die Zelle "IsDropSource" anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |IsDropSource  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle "IsDropSource" anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowMisc** <br/> |
|Zellenindex:  <br/> |**visDropSource** <br/> |
   

