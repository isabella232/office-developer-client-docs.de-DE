---
title: Zelle "CenterX" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60030
localization_priority: Normal
ms.assetid: 890e2537-66a5-2863-c78d-320b42565ea7
description: Bestimmt, ob das Zeichenblatt horizontal zentriert auf der Druckseite ausgerichtet wird.
ms.openlocfilehash: a12b60f7d183a27d938bd18a1f571ef01af455d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796624"
---
# <a name="centerx-cell-print-properties-section"></a>CenterX Cell (Print Properties Section)

Bestimmt, ob das Zeichenblatt horizontal zentriert auf der Druckseite ausgerichtet wird. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| WAHR  <br/> | Zeichenblatt wird horizontal zentriert auf der Druckseite ausgerichtet.  <br/> |
| FALSCH  <br/> | Zeichenblatt wird nicht horizontal zentriert auf der Druckseite ausgerichtet (Standardeinstellung).  <br/> |
   
## <a name="remarks"></a>Hinweise

In der Standardeinstellung werden Zeichenblätter am oberen und linken Rand der Druckseite ausgerichtet. Durch das Festlegen der Zellen CenterX und CenterY auf WAHR wird das Zeichenblatt auf der Druckseite zentriert (bzw. auf den Druckseiten, wenn eine Unterteilung erforderlich ist). 
  
Wenn Sie einen Verweis auf die Zelle CenterX aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | CenterX  <br/> |
   
Wenn Sie einen Verweis auf die Zelle CenterX aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
| Zellenindex:  <br/> |**visPrintPropertiesCenterX** <br/> |
   

