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
ms.openlocfilehash: cbe4d6a8b6fdd4b66acf064884d20999ff7e3b4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319803"
---
# <a name="noctlhandles-cell-miscellaneous-section"></a>Zelle "NoCtlHandles" (Abschnitt "Miscellaneous")

Aktiviert bzw. deaktiviert die Anzeige der Steuerpunkte für das ausgewählte Shape.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Steuerpunkte werden nicht angezeigt, wenn ein Shape ausgewählt wird.  <br/> |
| FALSE  <br/> | Steuerpunkte werden angezeigt, wenn ein Shape ausgewählt wird.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle Zelle NoCtlHandles aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle NoCtlHandles  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle NoCtlHandles aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zellenindex:  <br/> |**visNoCtlHandles** <br/> |
   

