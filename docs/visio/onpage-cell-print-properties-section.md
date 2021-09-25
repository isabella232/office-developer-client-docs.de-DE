---
title: Zelle "OnPage" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033793
ms.localizationpriority: medium
ms.assetid: 4015506a-e24a-0276-c854-7791a7019067
description: Gibt an, ob die Zeichnung auf einer bestimmten Anzahl von Seiten gedruckt wird.
ms.openlocfilehash: 265d5d02b17feddd8d7ff1865ec9ae2fbf7f355e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590191"
---
# <a name="onpage-cell-print-properties-section"></a>Zelle "OnPage" (Abschnitt "Print Properties")

Gibt an, ob die Zeichnung auf einer bestimmten Anzahl von Seiten gedruckt wird. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Passen Sie das Zeichenblatt an eine definierte Anzahl von Druckerseiten an.  <br/> |
|FALSE  <br/> |Das Zeichenblatt wird nicht auf einer definierten Anzahl von Druckseiten ausgegeben (Standardwert).  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn die Zelle OnPage auf WAHR festgelegt ist, bestimmt Microsoft Visio anhand der Zellen PagesX und PagesY die Anzahl der Druckseiten, auf denen die Zeichnung ausgegeben werden soll. Die Werte in den Zellen ScaleX und ScaleY werden ignoriert. Diese Einstellung ist eine AutoSkalieren-Einstellung.
  
Dieser Wert entspricht der Option **"Anpassen an"** auf der Registerkarte **"Druckeinrichtung"** im Dialogfeld **"Seite einrichten"** (klicken Sie auf der Registerkarte **"Entwurf"** auf den Pfeil neben **"Seite einrichten").** 
  
Um einen Verweis auf die OnPage-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |OnPage  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle "OnPage" anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
|Zellenindex:  <br/> |**visPrintPropertiesOnPage** <br/> |
   

