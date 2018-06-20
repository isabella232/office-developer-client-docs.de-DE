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
ms.openlocfilehash: fd24a8d23d62436a6d81cf6b8049dcabe47db677
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798078"
---
# <a name="shdwpattern-cell-fill-format-section"></a>Zelle "ShdwPattern" (Abschnitt "Fill Format")

Definiert das Füllmuster für den Schatten eines Shapes.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Keins (transparente Füllung).  <br/> |
|1  <br/> |Einfarbige Vordergrundfarbe  <br/> |
|2 – 40  <br/> |Verschiedene Füllmuster  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Um das Füllmuster festgelegt, geben Sie eine Zahl von 0 bis 40, einen Index in einer Auflistung von Muster. Sie können die Auflistung der Füllung Muster im Dialogfeld **Füllbereich** anzeigen (klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** klicken Sie auf **Füllbereich**, und klicken Sie dann auf **Optionen**).
  
Wenn Sie einen Verweis auf die Zelle ShdwPattern nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ShdwPattern  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ShdwPattern aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowFill** <br/> |
|Zellenindex:  <br/> |**visFillShdwPattern** <br/> |
   

