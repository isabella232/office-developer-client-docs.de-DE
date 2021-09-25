---
title: Zelle "PageWidth" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251372
ms.localizationpriority: medium
ms.assetid: b98c5bf3-10c8-7299-2836-3906d6a9135d
description: Legt die Breite der gedruckten Seite in Zeichnungseinheiten fest.
ms.openlocfilehash: a1cc3d1ab9371f0ec4c70dea7c8efc4c205a09f6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573789"
---
# <a name="pagewidth-cell-page-properties-section"></a>Zelle "PageWidth" (Abschnitt "Page Properties")

Legt die Breite der gedruckten Seite in Zeichnungseinheiten fest.
  
## <a name="remarks"></a>HinwBemerkungeneise

Sie können die Seitenbreite auch auf der Registerkarte **"Seitengröße"** des Dialogfelds **"Seite einrichten"** festlegen (klicken Sie auf der Registerkarte **"Entwurf"** auf den Pfeil neben **"Seite einrichten"),** oder indem Sie die Größe der Seite manuell mit der Maus ändern. Ziehen Sie dazu bei gedrückter STRG-TASTE den Seitenrand mit der Maus. 
  
Um einen Verweis auf die Zelle "PageWidth" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |PageWidth  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle PageWidth anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPage** <br/> |
|Zellenindex:  <br/> |**visPageWidth** <br/> |
   

