---
title: Zelle "PageHeight" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm760
localization_priority: Normal
ms.assetid: 0184814c-2d67-6ad4-e336-5694612e518d
description: Enthält die Höhe der gedruckten Seite in Zeichnungseinheiten.
ms.openlocfilehash: e198e90e9c70aad1e41ee02d5dcefea68846486c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797578"
---
# <a name="pageheight-cell-page-properties-section"></a>PageHeight Cell (Page Properties Section)

Enthält die Höhe der gedruckten Seite in Zeichnungseinheiten.
  
## <a name="remarks"></a>Bemerkungen

Sie können auch die Seitenhöhe auf der Registerkarte **Zeichenbl** im Dialogfeld **Seite einrichten** festlegen (klicken Sie auf den Pfeil neben **Seite einrichten** , klicken Sie auf der Registerkarte **Entwurf** ), oder die Seite mit der Maus manuell ändern. 
  
Wenn Sie einen Verweis auf die Zelle PageHeight nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |PageHeight  <br/> |
   
Wenn Sie einen Verweis auf die Zelle PageHeight aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPage** <br/> |
|Zellenindex:  <br/> |**visPageHeight** <br/> |
   

