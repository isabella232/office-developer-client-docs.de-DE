---
title: Zelle "LockEnd" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm620
localization_priority: Normal
ms.assetid: e9742142-4d34-1ba9-480e-d1ecff4fc7cd
description: Sperrt den Endpunkt (EndeX, EndeY) eines 1D-Shapes an einer bestimmten Position.
ms.openlocfilehash: d9fe0372c44fe3b029a4d06056c8d3871c3f91e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425582"
---
# <a name="lockend-cell-protection-section"></a>Zelle "LockEnd" (Abschnitt "Protection")

Sperrt den Endpunkt (EndeX, EndeY) eines 1D-Shapes an einer bestimmten Position.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Endpunkt ist gesperrt.  <br/> |
| FALSE  <br/> | Endpunkt ist nicht gesperrt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle Zelle LockEnd aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle LockEnd  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle LockEnd aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockEnd** <br/> |
   

