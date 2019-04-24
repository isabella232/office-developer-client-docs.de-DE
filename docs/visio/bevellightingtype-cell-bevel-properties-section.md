---
title: Zelle "BevelLightingType" (Abschnitt "Fase Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7fbb4b16-fe54-42d6-803a-c9980897166d
description: Bestimmt den Beleuchtungstyp, der vom Abschrägung-Effekt verwendet wird.
ms.openlocfilehash: 6d92c56b01d192c1df04eecdaca4eb915baebcae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315771"
---
# <a name="bevellightingtype-cell-bevel-properties-section"></a>Zelle "BevelLightingType" (Abschnitt "Fase Properties")

Bestimmt den Beleuchtungstyp, der vom Abschrägung-Effekt verwendet wird.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Keine Beleuchtung  <br/> |
|1  <br/> |Drei Punkt  <br/> |
|2  <br/> |Ausgleich  <br/> |
|3  <br/> |Weich  <br/> |
|4  <br/> |Harten  <br/> |
|5  <br/> |Flut  <br/> |
|6  <br/> |Kontrast  <br/> |
|7  <br/> |Morgen  <br/> |
|8  <br/> |Sonnenaufgang  <br/> |
|9  <br/> |Sonnenuntergang  <br/> |
|10  <br/> |Kühl  <br/> |
|11  <br/> |Reagiert  <br/> |
|12  <br/> |Flach  <br/> |
|13  <br/> |Zwei Punkt  <br/> |
|14  <br/> |Leuchteffekt  <br/> |
|15  <br/> |Heller Raum  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **BevelLightingType** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |BevelLightingType  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **BevelLightingType** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowBevelProperties** <br/> |
|Zellenindex:  <br/> |**visBevelLightingType** <br/> |
   

