---
title: Zelle "LocalizeMerge" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033773
localization_priority: Normal
ms.assetid: 734d4415-05dd-4c4d-763e-e035fa56dcec
description: Gibt an, ob Shapes beim Kopieren zwischen Dokumenten lokalisiert werden.
ms.openlocfilehash: ddd6041ec6531652deb38a0c16be2c741bac91a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405674"
---
# <a name="localizemerge-cell-miscellaneous-section"></a>Zelle "LocalizeMerge" (Abschnitt "Miscellaneous")

Gibt an, ob Shapes beim Kopieren zwischen Dokumenten lokalisiert werden.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Shapes werden in die Sprache des Zieldokuments lokalisiert.  <br/> |
| FALSE  <br/> | Lokalisieren Sie ein Shape nicht basierend auf der Sprache des Zieldokuments (standard).  <br/> |
   
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle LocalizeMerge anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LocalizeMerge  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die LocalizeMerge-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zeilenindex:  <br/> |**visObjLocalizeMerge** <br/> |
   

