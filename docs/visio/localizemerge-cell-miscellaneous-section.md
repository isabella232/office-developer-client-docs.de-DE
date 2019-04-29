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
| FALSE  <br/> | Ein Shape kann nicht basierend auf der Sprache des Zieldokuments lokalisiert werden (Standardeinstellung).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle Zelle LocalizeMerge aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle LocalizeMerge  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle LocalizeMerge aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zeilenindex:  <br/> |**visObjLocalizeMerge** <br/> |
   

