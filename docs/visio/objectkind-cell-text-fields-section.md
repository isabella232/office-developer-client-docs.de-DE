---
title: Zelle "ObjectKind" (Abschnitt "Text Fields")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60058
ms.localizationpriority: medium
ms.assetid: cc4c373c-f073-e3c9-3aaa-a4abf050cd20
description: Gibt den Textfeldtyp an.
ms.openlocfilehash: 0186c510ed47550f5c1194b84dbe7eec6ee4c539
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627828"
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
    
Um einen Verweis auf die Zelle "ObjectKind" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Fields.ObjectKind[  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ObjectKind anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionTextField** <br/> |
| Zeilenindex:  <br/> |**visRowField**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visFieldObjectKind** <br/> |
   

