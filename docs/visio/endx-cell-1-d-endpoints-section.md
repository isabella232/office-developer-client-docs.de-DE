---
title: Zelle "EndX" (Abschnitt "1-D Endpoints")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm335
localization_priority: Normal
ms.assetid: 24261b77-e3e8-7434-a503-9f23798bdab1
description: Stellt die X-Koordinate des Endpunkts des 1D-Shapes im Verhältnis zum Ursprung seines übergeordneten Objekts.
ms.openlocfilehash: f7324d9d4df5c428f734da255e7dd65b24cb0cb0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796948"
---
# <a name="endx-cell-1-d-endpoints-section"></a>EndX Cell (1-D Endpoints Section)

Stellt die *X* -Koordinate des Endpunkts des 1D-Shapes im Verhältnis zum Ursprung seines übergeordneten Objekts. 
  
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle EndX nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | EndX  <br/> |
   
Wenn Sie einen Verweis auf die Zelle EndX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowXForm1D** <br/> |
| Zellenindex:  <br/> |**vis1DEndX** <br/> |
   

