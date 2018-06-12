---
title: Zelle "CenterY" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033792
localization_priority: Normal
ms.assetid: 7ce0bf66-dc8b-9646-7b04-50c969ecd67a
description: Bestimmt, ob das Zeichenblatt vertikal zentriert auf der Druckseite ausgerichtet wird.
ms.openlocfilehash: 2fde1d6301d7b9de4540cd12f21e5af01d7a6239
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796643"
---
# <a name="centery-cell-print-properties-section"></a>CenterY Cell (Print Properties Section)

Bestimmt, ob das Zeichenblatt vertikal zentriert auf der Druckseite ausgerichtet wird. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| WAHR  <br/> | Zeichenblatt wird vertikal zentriert auf der Druckseite ausgerichtet.  <br/> |
| FALSCH  <br/> | Zeichenblatt wird nicht vertikal zentriert auf der Druckseite ausgerichtet (Standardeinstellung).  <br/> |
   
## <a name="remarks"></a>Hinweise

In der Standardeinstellung werden Zeichenblätter am oberen und linken Rand der Druckseite ausgerichtet. Durch das Festlegen der Zellen CenterX und CenterY auf WAHR wird das Zeichenblatt auf der Druckseite zentriert (bzw. auf den Druckseiten, wenn eine Unterteilung erforderlich ist). 
  
Wenn Sie einen Verweis auf die Zelle CenterY nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | CenterY  <br/> |
   
Wenn Sie einen Verweis auf die Zelle CenterY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
| Zellenindex:  <br/> |**visPrintPropertiesCenterY** <br/> |
   

