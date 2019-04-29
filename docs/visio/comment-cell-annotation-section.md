---
title: Zelle "Comment" (Abschnitt "Annotation")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60033
localization_priority: Normal
ms.assetid: b367841a-f31c-4b55-4491-2abab5811dbe
description: Enthält den in einem Kommentar enthaltenen Text.
ms.openlocfilehash: fd9dce2618c0b8c967b794b0beea8b772a231003
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415530"
---
# <a name="comment-cell-annotation-section"></a>Zelle "Comment" (Abschnitt "Annotation")

Enthält den in einem Kommentar enthaltenen Text.
  
> [!NOTE]
> Diese Zelle wird zum Nachverfolgen von Kommentaren nur beim Öffnen einer VSD-Datei in Microsoft Visio 2013 oder beim Speichern einer. vsdx-Datei im VSD-Dateiformat verwendet. Sie wird nicht zum Nachverfolgen von Kommentaren in vsdx-Dokumenten in Visio 2013 verwendet. 
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle Comment aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Annotation. comment [ *i* ] wobei *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Comment aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionAnnotation** <br/> |
| Zeilenindex:  <br/> |**visRowAnnotation** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visAnnotationComment** <br/> |
   

