---
title: Zelle "LangID" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60051
localization_priority: Normal
ms.assetid: 815e0df8-5ebf-ef1b-d620-bce8abb69f1a
description: Gibt die Sprache an, in der Zellformeln erstellt wurden.
ms.openlocfilehash: e1e5b92f01e97bc63003a4b195c159a50f61e77b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406675"
---
# <a name="langid-cell-miscellaneous-section"></a>Zelle "LangID" (Abschnitt "Miscellaneous")

Gibt die Sprache an, in der Zellformeln erstellt wurden. 
  
## <a name="remarks"></a>Hinweise

Eine Liste der von Microsoft Office-Anwendungen unterstützten Sprachen finden Sie im Thema [Zelle "DocLangID"](doclangid-cell-document-properties-section.md) (Abschnitt "Document Properties"). 
  
Um einen Verweis auf die LangID-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LangID  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die LangID-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zeilenindex:  <br/> |**visObjLangID** <br/> |
   

