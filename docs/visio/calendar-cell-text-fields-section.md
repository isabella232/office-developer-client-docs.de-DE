---
title: Zelle "Calendar" (Abschnitt "Text Fields")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60029
localization_priority: Normal
ms.assetid: 0c3e275e-25f0-3681-03f4-257145c19690
description: Bestimmt den Kalender, der für ein Textfeld verwendet wird, wenn der Datentyp Date lautet.
ms.openlocfilehash: 6d9d3ef0addb1d6081e2046ca7a5a663eb2a9c8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796548"
---
# <a name="calendar-cell-text-fields-section"></a>Calendar Cell (Text Fields Section)

Bestimmt den Kalender, der für ein Textfeld verwendet wird, wenn der Datentyp Date lautet.
  
## <a name="remarks"></a>Hinweise

Die folgenden Werte sind möglich: 0 (Westlich), 1 (Arabisch Hijri), 2 (Hebräischer Mondkalender), 3 (Taiwankalender), 4 (Japan - Kaiserherrschaft), 5 (Thai Buddhistisch), 6 (Koreanisch Danki), 7 (Indischer Kalender), 8 (Englisch transkribiert) und 9 (Französisch transkribiert). 
  
Wenn Sie einen Verweis auf die Zelle Calendar aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Fields.Calendar [ *i* ] wobei *i* = < 1 >, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Calendar aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionTextField** <br/> |
| Zeilenindex:  <br/> |**VisRowField** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visFieldCalendar** <br/> |
   

