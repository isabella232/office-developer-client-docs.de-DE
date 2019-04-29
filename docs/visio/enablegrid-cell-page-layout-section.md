---
title: Zelle "EnableGrid" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251642
localization_priority: Normal
ms.assetid: bfea4ef4-1b30-eb22-215d-3b9b73098da9
description: Bestimmt, ob die Anwendung Shapes an einem internen unsichtbaren Zeichenblattgitter ausrichtet, wenn Sie das Layout im Dialogfeld Layout konfigurieren festlegen. (Klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout auf Seite neu anordnen, und klicken Sie dann auf Weitere Layoutoptionen.)
ms.openlocfilehash: 11299ca7c9b0ea050542baf97e2cab3a27fa52ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424441"
---
# <a name="enablegrid-cell-page-layout-section"></a>Zelle "EnableGrid" (Abschnitt "Page Layout")

Bestimmt, ob die Anwendung Shapes an einem internen unsichtbaren Zeichenblattgitter ausrichtet, wenn Sie das Layout im Dialogfeld **Layout konfigurieren** festlegen. (Klicken Sie auf der Registerkarte **Entwurf** in der Gruppe **Layout** auf **Seite neu anordnen**, und klicken Sie dann auf **Weitere Layoutoptionen**.)
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Internes Zeichenblattgitter verwenden.  <br/> |
|FALSE  <br/> |Internes Zeichenblattgitter nicht verwenden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie erstellen dieses Zeichenblattgitter im Dialogfeld **Abstände für Layout und Routing** mit den Werten **Abstand zwischen Shapes** und **Durchschnittliche Shape-Größe**. (Klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**, wählen Sie **Layout und Routing** aus, und klicken Sie dann auf **Abstand**.) 
  
Wenn Sie dieses Feature aktivieren, richtet die Anwendung den Zentralpunkt jedes platzierbaren Shapes an der Mitte eines Blocks auf dem internen Seitenraster aus. 
  
Wenn Sie einen Verweis auf die Zelle Zelle EnableGrid aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Zelle EnableGrid  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle EnableGrid aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
|Zellenindex:  <br/> |**visPLOEnableGrid** <br/> |
   

