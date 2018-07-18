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
ms.openlocfilehash: ab00914a9c59cfe94b3f7273f89684f43328b4d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797545"
---
# <a name="nonprinting-cell-miscellaneous-section"></a>NonPrinting Cell (Miscellaneous Section)

Aktiviert bzw. deaktiviert das Drucken für das ausgewählte Shape.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| WAHR  <br/> | Das Drucken ist deaktiviert, doch das Shape wird im Zeichnungsfenster angezeigt.  <br/> |
| FALSCH  <br/> | Drucken ist aktiviert.  <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können eine Führungslinie drucken, indem Sie sie auswählen und anschließend den Wert ihrer Zelle NonPrinting auf FALSE setzen.
  
Wenn Sie einen Verweis auf die Zelle NonPrinting aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Nicht druckbare  <br/> |
   
Wenn Sie einen Verweis auf die Zelle NonPrinting aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zellenindex:  <br/> |**visNonPrinting** <br/> |
   

