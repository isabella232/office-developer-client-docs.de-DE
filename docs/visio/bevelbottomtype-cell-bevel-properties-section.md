---
title: Zelle "BevelBottomType" (Abschnitt "Fase Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ac7b39d4-3942-4b23-b188-2c3f69e54929
description: Gibt den unteren Abschrägung-Typ der Abschrägung eines Shapes an.
ms.openlocfilehash: 0cd360f633145c7dea95438ffe2bc746e519ce13
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431750"
---
# <a name="bevelbottomtype-cell-bevel-properties-section"></a>Zelle "BevelBottomType" (Abschnitt "Fase Properties")

Gibt den unteren Abschrägung-Typ der Abschrägung eines Shapes an.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Keine Abschrägung  <br/> |
|1  <br/> |Kreis-Abschrägung  <br/> |
|2  <br/> |GeLockerte Abschrägung  <br/> |
|3  <br/> |Kreuz Abschrägung  <br/> |
|4  <br/> |Kühle schräg Fase  <br/> |
|5  <br/> |Winkel Abschrägung  <br/> |
|6  <br/> |Weiche Rundung  <br/> |
|7  <br/> |Konvexe Abschrägung  <br/> |
|8  <br/> |Neigungs Abschrägung  <br/> |
|9  <br/> |Divot-Abschrägung  <br/> |
|10   <br/> |Abrundung-Abschrägung  <br/> |
|11   <br/> |Kanten Abschrägung  <br/> |
|12  <br/> |Art-Deco-Fase  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **BevelBottomType** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements im. vsdx-Dateiformat oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | BevelBottomType  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **BevelBottomType** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowBevelProperties** <br/> |
| Zellenindex:  <br/> |**visBevelBottomType** <br/> |
   

