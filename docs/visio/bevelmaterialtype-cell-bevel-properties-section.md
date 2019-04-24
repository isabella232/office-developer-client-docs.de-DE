---
title: Zelle "BevelMaterialType" (Abschnitt "Fase Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 30f50a94-88dc-41a3-bb46-45c92d6817a4
description: Bestimmt den Materialtyp, aus dem die Abschrägung besteht.
ms.openlocfilehash: b8efaa1f84594c803c79be02cd88dda1a5346dc7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315764"
---
# <a name="bevelmaterialtype-cell-bevel-properties-section"></a>Zelle "BevelMaterialType" (Abschnitt "Fase Properties")

Bestimmt den Materialtyp, aus dem die Abschrägung besteht. 
  
|**Beschreibung**|**Wert**|
|:-----|:-----|
|0  <br/> |Kein spezielles Material  <br/> |
|1  <br/> |Matt  <br/> |
|2  <br/> |Warm matt  <br/> |
|3  <br/> |Plastik  <br/> |
|4  <br/> |Metall  <br/> |
|5  <br/> |Dunkler Rand  <br/> |
|6  <br/> |Helle Kante  <br/> |
|7  <br/> |Flach  <br/> |
|8  <br/> |Drahtmodell  <br/> |
|9  <br/> |Pulver  <br/> |
|10  <br/> |Durchsichtiges Pulver  <br/> |
|11  <br/> |Deaktivieren  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **BevelMaterialType** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | BevelMaterialType  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **BevelMaterialType** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowBevelProperties** <br/> |
| Zellenindex:  <br/> |**visBevelMaterialType** <br/> |
   

