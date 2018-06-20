---
title: Zelle "NoCtlHandles" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251319
localization_priority: Normal
ms.assetid: 4345b3e5-f522-e300-307c-4f8992a3ddce
description: Aktiviert bzw. deaktiviert die Anzeige der Steuerpunkte für das ausgewählte Shape.
ms.openlocfilehash: 897e4cd97eeab8797f2652285ba395603c41a8e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797538"
---
# <a name="noctlhandles-cell-miscellaneous-section"></a>Zelle "NoCtlHandles" (Abschnitt "Miscellaneous")

Aktiviert bzw. deaktiviert die Anzeige der Steuerpunkte für das ausgewählte Shape.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| WAHR  <br/> | Steuerpunkte werden nicht angezeigt, wenn ein Shape ausgewählt wird.  <br/> |
| FALSCH  <br/> | Steuerpunkte werden angezeigt, wenn ein Shape ausgewählt wird.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle NoCtlHandles nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | NoCtlHandles  <br/> |
   
Wenn Sie einen Verweis auf die Zelle NoCtlHandles aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zellenindex:  <br/> |**visNoCtlHandles** <br/> |
   

