---
title: Zelle "ShdwPattern" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm935
localization_priority: Normal
ms.assetid: eca73b80-9835-9011-1dce-187ccee92e76
description: Definiert das Füllmuster für den Schatten eines Shapes.
ms.openlocfilehash: c2591fbc9f208b1bf9c7d0c85e6de765cd9825f6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427612"
---
# <a name="shdwpattern-cell-fill-format-section"></a>Zelle "ShdwPattern" (Abschnitt "Fill Format")

Definiert das Füllmuster für den Schatten eines Shapes.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Keins (transparente Füllung).  <br/> |
|1  <br/> |Einfarbige Vordergrundfarbe  <br/> |
|2 - 40  <br/> |Verschiedene Füllmuster  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie das Füllmuster festlegen möchten, geben Sie eine Zahl von 0 bis 40 ein. Diese Zahl ist ein Index für eine Mustersammlung. Sie können sich die Füllmustersammlung auch im Dialogfeld **Füllbereich** ansehen (klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Shape** auf **Füllbereich**, und klicken Sie dann auf **Füllbereichsoptionen**).
  
Wenn Sie einen Verweis auf die Zelle Zelle ShdwPattern aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Zelle ShdwPattern  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle ShdwPattern aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowFill** <br/> |
|Zellenindex:  <br/> |**visFillShdwPattern** <br/> |
   

