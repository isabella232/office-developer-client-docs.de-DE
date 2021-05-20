---
title: Zelle "NonPrinting" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251321
localization_priority: Normal
ms.assetid: 59fe0887-2092-4fad-ea38-2aba354f3b92
description: Aktiviert bzw. deaktiviert das Drucken für das ausgewählte Shape.
ms.openlocfilehash: c3e1fc1b2d91fa4808f8ea89c904218c2236f5b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437259"
---
# <a name="nonprinting-cell-miscellaneous-section"></a>Zelle "NonPrinting" (Abschnitt "Miscellaneous")

Aktiviert bzw. deaktiviert das Drucken für das ausgewählte Shape.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Das Drucken ist deaktiviert, doch das Shape wird im Zeichnungsfenster angezeigt.  <br/> |
| FALSE  <br/> | Drucken ist aktiviert.  <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können eine Führungslinie drucken, indem Sie sie auswählen und anschließend den Wert ihrer Zelle NonPrinting auf FALSE setzen.
  
Um einen Verweis auf die Zelle NonPrinting anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | NonPrinting  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle NonPrinting nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zellenindex:  <br/> |**visNonPrinting** <br/> |
   

