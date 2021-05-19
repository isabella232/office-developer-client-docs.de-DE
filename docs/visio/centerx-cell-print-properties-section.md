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
ms.openlocfilehash: 13b05ed71248a3f8fada947fca6b203c6ab19c6d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418078"
---
# <a name="centerx-cell-print-properties-section"></a>Zelle "CenterX" (Abschnitt "Print Properties")

Bestimmt, ob das Zeichenblatt horizontal zentriert auf der Druckseite ausgerichtet wird. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Zeichenblatt wird horizontal zentriert auf der Druckseite ausgerichtet.  <br/> |
| FALSE  <br/> | Zeichenblatt wird nicht horizontal zentriert auf der Druckseite ausgerichtet (Standardeinstellung).  <br/> |
   
## <a name="remarks"></a>Hinweise

In der Standardeinstellung werden Zeichenblätter am oberen und linken Rand der Druckseite ausgerichtet. Durch das Festlegen der Zellen CenterX und CenterY auf WAHR wird das Zeichenblatt auf der Druckseite zentriert (bzw. auf den Druckseiten, wenn eine Unterteilung erforderlich ist). 
  
Um einen Verweis auf die Zelle CenterX anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | CenterX  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die CenterX-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
| Zeilenindex:  <br/> |**visPrintPropertiesCenterX** <br/> |
   

