---
title: Zelle "ObjectKind" (Abschnitt "Text Fields")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60058
localization_priority: Normal
ms.assetid: cc4c373c-f073-e3c9-3aaa-a4abf050cd20
description: Gibt den Textfeldtyp an.
ms.openlocfilehash: c2f891620f704a3c48861124b886e49d356960ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360991"
---
# <a name="objectkind-cell-text-fields-section"></a>Zelle "ObjectKind" (Abschnitt "Text Fields")

Gibt den Textfeldtyp an.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Standard  <br/> |**visTFOKStandard** <br/> |
| 1  <br/> |Horizontal in Vertikal  <br/> |**visTFOKHorizontaInVertical** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die folgenden Typen von Textfeldern sind möglich:
  
- Standard. Damit wird angegeben, dass das Feld nach Feldkategorie eingefügt wurde.
    
- Horizontal in Vertikal. Damit wird angegeben, dass im Feld horizontaler Text in vertikalen Text gesetzt ist.
    
Wenn Sie einen Verweis auf die Zelle objectKind aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Fields. objectKind [ *i* ] wobei *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle objectKind aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionTextField** <br/> |
| Zeilenindex:  <br/> |**visRowField** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visFieldObjectKind** <br/> |
   

