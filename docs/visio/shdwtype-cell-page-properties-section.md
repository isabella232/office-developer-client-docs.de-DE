---
title: Zelle "ShdwType" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60084
localization_priority: Normal
ms.assetid: 551166d0-3aaa-0fd7-e742-cf3450ba90ed
description: Gibt den Standardschattentyp eines Zeichenblatts an.
ms.openlocfilehash: f1fc72484d94788ca2798760ca935c89c3e841ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342889"
---
# <a name="shdwtype-cell-page-properties-section"></a>Zelle "ShdwType" (Abschnitt "Page Properties")

Gibt den Standardschattentyp eines Zeichenblatts an.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 1  <br/> | Simple  <br/> |**visFSTSimple** <br/> |
| 2  <br/> | Oblique  <br/> |**visFSTOblique** <br/> |
|3  <br/> |Inneren  <br/> |**visFSTInner** <br/> |
   
## <a name="remarks"></a>Bemerkungen

 Der in dieser Zelle beschriebene Schattentyp wird verwendet, wenn die Zelle-Zelle (der Schattentyp für ein einzelnes Shape auf dem Zeichenblatt) auf Seiten Standard (**visFSTPageDefault** ) festgelegt ist. 
  
Einfache Schattentypen werden als Abstandsschatten auf der Benutzeroberfläche beschrieben. Ein einfacher Schatten gibt an, wie sich die Form auf eine parallele Ebene befindet, die sich dahinter befindet. Schräge Schatten werden als schräge Schatten auf der Benutzeroberfläche beschrieben und haben den Effekt, dass der Schatten auf einer zum Shape rechtwinkligen Ebene zu liegen scheint. 
  
Eine Liste vordefinierter einfacher und schräger Schattentypen finden Sie im Dialogfeld **Seite einrichten** auf der Registerkarte **Schatten** in der Liste **Formatvorlage** (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**). 
  
Wenn Sie einen Verweis auf die Zelle "ShdwType aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | "ShdwType  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle ShapeShdwOffsetX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPage** <br/> |
| Zellenindex:  <br/> |**visPageShdwType** <br/> |
   

