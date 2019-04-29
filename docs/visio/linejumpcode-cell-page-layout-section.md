---
title: Zelle "LineJumpCode" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm540
localization_priority: Normal
ms.assetid: 56f9043d-a632-65df-c710-45867cce1627
description: Definiert die Verbinder, denen Sie Liniensprünge hinzufügen möchten.
ms.openlocfilehash: 7b5b8c8f1de160a4dc766d30a5f518c5653c270b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416251"
---
# <a name="linejumpcode-cell-page-layout-section"></a>Zelle "LineJumpCode" (Abschnitt "Page Layout")

Definiert die Verbinder, denen Sie Liniensprünge hinzufügen möchten.
  
|**Wert**|**Verbinder, denen Sie Liniensprünge hinzufügen möchten**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |None  <br/> |**visPLOJumpNone** <br/> |
|1  <br/> |Horizontale Linien  <br/> |**visPLOJumpHorizontal** <br/> |
|2  <br/> |Vertikale Linien  <br/> |**visPLOJumpVertical** <br/> |
|3  <br/> |Letzte umgeleitete Linie  <br/> |**visPLOJumpLastRouted** <br/> |
|4  <br/> |Letzte angezeigte Linien (Oberes Shape in der *z* -Reihenfolge)  <br/> |**visPLOJumpDisplayOrder** <br/> |
|5  <br/> |Erste angezeigte Leitung (Form am unteren Rand der *z* -Reihenfolge)  <br/> |**visPLOJumpReverseDisplayOrder** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können den Wert dieser Zelle auch im Dialogfeld **Seite einrichten** auf der Registerkarte **Layout und Routing** festlegen (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**, und klicken Sie dann auf **Layout und Routing**).
  
Wenn Sie einen Verweis auf die Zelle Zelle LineJumpCode aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Zelle LineJumpCode  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle LineJumpCode aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
|Zellenindex:  <br/> |**visPLOJumpCode** <br/> |
   

