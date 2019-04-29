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
ms.openlocfilehash: ac24bee517f29da333a445f276447c1aa682f01c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427080"
---
# <a name="pageheight-cell-page-properties-section"></a>Zelle "PageHeight" (Abschnitt "Page Properties")

Enthält die Höhe der gedruckten Seite in Zeichnungseinheiten.
  
## <a name="remarks"></a>Bemerkungen

Sie können die Seitenhöhe auch auf der Registerkarte **Zeichenblattgröße** im Dialogfeld **Seite einrichten** festlegen (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**) oder die Seitengröße manuell mit der Maus ändern. 
  
Wenn Sie einen Verweis auf die Zelle PageHeight aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |PageHeight  <br/> |
   
Wenn Sie einen Verweis auf die Zelle PageHeight aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPage** <br/> |
|Zellenindex:  <br/> |**visPageHeight** <br/> |
   

