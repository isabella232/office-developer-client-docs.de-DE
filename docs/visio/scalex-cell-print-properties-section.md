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
description: Gibt den Prozentsatz der Vergrößerung des Zeichenblatts auf der Druckerseite an.
ms.openlocfilehash: d1c2f6c184f987e1e7190b1c208310b83a823ee3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410210"
---
# <a name="scalex-cell-print-properties-section"></a>Zelle "ScaleX" (Abschnitt "Print Properties")

Gibt den Prozentsatz der Vergrößerung des Zeichenblatts auf der Druckerseite an.
  
## <a name="remarks"></a>Bemerkungen

Dieser Wert wird nur verwendet, wenn der Wert der onPage-Zelle FALSE ist. Die Zellen ScaleX und ScaleY haben immer denselben Wert, der dem Wert entspricht, der im Dialogfeld **Seite einrichten** auf der Registerkarte **Druckeinrichtung** auf die Einstellung **Anpassen an** festgelegt ist (Klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil für die **Seite einrichten** ). 
  
Wenn Sie einen Verweis auf die Zelle ScaleX aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ScaleX  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ScaleX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
|Zellenindex:  <br/> |**visPrintPropertiesScaleX** <br/> |
   

