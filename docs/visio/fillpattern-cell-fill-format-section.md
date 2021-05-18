---
title: Zelle "FillPattern" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm375
localization_priority: Normal
ms.assetid: dac82a4f-4508-541a-e118-7d79df987232
description: Legt das Füllmuster für das Shape fest. Verwenden Sie die USE-Funktion in dieser Zelle, um ein benutzerdefiniertes Füllmuster anzugeben.
ms.openlocfilehash: 340ccdc9f3819fb29e210832107e270bd302433c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422929"
---
# <a name="fillpattern-cell-fill-format-section"></a>Zelle "FillPattern" (Abschnitt "Fill Format")

Legt das Füllmuster für das Shape fest. Verwenden Sie die USE-Funktion in dieser Zelle, um ein benutzerdefiniertes Füllmuster anzugeben.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Keine (transparente Füllung).  <br/> |
|1  <br/> |Einfarbige Vordergrundfarbe.  <br/> |
|2 - 40  <br/> |Verschiedene Füllmuster, die den indizierten Einträgen im Dialogfeld **Füllbereich** entsprechen.  <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können diesen Wert auch über das Dialogfeld **Füllbereich** festlegen (klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Shape** auf **Füllbereich**, und klicken Sie dann auf **Füllbereichsoptionen**).
  
Um einen Verweis auf die FillPattern-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |FillPattern  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die FillPattern-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowFill** <br/> |
|Zellenindex:  <br/> |**visFillPattern** <br/> |
   

