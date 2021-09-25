---
title: Zelle "LineJumpCode" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm540
ms.localizationpriority: medium
ms.assetid: 56f9043d-a632-65df-c710-45867cce1627
description: Definiert die Verbinder, denen Sie Liniensprünge hinzufügen möchten.
ms.openlocfilehash: ffe98e406e76568a5580b03af0498faaf372c549
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623432"
---
# <a name="linejumpcode-cell-page-layout-section"></a>Zelle "LineJumpCode" (Abschnitt "Page Layout")

Definiert die Verbinder, denen Sie Liniensprünge hinzufügen möchten.
  
|**Wert**|**Verbinder, denen Sie Liniensprünge hinzufügen möchten**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |None  <br/> |**visPLOJumpNone** <br/> |
|1  <br/> |Horizontale Linien  <br/> |**visPLOJumpHorizontal** <br/> |
|2  <br/> |Vertikale Linien  <br/> |**visPLOJumpVertical** <br/> |
|3  <br/> |Letzte umgeleitete Linie  <br/> |**visPLOJumpLastRouted** <br/> |
|4   <br/> |Zuletzt angezeigte Linie (obere Form in der *Z-Reihenfolge)*  <br/> |**visPLOJumpDisplayOrder** <br/> |
|5  <br/> |Erste angezeigte Linie (Form am  unteren Rand der Z-Reihenfolge)  <br/> |**visPLOJumpReverseDisplayOrder** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können den Wert dieser Zelle auch im Dialogfeld **Seite einrichten** auf der Registerkarte **Layout und Routing** festlegen (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**, und klicken Sie dann auf **Layout und Routing**).
  
Um einen Verweis auf die Zelle "LineJumpCode" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |LineJumpCode  <br/> |
   
Um einen Verweis auf die Zelle "LineJumpCode" anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
|Zellenindex:  <br/> |**visPLOJumpCode** <br/> |
   

