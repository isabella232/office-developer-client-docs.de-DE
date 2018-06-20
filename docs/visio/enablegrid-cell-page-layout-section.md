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
description: Bestimmt, ob die Anwendung erstellt das Layout Shapes basierend auf einer internen, unsichtbaren Zeichenblattgitter, wenn Sie im Dialogfeld Layout konfigurieren das Layout konfigurieren. (Klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout klicken Sie auf der Seite Re-Layout, und klicken Sie dann auf Weitere Layoutoptionen.)
ms.openlocfilehash: 3371767343132219ebc38134b93afd1da46c7a45
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796928"
---
# <a name="enablegrid-cell-page-layout-section"></a>Zelle "EnableGrid" (Abschnitt "Page Layout")

Bestimmt, ob die Anwendung erstellt das Layout Shapes basierend auf einer internen, unsichtbaren Zeichenblattgitter, wenn Sie im Dialogfeld **Layout konfigurieren** das Layout konfigurieren. (Klicken Sie auf der Registerkarte **Entwurf** in der Gruppe **Layout** klicken Sie auf **Der Seite Re-Layout**, und klicken Sie dann auf **Weitere Layoutoptionen**.)
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Internes Zeichenblattgitter verwenden.  <br/> |
|FALSE  <br/> |Internes Zeichenblattgitter nicht verwenden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie erstellen diese Zeichenblattgitter mithilfe der **Abstand zwischen Shapes** und die **durchschnittliche Shape-Größe** Werte im Dialogfeld **Layout Abstände und Routing** . (Klicken Sie auf der Registerkarte **Entwurf** klicken Sie auf den Pfeil neben **Seite einrichten** , klicken Sie auf **Layout und Routing**, und klicken Sie dann auf **Abstand**.) 
  
Wenn Sie dieses Feature aktivieren, richtet die Anwendung den Zentralpunkt jedes platzierbaren Shapes an der Mitte eines Blocks auf dem internen Seitenraster aus. 
  
Wenn Sie einen Verweis auf die Zelle EnableGrid nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |EnableGrid  <br/> |
   
Wenn Sie einen Verweis auf die Zelle EnableGrid aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
|Zellenindex:  <br/> |**visPLOEnableGrid** <br/> |
   

