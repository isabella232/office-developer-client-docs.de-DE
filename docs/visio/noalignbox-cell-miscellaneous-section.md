---
title: Zelle "NoAlignBox" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm700
localization_priority: Normal
ms.assetid: b2d51f4b-d64e-fd14-4ff1-ed67c69213bc
description: Aktiviert bzw. deaktiviert die Anzeige des Auswahlrechtecks für das ausgewählte Shape.
ms.openlocfilehash: 2ff9f051df54f4d424589332b9fbaea973552edc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319859"
---
# <a name="noalignbox-cell-miscellaneous-section"></a>Zelle "NoAlignBox" (Abschnitt "Miscellaneous")

Aktiviert bzw. deaktiviert die Anzeige des Auswahlrechtecks für das ausgewählte Shape.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Markierungsrechteck wird nicht angezeigt, wenn ein Shape ausgewählt wird.  <br/> |
| FALSE  <br/> | Markierungsrechteck wird angezeigt, wenn ein Shape ausgewählt wird.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle noAlignbox aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle NoAlignBox  <br/> |
   
Wenn Sie einen Verweis auf die Zelle noAlignbox nach Index aus einem Programm erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zellenindex:  <br/> |**visNoAlignBox** <br/> |
   

