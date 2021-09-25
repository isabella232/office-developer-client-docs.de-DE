---
title: Zelle "ShdwType" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60084
ms.localizationpriority: medium
ms.assetid: 551166d0-3aaa-0fd7-e742-cf3450ba90ed
description: Gibt den Standardschattentyp eines Zeichenblatts an.
ms.openlocfilehash: 0279aaab9e608f482d0f1ecbc24e48012c087b1c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607668"
---
# <a name="shdwtype-cell-page-properties-section"></a>Zelle "ShdwType" (Abschnitt "Page Properties")

Gibt den Standardschattentyp eines Zeichenblatts an.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 1  <br/> | Einfach  <br/> |**visFSTSimple** <br/> |
| 2  <br/> | Oblique  <br/> |**visFSTOblique** <br/> |
|3  <br/> |Inneren  <br/> |**visFSTInner** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

 Der in dieser Zelle beschriebene Schattentyp wird immer dann verwendet, wenn die ShapeShdwType Cell (der Schattentyp für eine einzelne Form auf der Seite) auf Page Default (**visFSTPageDefault** ) festgelegt ist. 
  
Einfache Schattentypen werden als Abstandsschatten auf der Benutzeroberfläche beschrieben. Ein einfacher Schatten bewirkt, dass die Form auf einer parallelen Ebene schattiert wird, die sich einige Entfernung dahinter befindet. Schräge Schatten werden als schräge Schatten auf der Benutzeroberfläche beschrieben und haben den Effekt, dass der Schatten auf einer zum Shape rechtwinkligen Ebene zu liegen scheint. 
  
Eine Liste vordefinierter einfacher und schräger Schattentypen finden Sie im Dialogfeld **Seite einrichten** auf der Registerkarte **Schatten** in der Liste **Formatvorlage** (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**). 
  
Um einen Verweis auf die Zelle "ShdwType" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ShdwType  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ShapeShdwOffsetX anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPage** <br/> |
| Zellenindex:  <br/> |**visPageShdwType** <br/> |
   

