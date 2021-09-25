---
title: Zelle "NoProofing" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: Bestimmt, ob die Rechtschreibung automatisch korrigiert wird und ob Für die ausgewählte Form Rechtschreibfehler angezeigt werden. Verwendet einen booleschen Wert.
ms.openlocfilehash: 6e4ffc00e9d45c808655363619a5331030cb84a2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573831"
---
# <a name="noproofing-cell-miscellaneous-section"></a>Zelle "NoProofing" (Abschnitt "Miscellaneous")

Bestimmt, ob die Rechtschreibung automatisch korrigiert wird und ob Für die ausgewählte Form Rechtschreibfehler angezeigt werden. Verwendet einen **booleschen** Wert. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Die Rechtschreibung wird nicht automatisch korrigiert, und für die ausgewählte Form werden keine Rechtschreibfehler angezeigt.  <br/> |
|FALSE  <br/> |Die Rechtschreibung wird automatisch korrigiert, und für das ausgewählte Shape werden Rechtschreibfehler angezeigt.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie zum Abrufen eines Verweises auf die Zelle "NoProofing" anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |NoProofing  <br/> |
   
Um einen Verweis auf die Zelle "NoProofing" anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowMisc** <br/> |
|Zellenindex:  <br/> |**visObjNoProofing** <br/> |
   

