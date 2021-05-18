---
title: Zelle "Calendar" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60028
localization_priority: Normal
ms.assetid: 7406b46d-b42d-187c-70e8-123c4da7e781
description: Bestimmt den Kalender, der verwendet wird, wenn eine Zellformel Datumsinformationen enthält.
ms.openlocfilehash: f756b0d445bd3f90b67e0b1412bd7ac51a8cdb7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421816"
---
# <a name="calendar-cell-miscellaneous-section"></a>Zelle "Calendar" (Abschnitt "Miscellaneous")

Bestimmt den Kalender, der verwendet wird, wenn eine Zellformel Datumsinformationen enthält.
  
## <a name="remarks"></a>Hinweise

Die folgenden Werte sind möglich: 0 (Westlich), 1 (Arabisch Hijri), 2 (Hebräischer Mondkalender), 3 (Taiwankalender), 4 (Japan - Kaiserherrschaft), 5 (Thai Buddhistisch), 6 (Koreanisch Danki), 7 (Indischer Kalender), 8 (Englisch transkribiert) und 9 (Französisch transkribiert). 
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle Calendar anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Kalender  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Calendar nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zeilenindex:  <br/> |**visObjCalendar** <br/> |
   

