---
title: Zelle "InhibitSnap" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251620
localization_priority: Normal
ms.assetid: ab9fcebc-1550-3b9e-e3b4-e8b92424390b
description: Legt fest, ob die Shapes auf einem Vordergrundblatt an anderen Objekten auf dem Zeichenblatt und an Shapes auf dem Hintergrundblatt einrasten.
ms.openlocfilehash: 665130e9f9f938349028ffa1d1c06224e746de5d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335322"
---
# <a name="inhibitsnap-cell-page-properties-section"></a>Zelle "InhibitSnap" (Abschnitt "Page Properties")

Legt fest, ob die Shapes auf einem Vordergrundblatt an anderen Objekten auf dem Zeichenblatt und an Shapes auf dem Hintergrundblatt einrasten.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Einrasten auf dem Zeichenblatt mit Ausnahme des Einrastens am Lineal und Gitter verhindern.  <br/> |
| FALSE  <br/> | Einrasten aktivieren.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle "InhibitSnap aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | "InhibitSnap  <br/> |
   
Wenn Sie einen Verweis auf die Zelle "InhibitSnap aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPage** <br/> |
| Zellenindex:  <br/> |**visPageInhibitSnap** <br/> |
   

