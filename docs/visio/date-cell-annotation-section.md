---
title: Zelle "Date" (Abschnitt "Annotation")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60036
localization_priority: Normal
ms.assetid: f1f11803-614b-a40d-0a2d-131093e7609e
description: Enthält Datum und Uhrzeit der letzten Bearbeitung des Kommentars.
ms.openlocfilehash: 60fd726db1056075f96519050cffa67c76977126
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360340"
---
# <a name="date-cell-annotation-section"></a>Zelle "Date" (Abschnitt "Annotation")

Enthält Datum und Uhrzeit der letzten Bearbeitung des Kommentars. 
  
> [!NOTE]
> Diese Zelle wird zum Nachverfolgen von Kommentaren nur beim Öffnen einer VSD-Datei in Microsoft Visio 2013 oder beim Speichern einer. vsdx-Datei im VSD-Dateiformat verwendet. Sie wird nicht zum Nachverfolgen von Kommentaren in vsdx-Dokumenten in Visio 2013 verwendet. 
  
## <a name="remarks"></a>Bemerkungen

Auf der Benutzeroberfläche wird im Kommentarfeld nur das Datum angezeigt.
  
Wenn Sie einen Verweis auf die Zelle Date aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Annotation. Date [ *i* ] wobei *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Date nach Index aus einem Programm abrufen möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionAnnotation** <br/> |
| Zeilenindex:  <br/> |**visRowAnnotation** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visAnnotationDate** <br/> |
   

