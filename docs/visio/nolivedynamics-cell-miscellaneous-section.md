---
title: Zelle "NoLiveDynamics" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm720
localization_priority: Normal
ms.assetid: d1c4b9d9-6d64-8ed1-9fc6-2dbf829a75b5
description: Bestimmt, ob ein Shape auf dynamische Art und Weise größenmäßig angepasst oder gedreht wird, während Sie es bearbeiten.
ms.openlocfilehash: e332546c1fc5dfc71dfa3b72ea5a58bfef59dc7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340985"
---
# <a name="nolivedynamics-cell-miscellaneous-section"></a>Zelle "NoLiveDynamics" (Abschnitt "Miscellaneous")

Bestimmt, ob ein Shape auf dynamische Art und Weise größenmäßig angepasst oder gedreht wird, während Sie es bearbeiten.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Shape beim Bearbeiten nicht dynamisch aktualisieren.  <br/> |
| FALSE  <br/> | Shape beim Bearbeiten dynamisch aktualisieren.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Während Sie ein zweidimensionales Shape (2D-Shape) bei deaktivierter Dynamik größenmäßig ändern oder drehen, wird ein Auswahlfeld angezeigt. Wenn das Shape eindimensional (1D-Shape) ist, hängt das visuelle Feedback vom Wert in der Zelle DynFeedback ab.
  
Wenn Sie einen Verweis auf die Zelle Zelle NoLiveDynamics aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle NoLiveDynamics  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle NoLiveDynamics aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zeilenindex:  <br/> |**visNoLiveDynamics** <br/> |
   

