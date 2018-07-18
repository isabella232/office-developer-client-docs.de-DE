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
ms.openlocfilehash: 47593802e412c1871685f7218dd2a810bc2bc469
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797353"
---
# <a name="localizemerge-cell-miscellaneous-section"></a>LocalizeMerge Cell (Miscellaneous Section)

Gibt an, ob Shapes beim Kopieren zwischen Dokumenten lokalisiert werden.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| WAHR  <br/> | Shapes werden in die Sprache des Zieldokuments lokalisiert.  <br/> |
| FALSCH  <br/> | Ein Shape auf Grundlage der Sprache des Zieldokuments (Standard) nicht lokalisiert.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle LocalizeMerge aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LocalizeMerge  <br/> |
   
Wenn Sie einen Verweis auf die Zelle LocalizeMerge aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zellenindex:  <br/> |**visObjLocalizeMerge** <br/> |
   

