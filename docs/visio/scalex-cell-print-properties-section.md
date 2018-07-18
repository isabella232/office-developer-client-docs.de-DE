---
title: Zelle "ScaleX" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60072
localization_priority: Normal
ms.assetid: 5916eadc-37f8-47af-fe54-f6062aea318f
description: Gibt den Prozentsatz der Vergrößerung des Zeichenblatts auf der Druckseite an.
ms.openlocfilehash: 1713e88f06dc93a2806e64cae3d7af20c9df1fc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797974"
---
# <a name="scalex-cell-print-properties-section"></a>ScaleX Cell (Print Properties Section)

Gibt den Prozentsatz der Vergrößerung des Zeichenblatts auf der Druckseite an.
  
## <a name="remarks"></a>Bemerkungen

Dieser Wert wird nur, wenn der Wert der Zelle OnPage auf false festgelegt ist. Die Zellen ScaleX und ScaleY haben immer den gleichen Wert dem Wert der Einstellung **Verkleinern** auf der Registerkarte **Druckeinrichtung** im Dialogfeld **Seite einrichten entspricht** (klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten** ). 
  
Wenn Sie einen Verweis auf die Zelle ScaleX aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ScaleX  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ScaleX aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
|Zellenindex:  <br/> |**visPrintPropertiesScaleX** <br/> |
   

