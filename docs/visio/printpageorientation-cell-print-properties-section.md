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
ms.openlocfilehash: 2adc7dadcb3702e6c5307bb569b2ae1df7aee54e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797738"
---
# <a name="printpageorientation-cell-print-properties-section"></a>Zelle "PrintPageOrientation" (Abschnitt "Print Properties")

Bestimmt, ob die Seite im Hoch- oder im Querformat gedruckt wird.
  
|**Wert**|**Orientation**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Druckereinstellungen übernehmen  <br/> |**visPPOSameAsPrinter** <br/> |
| 1  <br/> | Hochformat  <br/> |**visPPOPortrait** <br/> |
|2  <br/> |Querformat  <br/> |**visPPOLandscape** <br/> |
   
## <a name="remarks"></a>Hinweise

Beim Einfügen neuer Seiten in einem Dokument ist die Standardeinstellung die Einstellung in der aktiven Seite.
  
Wenn Sie einen Verweis auf die Zelle PrintPageOrientation nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | PrintPageOrientation  <br/> |
   
Wenn Sie einen Verweis auf die Zelle PrintPageOrientation aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
| Zellenindex:  <br/> |**visPrintPropertiesPageOrientation** <br/> |
   

