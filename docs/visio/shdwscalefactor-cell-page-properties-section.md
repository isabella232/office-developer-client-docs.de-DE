---
title: Zelle "ShdwScaleFactor" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60083
localization_priority: Normal
ms.assetid: 10979706-6dfe-5241-e862-3f94716d14fa
description: Gibt den Prozentsatz an, um den der Schatten eines Shapes vergrößert oder verkleinert wird.
ms.openlocfilehash: 99bc48f5332830512e1f5c2f6d93c70b67197c03
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798081"
---
# <a name="shdwscalefactor-cell-page-properties-section"></a>ShdwScaleFactor Cell (Page Properties Section)

Gibt den Prozentsatz an, um den der Schatten eines Shapes vergrößert oder verkleinert wird. 
  
## <a name="remarks"></a>Bemerkungen

Jeder Schatten weist eine schattierte Speicherorts eines Punkts auf der Schatten, die die Shape-PIN bis entspricht. Wenn ein Shape-Pin in der Mitte des Shapes befindet, würde der schattierte Speicherort beispielsweise den Punkt in der Mitte des Schattens sein. Skalierung auf einfache Schatten angewendet wird, wird an der Position schattierte Vergrößerung zentriert; Beim Skalieren einfache Schatten anwenden, wird die Vergrößerung in der Schräge angibt angewendet. 
  
 Dieser Prozentsatz wird verwendet, wenn der Schattentyp eines Shapes auf Seitenstandard festgelegt ist (Zelle ShapeShdwType ist gleich ** VisFSTPageDefault **). 
  
Wenn Sie dieses Verhalten für einen einzelnen Schatten festlegen möchten, verwenden Sie im Abschnitt Fill Format die Zelle ShapeShdwScaleFactor.
  
Dieser Wert entspricht dem Wert, den Sie im Dialogfeld **Seite einrichten** auf der Registerkarte **Schatten** im Feld **Vergrößerung** festlegen (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**). 
  
Wenn Sie einen Verweis auf die Zelle ShdwScaleFactor aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ShdwScaleFactor  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ShdwScaleFactor aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPage** <br/> |
| Zellenindex:  <br/> |**visPageShdwScaleFactor** <br/> |
   

