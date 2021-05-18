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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421480"
---
# <a name="nolivedynamics-cell-miscellaneous-section"></a>Zelle "NoLiveDynamics" (Abschnitt "Miscellaneous")

Bestimmt, ob ein Shape auf dynamische Art und Weise größenmäßig angepasst oder gedreht wird, während Sie es bearbeiten.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Shape beim Bearbeiten nicht dynamisch aktualisieren.  <br/> |
| FALSE  <br/> | Shape beim Bearbeiten dynamisch aktualisieren.  <br/> |
   
## <a name="remarks"></a>Hinweise

Während Sie ein zweidimensionales Shape (2D-Shape) bei deaktivierter Dynamik größenmäßig ändern oder drehen, wird ein Auswahlfeld angezeigt. Wenn das Shape eindimensional (1D-Shape) ist, hängt das visuelle Feedback vom Wert in der Zelle DynFeedback ab.
  
Um einen Verweis auf die Zelle NoLiveDynamics anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | NoLiveDynamics  <br/> |
   
Um einen Verweis auf die Zelle NoLiveDynamics nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zeilenindex:  <br/> |**visNoLiveDynamics** <br/> |
   

