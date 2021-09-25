---
title: Zelle "CenterY" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033792
ms.localizationpriority: medium
ms.assetid: 7ce0bf66-dc8b-9646-7b04-50c969ecd67a
description: Bestimmt, ob das Zeichenblatt vertikal zentriert auf der Druckseite ausgerichtet wird.
ms.openlocfilehash: b72acb3db2a56ab44da92dd30a3f748941ca7fbe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578025"
---
# <a name="centery-cell-print-properties-section"></a>Zelle "CenterY" (Abschnitt "Print Properties")

Bestimmt, ob das Zeichenblatt vertikal zentriert auf der Druckseite ausgerichtet wird. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Zeichenblatt wird vertikal zentriert auf der Druckseite ausgerichtet.  <br/> |
| FALSE  <br/> | Zeichenblatt wird nicht vertikal zentriert auf der Druckseite ausgerichtet (Standardeinstellung).  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

In der Standardeinstellung werden Zeichenblätter am oberen und linken Rand der Druckseite ausgerichtet. Durch das Festlegen der Zellen CenterX und CenterY auf WAHR wird das Zeichenblatt auf der Druckseite zentriert (bzw. auf den Druckseiten, wenn eine Unterteilung erforderlich ist). 
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle CenterY anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Centery  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle CenterY anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
| Zeilenindex:  <br/> |**visPrintPropertiesCenterY** <br/> |
   

