---
title: NoProofing Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: Bestimmt, ob die Rechtschreibung automatisch korrigiert wird und ob Rechtschreibfehler für das ausgewählte Shape angezeigt werden. Nimmt einen booleschen Wert an.
ms.openlocfilehash: 6c27e6740b547af83058519de8edd38fc3522b32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/21/2018
ms.locfileid: "19797547"
---
# <a name="noproofing-cell-miscellaneous-section"></a>NoProofing Cell (Miscellaneous Section)

Bestimmt, ob die Rechtschreibung automatisch korrigiert wird und ob Rechtschreibfehler für das ausgewählte Shape angezeigt werden. Nimmt einen **booleschen** Wert an. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Rechtschreibung wird nicht automatisch korrigiert und Rechtschreibfehler werden nicht für die markierte Form angezeigt.  <br/> |
|FALSE  <br/> |Rechtschreibung wird automatisch korrigiert und Rechtschreibfehler für das ausgewählte Shape angezeigt werden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Zum Abrufen eines Verweises auf die Zelle NoProofing nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |NoProofing  <br/> |
   
Wenn Sie einen Verweis auf die Zelle NoProofing aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowMisc** <br/> |
|Zellenindex:  <br/> |**visObjNoProofing** <br/> |
   

