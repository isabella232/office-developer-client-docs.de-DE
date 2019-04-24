---
title: Zelle "LangID" (Abschnitt "Annotation")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60048
localization_priority: Normal
ms.assetid: b6f5ea5e-b350-0817-d631-f059b9b95c23
description: Gibt die Sprache an, in der der Kommentar eingegeben wurde.
ms.openlocfilehash: b3b2cba3d0a04f75ef2d87f0ee8dcd1f8115e15e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360550"
---
# <a name="langid-cell-annotation-section"></a>Zelle "LangID" (Abschnitt "Annotation")

Gibt die Sprache an, in der der Kommentar eingegeben wurde.
  
> [!NOTE]
> Diese Zelle wird zum Nachverfolgen von Kommentaren nur beim Öffnen einer VSD-Datei in Microsoft Visio 2013 oder beim Speichern einer. vsdx-Datei im VSD-Dateiformat verwendet. Sie wird nicht zum Nachverfolgen von Kommentaren in vsdx-Dokumenten in Visio 2013 verwendet. 
  
## <a name="remarks"></a>Bemerkungen

Bei diesem Wert handelt es sich um den Gebietsschemabezeichner der Sprache, die bei Eingabe des Kommentars auf der Eingabegebietsschema-Leiste aktiv ist. Eine Liste der von Microsoft Office-Anwendungen unterstützten Sprachen finden Sie unter [Zelle "DocLangID"](doclangid-cell-document-properties-section.md) (Abschnitt "Document Properties"). 
  
Wenn Sie einen Verweis auf die Zelle "lang" aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Annotation. lang-e [ *i* ] wobei *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle lang aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionAnnotation** <br/> |
| Zeilenindex:  <br/> |**visRowAnnotation** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visAnnotationLangID** <br/> |
   

