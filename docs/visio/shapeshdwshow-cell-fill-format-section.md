---
title: ShapeShdwShow Cell (Fill Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece6c889-9291-40ea-b55a-072acdcb8a52
description: Bestimmt, ob das Shape als eine ganze Zahl zwischen 0 und 2 einen Schatten angezeigt wird.
ms.openlocfilehash: 72077e60089acd3cd3f8a9349691e1468f6b1f9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798044"
---
# <a name="shapeshdwshow-cell-fill-format-section"></a>ShapeShdwShow Cell (Fill Format Section)

Bestimmt, ob das Shape als eine ganze Zahl zwischen 0 und 2 einen Schatten angezeigt wird.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Den Schatten immer angezeigt, wenn Sie ein Schatten angegeben ist. Schatten für untergeordneten Shapes werden nicht angezeigt.  <br/> |
|1  <br/> |Einen Schatten werden nicht gerendert werden, es sei denn, das Shape nicht über ein übergeordnetes Element verfügt. Verwenden Sie untergeordnetes Shape-Kontrollpunkte, wenn zusammengefasst.  <br/> |
|2  <br/> |Einen Schatten immer angezeigt, wenn Sie ein Schatten angegeben ist. Schatten für die untergeordneten Formen werden angezeigt.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle **ShapeShdwShow** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ShapeShdwShow  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **ShapeShdwShow** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowFill** <br/> |
| Zellenindex:  <br/> |**visFillShdwShow** <br/> |
   

