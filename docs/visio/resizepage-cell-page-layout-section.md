---
title: Zelle "ResizePage" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm850
localization_priority: Normal
ms.assetid: d63fe874-1027-3436-dbc1-73e722bce22e
description: Bestimmt, ob die Seite, um die Zeichnung, nachdem das Layout von Shapes mithilfe des Dialogfelds Layout konfigurieren einzuschließen, vergrößert (klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout, klicken Sie auf der Seite Re-Layout, und klicken Sie dann auf Weitere Layoutoptionen).
ms.openlocfilehash: fab37ee4561ba82ea1f314ad595e513253478b30
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797853"
---
# <a name="resizepage-cell-page-layout-section"></a>Zelle "ResizePage" (Abschnitt "Page Layout")

Bestimmt, ob die Seite, um die Zeichnung, nachdem das Layout von Shapes mithilfe des Dialogfelds **Layout konfigurieren** einzuschließen, vergrößert (auf der Registerkarte **Entwurf** in der Gruppe **Layout** klicken Sie auf der Seite **Re-Layout** , und klicken Sie dann auf **mehr Layout Optionen**).
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Blatt vergrößern.  <br/> |
| FALSE  <br/> | Blatt nicht vergrößern.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Zum Abrufen eines Verweises auf die Zelle ResizePage nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ResizePage  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ResizePage aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
| Zellenindex:  <br/> |**visPLOResizePage** <br/> |
   

