---
title: Zelle "PlaceDepth" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1230
localization_priority: Normal
ms.assetid: 02c139db-fe67-f550-1d07-8c8a9a4fb427
description: Legt die Methode fest, anhand derer die Zeichnung vor Erstellen des Layouts analysiert wird, und definiert den Layouttyp.
ms.openlocfilehash: 463c7dad39955161538aa89d1482685189bf7fdc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346795"
---
# <a name="placedepth-cell-page-layout-section"></a>Zelle "PlaceDepth" (Abschnitt "Page Layout")

Legt die Methode fest, anhand derer die Zeichnung vor Erstellen des Layouts analysiert wird, und definiert den Layouttyp.
  
|**Wert**|**Platzierungstiefe für vertikale und horizontale Layouts**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Zeichenblattstandard  <br/> |**visPLOPlaceDepthDefault** <br/> |
| 1  <br/> | Mittel  <br/> |**visPLOPlaceDepthMedium** <br/> |
| 2  <br/> | Tiefe  <br/> |**visPLOPlaceDepthDeep** <br/> |
| 3  <br/> | Flache  <br/> |**visPLOPlaceDepthShallow** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle Zelle PlaceDepth aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle PlaceDepth  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle PlaceDepth aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
| Zellenindex:  <br/> |**visPLOPlaceDepth** <br/> |
   

