---
title: Zelle "PlaceDepth" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1230
ms.localizationpriority: medium
ms.assetid: 02c139db-fe67-f550-1d07-8c8a9a4fb427
description: Legt die Methode fest, anhand derer die Zeichnung vor Erstellen des Layouts analysiert wird, und definiert den Layouttyp.
ms.openlocfilehash: 10c116de99cce8fce65b6949341174aa6a3cf6b4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559780"
---
# <a name="placedepth-cell-page-layout-section"></a>Zelle "PlaceDepth" (Abschnitt "Page Layout")

Legt die Methode fest, anhand derer die Zeichnung vor Erstellen des Layouts analysiert wird, und definiert den Layouttyp.
  
|**Wert**|**Platzierungstiefe für vertikale und horizontale Layouts**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Zeichenblattstandard  <br/> |**visPLOPlaceDepthDefault** <br/> |
| 1  <br/> | Medium  <br/> |**visPLOPlaceDepthMedium** <br/> |
| 2  <br/> | Tief  <br/> |**visPLOPlaceDepthDeep** <br/> |
| 3  <br/> | Flachen  <br/> |**visPLOPlaceDepthShallow** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie zum Abrufen eines Verweises auf die Zelle PlaceDepth anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | PlaceDepth  <br/> |
   
Um einen Verweis auf die Zelle PlaceDepth anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
| Zellenindex:  <br/> |**visPLOPlaceDepth** <br/> |
   

