---
title: Zelle "ScaleY" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033788
localization_priority: Normal
ms.assetid: 02835aff-455b-ffeb-d53b-28387b6ce361
description: Gibt den Prozentsatz der Vergrößerung des Zeichenblatts auf der Druckerseite an.
ms.openlocfilehash: 0f8e86675a039002b60438eac7df92f4a2b13b98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342728"
---
# <a name="scaley-cell-print-properties-section"></a>Zelle "ScaleY" (Abschnitt "Print Properties")

Gibt den Prozentsatz der Vergrößerung des Zeichenblatts auf der Druckerseite an.
  
## <a name="remarks"></a>Bemerkungen

Dieser Wert wird nur verwendet, wenn der Wert der onPage-Zelle FALSE ist. Die Zellen ScaleX und ScaleY haben immer denselben Wert, der dem Wert entspricht, der im Dialogfeld **Seite einrichten** auf der Registerkarte **Druckeinrichtung** auf die Einstellung **Anpassen an** festgelegt ist (Klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil für die **Seite einrichten** ). 
  
Wenn Sie einen Verweis auf die Zelle ScaleY aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ScaleY  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ScaleY nach Index aus einem Programm erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
|Zellenindex:  <br/> |**visPrintPropertiesScaleY** <br/> |
   

