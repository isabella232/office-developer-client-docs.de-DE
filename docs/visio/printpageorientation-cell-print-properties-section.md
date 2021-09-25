---
title: Zelle "PrintPageOrientation" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033795
ms.localizationpriority: medium
ms.assetid: f8354d0d-0ce2-fb33-ddf7-611a2c24a8be
description: Bestimmt, ob die Seite im Hoch- oder im Querformat gedruckt wird.
ms.openlocfilehash: 7618077640875c9952a9c05e39ab1307407a3d91
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570316"
---
# <a name="printpageorientation-cell-print-properties-section"></a>Zelle "PrintPageOrientation" (Abschnitt "Print Properties")

Bestimmt, ob die Seite im Hoch- oder im Querformat gedruckt wird.
  
|**Wert**|**Orientation**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Druckereinstellungen übernehmen  <br/> |**visPPOSameAsPrinter** <br/> |
| 1  <br/> | Portrait  <br/> |**visPPOPortrait** <br/> |
|2  <br/> |Landschaft  <br/> |**visPPOLandscape** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn Sie neue Seiten in ein Dokument einfügen, ist diese Einstellung standardmäßig auf die Einstellung auf der aktiven Seite festgelegt.
  
Verwenden Sie zum Abrufen eines Verweises auf die Zelle "PrintPageOrientation" anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | PrintPageOrientation  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle PrintPageOrientation anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
| Zeilenindex:  <br/> |**visPrintPropertiesPageOrientation** <br/> |
   

