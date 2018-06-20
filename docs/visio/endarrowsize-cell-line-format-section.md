---
title: Zelle "EndArrowSize" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251630
localization_priority: Normal
ms.assetid: e2ecf7c0-a0e9-951f-676a-8e5857bb6544
description: Bestimmt die Pfeilspitzengröße am Linienende.
ms.openlocfilehash: e03871c75857297634300c2eee091de2d0144903
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796954"
---
# <a name="endarrowsize-cell-line-format-section"></a>Zelle "EndArrowSize" (Abschnitt "Line Format")

Bestimmt die Pfeilspitzengröße am Linienende.
  
|**Wert**|**Size**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Sehr klein  <br/> |**visArrowSizeVerySmall** <br/> |
|1  <br/> |Klein  <br/> |**visArrowSizeSmall** <br/> |
|2  <br/> |Mittel  <br/> |**visArrowSizeMedium** <br/> |
|3  <br/> |Groß  <br/> |**visArrowSizeLarge** <br/> |
|4  <br/> |Sehr groß  <br/> |**visArrowSizeVeryLarge** <br/> |
|5  <br/> |Jumbo  <br/> |**visArrowSizeJumbo** <br/> |
|6  <br/> |Kolossal  <br/> |**visArrowSizeColossal** <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können diesen Wert auch im Dialogfeld **Linie** festlegen (klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** klicken Sie auf **Zeile**, **Pfeile**, und klicken Sie dann auf **Weitere Pfeile**).
  
Wenn Sie einen Verweis auf die Zelle EndArrowSize nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |EndArrowSize  <br/> |
   
Wenn Sie einen Verweis auf die Zelle EndArrowSize aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowLine** <br/> |
|Zellenindex:  <br/> |**visLineEndArrowSize** <br/> |
   

