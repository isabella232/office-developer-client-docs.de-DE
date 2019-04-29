---
title: Zelle "noProofing" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: Bestimmt, ob die Rechtschreibung automatisch korrigiert wird und ob Rechtschreibfehler für das ausgewählte Shape angezeigt werden. Akzeptiert einen booleschen Wert.
ms.openlocfilehash: 8d7eebcc349c54db3cd48d6c5fa3c8fa6f4f760e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431253"
---
# <a name="noproofing-cell-miscellaneous-section"></a>Zelle "noProofing" (Abschnitt "Miscellaneous")

Bestimmt, ob die Rechtschreibung automatisch korrigiert wird und ob Rechtschreibfehler für das ausgewählte Shape angezeigt werden. Akzeptiert einen **booleschen** Wert. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Die Rechtschreibung wird nicht automatisch korrigiert, und es werden keine Rechtschreibfehler für das ausgewählte Shape angezeigt.  <br/> |
|FALSE  <br/> |Die Rechtschreibung wird automatisch korrigiert, und Rechtschreibfehler werden für das ausgewählte Shape angezeigt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle noProofing aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |NoProofing  <br/> |
   
Wenn Sie einen Verweis auf die Zelle noProofing aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowMisc** <br/> |
|Zellenindex:  <br/> |**visObjNoProofing** <br/> |
   

