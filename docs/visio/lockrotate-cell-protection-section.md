---
title: Zelle "LockRotate" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm655
localization_priority: Normal
ms.assetid: 2d97b31d-9008-307d-273a-1726007eeb34
description: Sperrt 2D-Shapes, damit sie nicht mit dem Drehpunkt oder den Befehlen Linksdrehung 90 Grad und Rechtsdrehung 90 Grad gedreht werden können.
ms.openlocfilehash: 36da1868e4f974bd19d00e86e31bea96eb8ad5bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404673"
---
# <a name="lockrotate-cell-protection-section"></a>Zelle "LockRotate" (Abschnitt "Protection")

Sperrt 2D-Shapes, damit sie nicht mit dem Drehpunkt oder den Befehlen **Linksdrehung 90 Grad** und **Rechtsdrehung 90 Grad** gedreht werden können. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Shape kann nicht gedreht werden.  <br/> |
| FALSE  <br/> | Shape kann gedreht werden (Standardeinstellung).  <br/> |
   
## <a name="remarks"></a>Hinweise

Die Zelle LockRotate verhindert nicht das Drehen eines 1D-Shapes, wenn an einem Endpunkt gezogen wird. Um ein 1D-Shape zu sperren, damit es nicht gedreht werden kann, legen Sie in der Zelle LockRotate einen Wert ungleich Null (TRUE) fest.
  
Um einen Verweis auf die Zelle LockRotate anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockRotate  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle LockRotate nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zeilenindex:  <br/> |**visLockRotate** <br/> |
   

