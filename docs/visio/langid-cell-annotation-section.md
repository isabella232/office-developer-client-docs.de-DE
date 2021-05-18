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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422257"
---
# <a name="langid-cell-annotation-section"></a>Zelle "LangID" (Abschnitt "Annotation")

Gibt die Sprache an, in der der Kommentar eingegeben wurde.
  
> [!NOTE]
> Diese Zelle wird nur zum Nachverfolgen von Kommentaren verwendet, wenn Sie eine VSD-Datei in Microsoft Visio 2013 öffnen oder eine VSDX-Datei im VSD-Dateiformat speichern. Es wird nicht zum Nachverfolgen von Kommentaren in VSDX-Dokumenten in Visio 2013 verwendet. 
  
## <a name="remarks"></a>Hinweise

Bei diesem Wert handelt es sich um den Gebietsschemabezeichner der Sprache, die bei Eingabe des Kommentars auf der Eingabegebietsschema-Leiste aktiv ist. Eine Liste der von Microsoft Office-Anwendungen unterstützten Sprachen finden Sie unter [Zelle "DocLangID"](doclangid-cell-document-properties-section.md) (Abschnitt "Document Properties"). 
  
Um einen Verweis auf die LangID-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Annotation.LangID[  *i*  ] wobei  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die LangID-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionAnnotation** <br/> |
| Zeilenindex:  <br/> |**visRowAnnotation**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visAnnotationLangID** <br/> |
   

