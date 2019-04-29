---
title: Zelle "PrintPageOrientation" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033795
localization_priority: Normal
ms.assetid: f8354d0d-0ce2-fb33-ddf7-611a2c24a8be
description: Bestimmt, ob die Seite im Hoch- oder im Querformat gedruckt wird.
ms.openlocfilehash: f7e73bea5120d878a1b2dbf553a66b349d247fce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434865"
---
# <a name="printpageorientation-cell-print-properties-section"></a>Zelle "PrintPageOrientation" (Abschnitt "Print Properties")

Bestimmt, ob die Seite im Hoch- oder im Querformat gedruckt wird.
  
|**Wert**|**Orientation**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Druckereinstellungen übernehmen  <br/> |**visPPOSameAsPrinter** <br/> |
| 1  <br/> | Portrait  <br/> |**visPPOPortrait** <br/> |
|2  <br/> |Landschaft  <br/> |**visPPOLandscape** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie neue Seiten in ein Dokument einfügen, ist diese Einstellung standardmäßig die Einstellung auf der aktiven Seite.
  
Wenn Sie einen Verweis auf die Zelle PrintPageOrientation aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | PrintPageOrientation  <br/> |
   
Wenn Sie einen Verweis auf die Zelle PrintPageOrientation aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
| Zeilenindex:  <br/> |**visPrintPropertiesPageOrientation** <br/> |
   

