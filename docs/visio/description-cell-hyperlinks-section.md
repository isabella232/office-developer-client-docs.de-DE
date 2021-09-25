---
title: Zelle "Description" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm230
ms.localizationpriority: medium
ms.assetid: 2f571c65-6b7a-5a3a-c075-3c52d3ab989b
description: Stellt eine beschreibende Textzeichenfolge für einen Hyperlink dar.
ms.openlocfilehash: 063d8463721f78699c3325739973c6663a949ead
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594608"
---
# <a name="description-cell-hyperlinks-section"></a>Zelle "Description" (Abschnitt "Hyperlinks")

Stellt eine beschreibende Textzeichenfolge für einen Hyperlink dar. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie diese Zelle, um Kommentare zu dem Hyperlink zu speichern. Beispiel: "Link zu unserer Preiswebsite".
  
Sie können den Wert dieser Zelle auch im Dialogfeld **Hyperlinks** festlegen (klicken Sie dazu auf der Registerkarte **Einfügen** auf **Hyperlink**). 
  
Um einen Verweis auf die Zelle Description anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Hyperlink.  *Name*  . Beschreibung, wo Hyperlink.  *Name*  ist der Name der Hyperlinkzeile.  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Description anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionHyperlink** <br/> |
| Zeilenindex:  <br/> |**visRow1stHyperlink**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visHLinkDescription** <br/> |
   

