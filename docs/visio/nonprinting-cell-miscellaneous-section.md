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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357232"
---
# <a name="nonprinting-cell-miscellaneous-section"></a>Zelle "NonPrinting" (Abschnitt "Miscellaneous")

Aktiviert bzw. deaktiviert das Drucken für das ausgewählte Shape.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Das Drucken ist deaktiviert, doch das Shape wird im Zeichnungsfenster angezeigt.  <br/> |
| FALSE  <br/> | Drucken ist aktiviert.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können eine Führungslinie drucken, indem Sie sie auswählen und anschließend den Wert ihrer Zelle NonPrinting auf FALSE setzen.
  
Wenn Sie einen Verweis auf die Zelle nonPrinting aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Druckbaren  <br/> |
   
Wenn Sie einen Verweis auf die Zelle nonPrinting aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zellenindex:  <br/> |**visNonPrinting** <br/> |
   

