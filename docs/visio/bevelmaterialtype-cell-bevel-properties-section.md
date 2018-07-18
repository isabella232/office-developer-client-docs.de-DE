---
title: BevelMaterialType Cell (Bevel Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 30f50a94-88dc-41a3-bb46-45c92d6817a4
description: Bestimmt den Typ der Inhalte, die aus der Abschrägung an.
ms.openlocfilehash: cd4ab223754ffcf7f46478cbc65faff373a3d692
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796459"
---
# <a name="bevelmaterialtype-cell-bevel-properties-section"></a>BevelMaterialType Cell (Bevel Properties Section)

Bestimmt den Typ der Inhalte, die aus der Abschrägung an. 
  
|**Beschreibung**|**Wert**|
|:-----|:-----|
|0  <br/> |Keine besondere material  <br/> |
|1  <br/> |Matt  <br/> |
|2  <br/> |Warm matt  <br/> |
|3  <br/> |Plastik  <br/> |
|4  <br/> |Metall  <br/> |
|5  <br/> |Dunkle Kante  <br/> |
|6  <br/> |Helle Kante  <br/> |
|7  <br/> |Flach  <br/> |
|8  <br/> |Drahtmodell  <br/> |
|9  <br/> |Pulver  <br/> |
|10  <br/> |Durchsichtiges Pulver  <br/> |
|11  <br/> |Transparent  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **BevelMaterialType** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | BevelMaterialType  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **BevelMaterialType** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowBevelProperties** <br/> |
| Zellenindex:  <br/> |**visBevelMaterialType** <br/> |
   

