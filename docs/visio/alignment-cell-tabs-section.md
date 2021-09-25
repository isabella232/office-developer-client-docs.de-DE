---
title: Zelle "Alignment" (Abschnitt "Tabs")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm35
ms.localizationpriority: medium
ms.assetid: 84234177-a2df-6acc-2761-230bc5d12627
description: Legt die Tabausrichtung fest.
ms.openlocfilehash: 5ec858ecff9222feccebdc84c520b7f3f9ec819f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578277"
---
# <a name="alignment-cell-tabs-section"></a>Zelle "Alignment" (Abschnitt "Tabs")

Legt die Tabausrichtung fest.
  
|**Wert**|**Alignment**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Left  <br/> |**visTabStopLeft** <br/> |
| 1  <br/> | Zentriert  <br/> |**visTabStopCenter** <br/> |
| 2  <br/> | Nach rechts  <br/> |**visTabStopRight** <br/> |
| 3  <br/> | Dezimal  <br/> |**visTabStopDecimal** <br/> |
| 4   <br/> | Komma  <br/> |**visTabStopComma** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die Zelle "Alignment" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Registerkarten.  *ij*            where  *i and j =*  <1>, 2, 3  <br/> |
   
Um einen Verweis auf die Zelle "Alignment" anhand des Indexes aus einem Programm abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionTab** <br/> |
| Zeilenindex:  <br/> |**visRowTab +** *i*            where  *i*  = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> | (*j*  *3) **+ visTabAlign** <br/> |
   

