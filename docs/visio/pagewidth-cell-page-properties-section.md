---
title: Zelle "PageWidth" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251372
localization_priority: Normal
ms.assetid: b98c5bf3-10c8-7299-2836-3906d6a9135d
description: Legt die Breite der gedruckten Seite in Zeichnungseinheiten fest.
ms.openlocfilehash: e03696c8f1c921c930d3563e9c73ef4ae613a7c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797602"
---
# <a name="pagewidth-cell-page-properties-section"></a>Zelle "PageWidth" (Abschnitt "Page Properties")

Legt die Breite der gedruckten Seite in Zeichnungseinheiten fest.
  
## <a name="remarks"></a>Bemerkungen

Sie können auch die Breite der Seite auf der Registerkarte **Zeichenbl** im Dialogfeld **Seite einrichten** festlegen (klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten** ) oder die Seite mit der Maus manuell ändern. Ziehen Sie hierzu den Rand der Seite halten Sie die STRG-Taste. 
  
Wenn Sie einen Verweis auf die Zelle PageWidth nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |PageWidth  <br/> |
   
Wenn Sie einen Verweis auf die Zelle PageWidth aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPage** <br/> |
|Zellenindex:  <br/> |**visPageWidth** <br/> |
   

