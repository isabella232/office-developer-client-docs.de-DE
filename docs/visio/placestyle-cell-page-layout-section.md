---
title: Zelle "PlaceStyle" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7dcd5a35-bd3d-447f-e4aa-986091d129de
description: Gibt an, wie Shapes auf dem Zeichenblatt platziert werden, wenn sie im Dialogfeld Layout konfigurieren (klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout auf Seite neu anordnen, und klicken Sie anschließend auf Weitere Layoutoptionen) angeordnet werden.
ms.openlocfilehash: 251bee427c732fe782c85c4991df07a1deb2a4dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797622"
---
# <a name="placestyle-cell-page-layout-section"></a>PlaceStyle Cell (Page Layout Section)

Gibt an, wie Shapes auf dem Zeichenblatt platziert werden, wenn sie im Dialogfeld **Layout konfigurieren** (klicken Sie auf der Registerkarte **Entwurf** in der Gruppe **Layout** auf **Seite neu anordnen**, und klicken Sie anschließend auf **Weitere Layoutoptionen**) angeordnet werden.
  
## <a name="remarks"></a>Bemerkungen

Sie können den Wert dieser Zelle auch im Dialogfeld **Layout konfigurieren** festlegen. 
  
Wenn Sie eine Referenz auf die Zelle PlaceStyle nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft erhalten möchten, verwenden Sie Folgendes. 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |PlaceStyle  <br/> |
   
Wenn Sie eine Referenz auf die Zelle PlaceStyle aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
|Zellenindex:  <br/> |**visPLOPlaceStyle** <br/> |
   

