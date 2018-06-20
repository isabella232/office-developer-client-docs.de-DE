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
ms.openlocfilehash: abb7208c2cfbd6b1423e091efc1d526f8b10b57d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797321"
---
# <a name="linejumpcode-cell-page-layout-section"></a>LineJumpCode Cell (Page Layout Section)

Definiert die Verbinder, denen Sie Liniensprünge hinzufügen möchten.
  
|**Wert**|**Verbinder, die Sie Liniensprünge hinzufügen möchten**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Keine  <br/> |**visPLOJumpNone** <br/> |
|1  <br/> |Horizontale Linien  <br/> |**visPLOJumpHorizontal** <br/> |
|2  <br/> |Vertikale Linien  <br/> |**visPLOJumpVertical** <br/> |
|3  <br/> |Letzte umgeleitete Linie  <br/> |**visPLOJumpLastRouted** <br/> |
|4  <br/> |Letzte angezeigte Linie (oberstes Shape in der *Z* -Reihenfolge)  <br/> |**visPLOJumpDisplayOrder** <br/> |
|5  <br/> |Erste angezeigte Linie (Shape am unteren Rand der *Z* -Reihenfolge)  <br/> |**visPLOJumpReverseDisplayOrder** <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können den Wert dieser Zelle auch festlegen, auf der Registerkarte **Layout und Routing** im Dialogfeld **Seite einrichten** (klicken Sie auf der Registerkarte **Entwurf** , klicken Sie auf den Pfeil neben **Seite einrichten** , und klicken Sie dann auf **Layout und Routing**).
  
Wenn Sie einen Verweis auf die Zelle LineJumpCode nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |LineJumpCode  <br/> |
   
Wenn Sie einen Verweis auf die Zelle LineJumpCode aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
|Zellenindex:  <br/> |**visPLOJumpCode** <br/> |
   

