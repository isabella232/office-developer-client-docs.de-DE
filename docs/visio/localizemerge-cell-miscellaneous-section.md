---
title: Zelle "LocalizeMerge" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033773
ms.localizationpriority: medium
ms.assetid: 734d4415-05dd-4c4d-763e-e035fa56dcec
description: Gibt an, ob Shapes beim Kopieren zwischen Dokumenten lokalisiert werden.
ms.openlocfilehash: 9f2e3e689814891f1a8cd4c69d7656fe6d1b22c9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615879"
---
# <a name="localizemerge-cell-miscellaneous-section"></a>Zelle "LocalizeMerge" (Abschnitt "Miscellaneous")

Gibt an, ob Shapes beim Kopieren zwischen Dokumenten lokalisiert werden.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Shapes werden in die Sprache des Zieldokuments lokalisiert.  <br/> |
| FALSE  <br/> | Lokalisieren Sie ein Shape nicht basierend auf der Sprache des Zieldokuments (Standard).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Um einen Verweis auf die Zelle "LocalizeMerge" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LocalizeMerge  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle LocalizeMerge anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zeilenindex:  <br/> |**visObjLocalizeMerge** <br/> |
   

