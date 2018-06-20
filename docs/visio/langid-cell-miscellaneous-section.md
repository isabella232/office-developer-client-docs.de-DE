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
ms.openlocfilehash: 669bde032daeda90b22cdab5d1758c6cbd4109d5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797317"
---
# <a name="langid-cell-miscellaneous-section"></a>LangID Cell (Miscellaneous Section)

Gibt die Sprache an, in der Zellformeln erstellt wurden. 
  
## <a name="remarks"></a>Hinweise

Eine Liste der von Microsoft Office-Anwendungen unterstützten Sprachen finden Sie unter dem Thema [DocLangID](doclangid-cell-document-properties-section.md) Zelle (Abschnitt "Document Properties"). 
  
Wenn Sie einen Verweis auf die Zelle LangID nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LangID  <br/> |
   
Wenn Sie einen Verweis auf die Zelle LangID aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zellenindex:  <br/> |**visObjLangID** <br/> |
   

