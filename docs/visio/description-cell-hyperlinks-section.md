---
title: Zelle "Description" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm230
localization_priority: Normal
ms.assetid: 2f571c65-6b7a-5a3a-c075-3c52d3ab989b
description: Stellt eine beschreibende Textzeichenfolge für einen Hyperlink dar.
ms.openlocfilehash: b58e6dc3ec2fc3b64db00e0f19e0718fe897aaa3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360242"
---
# <a name="description-cell-hyperlinks-section"></a>Zelle "Description" (Abschnitt "Hyperlinks")

Stellt eine beschreibende Textzeichenfolge für einen Hyperlink dar. 
  
## <a name="remarks"></a>Hinweise

Verwenden Sie diese Zelle, um Kommentare zum Hyperlink zu speichern. Beispiel: "Link zu unserer Preiswebsite".
  
Sie können den Wert dieser Zelle auch im Dialogfeld **Hyperlinks** festlegen (klicken Sie dazu auf der Registerkarte **Einfügen** auf **Hyperlink**). 
  
Um einen Verweis auf die Zelle Description anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Hyperlink.  *Name*  . Beschreibung, wo Hyperlink.  *Name*  ist der Name der Hyperlinkzeile  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Description nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionHyperlink** <br/> |
| Zeilenindex:  <br/> |**visRow1stHyperlink**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visHLinkDescription** <br/> |
   

