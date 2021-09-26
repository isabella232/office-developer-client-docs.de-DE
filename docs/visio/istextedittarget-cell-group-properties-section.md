---
title: Zelle "IsTextEditTarget" (Abschnitt "Group Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251627
ms.localizationpriority: medium
ms.assetid: 355cef8b-9213-479a-af95-b591f4bc51ad
description: Definiert die Textzuweisung für eine Gruppe.
ms.openlocfilehash: 8f33be46a6d5da733c34f4e0d57e39495fb8e36a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612582"
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
  
Verwenden Sie zum Abrufen eines Verweises auf die Zelle "IsTextEditTarget" anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |IsTextEditTarget  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle "IsTextEditTarget" anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowGroup** <br/> |
|Zellenindex:  <br/> |**visGroupIsTextEditTarget** <br/> |
   

