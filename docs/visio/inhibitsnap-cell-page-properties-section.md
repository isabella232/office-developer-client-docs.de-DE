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
ms.openlocfilehash: b95dafda9ebef36db34f60585ab3ed2164ade415
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797208"
---
# <a name="inhibitsnap-cell-page-properties-section"></a>InhibitSnap Cell (Page Properties Section)

Legt fest, ob die Shapes auf einem Vordergrundblatt an anderen Objekten auf dem Zeichenblatt und an Shapes auf dem Hintergrundblatt einrasten.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| WAHR  <br/> | Einrasten auf dem Zeichenblatt mit Ausnahme des Einrastens am Lineal und Gitter verhindern.  <br/> |
| FALSCH  <br/> | Einrasten aktivieren.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle InhibitSnap nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | InhibitSnap  <br/> |
   
Wenn Sie einen Verweis auf die Zelle InhibitSnap aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPage** <br/> |
| Zellenindex:  <br/> |**visPageInhibitSnap** <br/> |
   

