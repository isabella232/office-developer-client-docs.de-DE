---
title: Zelle "LangID" (Abschnitt "Shape Data")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033771
ms.localizationpriority: medium
ms.assetid: 6bd2781a-d4e7-136f-8996-62ebc5f890ab
description: Gibt die Sprache an, in der der Wert für die Shape-Daten eingegeben wurde.
ms.openlocfilehash: c591b005f75e8644f751883738f1fd02cbd03853
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554523"
---
# <a name="langid-cell-shape-data-section"></a>Zelle "LangID" (Abschnitt "Shape Data")

Gibt die Sprache an, in der der Wert für die Shape-Daten eingegeben wurde. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Eine Liste der von Microsoft Office System-Anwendungen unterstützten Sprachen finden Sie unter [Zelle "DocLangID"](doclangid-cell-document-properties-section.md) (Abschnitt "Document Properties"). 
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle "LangID" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Prop.  *Name*  . LangID where Prop.  *Name*  ist der Zeilenname  <br/> |
   
Um einen Verweis auf die Zelle "LangID" anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionProp** <br/> |
| Zeilenindex:  <br/> |**visRowProp**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visCustPropsLangID** <br/> |
   

