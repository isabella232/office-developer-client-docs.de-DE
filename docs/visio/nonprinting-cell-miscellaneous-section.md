---
title: Zelle "NonPrinting" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251321
ms.localizationpriority: medium
ms.assetid: 59fe0887-2092-4fad-ea38-2aba354f3b92
description: Aktiviert bzw. deaktiviert das Drucken für das ausgewählte Shape.
ms.openlocfilehash: f19e6f9e1c3ca140a16ac9ad8e5733ba70c3868c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573845"
---
# <a name="nonprinting-cell-miscellaneous-section"></a>Zelle "NonPrinting" (Abschnitt "Miscellaneous")

Aktiviert bzw. deaktiviert das Drucken für das ausgewählte Shape.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Das Drucken ist deaktiviert, doch das Shape wird im Zeichnungsfenster angezeigt.  <br/> |
| FALSE  <br/> | Drucken ist aktiviert.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Sie können eine Führungslinie drucken, indem Sie sie auswählen und anschließend den Wert ihrer Zelle NonPrinting auf FALSE setzen.
  
Um einen Verweis auf die Zelle "NonPrinting" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | NonPrinting  <br/> |
   
Um einen Verweis auf die Zelle "NonPrinting" anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zellenindex:  <br/> |**visNonPrinting** <br/> |
   

