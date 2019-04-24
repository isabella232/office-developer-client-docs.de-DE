---
title: Zelle "Type / C" (Abschnitt "Connection Points")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251723
localization_priority: Normal
ms.assetid: 2264d026-2041-3855-2b23-553ce67ae69d
description: Legt den Verbindungspunkttyp fest.
ms.openlocfilehash: a73554d9f3a3bce6a039689d2c0b192a1c5b69aa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359584"
---
# <a name="type--c-cell-connection-points-section"></a>Zelle "Type / C" (Abschnitt "Connection Points")

Legt den Verbindungspunkttyp fest.
  
|**Wert**|**Typ**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Innere  <br/> |**visCnnctTypeInward** <br/> |
|1  <br/> |Nach außen  <br/> |**visCnnctTypeOutward** <br/> |
|2  <br/> |Nach innen &amp; nach außen  <br/> |**visCnnctTypeInwardOutward** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können den Verbindungspunkttyp auch festlegen, indem Sie das Tool **Automatischer Verbinder** sowie ein Shape auswählen und anschließend mit der rechten Maustaste auf einen Verbindungspunkt klicken. Dazu müssen Sie in den [Entwicklermodus](run-in-developer-mode-display-the-developer-tab.md) wechseln. 
  
Wenn Sie einen Verweis auf die Zelle Type/C aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Connections. Type [ *i* ] wobei *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Type/C aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionConnectionPts** <br/> |
|Zeilenindex:  <br/> |**visRowConnectionPts** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visCnnctType** (nicht erweiterte Zeilen) **visCnnctC** (erweiterte Zeilen)  <br/> |
   
Informationen zu erweiterten und nicht erweiterten Zeilen finden Sie in der Zeile Connections Points.
  

